# Prediksi Suhu Udara Menggunakan Model Regresi

## Gambaran Proyek

Proyek ini mengimplementasikan dan membandingkan model Regresi Linear dan Regresi Polinomial untuk memprediksi suhu udara berdasarkan data cuaca historis. Model-model tersebut menganalisis hubungan antara berbagai parameter cuaca (kelembaban, tekanan udara, kecepatan angin) dan suhu untuk menciptakan sistem prediksi yang akurat.

## 📊 Dataset
Dataset berisi 96.453 catatan cuaca historis dengan fitur-fitur utama berikut:
- Suhu (°C) - Variabel target
- Apparent Temperature (°C)
- Kelembaban
- Kecepatan Angin (km/h)
- Arah Angin (derajat)
- Jarak Pandang (km)
- Tutupan Awan
- Tekanan Udara (millibars)
- Jenis Presipitasi (hujan/salju)

## 🔍 Metodologi
## Eksplorasi Data & Pra-pemrosesan
- Analisis statistik semua variabel
- Visualisasi distribusi menggunakan histogram dan boxplot
- Penanganan nilai kosong dan data duplikat
- Pengkodean fitur untuk variabel kategorikal
- Analisis korelasi untuk memahami hubungan antar fitur
- Deteksi dan penanganan outlier menggunakan metode IQR
- Normalisasi data dengan RobustScaler

## Implementasi Model

### Regresi Linear
- Implementasi sederhana dengan scikit-learn
- Pembagian data latih-uji 80/20

### Regresi Polinomial
- Implementasi dengan regularisasi Ridge
- Tuning hyperparameter melalui GridSearchCV
- Parameter optimal: degree=4, alpha=0.1

## Metrik Evaluasi
Kedua model dievaluasi menggunakan:
- Mean Squared Error (MSE)
- R-squared (R²)
- Mean Absolute Error (MAE)

## 📈 Hasil

| Model | MSE | R² | MAE |
| --- | --- | --- | --- |
| Regresi Linear | 0,0062 | 0,9862 | 0,0521 |
| Regresi Polinomial | 0,0015 | 0,9966 | 0,0184 |

## 🔑 Temuan Utama

- Apparent Temperature memiliki korelasi terkuat dengan suhu aktual
- Kelembaban menunjukkan korelasi negatif dengan suhu
- Regresi Polinomial dengan degree=4 memberikan akurasi prediksi yang sangat baik
- Kedua model menunjukkan nilai R² yang tinggi, namun Regresi Polinomial menawarkan performa yang lebih unggul

## 👥 Kontributor

- M. Nabil Maulana (2208107010011)
- Irfan Rizadi (2208107010062)
- Maulana Fikri (2208107010042)
- Indriani Miza Alfiyanti (2208107010026)
- Raihan Firyal (2208107010084)
