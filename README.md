# Docker Commands

<h1>docker pull ...</h1>
Docker hub dan bir image çekmemize yardımcı olacaktır. Image dosyasını indirir.

<h1>docker images</h1>
Docker üzerinde bulunan tüm image'leri listeler.

<h1>docker run ...</h1>
İndirilecek olan image dosyasını önce localde arar varsa çalıştırır yoksa indirme işlemi yapar sonra çalıştırır.
Bir konteynera isim verip çalıştırana dek her çalıştırmada, farklı isimler atayacaktır.

<h1>docker run -it ubuntu</h1>
<i>Örnek: </i> docker run -it imageAdı
<p>Bu kod ubuntuyu ayağa kaldırır ve ubuntu sistemine giriş yaparız. Konsoldan ubuntu üzerinde çalışabiliriz.</p>
-it : interactve terminal -> ubuntunun terminale gireriz.

<h1>docker ps / docker container ls</h1>
Ayakta olan konteynerları listeler.

<h1>docker ps -a / docker ps --all / docker container ls -a</h1>
Yapmış olduğumuz konteyner geçmiş hareketlerini gösterir.

<h1>docker container ls -aq</h1>
<p>Konteynerların id sini yazdırır.</p>

<h1>docker run --name [Verilecekİsim] [ImageAdı]</h1>
<i>Örnek: </i>  docker run --name bash_ubuntu ubuntu
<p>Yukarıdaki kod ubuntu image'ini bash_ubuntu ismiyle değiştirir.</p>

<h1>docker start [konteynerAdı]</h1>
<i>Örnek: </i>  docker start bash_ubuntu
<p>bash_ubuntu konteynerı ayağa kaldırıldı.</p>
  
<h1> docker stop [konteynerAdı]/[CONTAINER ID]</h1>
<i>Örnek: </i> docker stop bash_ubuntu
<p>bash_ubuntu konteynerını durdurur.</p>
Konteyner adı yerine, CONTAINER ID de yazılabilir unique olduğu için kullanılabilmektedir. 
  <p>CONTAINER ID : cac722f54f30 => docker stop ca</p>
  yazmak yeterli olabilir.

<h1>docker rm [konteynerAdı]/[konteynerID]</h1>
<i>Örnek: </i> docker rm kind_northcutt
<p>Örnekteki gibi veya id sini girerek konteynerı silebiliriz.</p>
<p>Veya idleri çoklu vereke de silme işlemi gerçkleştirilebilir. <i>Örnek: </i> docker rm 98 cm 0u</p>
<h2>Hepsini silmek için: docker container rm $(docker container ls -aq)</h2>
Bu kod tüm konteynerları siler.

