<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"><img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"></a>

<div align= "center">
    <h2> CUSTOMER-CHURN-ANALYSIS-TELWAVE-TECHNOLOGY </h2><br>
</div>

<div align= "center">
    <img src="https://camo.githubusercontent.com/896b68c9d0df47c2c13475f29506cdab373599559d1e231e624c655f3d46eace/68747470733a2f2f7370656369616c732d696d616765732e666f72626573696d672e636f6d2f696d61676573657276652f3566316664363739633430343964376265633637346339322f39363078302e6769663f6669743d7363616c65">
</div>

## Author - JCDS 2704
* Angga Sukma Budi Darmawan 
* Nabila Lailinajma
* Muhammad Hafizh Bayhaqi

## 🌐 Overview
Telwave Technology adalah perusahaan penyedia layanan internet, WiFi, dan telepon untuk pelanggan individu maupun bisnis. Beroperasi di industri yang kompetitif dan price-sensitive, Telwave menghadapi tantangan besar dalam mempertahankan pelanggan.

Dengan churn rate mencapai 26%, jauh di atas rata-rata industri, kehilangan pelanggan menjadi ancaman serius bagi profitabilitas. Karena biaya mendapatkan pelanggan baru jauh lebih mahal daripada mempertahankan pelanggan lama, pendekatan berbasis data sangat penting untuk memprediksi dan mencegah churn.

Proyek ini bertujuan untuk menganalisis pola perilaku pelanggan, mengidentifikasi faktor-faktor utama penyebab churn, serta membangun model prediktif untuk mendeteksi pelanggan berisiko tinggi.

## 🎯 Objective
* Menganalisis pola perilaku pelanggan dan faktor utama penyebab churn menggunakan data layanan, transaksi, dan kepuasan pelanggan.
* Mengidentifikasi segmen pelanggan dengan risiko churn tinggi sebagai dasar untuk strategi retensi yang lebih terarah.
* Membangun model machine learning prediktif untuk memproyeksikan kemungkinan churn dan mendukung pengambilan keputusan berbasis data.

## 💡 Key Insights
* Kontrak bulanan (month-to-month) menyebabkan tingkat churn yang lebih tinggi (42,71%)
* Skor kepuasan memiliki korelasi yang sangat kuat dengan churn
* Jenis layanan internet Fiber Optic menyebabkan tingkat churn yang lebih tinggi (41,9%)

## Dataset
```
01] CustomerID  
02] Gender  
03] SeniorCitizen  
04] Age  
05] Married  
06] City  
07] Country  
08] ZipCode  
09] Population  
10] Latitude  
11] Longitude  
12] Partner  
13] Dependents  
14] PhoneService  
15] MultipleLines  
16] InternetService  
17] StreamingTV  
18] StreamingMovies  
19] StreamingMusic  
20] UnlimitedData  
21] Contract  
22] PaperlessBilling  
23] PaymentMethod  
24] OnlineSecurity  
25] OnlineBackup  
26] DeviceProtection  
27] TechSupport  
28] Referrals  
29] ReferredFriend  
30] SatisfactionScore  
31] Tenure  
32] MonthlyCharges  
33] TotalCharges  
34] TotalExtraDataCharges  
35] TotalLongDistanceCharges  
36] TotalRefunds  
37] TotalRevenue  
38] AvgMonthlyGBDownload  
39] AvgMonthlyLongDistanceCharges  
40] Churn  
41] ChurnCategory  
42] ChurnReason  
43] ChurnScore  
44] CLTV
```

## 🧠 Model Candidate
Beberapa algoritma klasifikasi telah diuji, termasuk:
* Logistic Regression
* Random Forest
* XGBoost
* K-Nearest Neighbors
* Decision Tree
Evaluasi model dilakukan menggunakan metrik F2-Score.
Model dengan performa terbaik kemudian disempurnakan menggunakan GridSearchCV.

## ✅ Model Selected and Evaluation
|         ALGORITHMS        | RESAMPLER     |
| --------------------------| --------------| 
| Logistic Regression       | Random Under Sampler |

#### Classification Report - Train Data

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.98      | 0.95   | 0.96     | 4130    |
| 1     | 0.87      | 0.95   | 0.91     | 1495    |
| **Accuracy**   |           |        | 0.95     | 5625    |
| **Macro Avg**  | 0.92      | 0.95   | 0.94     | 5625    |
| **Weighted Avg** | 0.95    | 0.95   | 0.95     | 5625    |

#### Classification Report - Test Data

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.98      | 0.94   | 0.96     | 1033    |
| 1     | 0.86      | 0.94   | 0.90     | 374     |
| **Accuracy**   |           |        | 0.94     | 1407    |
| **Macro Avg**  | 0.92      | 0.94   | 0.93     | 1407    |
| **Weighted Avg** | 0.94    | 0.94   | 0.94     | 1407    |

#### F2-Score

| Dataset | F2-Score |
|---------|----------|
| Train   | 0.9347   |
| Test    | 0.9191   |

## ⭐️ Kesimpulan

Berdasarkan hasil analisis churn pada data pelanggan Telwave, dapat disimpulkan bahwa:

1. **Penyebab Utama Churn**: Tingginya churn rate disebabkan oleh faktor kompetitor, terutama penawaran yang lebih menarik, perangkat yang lebih baik, serta kuota data dan kecepatan internet yang lebih tinggi. Hal ini menandakan perlunya Telwave meningkatkan proposisi nilai yang ditawarkan kepada pelanggan dalam hal harga, promo, dan kualitas layanan.

2. **Peran Model Prediksi Churn**: Model prediksi churn yang dibangun dapat mengidentifikasi pelanggan berisiko tinggi untuk churn berdasarkan karakteristik dan perilaku mereka. Model ini dapat digunakan untuk:
   - Segmentasi pelanggan berisiko tinggi, seperti pelanggan dengan kontrak bulanan, pengguna fiber optic, dan skor kepuasan rendah.
   - Menyusun intervensi retensi yang lebih tepat, seperti penawaran bundling, diskon harga, atau program loyalitas.
   - Mengurangi churn rate secara proaktif dengan fokus pada pelanggan berisiko tinggi.

Dengan menggabungkan wawasan dari analisis churn dan model prediktif, Telwave memiliki peluang untuk meningkatkan retensi pelanggan dan memperkuat posisinya di pasar telekomunikasi yang kompetitif.

## 💸 Keuntungan Model

Dalam skenario tanpa model, seluruh pelanggan diasumsikan akan churn, sehingga seluruhnya menjadi target program retensi. Hal ini menyebabkan **tidak ada pelanggan yang diklasifikasikan sebagai "True Negative"**, dan semua pelanggan non-churn mendapat perlakuan intervensi yang tidak diperlukan.

Sebaliknya, model prediksi churn mampu mengklasifikasikan pelanggan dengan lebih tepat, mengurangi jumlah intervensi yang tidak perlu, serta meminimalkan kehilangan pelanggan akibat tidak ditindaklanjuti.

##### Asumsi Biaya:
- **False Positive (FP)**: Pelanggan tidak churn namun tetap diberi retensi → *Retention Cost*: **$10.3**
- **False Negative (FN)**: Pelanggan churn tapi tidak ditindaklanjuti → *Customer Acquisition Cost*: **$53**

##### Hasil Perhitungan Biaya:

| Metode             | FP  | FN | Total Kerugian                                 |
|--------------------|-----|----|------------------------------------------------|
| **Tanpa Model**    | 1033| 0  | (1033 × $10.3) + (0 × $53) = **$10,949.80**    |
| **Dengan Model**   | 67  | 25 | (67 × $10.3) + (25 × $53) = **$2,035.20**      |

##### Perbandingan:

| Metode             | Total Kerugian | Perbandingan              |
|--------------------|----------------|---------------------------|
| **Tanpa Model**    | $10,949.80     | **5.38× lebih buruk**     |
| **Dengan Model**   | $2,035.20      | **Paling optimal**        |

##### Kesimpulan:

Model prediksi churn secara signifikan **menurunkan biaya intervensi** dengan hanya menargetkan pelanggan yang benar-benar berisiko tinggi untuk churn. Strategi ini tidak hanya menghemat biaya retensi dan akuisisi pelanggan, tetapi juga memungkinkan alokasi sumber daya yang lebih efektif dan berdampak langsung pada **peningkatan efisiensi dan profitabilitas bisnis**.

Dengan total kerugian **lebih dari lima kali lebih rendah**, pendekatan berbasis model terbukti jauh lebih unggul dibandingkan asumsi tanpa segmentasi. Oleh karena itu, penggunaan model prediktif sangat direkomendasikan sebagai bagian dari strategi retensi pelanggan yang data-driven dan berkelanjutan.

## Link Resources

- [Link Tableau](https://s.id/Alpha-Tableau-ChurnAnalysis)
- [Link Powerpoint](https://s.id/Alpha-PPT-ChurnAnalysis)
- [Link App](https://telwave-customer-churn-prediction.streamlit.app/)
