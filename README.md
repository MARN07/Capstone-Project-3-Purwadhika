# Capstone Project 3 - California Housing

## A. Business Problem Understanding

**Context**

Dataset California Housing berisi informasi mengenai properti perumahan di California dan digunakan untuk menganalisis faktor-faktor yang mempengaruhi nilai properti. Data ini meliputi atribut-atribut seperti koordinat geografis, usia rumah, jumlah ruangan, penduduk, dan pendapatan median. Dataset ini sering digunakan untuk memodelkan dan memprediksi nilai rumah berdasarkan berbagai fitur, serta untuk mengevaluasi faktor-faktor yang mempengaruhi harga properti di wilayah tersebut.

Dataset ini digunakan pada bab kedua dari buku terbaru Aurélien Géron, Hands-On Machine Learning with Scikit-Learn and TensorFlow. Dataset ini berisi informasi dari sensus California tahun 1990 dan merupakan pengantar yang sangat baik untuk menerapkan algoritma machine learning. Dataset ini mencakup berbagai fitur terkait perumahan dan demografi dalam sebuah blok di California, menjadikannya cocok untuk mengajarkan dasar-dasar machine learning.

**Problem Statement**

Banyak developer dan individu yang sulit untuk mendapatkan harga rumah terbaik, dikarenakan minimnya informasi dan tidak adanya perhitungan dasar untuk menentukan harga rumah terutama di California. Tujuan dari analisis ini adalah untuk memahami faktor-faktor apa saja yang mempengaruhi nilai rumah di California dan bagaimana berbagai features mempengaruhi harga rumah. Dengan informasi ini, kita dapat membangun model yang memprediksi nilai rumah secara akurat. Dataset California Housing menyediakan data yang relevan untuk melakukan analisis ini.


**Goals**

1.  Identifikasi Faktor-Faktor yang Mempengaruhi Nilai Rumah:
    -   Menentukan variabel-variabel yang signifikan dalam mempengaruhi nilai rumah berdasarkan data yang tersedia.
        Mengidentifikasi pola-pola yang ada dalam data yang dapat menjelaskan variasi nilai rumah.
    
2.  Pengembangan Model Prediktif:
    -   Membangun model klasifikasi atau regresi yang dapat memprediksi nilai rumah berdasarkan fitur-fitur yang ada.
        Mengukur seberapa baik model tersebut dalam memprediksi nilai rumah dan mengevaluasi performanya.

3.  Penerapan Insights untuk Pengambilan Keputusan:
    -   Memberikan wawasan yang berguna untuk investor, agen real estate, atau perencana kota mengenai faktor-faktor yang mempengaruhi harga properti.
        Menyediakan informasi yang bisa digunakan untuk perencanaan dan pengambilan keputusan terkait investasi properti.


**Analytics Approach**

Kami akan melakukan analisis regresi dengan variabel target berupa harga rumah dan fitur-fitur yang meliputi housing_median_age, total_rooms, population, total_bedrooms, dan lainnya. Tahapan pertama dalam analisis ini adalah memahami data beserta atribut yang ada. Selanjutnya, kami akan membersihkan data dari nilai yang hilang (missing values), duplikasi, dan anomali lainnya. Setelah itu, kami akan mencari wawasan dari data melalui analisis eksplorasi data (Exploratory Data Analysis, EDA). Setelah data siap, langkah berikutnya adalah pengolahan data agar dapat diproses oleh model machine learning.

Setelah data dipersiapkan, kami akan melakukan proses pemodelan machine learning melalui beberapa eksperimen untuk memperoleh nilai skor yang memadai yang dapat menggambarkan hasil prediksi model. Untuk mengevaluasi goodness of fit dari model yang telah dikembangkan, kami akan menggunakan beberapa metrik, yaitu RMSE dan MAPE. Akhirnya, kami akan menyusun rekomendasi bisnis yang relevan berdasarkan analisis yang dilakukan, sehingga pemangku kepentingan dapat menggunakan prediksi harga rumah untuk meningkatkan keuntungan.


**Evaluation Metric**

Setelah melakukan evaluasi terhadap berbagai model, kami memutuskan untuk menggunakan Extra Gradient Boosting Regressor sebagai model utama, penggunakan model XGBoost (Extreme Gradient Boosting) baik digunakan pada data ini, dikarenakan data ini memiliki banyak outliers, sedangkan model XGBoost (Extreme Gradient Boosting) tahan terhadap banyaknya outliers. Metrik utama yang kami pilih adalah Root Mean Square Error (RMSE) dan Mean Absolute Percentage Error (MAPE), dengan dua metrik pendukung, yaitu Mean Absolute Error (MAE) dan R². Prediksi harga rumah merupakan tantangan yang kompleks karena banyaknya fitur yang memengaruhi kualitas prediksi. Beberapa fitur mengalami multikolinearitas, yang dapat memengaruhi hasil. Penggunaan XGBoost diharapkan dapat menangani data yang mengandung banyak outlier dan fitur dengan korelasi tinggi.

Dalam analisis ini, penggunaan RMSE dan MAPE dipilih karena RMSE efektif dalam mengukur kesalahan absolut dari prediksi, sementara MAPE menghitung persentase kesalahan relatif terhadap nilai aktual. Dengan pendekatan ini, kami bertujuan untuk mencapai skor yang tidak hanya menunjukkan kinerja yang baik, tetapi juga mencerminkan kondisi keadaan yang sebenarnya. Metodologi ini sangat krusial dalam konteks prediksi harga rumah, di mana variabilitas dalam total ruangan, total kamar, rata-rata penghasilan, dan faktor-faktor lain harus dipertimbangkan untuk memastikan model memberikan prediksi yang akurat dan konsisten.
