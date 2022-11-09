# KNN (K En Yakın Komşu Algoritması) Nedir?

![resim](https://www.veribilimiokulu.com/wp-content/uploads/2017/07/k_en_yakin_komsu_anime.png)
Makine öğrenmesi ile çözülebilen problemlerden biri çok geniş kullanım alanı ile sınıflandırma problemleridir. Günümüzdeki bir çok problem bir şekilde sınıflandırma problemi olarak tasarlanıp çözülebilmektdir. Sınıflandırmada bildiğimiz gibi eğittiğimiz bir model kullanarak hedef niteliğini bilmediğimiz ancak elimizde özellikleri olan bir nesnenin hangi sınıfa dahil olacağını tahmin ediyoruz. Sınıflandırma algoritmalarından k en yakın komşu en yaygın olarak kullanılan algoritmadır. Mantık kabaca şöyle; k sayısı belirlenir, nesnenin hangi sınıfa dahil olacağını belirlemek için kendisine en yakın olan kaç komşu kullanılacağına dair bir sayı. Bu komşulara olan mesafe bir yöntemle hesaplanır (örn. öklid) Daha sonra bu k sayısı içinde en fazla hangi sınıfa yakınlık var ise bilinmeyen nesnenin de o sınıfa dahil olduğuna hükmedilir.

K-en yakın komşuluk (KNN) algoritması, uygulaması kolay gözetimli öğrenme algoritmalarındandır. Hem sınıflandırma hem de regresyon problemlerinin çözümünde kullanılıyor olmakla birlikte, endüstride çoğunlukla sınıflandırma problemlerinin çözümünde kullanılmaktadır.

KNN algoritmaları, 1967 yılında T. M. Cover ve P. E. Hart tarafından önerilmiştir. 3 tip uzaklık fonksiyonu kullanılmaktadır:

“Euclidean” Uzaklık,
“Manhattan” Uzaklık,
“Minkowski” Uzaklığı.
## KNN Çalışma Mantığı
Sınıflandırmada (classification) kullanılan bu algoritmaya göre sınıflandırma sırasında çıkarılan özelliklerden (feature extraction), sınıflandırılmak istenen yeni bireyin daha önceki bireylerden k tanesine yakınlığına bakılmasıdır.

Örneğin k = 3 için yeni bir eleman sınıflandırılmak istensin. bu durumda eski sınıflandırılmış elemanlardan en yakın 3 tanesi alınır. Bu elamanlar hangi sınıfa dahilse, yeni eleman da o sınıfa dahil edilir. Mesafe hesabından genelde öklit mesafesi (euclid distance) kullanılabilir.

![resim](https://bilgisayarkavramlari.com/wp-content/uploads/2008/11/yerlestirme.jpg)

Örneğin yukarıda verilen ve özelliklerine göre 2 boyutlu koordinat sistemine yerleştirilmiş olan örnekleri ele alalım. Bu örneklerin birbirinden ayrılması doğrusal ayrıştırma (linear discrimination) problemidir ve buradaki yöntemlerle çözülür.

KNN yöntemine göre aşağıdaki şekilde yeni bir üyenin geldiğini düşünelim:

![resim](https://bilgisayarkavramlari.com/wp-content/uploads/2008/11/yeniuye.jpg)

Yukarıdaki bu yeni gelen üyenin en yakın olduğu 3 üyeyi (3 nearest neighbors) tespit edelim.

![resim](https://bilgisayarkavramlari.com/wp-content/uploads/2008/11/yeniuyemesafe.jpg)

En yakın 3 üyenin iki tanesi kırmızı yuvarlak üyeler olduğuna göre yeni üyemizi bu şekilde sınıflandırabiliriz:

![resim](https://bilgisayarkavramlari.com/wp-content/uploads/2008/11/yeniuyemesafesiniflandirma.jpg)

## K Değerinin Seçilmesi 

K değişkeni için sabit bir değer yoktur. Bu yüzden farklı k değerleri deneyip optimal bir k değerinin bulunması daha iyi sonuç verecektir. Bir örnek üzerinde bunu görelim.

![resim](https://mlhtnc.github.io/images/knn.png)

K değerini 3 yapalım. Sırasıyla en yakın komşular B,A,A olur. Bu durumda (5,5) noktası A sınıfına aittir. K değerini 5 yaptığımızda ise sırasıyla en yakın komşular B, A, A, B, B'dir. 2 tane A sınıfı ve 3 tane B sınıfı. Bu durumda ise (5,5) noktası B sınıfına aittir.

Görüldüğü gibi K değerinin değişmesi sınıflandırmayı etkilemiştir. Bu yüzden farklı K değerleriyle sınıflandırma yapıp en iyi sonucu veren değeri seçmemiz gerekir.

## Sınıflandırma Problemleri Örnekleri

- Müşterinin verilen krediyi ödeyip ödeyemeyeceği (Customer Default Risk)

- Müşterinin aldığı servisi bırakıp bırakmayacağı (Customer Churn)

- Müşteri segmantasyon (Customer Segmantation)

- Kişiye özel ilaç tespiti

- E-posta spam filitrelemesi

- Görüntü tanıma (Image Recognition)

- El yazısı tanıma (Handwriting Recognition)

- Biyometrik tanımlama (Biometric Identification)

## Kaynakça

- https://mlhtnc.github.io/knn-algorithm.html
- https://arslanev.medium.com/makine-%C3%B6%C4%9Frenmesi-knn-k-nearest-neighbors-algoritmas%C4%B1-bdfb688d7c5f
- https://www.veribilimiokulu.com/k-en-yakin-komsu-k-nearest-neighbor-siniflandirma-python-ornek-uygulama/
- https://medium.com/@k.ulgen90/makine-%C3%B6%C4%9Frenimi-b%C3%B6l%C3%BCm-2-6d6d120a18e1
