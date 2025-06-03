# Transformer Architecture Experiments
# Eksperimen Arsitektur Transformer untuk Klasifikasi dan Regresi
**Maulana Seno Aji Yudhantara — 152022065**

Repositori ini berisi implementasi eksperimen arsitektur **Transformer** pada tiga jenis tugas berbeda: klasifikasi sentimen, klasifikasi berita, dan prediksi deret waktu (time series regression). Tugas ini disusun sebagai bagian dari penilaian akhir mata kuliah *Deep Learning*.

## 📂 Isi Folder
- `IMDBDataset/` : Dataset IMDB untuk klasifikasi sentimen (50K movie reviews).
- `AGNewsDataset/` : Dataset AGNews untuk klasifikasi topik berita (4 kelas).
- `ElectricityDataset/` : Dataset time series untuk prediksi beban listrik.
- `transformer_experiment.ipynb` : Notebook utama yang berisi seluruh eksperimen dan hasil evaluasi.

## 🧪 Deskripsi Eksperimen
Setiap model Transformer dibangun dan dilatih dengan kombinasi parameter berikut:

- **Jumlah Layer (`num_layers`)**: 2, 4 (untuk klasifikasi), 2, 3 (untuk regresi)
- **Jumlah Head Attention (`num_heads`)**: 2, 4
- **Ukuran Feed Forward (`ff_dim`)**: 64, 128, 256
- **Ukuran Embedding (`embed_dim`)**: 64, 128 (untuk teks)
- **Ukuran Jendela (`window_size`)**: 24 dan 48 (khusus regresi time series)

Tujuan eksperimen adalah:
- Menilai pengaruh masing-masing kombinasi parameter terhadap **akurasi (klasifikasi)** dan **MAE (regresi)**.
- Menemukan **trade-off antara akurasi dan efisiensi waktu pelatihan**.

## 📈 Hasil Utama
- **Klasifikasi Sentimen (IMDB)**: Akurasi terbaik 0.8668 dicapai dengan `layers=4`, `heads=2`, `ff_dim=128`, `embed_dim=128`.
- **Klasifikasi Berita (AGNews)**: Akurasi terbaik 0.9068 dicapai dengan `layers=4`, `heads=4`, `ff_dim=128`, `embed_dim=64`.
- **Regresi Beban Listrik**: MAE terbaik 0.8822 dengan `window=48`, `layers=2`, `heads=2`, `ff_dim=64`.

## 📎 Catatan
- Semua eksperimen dilakukan dengan arsitektur **Transformer custom sederhana** tanpa pretrained model.

---

> Dibuat dan dieksperime+nkan oleh Maulana Seno Aji Yudhantara  
> NRP: 152022065 | DEEP LEARNING Semester Genap 2024/2025

