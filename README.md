# Ch.-3-Computer-Vision-and-Natural-Language-Processing

#### Daftar Isi

1. [Assignment Bab 3 - Kasus 1 (02_Kelompok_4_1.ipynb)](#1-assignment-bab-3---kasus-1)
2. [Assignment Bab 3 - Kasus 2 (02_Kelompok_4_2.ipynb)](#2-assignment-bab-3---kasus-2)
3. [Assignment Bab 3 - Kasus 3 (02_Kelompok_4_3.ipynb)](#3-assignment-bab-3---kasus-3)
4. [Assignment Bab 3 - Kasus 4 (02_Kelompok_4_4.ipynb)](#4-assignment-bab-3---kasus-4)

---

## 1. Assignment Bab 3 - Kasus 1

#### Ringkasan
Pada tugas ini, dilakukan replikasi algoritma untuk peningkatan kualitas gambar pada smartphone, serupa dengan *Deep Fusion* (iPhone) dan *Adaptive Tetra-squared Pixel Sensor* (Samsung Galaxy). Metode yang digunakan adalah **Max Pooling** dan **CLAHE** untuk memperbaiki kualitas visual pada kondisi minim cahaya.

#### Dataset
- **photo1.jpeg**: gambar utama untuk peningkatan.
- **lena.png**: gambar uji untuk eksplorasi.

> **Catatan**: Upload kedua file ke Google Colab sebelum menjalankan kode.

#### Library
- **NumPy**: Operasi matriks dan gambar.
- **OpenCV**: Konversi warna dan histogram.
- **Scikit-Image**: Pooling (Max, Min, Average).
- **Matplotlib**: Visualisasi.
- **PyTorch**: Max Pooling dengan GPU.

#### Langkah Pengerjaan
1. Pengolahan gambar dasar dengan OpenCV (konversi, histogram).
2. Max Pooling dengan `block_reduce` dan PyTorch.
3. Eksplorasi Min dan Average Pooling.
4. CLAHE untuk peningkatan kontras.
5. Simpan hasil sebagai `Tim 3.png`.

#### Hasil dan Kesimpulan
- **Max Pooling**: Gambar lebih terang, tetapi detail berkurang.
- **CLAHE**: Lebih baik untuk peningkatan gambar gelap karena mempertahankan detail dalam pencahayaan rendah.

---

## 2. Assignment Bab 3 - Kasus 2

#### Rangkuman
Tugas ini melatih model *pre-trained* (ResNet18, DenseNet121, dan ViT) untuk klasifikasi digit tulisan tangan dengan dataset MNIST.

#### Dataset
- **MNIST Handwritten Digits**: Gambar grayscale angka 0-9.

#### Library
- **PyTorch**: Pembuatan dan pelatihan model.
- **Torchvision**: Dataset MNIST dan model *pre-trained*.
- **Scikit-learn**: Visualisasi.
- **Matplotlib**: Visualisasi akurasi dan loss.

#### Langkah Pengerjaan
1. Modifikasi model pre-trained (DenseNet).
2. Hyperparameter tuning.
3. Latihan dan evaluasi.
4. Freezing beberapa layer DenseNet.
5. BONUS: Uji model ResNet18 dan ViT.

#### Hasil dan Kesimpulan
- Model dengan layer dibekukan lebih cepat tetapi kurang akurat.
- *Transfer learning* efisien, meskipun *freezing* layer mengurangi akurasi.

---

## 3. Assignment Bab 3 - Kasus 3

#### Ringkasan
Menggunakan YOLOv5 untuk deteksi objek secara *real-time* dari video YouTube.

#### Dataset
- Video YouTube dengan objek beragam.
    - Contoh URL:
        1. Keramaian: https://www.youtube.com/watch?v=dwD1n7N7EAg
        2. Tata Surya: https://www.youtube.com/watch?v=g2KmtA97HxY
        3. Lalu Lintas: https://www.youtube.com/watch?v=wqctLW0Hb_0

#### Library
- **PyTorch**: Model YOLOv5.
- **Numpy**: Pemrosesan frame video.
- **OpenCV2**: Penanganan video.
- **cap-from-youtube**: Mengambil video dari YouTube.

#### Langkah Pengerjaan
1. Instalasi library dan model YOLOv5.
2. Pemrosesan video frame-by-frame.
3. Evaluasi kinerja dengan perhitungan FPS.

#### Hasil dan Kesimpulan
- YOLOv5 mendeteksi objek dengan baik pada video realistis namun terbatas pada video animasi.
- FPS tinggi menunjukkan model mampu deteksi real-time.

---

## 4. Assignment Bab 3 - Kasus 4

#### Ringkasan
Klasifikasi tweet terkait bencana menggunakan BERT untuk analisis situasi darurat.

#### Dataset
- **Disaster Tweets**: Tweet dengan label terkait bencana (1) atau non-bencana (0).

#### Library
- **Pandas, Numpy**: Manipulasi data.
- **NLTK**: Pembersihan teks.
- **Scikit-learn**: Pembagian data.
- **PyTorch, Transformers (Hugging Face)**: Model BERT untuk klasifikasi teks.

#### Langkah Pengerjaan
1. Pembersihan teks.
2. Tokenisasi dengan BERT Tokenizer.
3. Pembagian dataset.
4. Pelatihan dan evaluasi model.

#### Hasil dan Kesimpulan
BERT mencapai akurasi tinggi (>80%) dalam mengklasifikasikan tweet terkait bencana, menunjukkan potensi sebagai sistem peringatan dini berbasis media sosial.
