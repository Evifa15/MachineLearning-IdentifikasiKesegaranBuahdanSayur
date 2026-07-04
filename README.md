# 🍎 Model Machine Learning: Identifikasi Kesegaran Buah dan Sayur
Proyek ini merupakan model identifikasi kesegaran buah dan sayur yang dikembangkan menggunakan teknik *Machine Learning* dengan arsitektur **CNN MobileNetV2** melalui metode ***Transfer Learning***. Model ini dirancang untuk memproses input gambar komoditas dan memberikan klasifikasi mengenai nama komoditas serta status kesegarannya (Segar atau Tidak Segar).
## Deskripsi Proyek
Model ini menggunakan pendekatan *Deep Learning* untuk membedakan kategori buah dan sayur. Prototipe ini telah dilatih menggunakan dataset dengan rincian sebagai berikut:
| No | Aspek | Total | Deskripsi |
| :--- | :--- | :--- | :--- |
| 1 | **Kelas** | 18 | *freshapples, freshbanana, freshbittergroud, freshcapsicum, freshcucumber, freshokra, freshoranges, freshpotato, freshtomato, rottenapples, rottenbanana, rottenbittergroud, rottencapsicum, rottencucumber, rottenokra, rottenoranges, rottenpotato, rottentomato.* |
| 2 | **Gambar** | 30.357 | Total seluruh gambar yang digunakan untuk proses pelatihan dan validasi. |
| 3 | **Komoditas** | 9 | *Apples, Banana, Bittergroud, Capsicum, Cucumber, Okra, Oranges, Potato, Tomato.* |
## Dataset
Keseluruhan dataset yang digunakan dalam pengembangan model ini bersumber dari [Kaggle: Fresh and Stale Classification](https://www.kaggle.com/datasets/swoyam2609/fresh-and-stale-classification). 
## Hasil & Evaluasi (Uji Kualitas)
Model mencapai akurasi keseluruhan sebesar **99%** pada data pengujian. Berikut adalah rincian metrik performa model:
| Kelas | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| freshapples | 0.99 | 1.00 | 0.99 | 189 |
| freshbanana | 1.00 | 1.00 | 1.00 | 180 |
| freshbittergroud | 1.00 | 1.00 | 1.00 | 32 |
| freshcapsicum | 1.00 | 1.00 | 1.00 | 99 |
| freshcucumber | 0.92 | 0.86 | 0.89 | 28 |
| freshokra | 0.97 | 0.95 | 0.96 | 61 |
| freshoranges | 1.00 | 1.00 | 1.00 | 170 |
| freshpotato | 1.00 | 0.91 | 0.95 | 53 |
| freshtomato | 0.99 | 0.99 | 0.99 | 178 |
| rottenapples | 1.00 | 0.99 | 1.00 | 269 |
| rottenbanana | 1.00 | 1.00 | 1.00 | 247 |
| rottenbittergroud | 1.00 | 1.00 | 1.00 | 36 |
| rottencapsicum | 1.00 | 1.00 | 1.00 | 90 |
| rottencucumber | 0.82 | 0.98 | 0.89 | 41 |
| rottenokra | 0.90 | 0.64 | 0.75 | 14 |
| rottenoranges | 1.00 | 1.00 | 1.00 | 182 |
| rottenpotato | 0.94 | 1.00 | 0.97 | 75 |
| rottentomato | 0.99 | 0.99 | 0.99 | 155 |
| **Accuracy** | | | **0.99** | **2099** |
* `requirements.txt`: Daftar dependensi *library* Python yang diperlukan.

## 📝 Dokumentasi Teknis
Detail lebih lanjut mengenai proses *training*, pengujian, dan teknis arsitektur dapat dilihat pada file:
* [models/model_documentation.ipynb](models/model_documentation.ipynb)
