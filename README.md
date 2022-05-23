# Tugas Akhir Kelompok Pemodelan Oseanografi 💻
Repositori ini dibuat untuk memenuhi tugas akhir mata kuliah Praktikum Pemodelan Oseanografi tahun 2022. Bahasa pemograman yang digunakan dalam repositori ini adalah bahasa pemograman *Python* yang dapat dikerjakan pada *text editor*, seperti *Google Colaboratory* dan *Jupyter Notebook*. Modul yang digunakan pada repositori ini adalah *matplotlib*, *numpy*, dan *sys*. Seluruh _script_ yang dibuat merupakan hasil kerja kelompok 9 Oseanografi 2020. 

Semoga bermanfaat <3

# **Adveksi-Difusi 1D**
penjelasan, coding, dan gambar

Adveksi merupakan mekanisme perpindahan massa suatu materi dari suatu titik ke titik lainnya sedangkan difusi dapat didefinisikan sebagai sebuah proses dimana suatu zat bergerak dari konsentrasi tinggi ke rendah. Persamaan gelombang linier orde satu termasuk ke dalam persamaan diferensial hiperbolik yang menggambarkan mekanisme transportasi fluida dengan arah tertentu. Persamaan tersebut dapat didiskritisasi menggunakan secara eksplisit maupun implisit. Tipe eksplisit memiliki keunggulan berupa stabilitas hitungan dan perhitungan yang lebih mudah dibandingkan tipe implisit tetapi tipe eksplisit memerlukan proses yang lama.

# **Adveksi-Difusi 2D**
penjelasan, coding, dan gambar

Adveksi merupakan proses transportasi berupa aliran rata-rata atau arus, seperti sungai atau gerakan pasang surut, yang digerakkan oleh gaya gravitasi atau tekanan dan berupa gerak horizontal sedangkan difusi merupakan proses transportasi materi dari suatu sistem ke bagian yang lain sebagai hasil pergerakan molekul acak, di mana setiap partikel difusi bergerak secara acak di bidang difusi. Adveksi-difusi merupakan proses transportasi materi dari satu bagian sistem ke bagian yang lain sebagai hasil dari gerakan molekul acak yang melibatkan proses transportasi fluida dalam bentuk aliran rata-rata atau arus yang dipengaruhi oleh gaya gravitasi atau tekanan dan berupa gerak horizontal. Persamaan adveksi-difusi merupakan persamaan matematis yang didesain untuk mempelajari fenomena transpor polutan. Persamaan transpor merupakan salah satu persamaan diferensial yang merepresentasikan sirkulasi aliran air di estuari dengan variabel C sebagai fungsi ruang dan waktu. Pergerakan polutan dipengaruhi oleh kecepatan aliran, koefisien difusi, arah arus, lama pergerakan polutan, dll. Pada mekanisme transpor difusi 2D dapat menggunakan pendekatan beda maju untuk turunan waktu dan beda pusat untuk turunan ruang sedangkan model adveksi 2D menggunakan pendekatan beda maju untuk turunan waktu dan turunan ruang dilakukan dengan melihat arah kecepatan u, di mana ketika u > 0 maka turunan ruang menggunakan pendekatan beda mundur sedangkan ketika u < 0 maka turunan ruang menggunakan pendekatan beda maju.

script dan keterangan
Berikut skenario yang dihasilkan dari pemodelan Adveksi Difusi 2D
![gif teta 64](https://user-images.githubusercontent.com/106040925/169803814-3aa9063b-bcf9-4031-90fa-9da6bfaf78c7.gif)
![gif teta 124](https://user-images.githubusercontent.com/106040925/169803852-16bb335c-c89b-4efe-abc9-eb496db3e117.gif)
![gif teta 199](https://user-images.githubusercontent.com/106040925/169803891-46fa22d6-1727-495f-822b-0a69d7f38865.gif)
![gif teta 379](https://user-images.githubusercontent.com/106040925/169803912-ce9362d3-e53c-46b2-ad1d-c8704c48799b.gif)
Gejala yang terjadi di perairan sangat penting untuk di pelajari terutama yang berhubungan dengan adveksi dan difusi polutan. Fenomena aliran dan transport merupakan suatu gejala alam yang penting untuk dipelajari karena mempunyai pengaruh terhadap beberapa studi rekayasa. Fenomena tersebut terjadi dalam berbagai macam situasi fisik, seperti transfer panas, proses pemisahan zat kimia, aliran fluida dalam media berpori, penyebaran kontaminan dalam cairan dan juga transport partikel-partikel kecil seperti penyebaran polutan, garam, sedimen dan lain-lain di dalam perairan dangkal. Model matematika dapat digunakan dalam persoalan-persoalan polusi lingkungan seperti yang terjadi pada perairan, dengan disimulasikan atau diturunkan fenomena kejadiannya. Berdasarkan hasil model yang telah dilakukan, pada Skenario 1 (theta = 42) didapatkan hasil bahwa konsetrasi polutan yang bersumber dari tengah bergerak kearah timur laut secara kontinu dengan iterasi waktu 0,5 sampai 104. Pada skenario 2 (theta =102) didapatkan hasil bahwa konsetrasi polutan yang bersumber dari tengah bergerak kearah tenggara secara kontinu dengan iterasi waktu 0,5 sampai 104. Pada skenario 3 (theta = 177) didapatkan hasil bahwa konsetrasi polutan yang bersumber dari tengah bergerak kearah barat daya secara kontinu dengan iterasi waktu 0,5 sampai 104. Pada Skenario 4 (theta = 357) didapatkan hasil bahwa konsetrasi polutan yang bersumber dari tengah bergerak kearah timur laut secara kontinu dengan iterasi waktu 0,5 sampai 104. Arus memberikan peranan dalam proses adveksi difusi 2 dimensi dengan pergerakan polutan yang sesuai dengan arah arus, sedangkan koefisien adveksi difusi   memberikan gambaran proses transport konsentrasi polutan ke segala arah. Kecepatan pergerakan dan penyebaran tergantung pada kecepatan arus.
Persamaan Adveksi-Difusi dapat diaplikasikan dalam mendeteksi penyebaran polusi di perairan. Sebagaimana definisi dari Adveksi sendiri adalah proses perpindahan panas sebagai akibat dari adanya aliran, sedangkan Difusi adaalah proses perpindahan panas berupa rambatan dari air dengan temperatur tinggi ke air dengan temperatur yang lebih rendah. Persamaan disperse atau difusi adveksi dapat diaplikasikan juga ada penyebaran polutan udara karena cerobong asap dari pabirk-pabrik. Pengaruh ketinggian sumber polutan terhadap konsentrasi (𝑥,) adalah semakin tinggi ketinggian sumber polutan maka semakin menurunnya kadar cemaran polutan. Sedangkan pengaruh ketinggian sumber polutan terhadap konsentrasi (𝑥,) adalah semakin tinggi ketinggian sumber polutan maka kadar cemaran polutan akan tetap sama Patmasari (2018). Dengan adanya penelitian yang menggunakan model seperti itu diharapkan kedepannya bisa mencegah terjadinya polutan sehingga pencemaran dapat dihindari

# **Hidrodinamika 1D**
penjelasan, coding, dan gambar

Model hidrodinamika adalah model yang didasarkan pada deskripsi proses-proses yang memengaruhi sirkulasi dan pencampuran massa air dengan hukum pembangun yang terdiri dari hukum konservasi massa, kontinuitas, dan momentum serta diasumsikan dengan adanya skenario. Beberapa kelemahan model hidrodinamika, yaitu:
1. Banyak data,
2. Rawan *error* ketika terdapat perhitungan aliran kritis, dan
3. Simulasi lama.

# **Hidrodinamika 2D**
penjelasan, coding, dan gambar

Pemodelan hidrodinamika 2D dapat digunakan untuk meninjau arah yang lain, misalnya pada sumbu x dan y atau pada sumbu x dan z. Persamaan ini dapat digunakan dalam pemodelan gelombang akibat angin, pemodelan sampah plastik di laut, pemodelan *coastal dynamics* dan sedimentasi pantai serta mengukur tingkat konsentrasi kimia berdasarkan kedalaman dan panjangnya. Pada pemodelan hidrodinamika 2D dapat ditemukan anomali yang menyebabkan hasil tidak sepenuhnya sesuai dengan kondisi aslinya.

# Pengunduhan *Script* Pemodelan Oseanografi
1. Klik *releases* pada repositori ini.

![ta1](https://user-images.githubusercontent.com/105653499/169699805-6ddcb857-d646-44e2-bfe4-f34d647ebcab.png)

2. Klik *script* yang ingin diunduh.

![ta2](https://user-images.githubusercontent.com/105653499/169699924-5d38bd87-71a9-40d1-bda2-b67069c1f84c.png)

3. *Script* akan terunduh secara otomatis.

![ta3](https://user-images.githubusercontent.com/105653499/169699931-7fd825c4-353f-4f59-9772-c32e135f2ac3.png)

# 👨‍💻 **Kelompok 9 Pemodelan Oseanografi** 👩‍💻
1.
2. Gabriela Vany Rosanta Sinaga/ 26050120120024/ Oseanografi A
3. Kirana Adhiningtyas/26050120130077/Oseanografi A
4. Zinedine Wira Mulyawan/26050120130046/Oseanografi A
