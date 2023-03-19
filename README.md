# Final Project Marketing Campaign 
1. [Description](#Description)
2. [Summary Stage 1 Insight](#Summary-Stage-1-Insight)
3. [Summary Stage 2 - 4 Insight](#Summary-Stage-2---4-Insight) 
# Description

**Goal:** Membuat marketing campaign yang tepat sasaran dengan memanfaatkan predictive modelling yang dapat memprediksi kemungkinan seorang customer untuk merespon campaignnya atau tidak.

**Dataset:** [Marketing Campaign](https://www.kaggle.com/rodsaldanha/arketing-campaign)

# Summary Stage 1 Insight:	
1.	Customer dengan income diatas 120000 tidak ada yang menerima campaign perusahaan. Jadi sebaiknya perusahaan fokus melakukan campaign kepada customer dengan income dibawah 120000.
2.	Kategori customer yang menerima Response (marketing campaign terakhir) terbanyak berasal dari tahun lahir 1970-1975. Jika perusahaan harus memprioritaskan beberapa customer saja, maka perusahaan dapat memilih customer yang lahir pada tahun 1970-1985 untuk menawarkan sebuah campaign.
3.	Berdasarkan Recency (kapan terakhir kali customer melakukan pembayaran), semakin rendah Recency maka semakin besar kemungkinan customer tersebut menerima marketing campaign perusahaan yang terakhir (Response). Sehingga marketing campaign selanjutnya dapat difokuskan kepada customer dengan Recency yang rendah.
4.	Semakin sedikit pembelian yang dilakukan (baik yang menggunakan diskon ataupun yang melalui web, catalog, store), maka semakin besar kemungkinan customer untuk menerima Response (marketing campaign terakhir). Sehingga perusahaan dapat menargetkan campaign kepada customer dengan jumlah pembelian yang masih sedikit.
5.	Semakin tinggi jumlah anak/remaja yang dimiliki customer, maka semakin kecil kemungkinan customer menerima Response (marketing campaign terakhir), sehingga lebih baik perusahaan menargetkan campaign kepada customer yang tidak memiliki anak/remaja.

# Summary Stage 2 -4  Insight:
1. Handle Missing Value: menghapus missing value yang ada di kolom Income
2. Handle Duplicated Data: tidak terdapat data duplikat
3. Feature Extraction: membuat kolom baru yaitu kolom Age dari kolom Year_Birth, dan kolom Dependent dari kolom Kidhome dan Teenhome
4. Feature Encoding:
    - Melakukan label encoding pada kolom Education
    - Melakukan OHE pada kolom Marital_Status
    - Kemudian dihapus kolom Education dan Marital_Status
5. Feature Selection: membuang kolom yang kurang relevan, yaitu: ID, Z_CostContract, Z_Revenue, Complain, Year_Birth, Kidhome, Teenhome, Dt_Customer
6. Handle outliers: menghapus data outlier pada kolom yang memiliki data outilier dengan menggunakan Z-Score
7. Split Data: memisahkan data train dan data test
8. Feature Transformation:
    - Melihat nilai skew data
    - Normalization pada kolom Income, Age, Dependents, dan Recency
    - Standarization pada kolom NumWebVisitsMonth
    - Melakukan Log Transformation pada kolom MntWines, MntFruits, MntMeatProducts, MntFishProducts,
MntSweetProducts, MntGoldProds, NumDealsPurchases, NumWebPurchases, dan NumStorePurchases
9. Handle Class Imbalance: melakukan oversampling dengan metode SMOTE
