# rent_estimate
# 🏠 Ev Fiyat Tahminleme Projesi (House Price Prediction)

Bu proje, bir makine öğrenimi uygulamasıdır. Amacı, verilen verilerle ev fiyatlarını tahmin etmektir. Model, eğitim verileri üzerinden öğrenerek test verilerinde fiyat tahminlemesi yapmaktadır.

---

## 📊 Kullanılan Veri Seti

Kaggle'dan alınmış [Istanbul Rent Flat Data]((https://www.kaggle.com/datasets/mgunerengineer/istanbul-rent-flat-data)) benzeri bir veri seti kullanılmıştır. Verideki bazı sütunlar:

- `Title`: İlan başlığı
- `Area`: Dairenin metrekare cinsinden büyüklüğü
- `NumberofRooms`: Dairedeki oda sayısı
- `Town`: Dairenin hangi ilçede olduğu
- `District`: Dairenin hangi mahallede olduğu
- `Price`: Ev fiyatı (hedef değişken)

---

## 🔧 Kullanılan Kütüphaneler

- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib` (grafikler için)
- `seaborn` (grafikler için)

---

## 🧠 Kullanılan Modeller

1. **Linear Regression**
2. **Random Forest Regressor**

Her iki model ayrı ayrı eğitilmiş ve test edilmiştir. Performans ölçütleri karşılaştırılarak en iyi model seçilmiştir.

---

## 📈 Model Performans Karşılaştırması

| Ölçüt           | Linear Regression | Random Forest Regressor |
|------------------|------------------|--------------------------|
| **MAE**          | 3,875 TL         | 1,213 TL                |
| **MSE**          | 109,276,524      | 53,715,233              |
| **RMSE**         | 10,453 TL        | 7,331 TL                |
| **R² Score**     | 0.66             | 0.83                    |
| **MAPE**         | %24.29           | %2.00                   |

📌 **Yorum:** Random Forest modeli, tüm metriklerde daha başarılı performans göstermiştir. Özellikle %2’lik MAPE değeri, oldukça güvenilir tahminler yapıldığını göstermektedir.

---

## 📁 Proje Dosyaları

- `ugurzi_kira_tahmin.ipynb.ipynb`: Tüm veri işleme, modelleme ve değerlendirme adımlarını içeren Jupyter defteri
- `istanbul_rent_data/`: Veri seti dosyalarının bulunduğu klasör (CSV formatında)
- `README.md`: Proje tanımı

---

## 🚀 Nasıl Çalıştırılır?

```bash
# Ortamı oluştur
python -m venv venv
source venv/bin/activate  # Windows için: venv\Scripts\activate

# Jupyter defterini aç
jupyter notebook
