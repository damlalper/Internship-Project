# Internship-Project
# FLO Satış Tahmin Sistemi - Staj Projesi

> **Not:** Bu repository yalnızca proje dokümantasyonu ve README için oluşturulmuştur. Kod ve veriler paylaşılmamaktadır.

---

## Proje Hakkında

Bu proje, FLO için bir **satış tahmin sistemi** geliştirme amacını taşımaktadır. Amaç, geçmiş satış verileri ve ek iş verilerini kullanarak, ürün ve mağaza bazında doğru tahminler yapmak ve iş kararlarını desteklemektir. Proje kapsamında hem klasik makine öğrenmesi modelleri hem de ileri teknikler (ensemble, hyperparameter tuning, pipeline) kullanılmıştır.

---

## Kullanılan Teknolojiler

- **Veri İşleme & ETL:**
  - Python (Pandas, PySpark)
  - SQL
  - Apache Airflow / Prefect / Luigi (ETL orkestrasyonu)
- **Veri Analizi (EDA):**
  - Python (Pandas, Matplotlib, Seaborn)
  - veri görselleştirme, trend ve sezon analizi, eksik veri tespiti.
- **Feature Engineering**
  -scaling, encoding, yeni feature yaratımı, etkileşim değişkenleri.
- **Modelleme & ML Ops:**
  - Scikit-Learn, XGBoost, LightGBM, CatBoost
  - MLflow (model versiyonlama & kaydı)
  - Optuna / RandomizedSearch (hyperparametre optimizasyonu)
  - Docker + Kubernetes (model dağıtımı ve ölçekleme)
- **API & Servis Katmanı:**
  - FastAPI (model tahminlerini API üzerinden sağlama)
  - Batch job entegrasyonu (periyodik tahmin üretimi)
- **Görselleştirme & Dashboard:**
  - Streamlit, Dash, Power BI
  - Grafikler: gerçek vs tahmin, senaryo bazlı analizler
- **Model İzleme:**
  - Evidently AI, Arize AI
  - Prometheus + Grafana (performans metric takibi)
- **Depolama:**
  - PostgreSQL, BigQuery, S3 (veri ve model saklama)

---

## Proje Akışı

1. **Veri Hazırlama:**
   - Eksik değer imputation, standartlaştırma (scaler) ve kategorik encoding.
   - KFold / TimeSeriesSplit ile doğrulama stratejisi uygulanması.
   - Veri Analizi (EDA)
   - Feature Engineering ve veri hazırlığı

2. **Modelleme:**
   - Baseline modeller ile başlangıç.
   - Hyperparameter tuning (Optuna/RandomizedSearch) ile model optimizasyonu.
   - Early stopping ve regularizasyon ile overfitting kontrolü.
   - Feature importance / SHAP ile en etkili değişkenlerin analizi.
   - Stacking ve ensemble yöntemleri ile performans artırımı.

3. **Model Sonrası Aşamalar:**
   - Model karşılaştırma raporu: RMSE, MAPE, R² gibi metrikler.
   - Tahmin görselleştirmeleri: gerçek vs tahmin, hata dağılımları, senaryo bazlı grafikler.
   - Pipeline oluşturulması: veri hazırlama + model + tahmin üretimi.
   - API veya batch job ile otomatik tahmin üretimi.
   - Dashboard: kullanıcı dostu görselleştirmeler, filtreler (bölge, ürün vb.)

4. **Model İzleme & Geri Bildirim:**
   - Model performans degradasyonu takibi (drift analizi).
   - İş birimi geri bildirimi ile tahminlerin doğruluğu ve iş değerine katkısı ölçülmesi.

5. **Kurumsal Katma Değer:**
   - What-if analizleri (kampanya artırımı, stok değişiklikleri vb.)
   - Risk ve güven aralıkları (%95 CI)
   - Tahminlerin iş değerine etkisinin ölçülmesi (ROI hesabı)

---

## Notlar

- Bu repository **sadece proje dokümantasyonu içindir**, kod ve veri paylaşımı yapılmamaktadır.
- Proje, **staj kapsamında gerçekleştirilmiş olup**, FLO iş süreçlerine örnek bir satış tahmin sistemi sunmaktadır.
- Projenin amacı **iş kararlarını desteklemek ve tahmin doğruluğunu artırmaktır**, gerçek veriler paylaşılamamaktadır.

---

## Yazar

**Damla Nur Alper** – Bilgisayar Mühendisliği 3. sınıf öğrencisi  
Staj Projesi: FLO Prediction System
