# 🐾 Proyek Klasifikasi Gambar : Anjing vs Kucing
Proyek ini bertujuan membangun model deep learning untuk membedakan gambar **Anjing** dan **Kucing** menggunakan **TensorFlow** dan aktivasi **ReLU**. Dataset diambil dari Kaggle.

---

## 📂 Dataset
- **Sumber**: [Kaggle - Cat vs Dog Dataset](https://www.kaggle.com/datasets/karakaggle/kaggle-cat-vs-dog-dataset)
- **Isi**: Ribuan gambar anjing dan kucing dengan berbagai variasi pose.
- **Format**: File gambar JPEG, ukuran bervariasi.

---

## 🛠 Tools & Library
- Python 3.x
- TensorFlow / Keras
- scikit-learn
- Matplotlib
- NumPy
- Kaggle API (untuk download dataset)

---

## 📈 Alur Proyek
1. Download dataset dari Kaggle
2. Ekstrak dan praproses gambar
3. Split data menjadi Train, Validation, dan Test
4. Augmentasi data untuk training set
5. Membangun dan melatih model CNN
6. Evaluasi model di data test
7. Visualisasi grafik akurasi dan loss
8. Simpan model dalam format SavedModel, TFLite, atau TFJS
9. Lakukan prediksi pada gambar baru

---

## ⚙️ Langkah Menjalankan

1. **Clone repo / buat folder kerja**
2. **Download dataset dari Kaggle**
3. **Install dependensi**
    ```bash
    pip install tensorflow keras scikit-learn matplotlib kaggle
    ```
4. **Setting Kaggle API key** (upload `kaggle.json`)
    ```python
    from google.colab import files
    files.upload()
    
    !mkdir -p ~/.kaggle
    !cp kaggle.json ~/.kaggle/
    !chmod 600 ~/.kaggle/kaggle.json
    ```
5. **Download Dataset**
    ```bash
    !kaggle datasets download -d karakaggle/kaggle-cat-vs-dog-dataset
    !unzip kaggle-cat-vs-dog-dataset.zip
    ```

6. **Training Model** menggunakan TensorFlow

---

## 🎯 Hasil
- Model dapat mencapai akurasi validasi hingga **~89,72%**.
- Model dapat mengklasifikasikan gambar baru dengan akurasi tinggi.


## ✨ Catatan Tambahan
- Data augmentasi (`ImageDataGenerator`) sangat penting untuk mencegah overfitting.
- Gunakan **EarlyStopping** untuk mengoptimalkan waktu training.
- Model dapat disimpan ke berbagai format untuk keperluan deployment.
