# Tugas Akhir Kelompok Pemodelan Oseanografi 💻
Repositori ini dibuat untuk memenuhi tugas akhir mata kuliah Praktikum Pemodelan Oseanografi tahun 2022. Bahasa pemograman yang digunakan dalam repositori ini adalah bahasa pemograman *Python* yang dapat dikerjakan pada *text editor*, seperti *Google Colaboratory* dan *Jupyter Notebook*. Modul yang digunakan pada repositori ini adalah *matplotlib*, *numpy*, dan *sys*. Seluruh _script_ yang dibuat merupakan hasil kerja kelompok 9 Oseanografi 2020. 

Semoga bermanfaat <3

# **Adveksi-Difusi 1D**
penjelasan, coding, dan gambar

Adveksi merupakan mekanisme perpindahan massa suatu materi dari suatu titik ke titik lainnya sedangkan difusi dapat didefinisikan sebagai sebuah proses dimana suatu zat bergerak dari konsentrasi tinggi ke rendah. Persamaan gelombang linier orde satu termasuk ke dalam persamaan diferensial hiperbolik yang menggambarkan mekanisme transportasi fluida dengan arah tertentu. Persamaan tersebut dapat didiskritisasi menggunakan secara eksplisit maupun implisit. Tipe eksplisit memiliki keunggulan berupa stabilitas hitungan dan perhitungan yang lebih mudah dibandingkan tipe implisit tetapi tipe eksplisit memerlukan proses yang lama.

#**Difusi**
Difusi adalah peristiwa dimana terjadi transfer materi melalui materi lain. Transfer materi ini berlangsung karena atom atau partikel selalu bergerak oleh agitasi thermal. Difusi merupakan proses irreversible (tidak dapat diubah). Pada fase gas dan cair, peristiwa difusi mudah terjadi, sedangkan pada fase padat difusi juga terjadi walaupun memerlukan waktu yang lebih lama. 
Fenomena difusi massa digambarkan sebagai berikut : 


![image](https://user-images.githubusercontent.com/106045814/169815374-47edb95b-3055-46c9-a414-7fdf7fa48c5c.png)


Pada gambar (1) di atas merupakan proses difusi. Saat baru terjadi pelepasan massa, kerapatan massa masih berkonsentrasi disekitar sumber dan belum menyebar. Hal ini terlihat dari daerah hitam yang terkonsentrasi di sekitar sumber dan terang di titik-titik yang jauh dari sumber (Gambar 1a). Berikutnya, pada gambar 1b, daerah hitam di sekitar sumber mulai membesar, menunjukan massa telah mulai menyebar. Penyebaran massa ini terus terjadi dan semakin tampak jelas pada gambar 1c yaitu dengan membesarnya daerah hitam dan juga memudarnya warna hitam di sekitar sumber. Pada gambar 1d, di sekitar sumber tidak hitam lagi, yang menunjukan penurunan kerapatan massa yang cukup berarti di titik sumber. Penurunan kerapatan massa di sekitar sumber ini semata-mata karena massa telah menyebar dan secara total tidak terjadi pengurangan ataupunpenambahan massa

Persamaan Adveksi- Difusi 1D
1. Difusi 


![image](https://user-images.githubusercontent.com/106045814/169814201-222a9150-dcd1-49b6-9852-10ee3d0e0dff.png)


2. Deskritisasi 1D proses Difusi 


![image](https://user-images.githubusercontent.com/106045814/169814299-43b87601-02e5-4fae-b934-70f52fc9461d.png)


3. Persamaan Adveksi Difusi 


![image](https://user-images.githubusercontent.com/106045814/169814451-0ff1ead3-53cd-4732-a937-8f9a8f79f835.png)


dengan kriteria : 


![image](https://user-images.githubusercontent.com/106045814/169814549-2306dd0f-2ae9-44ff-97a2-c5685223c0bb.png)



# **Adveksi-Difusi 2D**
Gejala yang terjadi di perairan sangat penting untuk dipelajari terutama yang berhubungan dengan adveksi dan difusi polutan. Fenomena aliran dan transportasi merupakan suatu gejala alam yang penting untuk dipelajari karena mempunyai pengaruh terhadap beberapa studi rekayasa. Fenomena tersebut terjadi dalam berbagai macam situasi fisik, seperti transfer panas, proses pemisahan zat kimia, aliran fluida dalam media berpori, penyebaran kontaminan dalam cairan, dan transportasi partikel-partikel kecil, seperti penyebaran polutan, garam, dan sedimen di perairan dangkal. Model matematika dapat digunakan dalam persoalan-persoalan polusi lingkungan yang terjadi pada perairan dengan disimulasikan atau diturunkan fenomena kejadiannya. 

Adveksi merupakan proses transportasi berupa aliran rata-rata atau arus, seperti sungai atau gerakan pasang surut, yang digerakkan oleh gaya gravitasi atau tekanan dan berupa gerak horizontal sedangkan difusi merupakan proses transportasi materi dari suatu sistem ke bagian yang lain sebagai hasil pergerakan molekul acak, di mana setiap partikel difusi bergerak secara acak di bidang difusi. Adveksi-difusi merupakan proses transportasi materi dari satu bagian sistem ke bagian yang lain sebagai hasil dari gerakan molekul acak yang melibatkan proses transportasi fluida dalam bentuk aliran rata-rata atau arus yang dipengaruhi oleh gaya gravitasi atau tekanan dan berupa gerak horizontal. 

Persamaan adveksi-difusi merupakan persamaan matematis yang didesain untuk mempelajari fenomena transpor polutan. Persamaan transpor merupakan salah satu persamaan diferensial yang merepresentasikan sirkulasi aliran air di estuari dengan variabel C sebagai fungsi ruang dan waktu. Pergerakan polutan dipengaruhi oleh kecepatan aliran, koefisien difusi, arah arus, lama pergerakan polutan, dll. Pada mekanisme transpor difusi 2D dapat menggunakan pendekatan beda maju untuk turunan waktu dan beda pusat untuk turunan ruang sedangkan model adveksi 2D menggunakan pendekatan beda maju untuk turunan waktu dan turunan ruang dilakukan dengan melihat arah kecepatan u, di mana ketika u > 0 maka turunan ruang menggunakan pendekatan beda mundur sedangkan ketika u < 0 maka turunan ruang menggunakan pendekatan beda maju. Berikut terdapat beberapa skenario yang dihasilkan dari pemodelan persamaan adveksi-difusi 2D:

**Skenario 1**

![gif teta 64](https://user-images.githubusercontent.com/106040925/169803814-3aa9063b-bcf9-4031-90fa-9da6bfaf78c7.gif)

Pada skenario 1 (theta = 42) didapatkan hasil bahwa konsetrasi polutan yang bersumber dari tengah bergerak kearah timur laut secara kontinu dengan iterasi waktu 0,5 sampai 104. 

**Skenario 2**

![gif teta 124](https://user-images.githubusercontent.com/106040925/169803852-16bb335c-c89b-4efe-abc9-eb496db3e117.gif)

Pada skenario 2 (theta =102) didapatkan hasil bahwa konsetrasi polutan yang bersumber dari tengah bergerak kearah tenggara secara kontinu dengan iterasi waktu 0,5 sampai 104. 

**Skenario 3**

![gif teta 199](https://user-images.githubusercontent.com/106040925/169803891-46fa22d6-1727-495f-822b-0a69d7f38865.gif)

Pada skenario 3 (theta = 177) didapatkan hasil bahwa konsetrasi polutan yang bersumber dari tengah bergerak kearah barat daya secara kontinu dengan iterasi waktu 0,5 sampai 104.

**Skenario 4**

![gif teta 379](https://user-images.githubusercontent.com/106040925/169803912-ce9362d3-e53c-46b2-ad1d-c8704c48799b.gif)

Pada skenario 4 (theta = 357) didapatkan hasil bahwa konsetrasi polutan yang bersumber dari tengah bergerak kearah timur laut secara kontinu dengan iterasi waktu 0,5 sampai 104. 

Arus memberikan peranan dalam proses adveksi-difusi 2D dengan pergerakan polutan yang sesuai dengan arah arus sedangkan koefisien adveksi-difusi memberikan gambaran proses transportasi konsentrasi polutan ke segala arah. Kecepatan pergerakan dan penyebaran bergantung pada kecepatan arus. Persamaan adveksi-difusi dapat diaplikasikan dalam mendeteksi penyebaran polusi di perairan. Hal ini sesuai dengan definisi adveksi yang berarti proses perpindahan panas akibat adanya aliran dan difusi berarti proses perpindahan panas berupa rambatan dari air dengan temperatur tinggi ke air dengan temperatur yang lebih rendah. Persamaan adveksi-difusi dapat diaplikasikan juga untuk mengetahui penyebaran polutan udara akibat cerobong asap dari pabirk-pabrik, di mana semakin tinggi ketinggian sumber polutan maka semakin menurun kadar cemaran polutannya dan semakin tinggi ketinggian sumber polutan maka kadar cemaran polutan akan tetap sama. Dengan adanya penelitian yang menggunakan model seperti itu diharapkan dapat mencegah terjadinya polutan sehingga pencemaran dapat dihindari.



# **Hidrodinamika 1D**
hidrodinamika itu adalah cabang ilmu yang mempelajari pergerakan suatu fluida, faktor apa saja yang mempengaruhi pergerakan tersebut. Pada modul 3 ini akan di buat pemodelan dengan dasar hidrodinamika satu dimensi. Di praktikum kali ini memprogramkan suatu simulasi elevasi muka air laut dan kecepatan arus yang dipengaruhi oleh beberapa parameter. pada model ini akan dipengaruhi oleh beberapa hal yaitu faktor eksternal seperti pasang surut, gelombang, viskositas, gaya coriolis, dan lain lain. faktor faktor tersebut merupakan faktor oseanorafi yang berpengaruh pada model yang akan dijalankan pada program hidrodinamika satu dimensi ini. untuk model hidrodinamika ini dibangun berdasarkan persamaan atau hukum konservasi massa atau kontinuitas dan persamaan momentum : ![persamaan momentum](https://user-images.githubusercontent.com/106046240/169879942-41973951-7f7f-4216-a58a-9a44caedd487.jpg)
![persamaa kontinuitas](https://user-images.githubusercontent.com/106046240/169880358-a3292cdf-98d8-4964-bb36-c7f76560c3e9.jpg)

persamaan diatas merupakan persamaan yang menjadi dasar dari model ini. Kemudian selanjutnya model hidrodinamika ini akam menggunakan persamaan pembangun. persamaan pembangun ini nantinya akan dikembangkan lagi dan juga ditambah dengan persamaan transport yang berubah terhadap waktu dan arah. persamaan persamaan yang digunakan pada modul ini sudah pernah digunakan pada modul sebelumnya yaitu modul 1 dan modul 2. dalam program modul 3 ini juga diperlukan diskritisasi supaya modelnya bisa berjalan dan menghasilkan hasil yang akurat.

setelah hasil coding di run maka akan menghasilkan beberapa grafik seperti dibawah ini :
![Fig0](https://user-images.githubusercontent.com/106046240/169881348-c9697e79-bc0e-470c-b01c-d6fc2319e4f2.png)
![fig1](https://user-images.githubusercontent.com/106046240/169881376-d06a015e-19b0-495b-8398-42f3ae037cb3.png)
![Fig2](https://user-images.githubusercontent.com/106046240/169881396-8a74f51a-46a9-4ffa-9302-daf13f4a16bc.png)
![Fig3](https://user-images.githubusercontent.com/106046240/169881789-b286de83-6424-440a-8aca-bebfd2e4fc2f.png)

Berdasarkan grafik yang dihasilkan terdapat 2 jenis grafik dengan perbedaan berdasarkan kedalaman atau elevasi pada masing-masing grafik. Grafik 1 dan 2 menunjukan pola grafik yang tidak konsisten apabila ditinjau berdasarkan besar elevasi pada grafik tersebut menunjukan kedalaman tersebut berada pada perairan dangkal dengan kondisi batas yang tidak terpenuhi. Grafik 3 dan 4 dimana terlihat pola grafik yang konsisten dengan semakin besar grid elevasi maka nilai kecepatannya akan semakin meningkat. Grafik 3 dan 4 terlihat lebih konsisten yang dapat diartikan bahwa jenis perairan pada grafik 3 dan 4 yang menjadi objek analisis merupakan perairan dalam. Berdasarkan pola pada grafik dan nilai yang didapat antara besar elevasi dengan kecepatan terlihat sinkorn, sehingga untuk grafik 3 dan 4 tidak diperlukan analisis dengan model 2 dimensi atau 3 dimensi, akan tetapi grafik 1 dan 2 dimana lokasinya adalah perairan pesisir diperlukan analisis lanjutan menggunakan pemodelan 2 ataupun 3 dimensi 

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
5. Marto Naldo Sitanggang/26050120140038/Oseanografi B
6. Valiant Muhammad Wening/26050120130107/Oseanografi A
