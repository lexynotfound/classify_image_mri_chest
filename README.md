# X-Ray Pneumonia Detection Model

Proyek ini bertujuan untuk membangun model **Convolutional Neural Network (CNN)** yang dapat mengklasifikasikan **pneumonia** dari gambar **X-ray paru-paru**. Dataset yang digunakan berasal dari **Chest X-Ray Pneumonia Dataset** yang diambil dari Kaggle. Model ini menggunakan **TensorFlow dan Keras** untuk membangun serta melatih arsitektur CNN.

---

## 🔥 **Fitur Utama**
- **Mendeteksi pneumonia** dari gambar X-ray dengan model berbasis Deep Learning.
- **Menggunakan augmentasi data** untuk meningkatkan generalisasi model.
- **Dapat dikonversi ke berbagai format (Keras, TensorFlow Lite, TensorFlow.js).**
- **Memanfaatkan Early Stopping dan ReduceLROnPlateau** untuk optimasi pelatihan.

---

## 📂 **Dataset**
Dataset yang digunakan adalah **Chest X-Ray Pneumonia Dataset** dari Kaggle. Dataset ini terdiri dari:
- **Gambar X-ray pasien normal**
- **Gambar X-ray pasien dengan pneumonia**

### 📌 **Alasan Pemilihan Dataset**
- Dataset ini relevan untuk **deteksi penyakit dengan Deep Learning**.
- Dataset cukup seimbang antara kelas pneumonia dan normal.
- Banyak digunakan dalam penelitian medis berbasis AI sehingga memungkinkan perbandingan hasil dengan model lain.

---

## 🏰 **Arsitektur Model**
Model ini dibangun menggunakan **Convolutional Neural Network (CNN)** dengan arsitektur sebagai berikut:
1. **4 lapisan Conv2D dengan BatchNormalization dan MaxPooling** untuk ekstraksi fitur.
2. **Flatten Layer** untuk mengubah tensor menjadi vektor.
3. **Dense Layer dengan 256 neuron** untuk memproses fitur lebih lanjut.
4. **Dropout Layer (0.5)** untuk menghindari overfitting.
5. **Output Layer dengan Softmax** untuk klasifikasi multi-kelas.

### 📌 **Alasan Memilih CNN**
- CNN **unggul dalam analisis gambar** karena mampu menangkap pola visual.
- CNN dapat **mengekstrak fitur dari gambar X-ray secara otomatis**.
- CNN digunakan secara luas dalam penelitian medis berbasis AI.

---

## 💻 **Cara Instalasi dan Penggunaan**
Ikuti langkah-langkah berikut untuk menjalankan model ini di sistem Anda.

### 🔹 **1. Clone Repository**
```bash
git clone https://github.com/yourusername/xraymodel.git
cd xraymodel
```

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

