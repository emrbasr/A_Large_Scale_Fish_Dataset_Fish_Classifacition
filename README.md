# A Large Scale Fish Dataset - Fish Classification
[Proje Linki - Kaggle](https://www.kaggle.com/code/emrebaar/a-large-scale-fish-dataset-fish-classifacition)

Bu proje, A Large Scale Fish Dataset veri setini kullanarak farklı balık türlerinin sınıflandırılmasını amaçlamaktadır. TensorFlow ve Keras kullanarak bir yapay sinir ağı modeli (ANN) oluşturulmuş ve modelin performansını artırmak için çeşitli yöntemler uygulanmıştır.

## İçindekiler
Gerekli Kütüphanelerin Yüklenmesi
Veri Setinin Yüklenmesi ve Etiketlerin Oluşturulması
Kategorilerin ve Görsellerin Görselleştirilmesi
Görsellerin Yüklenmesi ve İşlenmesi
Eğitim ve Test Verilerinin Ayrılması
Modelin Oluşturulması ve Derlenmesi
Modelin Eğitilmesi
Başarı Metriklerinin Görselleştirilmesi
Confusion Matrix ve Classification Report

## 1. Gerekli Kütüphanelerin Yüklenmesi
Bu projede aşağıdaki kütüphaneler kullanılmıştır:

Pandas: Veri işleme ve düzenleme.
NumPy: Diziler üzerinde işlem yapma.
TensorFlow / Keras: Derin öğrenme modeli oluşturma.
Matplotlib ve Seaborn: Veri görselleştirme.
Bu kütüphaneler, veri analizi ve modelleme süreçlerini yönetmek için gereklidir.

## 2. Veri Setinin Yüklenmesi ve Etiketlerin Oluşturulması
Bu aşamada, balık veri setindeki görüntüler klasör yapısından taranır ve her bir görüntüye ait etiketler (balık türleri) ve yol bilgileri toplanır. Bu bilgiler bir veri çerçevesi (DataFrame) olarak düzenlenir. Veri setindeki her bir görüntü, kendi sınıfına (balık türüne) göre etiketlenir.

## 3. Kategorilerin ve Görsellerin Görselleştirilmesi
Veri setinde bulunan farklı balık türleri görselleştirilir. Her bir sınıftan örnek bir görsel seçilerek balık türleri arasında görsel bir analiz yapılır. Bu adım, veri setindeki çeşitliliği anlamak için önemlidir ve sınıflandırma için kullanılacak sınıfları tanımlar.

## 4. Görsellerin Yüklenmesi ve İşlenmesi
Görüntüler 28x28 piksel boyutunda olacak şekilde yeniden boyutlandırılır ve normalizasyon işlemi yapılır. Normalizasyon, her bir pikselin değerinin 0 ile 1 arasında olacak şekilde ölçeklenmesi işlemidir. Bu işlem, modelin öğrenme performansını artırır.

## 5. Eğitim ve Test Verilerinin Ayrılması
Veri seti eğitim ve test olarak ikiye ayrılır. Eğitim verileri modelin öğrenmesi için kullanılırken, test verileri modelin performansını ölçmek için kullanılır. Etiketler, sayısal değerlere dönüştürülüp one-hot encoding yöntemiyle kategorik hale getirilir.

## 6. Modelin Oluşturulması ve Derlenmesi
Bir yapay sinir ağı (ANN) modeli oluşturulmuştur. Modelin ilk katmanı, görüntülerin boyutlarını düzleştirir (flatten). Daha sonra birden fazla gizli katman eklenir ve bu katmanlarda ReLU aktivasyon fonksiyonu kullanılır. Dropout katmanları ise aşırı öğrenmenin (overfitting) önüne geçmeyi hedefler. Son olarak, softmax aktivasyon fonksiyonu ile sınıf tahmini yapılır.

## 7. Modelin Eğitilmesi
Model, adam optimizasyon algoritması ve categorical_crossentropy kayıp fonksiyonu ile derlenir ve 10 epoch boyunca eğitilir. Eğitim sırasında modelin performansı, doğruluk (accuracy) ve kayıp (loss) gibi metriklerle izlenir. Validation seti de kullanılarak modelin genelleme performansı değerlendirilir.

## 8. Başarı Metriklerinin Görselleştirilmesi
Eğitim ve doğrulama süreçleri boyunca elde edilen accuracy ve loss değerleri grafiksel olarak gösterilmiştir. Bu grafikler, modelin eğitim sürecindeki iyileşmelerini ve overfitting olup olmadığını anlamaya yardımcı olur.

## 9. Confusion Matrix ve Classification Report
Modelin test seti üzerindeki performansı, confusion matrix ve classification report ile değerlendirilmiştir. Confusion matrix, modelin her sınıf için doğru ve yanlış tahminlerini görsel olarak gösterirken, classification report, doğruluk, hatırlama (recall), F1 skoru gibi önemli sınıflandırma metriklerini sağlar.

