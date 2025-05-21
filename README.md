# CC-topic-modelling-python

This repository holds the data for the _Topic Modelling in Python: Unsupervised Machine Learning to Find Tweet Topics_ tutorial.

The tutorial is available here: https://ourcodingclub.github.io/2018/12/10/topic-modelling-python.html

We would love to hear your feedback on the tutorial: 
https://www.surveymonkey.co.uk/r/7C5N3QV

Check out https://ourcodingclub.github.io/workshop/ to learn how you can get involved!

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

[![License: CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/)

## Kesimpulan dalam analisis
Dalam analisis ini, dilakukan serangkaian proses untuk menemukan pola topik tersembunyi di balik tweet-tweet yang membahas isu perubahan iklim. Berikut langkah-langkah dan temuan utamanya:

- ✅ Langkah-Langkah yang Telah Dilakukan:
    1. Pembersihan Data (Cleaning)
        - Menghapus tanda baca, angka, dan stopword
        - Mengubah semua teks menjadi huruf kecil
        - Hasil: tweet bersih yang siap untuk dianalisis
    2. Ekstraksi Fitur (Feature Extraction)
        - Menggunakan CountVectorizer untuk mengubah teks ke dalam bentuk matriks frekuensi kata (term frequency)
        - Disaring dengan max_df=0.9 dan min_df=25 untuk menghindari kata terlalu umum atau terlalu jarang
    3. Penerapan Model Topik
        - LDA (Latent Dirichlet Allocation) digunakan sebagai metode utama
        - Topik yang dihasilkan cenderung didominasi kata seperti: global, warming, climate, change, yang memang sangat umum pada data ini
        - Disadari bahwa kata-kata tersebut sebaiknya dihapus karena tidak informatif
    4. Eksperimen Alternatif dengan NMF (Non-negative Matrix Factorization)
        - NMF memberikan hasil topik yang lebih beragam dan mudah diinterpretasi
        - Lebih cocok untuk teks pendek seperti tweet

🔍 Temuan Utama:
Banyak topik didominasi oleh kata "climate", "global", dan "warming", menunjukkan bahwa kata-kata ini terlalu umum untuk dipakai dalam penentuan topik:
1. Dengan membersihkan kata-kata umum tersebut, model mampu menampilkan topik yang lebih spesifik, misalnya soal:
2. Kebijakan lingkungan (policy, carbon, emission)
3. Tokoh publik & politik (gore, trump, greta)
4. Kejadian alam (floods, storm, fire)

📌 Kesimpulan Akhir:
Model topik seperti LDA dan NMF dapat digunakan untuk menemukan pola dan tema besar dari kumpulan tweet tentang perubahan iklim. Namun, karena tweet bersifat sangat pendek, metode seperti NMF cenderung lebih efektif. Proses pra-pemrosesan seperti pembersihan teks dan penghapusan kata terlalu umum sangat penting agar topik yang dihasilkan benar-benar informatif dan relevan.

