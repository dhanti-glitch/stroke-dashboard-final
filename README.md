🧠***Early Stroke Risk Prediction & Prevention System***
<p>Sistem deteksi dini risiko stroke berbasis data kesehatan sederhana <br>memberikan prediksi risiko, insight faktor penyebab, dan rekomendasi pencegahan secara otomatis.</p>
<img width="216" height="226" alt="image" src="https://github.com/user-attachments/assets/1885cd88-d47f-4866-aa7c-8bec0aa90885" />  <img width="580" height="350" alt="image" src="https://github.com/user-attachments/assets/f88f93d5-2c78-4937-8445-d5ae7ca8f196" />

<br>

**"Stroke adalah penyebab kematian nomor 2 di dunia — namun 80% kasusnya bisa dicegah jika risikonya diketahui lebih awal."**
— WHO, 2023

<br>
</div>

**🔍 Tentang Proyek Ini**
Sebagian besar orang tidak tahu bahwa mereka berisiko stroke — sampai gejalanya muncul dan sudah terlambat. Padahal, faktor risikonya (usia, hipertensi, kadar glukosa, BMI) bisa dideteksi lebih awal dari data kesehatan sederhana.
Proyek ini menjawab pertanyaan:

🩺 Faktor kesehatan apa yang paling berpengaruh terhadap risiko stroke?<br>
🤖 Bisakah model AI memprediksi risiko stroke dari input data sederhana?<br>
📊 Bagaimana menyajikan hasil prediksi agar mudah dipahami orang awam?<br>

***Solusinya***: Aplikasi web berbasis Streamlit yang menerima input data kesehatan pengguna, lalu menampilkan prediksi risiko stroke beserta tingkat probabilitasnya dan rekomendasi pencegahan.

**📁 Struktur Repository**
CC26-PRU459/

    notebooks/
        DS_StrokePrediction.ipynb
        DS_Dashboard_Preprocessing.ipynb

    model/
        AI_StrokeModel.ipynb
        stroke_model.keras
        inference.py

    dashboard/
        app.py
        assets/

    data/
        healthcare-dataset-stroke-data.csv
        stroke_dataset_cleaned_final.csv

    plots/

    requirements.txt
    README.md

📊**Dataset**
Sumber       : Stroke Prediction Dataset — Kaggle <br>
Jumlah data  : 5.110 pasien <br>
Fitur input  : 10 fitur kesehatan <br>
Target       : stroke — 0 (Tidak) / 1 (Ya) <br>

**Fitur yang Digunakan**
Age - Numerik - Usia pasien (tahun) <br>
hypertension - Biner - Riwayat hipertensi (0/1) <br>
heart_disease - Biner - Riwayat penyakit jantung (0/1) <br>
ever_married - Kategorikal - Status pernikahan <br>
work_type - Kategorikal - Jenis pekerjaan <br>
Residence_type - Kategorikal - Urban / Rural <br>
avg_glucose_level - Numerik - Rata-rata kadar glukosa (mg/dL) <br>
bmi - Numerik - Body Mass Index (kg/m²) <br>
smoking_status - Kategorikal - Status merokok <br>
stroke - Biner - Target <br>

💡 Insight Utama dari EDA
<table>
<tr>
<td width="50%">

🔴 Faktor Risiko Tertinggi

Usia — Penderita stroke rata-rata 67 th vs non-penderita 41 th (p < 0.05) <br>
Hipertensi — Risiko stroke 2–3× lebih tinggi <br>
Penyakit Jantung — Risiko stroke ~2× lebih tinggi <br>
Kadar Glukosa Tinggi — Berbeda signifikan antar kelompok <br>

</td>
<td width="50%">
🟡 Faktor Risiko Sedang

Mantan Perokok — % stroke tertinggi dibanding kategori lain <br>
BMI — Sedikit lebih tinggi pada penderita stroke <br>
Self-employed / Govt Job — Lebih berisiko (korelasi dengan usia) <br>

⚪ Faktor Kurang Signifikan

Gender → tidak berbeda nyata <br>
Urban/Rural → tidak berbeda nyata <br>

</td>
</tr>
</table>

🚀**Cara Menjalankan**

***Opsi 1 — Google Colab (Rekomendasi)***
1. Upload file DS_StrokePrediction.ipynb ke Google Colab
2. Upload dataset ZIP ke Google Drive:
   **MyDrive/CC26-PRU459/dataset kaggle/archive.zip**
3. Jalankan semua cell dari atas ke bawah
***Opsi 2 — Lokal***
1. Clone repository
git clone https://github.com/[username]/CC26-PRU459.git
cd CC26-PRU459

2. Install dependencies
pip install -r requirements.txt

3. Jalankan notebook
jupyter notebook notebooks/DS_StrokePrediction.ipynb

4. Jalankan dashboard
streamlit run dashboard/app.py

📦 **Dependencies**
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
scipy>=1.9.0
tensorflow>=2.10.0
scikit-learn>=1.1.0
streamlit>=1.20.0


<div align="center">
⭐ Jika project ini bermanfaat, jangan lupa kasih star!
<br>
CC26-PRU459 · Coding Camp 2026 · DBS Foundation
Healthy Lives & Well-being
</div>
