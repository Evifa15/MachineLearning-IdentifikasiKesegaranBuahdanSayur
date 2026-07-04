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
## 📊 Hasil & Evaluasi (Uji Kualitas)
Kinerja sistem telah divalidasi berdasarkan standar kualitas perangkat lunak ISO 25010 dengan hasil sebagai berikut:

* **Fungsionalitas:** Model berhasil mengenali 9 jenis komoditas dengan akurasi tinggi dan mampu membedakan status kesegaran secara konsisten meski terdapat variasi posisi dan sudut pengambilan foto.
* **Keandalan:** Sistem menunjukkan stabilitas tinggi, mampu memproses gambar dengan kondisi pencahayaan atau resolusi yang kurang ideal, serta dilengkapi dengan penanganan *error* yang informatif.
* **Kemudahan Penggunaan:** Hasil prediksi dilengkapi dengan *confidence score* yang jelas dan mudah diinterpretasikan oleh pengguna aplikasi *mobile*.
* **Efisiensi:** Menggunakan arsitektur MobileNetV2, sistem ini sangat ringan sehingga memberikan *response time* yang sangat cepat di *cloud server*.
* **Pemeliharaan & Portabilitas:** Struktur kode dirancang secara modular, memudahkan pengembangan fitur baru maupun integrasi ke berbagai *platform* aplikasi.

## ⚙️ Panduan Implementasi (Mobile to Cloud)
Untuk mengimplementasikan model ini ke dalam aplikasi *mobile* via *cloud server*, ikuti alur berikut:

1. **Backend (Cloud Server):**
    * Muat model menggunakan: `tf.keras.models.load_model('Fresee.h5')`.
    * Buat API *endpoint* (misal: menggunakan Flask/FastAPI) yang menerima gambar melalui HTTP `POST` request.
    * Pastikan gambar di-*resize* ke (224, 224) dan dinormalisasi sebelum masuk ke model.

2. **Frontend (Aplikasi Mobile):**
    * Aplikasi menangkap foto menggunakan kamera/galeri.
    * Gambar dikirimkan ke *endpoint* server.
    * Tampilkan label (Segar/Busuk) dan *confidence score* yang diterima dari respon server.

## 📁 Struktur Repositori
* `models/`: Berisi dokumentasi teknis dan panduan penggunaan model `.h5`.
* `notebooks/`: Berisi file `Fresee.ipynb` (seluruh kode pengembangan sistem).
* `requirements.txt`: Daftar dependensi *library* Python yang diperlukan.

## 📝 Dokumentasi Teknis
Detail lebih lanjut mengenai proses *training*, pengujian, dan teknis arsitektur dapat dilihat pada file:
* [models/model_documentation.ipynb](models/model_documentation.ipynb)
