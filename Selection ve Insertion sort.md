# Proje 1
## İstenenler 
+ [22,27,16,2,18,6] -> Insertion Sort
+ Yukarıda verilen dizinin sort türüne göre aşamalarını yazınız.
+ Big-O gösterimini yazınız.
+ Time Complexity: Dizi sıralandıktan sonra 18 sayısı case'lerden hangisinin kapsamına girer? Yazınız
+ [7,3,5,8,2,9,4,15,6] dizisinin Selection Sort'a göre ilk 4 adımını yazınız.

## Dizinin insertion sort aşamaları
+ 22 | 27, 16, 2, 18, 6 ---> ilk verimizi sıralı kabul ettik.

+ 22, 27 | 16, 2, 18, 6 ---> sıradaki veriyi 22 ile karşılaştırıp büyük olduğu için sağında bırakıp u kısmı sıralı kabul ettik.

+ 16, 22, 27 | 2, 18, 6 ---> sıradaki veriyi yani 16'yı aldık sıralı kısmın en sağındaki veriyle karşılaştırdık. 16 27'den küçük olduğu için bir sola atladık. Bu adımda ise 22 ile karşılaştırdık. 16 22'den de küçük olduğu için tekrar sola atladık, karşılaştıracak veri kalmadığından en solda yani sıralı kısmın en küçük verisi olarak bıraktık.

+ 2, 16, 22, 27 | 18, 6 --->  sıradaki veriyi yani 2'yi aldık sıralı kısmın en sağındaki veriyle karşılaştırdık. 2 27'den küçük olduğu için bir sola atladık. Bu adımda ise 22 ile karşılaştırdık. 2 22'den de küçük olduğu için tekrar sola atladık, bu adımda 16 ile karşılaştırdık  yine küçük olduğu için tekrar sola attık. Karşılaştıracak veri kalmadığından en solda yani sıralı kısmın en küçük verisi olarak bıraktık.

+ 2, 16, 18, 22, 27 | 6 ---> sıradaki veriyi yani 18'i aldık sıralı kısmın en sağındaki veriyle karşılaştırdık. 18 27'den küçük olduğu için bir sola atladık. Bu adımda ise 22 ile karşılaştırdık. 18 22'den de küçük olduğu için tekrar sola atladık, bu adımda 16 ile karşılaştırdık, 18 16'dan büyük olduğu için veriyi burada bıraktık.

+ 2, 6, 16, 18, 22, 27| ---> sıradaki veriyi yani 6'yı aldık sıralı kısmın en sağındaki veriyle karşılaştırdık. 6 27'den küçük olduğu için bir sola atladık. Bu adımda ise 22 ile karşılaştırdık. 6 22'den de küçük olduğu için tekrar sola atladık, bu adımda 16 ile karşılaştırdık yine küçük olduğu için tekrar sola attık. Verimizi yani 6'yı 2 ile karşılaştırdık. 6 2'den büyük olduğu için tekrar sola atmadık ve 2 ile 16 arasında bıraktık. Sıralama çizgimizin sağında sıralanacak veri kalmadığından sıralamamız tamamlanmış oldu.

## Big-O gösterimi
Worst case'de yani veriler elimize büyükten küçüğe doğru ilerleyen şekilde elimize geçerse. İşlem sayısı 1 azalarak devam edecek. 
       
       n  + (n-1) + (n-2)+....  ---> n.(n+1) / 2 buradan gelen dominant değer n^2  
         
Worst case'de big-O (n^2) olur.

Best case'de ise yani elimize halihazırda küçükten büyüğe sıralanmış bir veri dizisi gelirse tek yapacağımız sıralama çizgisini sağa kaydırmak olacağından n işlem yaparız bu da bize Big-O(n) değerini verir.
     
## 18 hangi case kapsamında
18 sayısı sıralama yaparken sıralı kısımların hepsini gezmemize sebep olmadığı için worst case'de değil. Direkt bulunduğu yerde kalmadığı için de best case'de değil. Sıralı verinin ortalarında bir yere yerleşmesi ve işlem sayımızı ortalamada bıraktığı için average case kapsamında bulunur.


## [7,3,5,8,2,9,4,15,6] dizisinin Selection Sort'a göre ilk 4 adımı

+ 2 | 3, 5, 8, 7, 9, 4, 15, 6  Öncelikle tüm verileri taradık en küçüğün 2 olduğuna karar verdik ve en baştaki veri ile en küçük verinin yerini değiştirdik. 2'yi sabitledik.

+ 2, 3 | 5, 8, 7, 9, 4, 15, 6 Sonrasında kalan verileri tekrar taradık. Halihazırda 2'nin yanında olan verinin yani 3'ün bir sonraki veri olması gerektiğini anlayıp hiçbir yer değişikliği yapmadan yalnızca 3'ü de sabitledik.

+ 2, 3, 4 | 8, 7, 9, 5, 15, 6 Tekrar kalan tüm verileri taradık ve 4'ü sıraya almamız gerektiğine karar verdik. 4 ile 5'in yerini değiştirerek 4'ü de sabitledik.

+ 2, 3, 4, 5 | 7, 9, 8, 15, 6 Kalan verileri tekrar tarayıp sıraya 5'in gelmesi gerektiğine karar verdik. 5'i 9 ve 15'in arasından alıp 4'ün sağına yazdık. 4'ün sağındaki 8'i 5'in eski yerine yerleştirdik. Son olarak da 5'i sabitledik. 

+ Devamında da sıradaki eleman yerinde mi kalmalı yoksa sırasız elemanların içinden uygun olanla yer mi değiştirmeli kararını vererek dizimizi sıraladığımızda elimizde sıralı [2, 3, 4, 5, 6, 7, 8, 9, 15] dizimizi elde etmiş olduk.


