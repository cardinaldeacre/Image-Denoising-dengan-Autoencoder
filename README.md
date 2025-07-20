# Proyek Denoising Gambar Menggunakan Autoencoder

## Ringkasan Proyek

Proyek ini bertujuan untuk mengembangkan dan melatih model autoencoder konvolusional untuk tugas denoising gambar. Kami menggunakan dataset CIFAR-10, menambahkan Gaussian noise pada gambar, kemudian melatih autoencoder untuk merekonstruksi gambar asli dari versi yang bernoise. Tujuan utamanya adalah untuk menunjukkan kemampuan autoencoder dalam mempelajari representasi fitur yang efektif dan merekonstruksi input yang bersih dari data yang rusak.

## Fitur Utama

- **Pemuatan Data**: Menggunakan dataset CIFAR-10 yang tersedia di TensorFlow Keras
- **Normalisasi Gambar**: Gambar dinormalisasi ke rentang `[0, 1]` untuk pelatihan model yang optimal
- **Penambahan Noise**: Implementasi fungsi untuk menambahkan Gaussian noise ke gambar untuk simulasi data yang bernoise
- **Arsitektur Autoencoder**: Membangun autoencoder konvolusional dengan lapisan Encoder dan Decoder yang simetris, menggunakan `Conv2D`, `MaxPooling2D`, dan `UpSampling2D`
- **Kompilasi Model**: Menggunakan optimizer 'adam' dan Mean Squared Error (MSE) sebagai fungsi loss, yang umum untuk tugas denoising
- **Pelatihan Model**: Melatih model pada data gambar yang bernoise sebagai input dan gambar asli sebagai target, dengan implementasi `EarlyStopping` untuk mencegah overfitting
- **Visualisasi Hasil**: Menampilkan perbandingan gambar asli, gambar bernoise, dan gambar hasil denoising untuk evaluasi kualitatif
- **Visualisasi Loss**: Menampilkan grafik loss pelatihan dan validasi untuk memantau kinerja model selama pelatihan

## Struktur Kode

Kode ini disusun dalam format Jupyter Notebook (`.ipynb`) dan mencakup bagian-bagian berikut:

1. **Impor Pustaka dan Memuat Data**: Mengimpor semua pustaka yang diperlukan (NumPy, Matplotlib, TensorFlow) dan memuat dataset CIFAR-10
2. **Menambahkan Noise ke Gambar**: Mendefinisikan fungsi `add_gaussian_noise` dan mengaplikasikannya ke dataset pelatihan dan pengujian. Visualisasi gambar asli dan bernoise juga disertakan
3. **Membangun Arsitektur Autoencoder**: Mendefinisikan arsitektur autoencoder dengan detail lapisan encoder dan decoder, serta menampilkan ringkasan model
4. **Kompilasi Model**: Mengkompilasi model autoencoder dengan optimizer dan fungsi loss yang ditentukan
5. **Pelatihan Model**: Melatih model menggunakan data yang disiapkan dan menerapkan `EarlyStopping`
6. **Evaluasi Hasil dan Visualisasi**: Membuat prediksi menggunakan model yang telah dilatih dan memvisualisasikan hasilnya, termasuk grafik loss dan perbandingan gambar

## Cara Menjalankan Proyek

### 1. Klon Repositori

```bash
git clone https://github.com/cardinaldeacre/Image-Denoising-dengan-Autoencoder.git
```


### 2. Instal Dependensi

Pastikan Anda memiliki Python terinstal. Kemudian instal pustaka yang diperlukan:

```bash
pip install numpy matplotlib tensorflow
```

### 3. Jalankan Jupyter Notebook

```bash
jupyter notebook mini-project-ml2.ipynb
```

Ini akan membuka Jupyter Notebook di browser web Anda.

### 4. Eksekusi Sel

Di antarmuka Jupyter Notebook, Anda dapat menjalankan setiap sel secara berurutan dari atas ke bawah untuk memuat data, melatih model, dan melihat hasilnya.

## Hasil dan Analisis

Setelah pelatihan, model akan menghasilkan gambar-gambar yang telah di-denoise. Anda akan melihat bahwa autoencoder mampu mengurangi noise pada gambar dan merekonstruksi fitur-fitur penting dari gambar asli. Grafik loss akan menunjukkan konvergensi model, dengan loss validasi yang stabil setelah beberapa epoch, menandakan model telah belajar dengan baik dan tidak mengalami overfitting yang parah.

## Kontributor

| **Nama Kontributor** | **Jobdesk** |
|----------------------|-------------|
| Iqbal Maulana | Merancang Arsitektur Model |
| Farid Fajar | Pra-pemrosesan Data dan Penambahan Noise |
| Abdullah Sukma Jati | Kompilasi dan Pelatihan Model |
| Gusti Ahmad | Visualisasi Hasil dan Analisis Loss |
| Ahmad Nugrahadi | Dokumentasi Kode dan README |
| Atha Fatur | Pengujian  Model |

## Teknologi yang Digunakan

- **Python 3.x**
- **TensorFlow/Keras** - Framework deep learning
- **NumPy** - Komputasi numerik
- **Matplotlib** - Visualisasi data
- **Jupyter Notebook** - Environment pengembangan

## Struktur File

```
nama-repo-denoising/
├── mini-project-ml2.ipynb    # Notebook utama
├── README.md                 # Dokumentasi proyek
└── requirements.txt          # Daftar dependensi (opsional)
```
