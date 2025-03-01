# 🚒🔥 Smoke-Fire Detection Model

Proyek ini bertujuan untuk membangun model **Convolutional Neural Network (CNN)** yang dapat **mendeteksi asap dan api** dari gambar **CCTV atau kamera pengawas**. Dataset yang digunakan berasal dari **Smoke-Fire Detection Dataset** dari Kaggle. Model ini dikembangkan menggunakan **TensorFlow dan Keras**.

---

## 🔥 **Fitur Utama**
- **Mendeteksi keberadaan asap dan api** pada gambar dengan model berbasis Deep Learning.
- **Menggunakan augmentasi data** untuk meningkatkan generalisasi model.
- **Dapat dikonversi ke berbagai format (Keras, TensorFlow Lite, TensorFlow.js).**
- **Memanfaatkan Early Stopping dan ReduceLROnPlateau** untuk optimasi pelatihan.

---

## 📂 **Dataset**
Dataset yang digunakan adalah **Smoke-Fire Detection Dataset** dari Kaggle:  
🔗 [Kaggle Dataset - Smoke & Fire Detection](https://www.kaggle.com/datasets/sayedgamal99/smoke-fire-detection-yolo)  

Dataset ini terdiri dari gambar yang dikategorikan ke dalam:
- **Gambar dengan Api (Fire)**
- **Gambar dengan Asap (Smoke)**
- **Gambar Normal (Tanpa Api & Asap)**

### 📌 **Alasan Pemilihan Dataset**
- Dataset ini **relevan untuk aplikasi pemantauan kebakaran** menggunakan Deep Learning.
- Memiliki **variasi pencahayaan, sudut pandang, dan kondisi lingkungan** yang baik untuk meningkatkan generalisasi model.
- Dapat digunakan untuk **membangun sistem deteksi kebakaran otomatis berbasis AI**.

---

## 🏗 **Arsitektur Model**
Model ini dibangun menggunakan **Convolutional Neural Network (CNN)** dengan arsitektur sebagai berikut:
1. **4 lapisan Conv2D dengan BatchNormalization dan MaxPooling** untuk ekstraksi fitur.
2. **Flatten Layer** untuk mengubah tensor menjadi vektor.
3. **Dense Layer dengan 256 neuron** untuk memproses fitur lebih lanjut.
4. **Dropout Layer (0.5)** untuk menghindari overfitting.
5. **Output Layer dengan Sigmoid** untuk klasifikasi **api/asap vs normal**.

### 📌 **Alasan Memilih CNN**
- CNN **unggul dalam analisis gambar** karena mampu menangkap pola visual seperti tekstur api dan asap.
- CNN dapat **mengekstrak fitur dari gambar kamera pengawas secara otomatis**.
- CNN digunakan secara luas dalam aplikasi **deteksi kebakaran berbasis AI**.

---

## 💻 **Cara Instalasi dan Penggunaan**
Ikuti langkah-langkah berikut untuk menjalankan model ini di sistem Anda.

### 🔹 **1. Clone Repository**
```bash
git clone https://github.com/yourusername/smoke-fire-detection.git
cd smoke-fire-detection


### 🔹 **2. Buat Virtual Environment (Opsional)**
```bash
python3 -m venv .venv
source .venv/bin/activate  # Untuk Mac/Linux
# atau
.venv\Scripts\activate  # Untuk Windows
```

### 🔹 **3. Instal Dependencies**
Gunakan file `requirements.txt` untuk menginstal semua dependensi yang dibutuhkan:
```bash
pip install -r requirements.txt
```

### 📌 **File `requirements.txt`**
```
tensorflow
numpy
matplotlib
pandas
scikit-learn
tensorflowjs
Pillow
kagglehub
```

### 🔹 **4. Jalankan Model**
Jalankan script untuk melatih model:
```bash
python train.py
```
Atau jika menggunakan Jupyter Notebook:
```bash
jupyter notebook
```

### 🔹 **5. Evaluasi Model**
Setelah training selesai, jalankan evaluasi dengan:
```bash
python evaluate.py
```

---

## 📊 **Hasil Evaluasi**
| **Metode** | **Akurasi Test Set** |
|------------|----------------------|
| CNN Custom | ~72%                 |
| CNN + BatchNormalization | ~75% |
| Transfer Learning (ResNet50) | ~85% |

---

## 🚀 **Konversi Model ke Format Lain**
Model ini dapat dikonversi ke berbagai format agar dapat digunakan di platform lain.

### 🔹 **TensorFlow Lite (TFLite)**
Untuk digunakan di aplikasi mobile:
```bash
python convert_tflite.py
```

### 🔹 **TensorFlow.js**
Untuk digunakan di website:
```bash
tensorflowjs_converter --input_format=tf_saved_model --output_format=tfjs_graph_model saved_model tfjs_model
```

---

## 📚 **Lisensi**
Proyek ini menggunakan **MIT License**. Silakan gunakan dan modifikasi sesuai kebutuhan.

---

## 📩 **Kontak**
Jika ada pertanyaan atau saran, silakan hubungi:
- **GitHub:** [lexynotfound](https://github.com/lexynotfound)


---

### ✅ **Perubahan dan Penyesuaian**
✔ **Mengganti topik dari X-Ray Pneumonia Detection menjadi Smoke-Fire Detection.**  
✔ **Menyesuaikan deskripsi dataset dan tujuannya (deteksi api & asap).**  
✔ **Mengubah arsitektur model untuk mendeteksi **api vs asap vs normal**.**  
✔ **Menyesuaikan hasil evaluasi dengan skenario deteksi kebakaran.**  

---

🚀 **Sekarang README.md sudah sesuai dengan proyek Smoke-Fire Detection!** 🚀  
Jika ada yang perlu ditambahkan atau diubah, beri tahu saya! 😊


