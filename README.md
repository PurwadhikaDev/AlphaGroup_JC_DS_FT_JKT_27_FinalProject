<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"><img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"></a>

<div align= "center">
    <h2> CUSTOMER-CHURN-ANALYSIS-TELWAVE-TECHNOLOGY </h2><br>
</div>

<div align= "center">
    <img src="https://camo.githubusercontent.com/896b68c9d0df47c2c13475f29506cdab373599559d1e231e624c655f3d46eace/68747470733a2f2f7370656369616c732d696d616765732e666f72626573696d672e636f6d2f696d61676573657276652f3566316664363739633430343964376265633637346339322f39363078302e6769663f6669743d7363616c65">
</div>

## Overview
Telwave Technology adalah perusahaan penyedia layanan internet, WiFi, dan telepon untuk pelanggan individu maupun bisnis. Beroperasi di industri yang kompetitif dan price-sensitive, Telwave menghadapi tantangan besar dalam mempertahankan pelanggan.

Dengan churn rate mencapai 26%, jauh di atas rata-rata industri, kehilangan pelanggan menjadi ancaman serius bagi profitabilitas. Karena biaya mendapatkan pelanggan baru jauh lebih mahal daripada mempertahankan pelanggan lama, pendekatan berbasis data sangat penting untuk memprediksi dan mencegah churn.

Proyek ini bertujuan untuk menganalisis pola perilaku pelanggan, mengidentifikasi faktor-faktor utama penyebab churn, serta membangun model prediktif untuk mendeteksi pelanggan berisiko tinggi.

## Objective
* Menganalisis pola perilaku pelanggan dan faktor utama penyebab churn menggunakan data layanan, transaksi, dan kepuasan pelanggan.
* Mengidentifikasi segmen pelanggan dengan risiko churn tinggi sebagai dasar untuk strategi retensi yang lebih terarah.
* Membangun model machine learning prediktif untuk memproyeksikan kemungkinan churn dan mendukung pengambilan keputusan berbasis data.

## Key Insights
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

## Modeling
Beberapa algoritma klasifikasi telah diuji, termasuk:
* Logistic Regression
* Random Forest
* XGBoost
* K-Nearest Neighbors
* Decision Tree
Evaluasi model dilakukan menggunakan metrik F2-Score.
Model dengan performa terbaik kemudian disempurnakan menggunakan GridSearchCV.

## Model Evaluation
|         ALGORITHMS        | TRAINING  DATA F-2 SCORE | TESTING DATA F-2 SCORE |
| --------------------------| ----------------------------- | --------------------------- |
| Logistic Regression       |            0.9271             |           0.8639            |
| Random Forest             |            0.8902             |           0.8413            |
| Support Vector Machine    |            0.9349             |           0.8662            |
| XGBoost                   |            1.0000             |           0.8526            |
| LightGBM                  |            1.0000             |           0.8390            |
| CatBoost                  |            0.9845             |           0.8503            |
| AdaBoost                  |            0.9077             |           0.8322            |
