# NLP-Projesi
Teknofest Türkçe Doğal Dil İşleme Yarışması Projesi

# NLP-Projesi

# Duygu Sınıflandırma NLP Projesi

Bu proje, metin verilerinden duyguları sınıflandırmayı amaçlayan çeşitli makine öğrenimi modellerini kullanmaktadır. Kullanılan veri seti, farklı duygularla etiketlenmiş metin verilerini içermektedir.

## Veri Seti

Veri seti üç dosyadan oluşmaktadır:
- `train.txt`: 16.000 giriş içeren eğitim verileri.
- `test.txt`: 2.000 giriş içeren test verileri.
- `val.txt`: 2.000 giriş içeren doğrulama verileri.

Her dosyada iki sütun bulunmaktadır:
- `Text`:  Metin verisi.
- `Emotion`: İlgili metin için duygu etiketi.

## Veri Ön İşleme

1. **Keşifsel Veri Analizi (EDA)**
   - Veri setlerini yükleyin ve temel bilgileri görüntüleyin.
   - Veri setlerinde her duygunun sıklığını sayın ve görüntüleyin.
   - Model performansını artırmak için düşük temsili olan duyguları ('love' ve 'surprise') kaldırın.

2. **Metin İşleme**
   - Metin ön işleme için özel bir `TextProcessor` sınıfı tanımlayın.
   - Metni küçük harfe çevirin ve durdurma kelimelerini kaldırın.
   - İsteğe bağlı olarak metin üzerinde köklerini bulma (stemming) uygulayın.

3. **Metin Vektörizasyonu**
   - Metin verilerini sayısal vektörlere dönüştürmek için `CountVectorizer` kullanın.

## Modeller

Ön işlenmiş veriler üzerinde çeşitli modeller eğitildi ve değerlendirildi:

1. **Rastgele Orman Sınıflandırıcısı (Random Forest Classifier)**
   - Eğitim setinde %99.94 doğruluk sağladı.
   - Doğrulama setinde %89.77 doğruluk sağladı.
   - Test setinde %91.10 doğruluk sağladı.

2. **Destek Vektör Makinesi (SVM)**
   - Eğitim setinde %98.05 doğruluk sağladı.
   - Doğrulama setinde %92.88 doğruluk sağladı.
   - Test setinde %93.75 doğruluk sağladı.

3. **Lojistik Regresyon (Logistic Regression)**
   - Eğitim setinde %99.21 doğruluk sağladı.
   - Doğrulama setinde %93.16 doğruluk sağladı.
   - Test setinde %93.92 doğruluk sağladı.

4. **Çok Terimli Naive Bayes (Multinomial Naive Bayes)**
   - Eğitim setinde %93.46 doğruluk sağladı.
   - Doğrulama setinde %86.56 doğruluk sağladı.
   - Test setinde %84.90 doğruluk sağladı.

5. **Gradient Boosting Sınıflandırıcısı (Gradient Boosting Classifier)**
   - Eğitim setinde %89.90 doğruluk sağladı.
   - Doğrulama setinde %87.71 doğruluk sağladı.
   - Test setinde %87.72 doğruluk sağladı.

## Model Değerlendirmesi

- Her model için performansı görselleştirmek amacıyla karışıklık matrisleri (confusion matrix) çizildi.
- En iyi performansı gösteren model, test setinde en yüksek doğruluk oranı olan %93.92 ile Lojistik Regresyon olarak belirlendi.

## Uygulama

### Bağımlılıklar

Gerekli bağımlılıkları yüklemek için:

```bash
pip install -r requirements.txt

