# GeneticAlgorithm

1. Desain Kromosom dan Metode Pendekodean
Desain kromosom yang saya gunakan adalah Binary (Bilangan Biner), dengan teknik pendekodean menggunakan binary encoding. Cara kerjanya adalah dengan membagi 2 panjang kromosom sehingga didapatkan 2 buah kelompok individu yang direpresentasikan dengan x1 dan x2. Selanjutnya hasil x1 dan x2 tersebut akan menjadi variabel untuk perhitungan fungsi h (Soal Tugas 1).

2. Jumlah Populasi, Kromosom, dan Generasi
Dalam melakukan observasi, saya akan memulai dengan jumlah populasi sebesar 50, panjang kromosom sebesar 50, dan maksimal generasi sebesar 500 generasi. Jika dirasa hasil yang didapatkan konsisten dan tidak mengalami penurunan yang signifikan, saya akan mencoba mengurangi jumlah populasi, kromosom, dan maksimal generasinya sampai hasil yang didapatkan turun dengan signifikan.

3. Nilai Fitness
Selanjutnya perhitungan nilai fitness menggunakan rumus 1/h+a, dimana a adalah konstanta bernilai 1 karena pada source kode yang saya buat akan lebih terlihat perbedaan nilai fitness nya dibanding dengan konstanta 0.01.

4. Pemilihan Orang Tua
Teknik pemilihan orang tua yang saya gunakan adalah Tournament Selection. Cara kerja nya adalah dengan memilih merandom k-buah nilai fitness sebuah kromosom yang akan diikut sertakan dalam tournament selection. Metode ini dipilih karena menurut saya lebih cepat dan gampang untuk diimplementasikan. Dan apabila h bernilai negatif maka h akan langsung dikali dengan “-“ untuk menghasilkan nilai positif.

5. Crossover dan Mutasi
Teknik crossover yang saya gunakan adalah metode general scheme dengan single point crossover. Probabilitas dalam crossover ini digunakan sebesar 60% - 70%. Selanjutnya dilakukan mutasi untuk menghasilkan kromosom yang lebih baik. Dilakukan iterasi secara berulang sepanjang kromosom untuk me-replace nilai gen dengan probabilitas sebesar 1%.

6. Probabilitas Crossover dan Mutasi
Probabilitas dalam crossover ini digunakan sebesar 60% - 70%. Pada observasi kali ini saya akan menggunakan probabilitas crossover sebesar 70% (0.7) dan probabilitas mutasi sebesar 1% (0.01). Karena semakin besar probabilitas yang diterapkan maka semakin besar juga kemungkinan terjadinya crossover.

7. Survivor Selection
Metode yang saya gunakan dalam survivor selection adalah general replacement dengan menambahkan mekanisme elitisme untuk menampung 5 individu terbaik untuk bertahan pada
generasi berikutnya. Berbeda dengan metode steady-state yang akan mengeliminasi 2 individu terburuk pada setiap generasinya.

8. Kriteria Pemberhentian Generasi
Stopping Criteria yang saya terapkan menggunakan 2 kondisi. Kondisi pertama apabila jumlah generasi telah mencapai maksimal generasi. Kondisi kedua apabila nilai fitness yang
dihasilkan konvergen atau setiap generasi menghasilkan nilai fitness yang sama dan konsisten, maka program akan menghasilkan generasi terakhir pada saat iterasi.

