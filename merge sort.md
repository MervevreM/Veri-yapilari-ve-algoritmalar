# Proje 2

## İstenenler

+ [16,21,11,8,12,22] -> Merge Sort
+ Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
+ Big-O gösterimini yazınız.


## Dizinin merge sort aşamaları
Bu sort biçiminde veri yarıya bölüne bölüne tek eleman kalana kadar parçalanıyor sonra adım adım her adım sıralı olacak biçimde birleştiriliyordu.

+ 16, 24, 11 ||| 8, 12, 22  ---> ilk adımda dizimizi 2 parçaya ayırdık.
 
+ 16 || 24, 11 ||| 8 || 12, 22 ---> İkinci adımda elimdeki parçaları da iki parçaya ayırdık.

+ 16 || 24 || 11 || 8 || 12 || 22 ---> Üçüncü adımda ise her veri yalnız kalacak biçimde dizimi parçalayabilmiş oldum. Şimdi sıralı biçimde veri parçacıkları oluşturma kısmına geldik.

+ 16 || 11, 24 ||| 8 || 12, 22 ---> Bu adımda tek verileri minik sıralı parçacıklar haline getirmeye başlıyoruz. 11 ile 24'ü tekrar birleştirirken,
11 daha küçük olduğu için sola alarak birleştirdik. 12 ve 22 doğru sırada olduğundan yer değişikliği yapmadan birleştirdik.

+ 11, 16, 24 ||| 8, 12, 22 ---> soldaki tek veri yani 16 diğer ikilinin ilk verisinden büyük mü küçük mü diye kontrol ettik 16 11'den büyük olduğu için atladık ve
ikinci veriye de sorduk, 16 24'ten küçük olduğundan bulunduğu yere bıraktık. Soldaki ilk yarım oluştu. Sağ kanatta ise tek veri olan 8 ile 12, 22 sıralı veri parçasını
birleştirmek için 8 büyük mü küçük mü diye kontrol ettik. 8 12'den küçük olduğu için 12'nin soluna yazdık. Bu sayede de 2. yarımımızı elde ettik.

+ 8, 11, 12, 16, 22, 24 ---> 2 yarımı birleştirmek için sol yarımla sağ yarımın ilk verilerini karşılaştırdık. Karşılaştırma detayları aşağıda:

      Sol yarımda 11, 16, 24
      Sağ yarımda 8, 12, 22 
      
      11 8 karşılaştırması sonucu 8'i en sola yazdık.
      11 12 karşılaştırması sonucu 11', 8'in sağına ekledik.
      12 16 karşılaştırması sonucu 12'yi 11'in sağına ekledik.
      16 22 karşılaştırması sonucu 16'yı 12'nin sağına ekledik.
      22 24 karşılaştırması sonucu 22'yi 16'nın sağına ekledik.
      Son kalan 24'ü de dizinin en sağına eklediğimizde soldan sağa gittikçe sayı artışının olduğu sıralıdizimizi elde etmiş olduk.
      
      
## Big-O gösterimi
+ Her adımda O(n) kadar işlem yapıyoruz
+ Adımlarda verileri ikiye bölerek ilerlediğimiz için 2^x = n  --> O(logn)
+ Big-O ---> O(n). O(logn)  ---> O(nlogn)
