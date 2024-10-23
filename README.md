# A_Large_Scale_Fish_Dataset_Fish_Classifacition

## 1. Gerekli Kütüphanelerin Yüklenmesi
Bu bölümde projemiz için gerekli olan kütüphaneler yüklenmektedir. Bu kütüphaneler arasında pandas, tensorflow, matplotlib gibi veri işleme, model oluşturma ve görselleştirme için gerekli araçlar bulunmaktadır.

## 2. Veri Setinin Yüklenmesi ve Etiketlerin Oluşturulması
Bu bölümde, balık veri setindeki görüntüler klasör yapısı içerisinden taranır ve her bir görüntüye ait etiketler (label) ile yol bilgileri (path) toplanır. Bu veriler daha sonra bir DataFrame'e dönüştürülür.

## 3. Kategorilerin ve Görsellerin Görselleştirilmesi
Bu bölümde, veri setindeki farklı balık türleri görselleştirilir. Her bir sınıftan bir örnek görsel ekrana bastırılarak balık türleri arasında görsel bir analiz yapılır.

## 4. Görsellerin Yüklenmesi ve İşlenmesi
Bu bölümde, veri setindeki her bir görüntü belirlenen boyutlara (28x28) küçültülerek işlenir. Görseller normalleştirilir ve daha sonra model için kullanılmak üzere numpy dizisine dönüştürülür.

## 5. Eğitim ve Test Verilerinin Ayrılması
Bu bölümde, veri seti eğitim ve test olarak ayrılır. Etiketler LabelEncoder ile sayısal değerlere çevrilir ve to_categorical ile one-hot encoding formatına dönüştürülür.

## 6. Modelin Oluşturulması ve Derlenmesi
Bu bölümde, basit bir yapay sinir ağı (ANN) modeli oluşturulmuştur. İlk katman Flatten ile görüntülerin boyutu düzleştirilir ve ardından gizli katmanlar eklenir. Dropout kullanarak aşırı öğrenme (overfitting) azaltılmaya çalışılır. Son katmanda softmax fonksiyonu kullanılarak sınıflar arasında tahmin yapılır.

## 7. Modelin Derlenmesi ve Eğitilmesi
Model adam optimizasyon algoritması ve categorical_crossentropy loss fonksiyonu ile derleniyor ve ardından 10 epoch boyunca eğitiliyor.

## 8. Başarı Metriklerinin Görselleştirilmesi
Accuracy ve loss değerlerinin eğitim ve validasyon süreçleri boyunca değişimi ayrı grafiklerde gösteriliyor.

## 9. Confusion Matrix ve Classification Report
Bu bölümde modelin test seti üzerindeki performansını analiz etmek için confusion matrix ve classification report kullanılıyor.
