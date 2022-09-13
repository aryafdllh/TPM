**KELOMPOK 1** 
- MUHAMMAD ARYA FADILLAH
- MUHAMMAD FADIL HIDAYAT
- AHMAD HUSNI

# Deteksi Berita Hoax di Media Sosial Twitter dengan
**_Ekspansi Fitur Menggunakan Glove_**

Hoax (baca: / ho.aks /) adalah berita atau liputan yang mencoba menarik perhatian pembaca mengenai kebenaran lalu mencoba untuk meyakinkan pembaca. Persebaran hoax bergantung pada siapa yang membacanya apakah akan ikut menyebarkan tanpa cek kembali kebenarannya atau dengan sengaja mengirimkan ulang kesemua orang di media sosial. Pada kamus besar bahasa Indonesia kata hoax dibaca menjadi hoaks, yang artinya informasi bohong.
Terdapat banyak berita hoax yang saat ini banyak beredar di masyarakat. Bahkan di Indonesia, khusus- nya di media sosial, fenomena hoax tidak jarang terjadi. Hoax bisa membuat orang resah karena informasi yang tidak diketahui kebenarannya. Untuk mengetahui informasi yang disebarluaskan, kita perlu mengklasifikasikannya untuk mengetahui apakah itu hoax atau tidak. Oleh karena itu, di kembangkan sistem yang mampu mendeteksi informasi hoax di media sosial Twitter dengan menggunakan metode ekspansi fitur Global Vectors for Word Representation (GloVe). Metode ekspansi fitur Glove digunak- an untuk mengurangi adanya ketidakcocokan kosakata pada sebuah tweet pada Twitter. Proses klasifikasi yang digunakan beberapa metode yaitu, Support Vector Machine (SVM), Naive Bayes dan Recurrent Neural Network (RNN).
GloVe merupakan word embeddings dari Stanford University untuk memrepresentasikan kata-kata. GloVe ada- lah metode pengajaran tanpa pengawasan untuk representasi kata yang melampaui model lain dalam kesetaraan kata dan identifikasi nama. Unsupervised learning adalah cara pengumpulan data tanpa data latih sehingga data diambil dari data yang ada di banyak bagian. GloVe menggunakan skrip korpus Twitter. Kata-kata ini mengha- silkan vektor dengan ratusan dimensi untuk setiap kata yang dapat ditemukan nanti di kamus. Algoritma mencakup probabilitas bahwa sebuah kata akan muncul didalam perhitungan. Model GloVe ditetapkan berdasarkan:

![Picture14](https://user-images.githubusercontent.com/112482818/189793456-8a2e3439-a272-44d8-b4da-ac47a80c1682.jpg)

Dijelaskan bahwa w merupakan vektor kata, sementara ~w merupakan vektor kontek kata. bi dan bk merupakan arah skalar pada kata utama dan kontek kata. X merupakan matriks kemunculan dimana Xik menyatakan jumlah berapa waktu kata k ada pada kontek kata i. Untuk menghitung nilai Xik dilakukan dengan menjumlahkan statistik di keberadaan kata dalam bentuk matrik keberadaan x. Dimana setiap elemen pada matriks Xik mewakili seberapa sering kata muncul dalam konteks kata j. Konteks kata adalah kumpulan kata yang berada sebelum dan sesudah kata i sebanyak windows size yang diberikan. Pada setiap kata dilakukan pembobotan kata dengan cara _1 dimana distance dihitung dari panjang kontek kata dikurang posisi kata tersebut. Kemudian perhitungan nilai pada f (Xik) yaitu dengan menggunakan persamaan dibawah ini:

![Picture13](https://user-images.githubusercontent.com/112482818/189793580-0533cce3-ac07-4a47-9c9f-34e3ff4a6a2b.jpg)

Rumus Model Glove diatas merupakan fungsi pembobotan ke dalam fungsi cost yang memberikan model seperti di bawah ini :

![Picture12](https://user-images.githubusercontent.com/112482818/189793741-809aace8-8338-4340-812c-6f1c9ad92b16.jpg)

Support Vektor Machine (SVM) cara kerjanya yaitu dengan menemukan fungsi pemisah line yang dapat memi-sahkan dua set dari data antara dua kelas yang berbeda. Metode ini disebut dengan metode learning machine yang memiliki prinsip Sructural Risk Minimazation (SRM) yang bertujuan menemukan hyperplane terbaik untukmemisahkan dua buah dari kelas pada inputan space. Secara umum cara kerja SVM ini berprinsip dengan lini-er clasifier, lalu kemudian dikembangkan untuk mendapat hasil pada kasus non linear dengan cara menggunakankonsep kernel pada ruang kerja yang berdimesi tinggi.
NaiVe Bayes atau NaiVe Bayes Classifier (NBC) merupakan cara yang biasa dimanfaatkan untuk peng- klasifikasi text pada dokumen. Konsep yang digunakan NBC adalah probabilitas sebagai acuan teorinya. Dalam tulisannya, Han, J. dan Kamber, M. mengatakan: ”Bayesian classffiers memiliki tingkat kecepatan dan accuracy yang unggul ketika diterapkan dalam basedata yang besar” (2001, hlm. 296). Dengan buku tersebut, maka sistem Naive Bayes merupakan sistem yang dipergunakan untuk proses tahapan klasifikasi text dalam eksperimen ini. Ada 2 tahap pada proses yang di lakukan pada klasifikasi text. Yakni proses pertama merupakan training terhadap himpunan artikel.

![Picture11](https://user-images.githubusercontent.com/112482818/189794283-fa165372-0534-4ac9-a712-e464f5ac000c.jpg)

Sedangkan untuk proses kedua yang dilakukan merupakan tahapan klasifikasi dokumen yang belum diketahui topiknya. Theorema Bayes:

![Picture10](https://user-images.githubusercontent.com/112482818/189794167-4e0c3f12-5dc2-4d1e-8dcd-2cd9dc18a6fa.jpg)

Recurrent Neural Network (RNN) merupakan sistem jaringan saraf yang berulang dan menggunakan hidden layer untuk nilai neuron akan diproses untuk data inputan. Proses yang dilakukan untuk Recurrent Neural Network (RNN) akan memanggil secara berkali-kali untuk menjalankan inputan yang masuk, yaitu data linear. Recurrent Neural Network (RNN) juga mempunyai beragam bentuk, salah satu bentuknya yaitu global digunakan standar Multi-Layer Perceptron (MLP) yang ditambah dengan loop tambahan. Maka dari itu tahapan ini dapat memanfaatkan kinerja pemetaan nonlinear yang dari MLP. Terdapat identitas dari Recurrent Neural Network (RNN) yaitu mengklasifika- sikan data time series dan sekuensial. Data time series sendiri adalah data yang disatukan menurut deretan waktu dengan rentang tertentu, sedangkan untuk data sekuensial yaitu suatu contoh data yang dipakai secara terurut dan setiap deretan bersinambungan satu sama lain. Recurrent Neural Network (RNN) juga mempunyai fungsi aktivasi deterministik, yaitu fungsi aktivasi Recurrent Neural Network (RNN) ialah han h, dengan perhitungan matematiknya sebagai berikut :

![Picture9](https://user-images.githubusercontent.com/112482818/189794355-4071b5c6-da05-478a-a08f-d06315e8c9ab.jpg)

__Hasil dan Analisis__
Terdapat 3 skenario percobaan yang dilakukan di penelitian ini dengan menggunakan 3 metode klasifikasi yang berbeda yaitu Naive Bayes (NB), Recurrent Neural Network (RNN) dan Support Vector Machine (SVM). Skena- rio pertama merupakan pembuatan model awal yang menggunakan metode Naive Bayes, RNN dan SVM dengan hyperparameter tuning. Skenario kedua merupakan percobaan terhadap model yang telah di buat dan dikombina- sikan dengan TF-IDF. Skenario ketiga merupakan skenario dimana model dikombinasikan dengan ekspansi fitur GloVe dengan menggunakan beberapa korpus yaitu, korpus tweet, korpus IndoNews dan korpus IndoNews + tweet.Untuk proporsi data yang di gunakan adalah 75:25 data.
Pengujian Pertama
Pengujian ini dilakukan terhadap data tweet yang telah dicrawling pada gambar 2 dan hasil dari pengujian dapat dilihat pada Tabel 6, untuk menjadi model awal dan sudah dilakukan hyperparameter tuning dimana nilai yang terbesar adalah untuk metode Support Vector Machine (SVM) dengan nilai akurasi sebesar 76,52% dan nilai F-1Score sebesar 69,94%.

Tabel 1. Nilai Akurasi dan F-1 Score Model Awal
Metode	Akurasi(%)	F1-Score
Naive Bayes	72,20	68,10
RNN	46,75	41,57
SVM	76,52	69,94

Pengujian   Kedua   (Model   Awal   +   TF-IDF)
Pengujian kedua dilakukan dengan menggunakan TF- IDF untuk pembobotan setiap kata pada data tweet yang digunakan untuk menjadi perbandingan dengan model awal. Hasil pengujian dengan menggunakan vektor TF-IDF terhadap SVM, Naive Bayes dan RNN dapat dilihat pada Gambar 4. Nilai yang naik pada pengujian ini hanya metode Naive Bayes dan RNN sedangkan metode SVM mengalami penurunan.

![Picture8](https://user-images.githubusercontent.com/112482818/189794531-da136238-b933-4d7f-ba12-a3a75f6b62f2.jpg)

Gambar  Hasil Pengujian Model Awal dan TF-IDF
Pengujian Ketiga (Model Awal + GloVe)
Dilakukan pengujian ketiga untuk mencari model terbaik pada metode SVM dengan hyperparameter tuning, Naive Bayes dan RNN dengan menggunakan ekspansi fitur metode GloVe. Pengujian menggunakan ekspansi fitur dilakukan terhadap Top 1, 5 dan 10 yaitu dari feature yang ada pada korpus GloVe. Korpus GloVe yang akandigunakan adalah korpus dari dataset tweet, korpus dari dataset IndoNews, dan korpus gabungan dari dataset tweetdan IndoNews. Pemilihan Top 1, Top 5 dan Top 10 adalah jumlah n kata yang memiliki similarity dengan kata yang di tuju. Dengan artian Top 1 merupakan 1 kata paling similar, Top 5 merupakan 5 kata paling similar dan Top 10merupakan 10 kata paling similar. Pada penelitian ini, melakukan eksperimen dan analisa terhadap pengaruh dari classification dengan dan tanpa Feature Expansion, dengan harapan memperluas hal tersebut dapat meningkatkanhasil train model agar mendapat akurasi yang lebih memuaskan. Lalu mengapa tidak menggunakan Top 1, Top2 dan Top 3, kami berusaha menghindari overfit dan underfit, memakai rentang yang besar untuk menghindari underfit, dan menggunakan rentang yang tidak terlalu besar untuk menghindari overfit.
Naive Bayes
Perfomansi untuk untuk nilai akurasi dan F1-Score Feature Exspansion menggunakan algoritma klasifikasi Naive Bayes dapat dilihat pada Gambar 5 dan 6. Terjadi peningkatan nilai akurasi pada semua fitur.

![Picture7](https://user-images.githubusercontent.com/112482818/189794574-9677782b-24d5-4cf9-9f3c-222f0d79a610.jpg)

Gambar  Hasil Akurasi Fitur Ekspansi Pada Metode Naive Bayes Feature

![Picture6](https://user-images.githubusercontent.com/112482818/189794615-8bb45bb3-bdd8-4d72-8e6d-1c0d7c681b08.jpg)

Gambar  Hasil F1-Score Fitur Ekspansi Pada Metode Naive Bayes
Recurrent Neural Network (RNN)
Perfomansi untuk untuk nilai akurasi dan F1-Score Feature Exspansion menggunakan algoritma klasifikasi Recurrent Neural Network (RNN) dapat dilihat pada Tabel 10 dan 

![Picture5](https://user-images.githubusercontent.com/112482818/189794789-a9d6cf11-c9e1-4921-83a2-507b5843e1a2.jpg)

11. Terjadi peningkatan nilai akurasi pada fitur Top 1 untuk semua korpus, fitur Top 5 mengalami kenaikan pada korpus IndoNews dan Tweet +IndoNews, sedangkan fitur Top 10 kenaikan terjadi pada korpus Tweet dan IndoNews.

![Picture4](https://user-images.githubusercontent.com/112482818/189794834-afd610da-6d96-40a6-97d2-3e2f5eedcf25.jpg)

Gambar  Hasil Akurasi Fitur Ekspansi Pada Metode Recurrent Neural Network (RNN)

Support Vector Machine (SVM)
Perfomansi untuk untuk nilai akurasi dan F1-Score Feature Exspansion menggunakan algoritma klasifikasi Support Vector Machine (SVM) dapat dilihat pada Gambar 8 dan 9. Terjadi peningkatan nilai akurasi pada semua fitur.

![Picture3](https://user-images.githubusercontent.com/112482818/189794864-a3b3a1ad-7dfd-418b-bd05-e5410131bb87.jpg)

Gambar  Hasil Akurasi Fitur Ekspansi Pada Metode Support Vector
Machine (SVM)

![Picture2](https://user-images.githubusercontent.com/112482818/189794900-faf8427b-ffea-47bf-927e-98c54d8aced0.jpg)

Gambar  Hasil F1-Score Fitur Ekspansi Pada Metode Support Vector Machine (SVM)
Analisis Hasil Pengujian
Berdasarkan hasil dari pengujian ini, dapat di lihat melalui diagram Gambar 3. Dengan model Top 1 features terjadi peningkatan nilai akurasi pada metode SVM sebesar 87,64% pada korpus Tweet+Berita serta nilai f1-scoresebesar 84,64% dari model awal yang hasilnya 76,52% dan mengalami kenaikan 11,12%, sedangkan untuk metode Naive Bayes mengalami penaikan yang konsisten tidak mengalami penurunan dari 72,20% sampai 82,32%, dan metode RNN terjadi tidak konsisten mengalami naik dan turun di semua model yang di bangun.
Sedangkan pada model dengan Top 5 features dengan menggunakan metode RNN tidak mengalami perubahanyang signifikan hanya naik sekitar 2%, dan untuk model SVM mengalami penaikan kecuali pada korpus Twe- et+Berita enjadi turun sekitar 1%. Pada metode Naive Bayes di Top 5 features model Tweet+Berita menjadi turunkembali sekitar 0,32%.
Selanjutnya, pada model Top 10 features terjadi penurunan akurasi kembali untuk metode RNN dari nilai model awal 46,75% turun menjadi 44,99% pada korpus Tweet+Berita dengan nilai F1-Score 42,84%, untuk metode NaiveBayes dan SVM selalu mengalami peningkatan yang signifikan.

![Picture1](https://user-images.githubusercontent.com/112482818/189794936-3b484e7f-7a47-48bd-a01d-58a2c3b5dc2f.jpg)

Gambar  Persebaran Data

__KESIMPULAN__

Hasil dari rangkuman ini telah dibangun deteksi hoax menggunakan ekspansi fitur metode GloVe dengan metode klasifikasi Naive Bayes, Recurrent Neural Network (RNN), Support Vector Machine (SVM). Ekspansi Fitur GloVe digunakan pada sistem pendeteksi hoax ini bertujuan untuk mengurangi ketidakcocokan kosakata pada kalimat tweet. Ekspansi fitur dilakukan dengan menggunakan 3 korpus GloVe (Tweet, IndoNews, dan Tweet + IndoNews)dan juga 3 variasi ekspansi fitur (Top 1, Top 5, Top 10) untuk mencari model terbaik. Pada hasil penelitian menunjukan bahwa metode ekspansi fitur GloVe berhasil meningkatkan akurasi nilai pada sistem yang telah di bangun. Pada penelitian ini peningkatan nilai akurasi tertinggi terdapat pada model dengan metode klasifikasi SVM dengan korpus GloVe Tweet+Berita dan menggunakan Top 10, yaitu sebesar 91,92% dengan penambahan nilai akurasi 15,4% dari model awal.
Hasil dari peningkatan nilai akurasi yang konsisten terjadi pada Top 1 features dengan metode Naive Bayes dan SVM, Top 5 features dengan metode Naive Bayes dan SVM mengalami kenaikan tetapi di korpusTweet+Berita mengalami turun kembali , Top 10 features dengan metode Naive Bayes dan SVM, mengalami kenaikan di setiap korpus yang di gunakan.
