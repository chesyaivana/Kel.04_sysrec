# Sentimen dari Kolom Reviews Untuk Mengetahui Apakah Ulasan Cenderung Positif, Netral, atau Negatif.

<p align="center">
  <img src="https://github.com/user-attachments/assets/3e825d09-07f9-40ae-8cc8-fd89f768364b" alt="Sentimen dari Kolom Reviews" />
</p>

**NIM/Nama:**

- 12S210 - Dame Sitinjak
- 12S210 - Elshaday Simamora
- 12S21053 - Chesya Sitorus


# Model Pembanding
Model pembanding digunakan untuk mengevaluasi dan mengukur kinerja model utama dengan membandingkan hasil yang diperoleh dari keduanya. Tujuan utamanya adalah untuk menilai apakah model utama mampu memberikan hasil yang lebih baik atau lebih akurat dibandingkan dengan alternatif lainnya. Dengan menggunakan model pembanding, dapat diperoleh pemahaman yang lebih jelas tentang kelebihan dan kekurangan model utama, serta untuk menentukan apakah ada pendekatan yang lebih efektif dalam menyelesaikan masalah yang dihadapi. Proses perbandingan ini membantu dalam pengambilan keputusan terkait pemilihan model yang optimal berdasarkan kriteria evaluasi yang relevan.
## Model Convolutional neural network
![image](https://github.com/user-attachments/assets/ae1e3081-3f9a-4409-9ea1-bad520061c61)

Grafik ini menunjukkan perkembangan **akurasi model** selama pelatihan (train accuracy) dan validasi (validation accuracy) sepanjang beberapa **epochs**. Pada sumbu x, terdapat epoch yang mewakili jumlah iterasi atau siklus pelatihan yang dilakukan oleh model, sementara sumbu y menunjukkan nilai akurasi yang dicapai pada setiap epoch. Garis biru menunjukkan **akurasi pelatihan**, yang meningkat secara signifikan dengan bertambahnya epoch. Peningkatan ini menunjukkan bahwa model mampu belajar dari data pelatihan dan memperbaiki kinerjanya pada data yang telah dilatih.

Di sisi lain, garis oranye menggambarkan **akurasi validasi**, yang mengukur performa model pada data yang tidak digunakan selama pelatihan. Meskipun akurasi validasi juga meningkat seiring waktu, namun tidak meningkat secepat akurasi pelatihan, yang mungkin menunjukkan adanya perbedaan antara data pelatihan dan data validasi. Hal ini bisa menjadi indikasi bahwa model belum sepenuhnya dioptimalkan untuk generalisasi pada data baru, dan mungkin perlu penyesuaian lebih lanjut untuk mengurangi potensi overfitting atau meningkatkan kemampuan model untuk menangani data yang belum pernah dilihat sebelumnya.

![image](https://github.com/user-attachments/assets/1b1a45ae-fb02-448c-a69c-91ce3a5f9db4)

Grafik ini menggambarkan perubahan **akurasi model** selama pelatihan (train accuracy) dan validasi (validation accuracy) pada setiap **epoch**. Sumbu x mewakili epoch yang menunjukkan jumlah iterasi pelatihan, sementara sumbu y menunjukkan nilai akurasi yang diperoleh model pada data pelatihan dan validasi. **Akurasi pelatihan** yang diwakili oleh garis biru meningkat tajam seiring bertambahnya epoch, yang menandakan bahwa model semakin baik dalam mempelajari pola dari data pelatihan. Peningkatan ini menunjukkan bahwa model dapat belajar lebih banyak dan mengoptimalkan kinerjanya dengan data yang digunakan untuk pelatihan.

Di sisi lain, **akurasi validasi** yang digambarkan dengan garis oranye juga menunjukkan peningkatan, namun tidak secepat akurasi pelatihan. Hal ini mungkin menunjukkan adanya **overfitting**, yaitu kondisi di mana model terlalu fokus pada data pelatihan dan tidak cukup baik dalam menggeneralisasi untuk data yang belum pernah dilihat sebelumnya. Meskipun akurasi validasi meningkat, selisih antara akurasi pelatihan dan validasi ini mengindikasikan bahwa model perlu disesuaikan agar lebih mampu mengatasi data baru, dengan tujuan mengurangi ketergantungan model terhadap data pelatihan dan meningkatkan kemampuan generalisasi.

![image](https://github.com/user-attachments/assets/97c4fc74-9801-4c9a-9e4f-f5096d785d80)

MAE (Mean Absolute Error) pada grafik ini diwakili oleh batang biru dengan nilai **0.15**, yang menunjukkan bahwa model memiliki kesalahan rata-rata yang kecil, tanpa memperhatikan arah kesalahan. Semakin rendah nilai MAE, semakin baik kinerja model dalam hal akurasi prediksi. Di sisi lain, RMSE (Root Mean Squared Error) yang diwakili oleh batang hijau lebih tinggi, yaitu **0.47**. RMSE mengukur akar kuadrat dari rata-rata selisih kuadrat antara nilai prediksi dan nilai aktual, memberikan penalti yang lebih besar untuk kesalahan besar dibandingkan MAE. Oleh karena itu, meskipun model ini memiliki MAE yang relatif rendah, nilai RMSE yang lebih tinggi menunjukkan adanya kemungkinan kesalahan besar yang masih terjadi dalam beberapa prediksi.


![image](https://github.com/user-attachments/assets/591c644c-8a7f-4c99-bf63-2be5dbfd777f)

**Model Performance Metrics** dengan tiga metrik utama: **Precision**, **Recall**, dan **Mean Average Precision (MAP)**. Precision, yang diwakili oleh batang biru dengan nilai **0.78**, mengukur proporsi prediksi positif yang benar dari semua prediksi positif, menunjukkan bahwa model cukup baik dalam mengidentifikasi hasil positif yang relevan. Recall, dengan nilai **0.89** yang diwakili oleh batang hijau, menunjukkan kemampuan model untuk menangkap sebagian besar data positif yang ada, dengan nilai recall yang lebih tinggi menunjukkan bahwa model mampu mengidentifikasi sebagian besar instance positif. Sementara itu, **MAP** dengan nilai **0.86** mengukur rata-rata precision pada berbagai threshold, memberikan gambaran keseluruhan tentang seberapa baik model dalam memberikan ranking relevansi pada data positif. Secara keseluruhan, meskipun precision lebih rendah dibandingkan recall, nilai MAP yang tinggi menunjukkan bahwa model memberikan performa yang baik dalam mengurutkan hasil relevansi, meskipun masih ada ruang untuk perbaikan pada precision.


![image](https://github.com/user-attachments/assets/a4dddaf0-29a6-495d-bf19-5a9ecb2019a3)

Pembandingkan **Training RMSE** dan **Validation RMSE** seiring dengan bertambahnya jumlah **Latent Factors** dalam model. Titik bulat hitam mewakili **Training RMSE**, yang menunjukkan penurunan nilai RMSE pada data pelatihan seiring dengan meningkatnya jumlah latent factors, menandakan bahwa model semakin baik dalam menyesuaikan diri dengan data pelatihan. Sementara itu, tanda silang mewakili **Validation RMSE**, yang juga menunjukkan penurunan, meskipun dengan pola yang lebih halus. Hal ini menunjukkan bahwa model semakin baik dalam menggeneralisasi pada data validasi, meskipun peningkatan jumlah latent factors yang berlebihan dapat menyebabkan overfitting. Area yang diarsir pada grafik menggambarkan variasi RMSE pada data pelatihan dan validasi, menunjukkan bahwa semakin banyak latent factors, semakin baik kinerja model, meskipun ada potensi penurunan kinerja akibat overfitting jika jumlahnya terlalu tinggi.

## Model SVD
![image](https://github.com/user-attachments/assets/28cee611-f517-4472-b084-7447b85dfd48)

![image](https://github.com/user-attachments/assets/09eddbf3-cd1e-49a2-9d93-85960619100a)

![image](https://github.com/user-attachments/assets/e08bfc01-720b-4a73-89d9-db35cb772968)

![image](https://github.com/user-attachments/assets/9197d9e7-3f06-4dea-a6bd-0af5fcb4d097)

![image](https://github.com/user-attachments/assets/51437d8a-1779-4560-be3b-d6db2237ec96)

![image](https://github.com/user-attachments/assets/1e9107de-d52b-480f-a207-212054078800)

![image](https://github.com/user-attachments/assets/f1c7a209-4bb1-4906-9b2e-d676f8d3e06c)

![image](https://github.com/user-attachments/assets/81bda800-67b2-47df-a132-664fd3bed799)

![image](https://github.com/user-attachments/assets/f289dba7-7c03-4c91-8e53-084891b1ca4e)


# Model Hybrid Recommender Systems (CTF-IDF dan Cosine Similarity)
![image](https://github.com/user-attachments/assets/83e6ddf1-3259-4f67-b3a0-426b929a3154)
![image](https://github.com/user-attachments/assets/863dd6b3-c7af-4e02-b9c8-01fb028268f9)
![image](https://github.com/user-attachments/assets/6c6929e5-31f6-4cc6-b561-66002c42a899)
![image](https://github.com/user-attachments/assets/0366b44d-c521-43d1-a103-d12112578d70)


