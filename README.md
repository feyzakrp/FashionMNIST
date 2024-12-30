# PyTorch ile FashionMNIST Sınıflandırması  

## Genel Bakış  
Bu proje, PyTorch kullanarak FashionMNIST veri seti üzerinde bir sinir ağı modelinin eğitim, test ve görselleştirme işlemlerini gerçekleştiren bir makine öğrenimi pipeline'ını sunar. Kod, kütüphanelerin içe aktarılmasından GPU kullanımının ayarlanmasına, veri yükleme ve ön işleme aşamalarına, model tanımlama ve eğitimine, test ve performans görselleştirmesine kadar tüm adımları içerir.  

---

## Proje Özellikleri  

### GPU Kullanımı  
- Proje, mevcut bir GPU'yu otomatik olarak algılar ve işlemleri hızlandırmak için kullanır.  
- Eğer GPU mevcut değilse, işlem CPU üzerinde gerçekleştirilir.  

### FashionMNIST Veri Seti  
- **Eğitim ve Test Veri Setleri:** PyTorch `datasets` modülü kullanılarak veri seti otomatik olarak yüklenir ve işlenir.  
- **Dönüşümler:** Görüntüler tensörlere dönüştürülür ve normalize edilir.  

### Sinir Ağı Modeli  
- **Mimari:** Tam Bağlantılı Sinir Ağı (Fully Connected Neural Network).  
- **Girdi:** 28x28 boyutunda gri tonlamalı görüntüler.  
- **Çıkış:** 10 sınıfa ait olasılık değerleri.  

### Eğitim  
- **Kayıp Fonksiyonu:** CrossEntropyLoss.  
- **Optimizasyon Algoritması:** Adam optimizasyon yöntemi.  
- 10 epoch boyunca eğitim yapılır ve her epoch için kayıp değeri görüntülenir.  

### Test ve Performans Değerlendirmesi  
- Test veri seti üzerinde doğruluk hesaplanır.  
- Model performansı renkli görselleştirme ile analiz edilir.  

### Görselleştirme  
- Test veri setinden örnekler seçilir ve gerçek etiketler ile modelin tahmin ettiği etiketler karşılaştırılır.  
- **Yeşil Başlık:** Doğru tahmin.  
- **Kırmızı Başlık:** Yanlış tahmin.  

---

## Projenin Kurulumu ve Çalıştırılması  

### Gereksinimler  
Aşağıdaki Python kütüphanelerinin yüklü olması gerekir:  
- `torch`  
- `torchvision`  
- `numpy`  
- `matplotlib`  
- `scikit-learn`  
- `Pillow`  

### Kurulum  
Gerekli kütüphaneleri yüklemek için aşağıdaki komutu çalıştırabilirsiniz:  
```bash
pip install torch torchvision numpy matplotlib scikit-learn pillow tqdm
