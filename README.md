# CIFAR-10 ile Görüntü Sınıflandırma

Bu proje, CIFAR-10 veri seti kullanılarak konvolüsyonel sinir ağları (CNN) ile görüntü sınıflandırma işlemi gerçekleştirmektedir. Aşağıda proje ile ilgili detaylı bilgiler bulunmaktadır.

## İçindekiler

1. [Proje Hakkında](#proje-hakkında)
2. [Veri Seti](#veri-seti)
3. [Yöntemler](#yöntemler)
4. [Tartışma](#tartışma)
5. [Kurulum ve Kullanım](#kurulum-ve-kullanım)
6. [Katkıda Bulunma](#katkıda-bulunma)
7. [Lisans](#lisans)

## Proje Hakkında

Bu projenin amacı, derin öğrenme yöntemleri kullanarak CIFAR-10 veri setindeki görüntüleri sınıflandırmak ve elde edilen sonuçları değerlendirerek modelin performansını incelemektir.

## Veri Seti

CIFAR-10, 10 farklı sınıfa ait 60.000 renkli görüntüden oluşan bir veri setidir. Her sınıfta 6.000 görüntü bulunmaktadır. CIFAR-10 veri seti, küçük boyutlu ve çeşitli sınıflar içerdiğinden, görüntü sınıflandırma modellerini eğitmek ve değerlendirmek için ideal bir veri setidir.

### Sınıflar:

1. Airplane
2. Automobile
3. Bird
4. Cat
5. Deer
6. Dog
7. Frog
8. Horse
9. Ship
10. Truck

## Yöntemler

### Veri Setinin Hazırlanması

- Veri seti %80 eğitim ve %20 test olarak ayrıldı.
- Görüntü verileri 0-255 aralığından 0-1 aralığına normalize edildi.
- Etiketler one-hot encoding yöntemiyle dönüştürüldü.

### Model Mimarisi

Konvolüsyonel Sinir Ağı (CNN) kullanıldı. Modelin mimarisi şunları içerir:

- 3 adet konvolüsyon katmanı
- 2 adet max-pooling katmanı
- 1 adet flatten katmanı
- 2 adet dense katmanı
- Dropout uygulaması

### Modelin Eğitilmesi

- Model, 20 epoch boyunca eğitim verileri üzerinde eğitildi.
- Adam optimizer ve categorical cross-entropy loss fonksiyonu kullanıldı.


### Performans Metrikleri

- **Accuracy:** % (doğruluk oranı)
- **F1 Score:** % (F1 skoru)

## Tartışma

### Başarılar

- Model, CIFAR-10 veri seti üzerinde yüksek doğruluk oranı ve F1 skoru elde etti.
- Eğitim süreci stabil ilerledi ve beklenen iyileşmeler gözlemlendi.

### Sınırlamalar

- Veri setinin boyutu ve çeşitliliği, modelin genelleme yeteneğini sınırladı.
- Donanım kaynakları sınırlıydı; daha gelişmiş donanımlarla daha derin modeller eğitilebilir.
- Veri artırma teknikleri kullanılmadı.

## Kurulum ve Kullanım

Bu projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyebilirsiniz.

### Gereksinimler

- Python 3.6 veya üstü
- TensorFlow ve Keras
- NumPy
- Matplotlib
- Scikit-learn

### Kurulum

1. Bu projeyi klonlayın:

    ```bash
    git clone https://github.com/kullaniciadi/proje-adi.git
    cd proje-adi
    ```

2. Gerekli paketleri yükleyin:

    ```bash
    pip install -r requirements.txt
    ```

3. `cifar10_classification.py` dosyasını çalıştırın:

    ```bash
    python cifar10_classification.py
    ```

## Katkıda Bulunma

Katkıda bulunmak isterseniz, lütfen bir pull request gönderin. Her türlü katkı memnuniyetle karşılanır!

## Lisans

Bu proje MIT Lisansı ile lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına bakın.

---

