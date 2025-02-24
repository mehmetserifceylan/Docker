# DOCKER
---
## Docker Nedir? 
Docker, bir konteynerleştirme teknolojisidir. Yazılım uygulamalarının bağımsız ve izole bir ortamda çalıştırılmasını sağlar.

Docker öğrenmeye başlamadan öncelikle Virtualization (Sanallaştırma) ve Container (Konteyner) teknolojilerini öğrenmek gerek.

## Virtualization (Sanallaştırma)
Sanallaştırma temelde fiziksel makinanın üzerinde birden fazla sanal makina kurmamıza imkan veren, kaynak dağıtımını ve ortak kaynak kullanımını sağlar. Donanımın verimli kullanılması ve üzeride çalıştırılan sistem ve uygulamaların izole bir şekilde çalıştırılması sağladığı bazı avantajlardır.

![Temsili sanallaştırma mimarisi](sanallaştırma1.jpg)

## Container (Konteyner)
Container'lar, birden çok ortam genelinde uygulamaları tahmin edilebilir ve tekrarlanabilir bir şekilde paketleyip çalıştırmak için oluşturulmuştur. Ortamı yeniden oluşturmak yerine, uygulamayı tüm fiziksel veya sanal ortamlarda çalışacak şekilde paketlemeye denir.

Container ve sanal makinanın bir kaç farkından bahsetmek gerekirse;

1. Boyut farkı; Container'lar daha az boyut kaplar. Sebebi Container temelde Linux teknolojisidir. Linux temelde kernel ve uzerine eklenen arayüz ve uygulamalardan ibaret olduğundan container oluşturlduğu zaman ortam için gerekli tüm bileşenlerden çekirdek kısmını paketlemez. Bu yüzden boyut olarak daha az yer kaplar.
2. Ölçeklenebilirlik; Container'ları ölçeklendirmek çok daha basittir sanal makinaya nispeten.
3. Hız farkı; Sıklıkla yeni özellikler oluşturmak, test etmek ve kullanıma sunmak istiyorsanız ccontainerlar sizin için daha iyi bir yöntemdir.

![Container ve sanal makina temsil eden görseller](docker_container-1024x419.png)

Bu iki kavramdan bahsettikten sonra docker için kaldığımız yerden devam edelim. 

## Docker İmajları
Docker'ın temel yapı taşları, Docker İmajları olarak adlandırılır. Bir Docker imajı, bir uygulamanın çalışması için gerekli olan tüm bileşenleri içerir. İmajlar, konteynerleri başlatmak için kullanılır. Docker imajları katmanlı yapıdadır, yani her katman bir önceki katmana eklenir ve sadece değişiklikler saklanır. Bu yapı, depolama verimliliğini artırır ve ağ üzerinden hızlı dağıtım sağlar.

## Docker Konteynerleri
Docker konteynerleri, ana işletim sistemi üzerinde çalışırken, kendi bağımsız dosya sistemine ve işletim sistemine sahiptirler. Bu izolasyon, uygulamaların birbirleriyle ve ana işletim sistemiyle çakışmasını engeller. Docker, Cgroups ve Namespaces gibi Linux çekirdek özelliklerini kullanarak bu izolasyonu sağlar. 

## Docker Ekosistemi
- **Docker Engine:** Docker konteynerlerini oluşturmak ve çalıştırmak için kullanılan çekirdek bileşenidir.
- **Docker Hub:** Kullanıcıların Docker imajlarını paylaşabileceği ve keşfedebileceği çevirimiçi depodur.
- **Docker Compose:** Birden fazla konteyneri içeren uygulamaların tanımlanması ve yönetilmesi için kullanılan bir araçtır.
- **Docker Swarm:** Docker konteynerlerinin cluster ortamlarında orkestrasyonu için kullanılan bir araçtır.

## Kullanım Alanları ve Avantajları

- **Taşınabilirlik:** Docker konteynerleri, herhangi bir platformda aynı şekilde çalışabilir, bu da geliştiriciler ve operasyon ekipleri arasındaki uyumu artırır.
- **İzolasyon:** Konteynerler, uygulamaların ve bağımlılıklarının birbirlerinden ve ana sistemden izole edilmesini sağlar.
- **Verimlilik:** Docker, kaynak kullanımını optimize eder ve aynı sunucuda birden fazla uygulamanın verimli bir şekilde çalışmasını sağlar.
- **Hız:** Docker konteynerlerinin başlatılması ve durdurulması, geleneksel sanal makinelerden çok daha hızlıdır.
---

**_Mehmet Şerif Ceylan_**
