# Balık Sınıflandırma Projesi

## Veri Kümesi
Proje, [A Large Scale Fish Dataset](https://www.kaggle.com/datasets/your-dataset-link) adlı veri setini kullanmaktadır. Bu veri seti, farklı balık türlerine ait etiketlenmiş görüntüleri içeren geniş bir veri kümesidir. İki ana parçaya ayrılmıştır:
- **Eğitim Seti**: Modelin öğrenmesi için kullanılan görüntüler.
- **Doğrulama Seti**: Modelin performansını değerlendirmek için kullanılan görüntüler.

## Proje Bileşenleri

### 1. Veri Ön İşleme
Veri ön işleme, modelin daha etkili bir şekilde öğrenebilmesi için ham verilerin uygun bir forma sokulmasıdır.
- **Görüntü Artırma (Data Augmentation)**: Modelin genel performansını artırmak için kullanılan bir tekniktir. Görüntülerin döndürülmesi, kaydırılması, yakınlaştırılması ve ters çevrilmesi gibi dönüşümler yapılır. Bu teknik, modelin farklı görüntü varyasyonlarını görmesini sağlar ve aşırı öğrenmeyi (overfitting) azaltır.
- **Normalization (Normalize Etme)**: Görüntü piksellerinin değerlerini 0 ile 1 arasında bir aralığa ölçeklendirme işlemidir. Normalizasyon, modelin öğrenme sürecini hızlandırır ve daha stabil hale getirir.

### 2. Model Mimarisinin Oluşturulması
Modelin mimarisi, hangi katmanların kullanılacağını ve bu katmanların nasıl bir araya getirileceğini belirler.
- **Konvolüsyonel Katmanlar (Conv2D)**: Görüntülerin özelliklerini çıkarmak için kullanılır. Genellikle birden fazla konvolüsyonel katman bulunmaktadır.
- **Batch Normalization**: Konvolüsyonel katmanlardan sonra uygulanan bir normalizasyon tekniğidir. Bu, modelin daha hızlı ve stabil öğrenmesini sağlar.
- **MaxPooling Katmanları**: Görüntüdeki boyutları küçültmek ve önemli özellikleri vurgulamak için kullanılır.
- **Dense Katmanı**: Modelin çıktısını sınıflandırmak için kullanılan son katmandır. Softmax aktivasyon fonksiyonu kullanarak her bir sınıf için olasılık değerleri üretir.

### 3. Hiperparametre Optimizasyonu
Hiperparametre optimizasyonu, modelin performansını artırmak için ayarlanması gereken parametrelerin belirlenmesini içerir.
- **Keras Tuner**: Hiperparametrelerin otomatik olarak optimize edilmesine olanak tanır.
- **Random Search**: Belirli bir sayıdaki deneme ile en iyi model yapılandırmasının belirlenmesini sağlar.

### 4. Eğitim ve Doğrulama
Eğitim süreci, modelin öğrenme yeteneğini geliştirmek için gerçekleştirilir.
- **Early Stopping**: Eğitim sırasında doğrulama kaybı belirli bir süre boyunca iyileşmezse, eğitim durdurulur. Bu, aşırı öğrenmeyi önlemek için önemlidir.

## Özet
Bu proje, derin öğrenme tekniklerini kullanarak balık türlerini sınıflandırmak için kapsamlı bir yaklaşım sunar. Veri ön işleme, model mimarisi oluşturma, hiperparametre optimizasyonu ve eğitim adımlarıyla, görüntü sınıflandırma görevini etkili bir şekilde yerine getirecek bir sistem geliştirilmiştir.
## Proje İçeriği

Bu projeyle ilgili detaylı incelemeleri ve analizleri görmek için aşağıdaki Kaggle notebook'unu inceleyebilirsiniz:

[Kaggle'daki Akbank Derin Öğrenme Projesi Notebook'u](https://www.kaggle.com/code/sladeniz/akbank-derin-renme-projesi/edit)




