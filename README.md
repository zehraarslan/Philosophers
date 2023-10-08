# Philosophers

#Proje Hakkında

Philosophers projesi, C dilinde multithreading'in nasıl kullanılacağını göstermek için tasarlanmıştır. Bu proje, filozofların yemek yeme problemini modelleyerek, threadlerin kullanımını gösterir.

#Threadler Hakkında

Bu proje, her bir filozofun ayrı bir thread olarak temsil edildiği bir modeli kullanır. Bu sayede, her filozofun yemek yeme, düşünme ve uyuma eylemlerini aynı anda gerçekleştirmesi sağlanır.

Threadler, aşağıdaki gibi oluşturulur ve başlatılır:
pthread_t thread_id;

// Thread oluşturma
pthread_create(&thread_id, NULL, philosopher_activity, philosopher);

// Thread'in bitmesini bekleyen ana thread
pthread_join(thread_id, NULL);
Burada, philosopher_activity fonksiyonu, her filozofun (yani her threadin) gerçekleştireceği eylemleri tanımlar.

#Kurulum

Projeyi kurmak için aşağıdaki adımları izleyin:

- İlk önce, projeyi GitHub deposundan klonlayın: git clone https://github.com/zehraarslan/Philosophers.git
- Dizin içerisine gidin: cd Philosophers
- Projeyi build edin: make

# Kullanım

Proje, filozofların yemek yeme problemi modelini simüle eder. Her filozofun eylemlerini görmek için, uygulamayı çalıştırın.

./philosophers 
