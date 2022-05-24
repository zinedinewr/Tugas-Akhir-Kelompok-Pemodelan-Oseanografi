# Tugas Akhir Kelompok Pemodelan Oseanografi 💻
Repositori ini dibuat untuk memenuhi tugas akhir mata kuliah Praktikum Pemodelan Oseanografi tahun 2022. Bahasa pemograman yang digunakan dalam repositori ini adalah bahasa pemograman *Python* yang dapat dikerjakan pada *text editor*, seperti *Google Colaboratory* dan *Jupyter Notebook*. Modul yang digunakan pada repositori ini adalah *matplotlib*, *numpy*, dan *sys*. Seluruh _script_ yang dibuat merupakan hasil kerja kelompok 9 Oseanografi 2020. 

Semoga bermanfaat <3

# **Adveksi-Difusi 1D**
Adveksi merupakan mekanisme perpindahan massa suatu materi dari suatu titik ke titik lainnya sedangkan difusi dapat didefinisikan sebagai sebuah proses dimana suatu zat bergerak dari konsentrasi tinggi ke rendah. Persamaan gelombang linier orde satu termasuk ke dalam persamaan diferensial hiperbolik yang menggambarkan mekanisme transportasi fluida dengan arah tertentu. Persamaan tersebut dapat didiskritisasi menggunakan secara eksplisit maupun implisit. Tipe eksplisit memiliki keunggulan berupa stabilitas hitungan dan perhitungan yang lebih mudah dibandingkan tipe implisit tetapi tipe eksplisit memerlukan proses yang lama. Sementara itu, difusi merupakan peristiwa dimana terjadi transfer materi melalui materi lain. Transfer materi ini berlangsung karena atom atau partikel selalu bergerak oleh agitasi thermal. Difusi merupakan proses irreversible (tidak dapat diubah). Pada fase gas dan cair, peristiwa difusi mudah terjadi, sedangkan pada fase padat difusi juga terjadi walaupun memerlukan waktu yang lebih lama.

![image](https://user-images.githubusercontent.com/106045814/169815374-47edb95b-3055-46c9-a414-7fdf7fa48c5c.png)

Gambar 1 menggambarkan fenomena proses difusi. Ketika baru terjadi pelepasan massa, kerapatan massa masih berkonsentrasi di sekitar sumber dan belum menyebar. Hal ini terlihat dari daerah hitam yang terkonsentrasi di sekitar sumber dan terang di titik-titik yang jauh dari sumber (Gambar 1a). Pada gambar 1b, daerah hitam di sekitar sumber mulai membesar, menunjukan massa telah mulai menyebar. Penyebaran massa ini terus terjadi dan semakin tampak jelas pada gambar 1c yaitu dengan membesarnya daerah hitam dan juga memudarnya warna hitam di sekitar sumber. Pada gambar 1d, di sekitar sumber tidak hitam lagi yang menunjukan penurunan kerapatan massa yang cukup berarti di titik sumber. Penurunan kerapatan massa di sekitar sumber ini semata-mata karena massa telah menyebar dan secara total tidak terjadi pengurangan ataupun penambahan massa.

**Persamaan Adveksi-Difusi 1D**
1. Difusi 

![image](https://user-images.githubusercontent.com/106045814/169814201-222a9150-dcd1-49b6-9852-10ee3d0e0dff.png)

2. Diskritisasi Proses Difusi 1D

![image](https://user-images.githubusercontent.com/106045814/169814299-43b87601-02e5-4fae-b934-70f52fc9461d.png)

3. Persamaan Adveksi-Difusi 

![image](https://user-images.githubusercontent.com/106045814/169814451-0ff1ead3-53cd-4732-a937-8f9a8f79f835.png)

dengan kriteria : 

![image](https://user-images.githubusercontent.com/106045814/169814549-2306dd0f-2ae9-44ff-97a2-c5685223c0bb.png)

# **Adveksi-Difusi 2D**
Gejala yang terjadi di perairan sangat penting untuk dipelajari terutama yang berhubungan dengan adveksi dan difusi polutan. Fenomena aliran dan transportasi merupakan suatu gejala alam yang penting untuk dipelajari karena mempunyai pengaruh terhadap beberapa studi rekayasa. Fenomena tersebut terjadi dalam berbagai macam situasi fisik, seperti transfer panas, proses pemisahan zat kimia, aliran fluida dalam media berpori, penyebaran kontaminan dalam cairan, dan transportasi partikel-partikel kecil, seperti penyebaran polutan, garam, dan sedimen di perairan dangkal. Model matematika dapat digunakan dalam persoalan-persoalan polusi lingkungan yang terjadi pada perairan dengan disimulasikan atau diturunkan fenomena kejadiannya. 

Adveksi merupakan proses transportasi berupa aliran rata-rata atau arus, seperti sungai atau gerakan pasang surut, yang digerakkan oleh gaya gravitasi atau tekanan dan berupa gerak horizontal sedangkan difusi merupakan proses transportasi materi dari suatu sistem ke bagian yang lain sebagai hasil pergerakan molekul acak, di mana setiap partikel difusi bergerak secara acak di bidang difusi. Adveksi-difusi merupakan proses transportasi materi dari satu bagian sistem ke bagian yang lain sebagai hasil dari gerakan molekul acak yang melibatkan proses transportasi fluida dalam bentuk aliran rata-rata atau arus yang dipengaruhi oleh gaya gravitasi atau tekanan dan berupa gerak horizontal. 

Persamaan adveksi-difusi merupakan persamaan matematis yang didesain untuk mempelajari fenomena transpor polutan. Persamaan transpor merupakan salah satu persamaan diferensial yang merepresentasikan sirkulasi aliran air di estuari dengan variabel C sebagai fungsi ruang dan waktu. Pergerakan polutan dipengaruhi oleh kecepatan aliran, koefisien difusi, arah arus, lama pergerakan polutan, dll. Pada mekanisme transpor difusi 2D dapat menggunakan pendekatan beda maju untuk turunan waktu dan beda pusat untuk turunan ruang sedangkan model adveksi 2D menggunakan pendekatan beda maju untuk turunan waktu dan turunan ruang dilakukan dengan melihat arah kecepatan u, di mana ketika u > 0 maka turunan ruang menggunakan pendekatan beda mundur sedangkan ketika u < 0 maka turunan ruang menggunakan pendekatan beda maju. Pemodelan persamaan adveksi-difusi 2D dapat menghasilkan beberapa skenario.

**Impor Modul**
```
import matplotlib.pyplot as plt
import numpy as np
import sys
#%%
def percentage(part, whole):
        percentage = 100 * float(part)/float(whole)
        return str(round(percentage,2)) + "%"
#%%
```

**Input Parameter Awal**
```
C = 1.77 #Kecepatan Aliran
ad = 1.77 #Koefisien Difusi
theta = 0 + 77 #Arah Arus
```

**Input Parameter Lanjutan**
```
q = 0.95 #Kriteria Kestabilan
x = 500 #Jumlah Grid Horizontal x
y = 500 #Jumlah Grid Vertikal y
dx = 5
dy = 5
Tend = 100 + 7 #Lama Simulasi
dt = 0.5
px = 250 #Polutan pada Grid x
py = 230 + 7 #Polutan pada Grid y
Ic = 1000 + 77 #Jumlah Polutan
```

**Perhitungan U dan V**
```
u = C * np.sin(theta*np.pi/180)
v = C * np.cos(theta*np.pi/180)
dt_count = 1/((abs(u)/(q*dx))+(abs(v)/(q*dy))+(2*ad/(q*dx**2))+(2*ad/(q*dx**2)))
```

**Perhitungan Jumlah *Mesh* dan *Timestep***
```
Nx = int(x/dx) #Jumlah Mesh dalam Arah x
Ny = int(x/dy) #Jumlah Mesh dalam Arah y
Nt = int(Tend/dt) #Jumlah timestep
```

**Perhitungan Titik lepas Polutan**
```
px1 = int (px/dx)
py1 = int (py/dy)
```

**Penyederhanaan Fungsi**
```
lx = u*dt/dx
ly = v*dt/dy
ax = ad*dt/dx**2
ay = ad*dt/dy**2
cfl = (2*ax + 2*ay + abs(lx) + abs(ly))
```

**Perhitungan CFL**
```
if cfl >= q:
    print('CFL Violated, Please use dt :'+str(round(dt_count,4)))
    sys.exit()
```

**Pembuatan Grid**
```
x_grid = np.linspace(0-dx, x+dx, Nx+2) #GhostNode pada Ujung Boundary
y_grid = np.linspace(0-dy, y+dx, Ny+2) #GhostNode pada Ujung Boundary
t = np.linspace(0, Tend, Nt+1)
x_mesh,y_mesh = np.meshgrid(x_grid, y_grid)
F = np.zeros((Nt+1,Ny+2,Nx+2))
F[0,py1,px1] = Ic #Kondisi Awal
```

**Iterasi**
```
for n in range (0,Nt):
    for i in range (1,Ny+1):
        for j in range (1,Nx+1):
            F[n+1,i,j]=((F[n,i,j]*(1-abs(lx)-abs(ly))) + (0.5*(F[n,i-1,j]*(ly+abs(ly)))) + (0.5*(F[n,i+1,j]*(abs(ly)-ly))))
    #Kondisi Batas (Dirichlet Condition)
    F[n+1,0,:] = 0 #BC Bawah
    F[n+1,:,0] = 0 #BC Kiri
    F[n+1,Ny+1,:] = 0 #BC Atas
    F[n+1,:,Nx+1] = 0 #BC Kanan
```

**Pembuatan Grafik**
```
    #Output Gambar
    plt.clf()
    plt.pcolor(x_mesh, y_mesh, F[n+1,:,:],cmap = 'jet',shading = 'auto', edgecolors = 'k')
    cbar = plt.colorbar(orientation = 'vertical',shrink = 0.95, extend ='both')
    cbar.set_label(label='concentration', size = 8)
    #plt.clim(0,100)
    plt.title('Kirana Adhiningtyas_26050120130077 - Skenario 1 \n t='+str(round(dt*(n+1),3))+', Kondisi Awal='+str(Ic),fontsize=10)
    plt.xlabel('x_grid',fontsize=9)
    plt.ylabel('y_grid',fontsize=9)
    plt.axis([0,x,0,y])
    #plt.pause(0.01)
    plt.savefig(str(n+1)+'.png', dpi = 300)
    plt.close()
    print('running timestep ke :' + str(n+1) + ' dari :' + str(Nt) + ' ('+ percentage(n+1,Nt)+')')
```

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
Hidrodinamika merupakan cabang ilmu yang mempelajari pergerakan suatu fluida dan faktor yang memengaruhi pergerakan tersebut. Model hidrodinamika adalah model yang didasarkan pada deskripsi proses-proses yang memengaruhi sirkulasi dan pencampuran massa air dengan hukum pembangun yang terdiri dari hukum kontinuitas dan momentum serta diasumsikan dengan adanya skenario. Pemodelan hidrodinamika 1D dapat digunakan untuk memodelkan suatu simulasi elevasi muka air laut dan kecepatan arus yang dipengaruhi oleh beberapa parameter. Model ini dipengaruhi oleh faktor eksternal, seperti pasang surut, gelombang, viskositas, gaya coriolis, dan lain lain. Faktor-faktor tersebut merupakan faktor oseanografi yang berpengaruh pada model hidrodinamika 1D yang akan dijalankan. Beberapa kelemahan model hidrodinamika adalah terdapat banyak data, rawan *error* ketika terdapat perhitungan aliran kritis, dan simulasi lama.

**Persamaan Momentum**

![persamaan momentum](https://user-images.githubusercontent.com/106046240/169879942-41973951-7f7f-4216-a58a-9a44caedd487.jpg)

**Persamaan Kontinuitas**

![persamaa kontinuitas](https://user-images.githubusercontent.com/106046240/169880358-a3292cdf-98d8-4964-bb36-c7f76560c3e9.jpg)

Pemodelan hidrodinamika 1D juga menggunakan persamaan pembangun yang nantinya akan dikembangkan lagi dan persamaan transport yang berubah terhadap waktu dan arah. Persamaan-persamaan yang digunakan pada pemodelan ini perlu didiskritisasi agar pemodelan bisa berjalan dan menghasilkan hasil yang akurat. Pemodelan hidrodinamika 1D dapat menghasilkan dua jenis grafik dengan perbedaan berdasarkan kedalaman atau elevasi pada masing-masing grafik.

**Impor Modul**
```
import matplotlib.pyplot as plt
import numpy as np
```

**Input Parameter Awal**
```
p = 5000 #Panjang grid
t = 1200 #Waktu simulasi
A = 0.5 #Amplitudo
D = 15 #Kedalaman
dt = 2
dx = 100
To = 300 #Periode
```

**Input Parameter Lanjutan**
```
g = 9.8 #Koefisien gravitasi
pi = np.pi
C = np.sqrt(g*D) #Kecepatan arus
s = 2*pi/To #Kecepatan sudut gelombang
L = C*To #Panjang gelombang
k = 2*pi/L #Koefisien panjang gelombang
Mmax = int(p//dx)
Nmax = int(t//dt)

zo = [None for _ in range(Mmax)]
uo = [None for _ in range(Mmax)]

hasilu = [None for _ in range(Nmax)]
hasilz = [None for _ in range(Nmax)]

for i in range(1, Mmax+1):
  zo[i-1] = A*np.cos(k*(i)*dx)
  uo[i-1] = A*C*np.cos(k*((i)*dx+(0.5)*dx))/(D+zo[i-1])
for i in range(1, Nmax+1):
  zb = [None for _ in range(Mmax)]
  ub = [None for _ in range(Mmax)]
  zb[0] = A*np.cos(s*(i)*dt)
  ub[-1] = A*C*np.cos(k*L-s*(i)*dt)/(D+zo[-1])
  for j in range(1, Mmax):
    ub[j-1] = uo[j-1]-g*(dt/dx)*(zo[j]-zo[j-1])
  for k in range(2, Mmax+1):
    zb[k-1] = zo[k-1]-(D+zo[k-1])*(dt/dx)*(ub[k-1]-ub[k-2])
    hasilu[i-1] = ub
    hasilz[i-1] = zb
  for p in range(0, Mmax):
    uo[p] = ub[p]
    zo[p] = zb[p]
```

**Pembuatan Grafik**
```
def rand_col_hex_string():
  return f'#{format(np.random.randint(0,16777215), "#08x")[2:]}'

hasilu_np = np.array(hasilu)
hasilz_np = np.array(hasilz)

fig0, ax0 = plt.subplots(figsize=(12,8))
for i in range (1, 16):
  col0 = rand_col_hex_string()
  line, = ax0.plot(hasilu_np[:,i-1], c=col0, label=f'n={i}')
  ax0.legend()

  ax0.set(xlabel='Waktu', ylabel='Kecepatan Arus',
          title=''' Kirana Adhiningtyas_26050120130077
          Perubahan Kecepatan Arus dalam Grid Tertentu di Sepanjang Waktu''')
  ax0.grid()

fig1, ax1 = plt.subplots(figsize=(12,8))
for i in range (1, 16):
  col1 = rand_col_hex_string()
  line, = ax1.plot(hasilz_np[:,i-1], c=col1, label=f'n={i}')
  ax1.legend()

  ax1.set(xlabel='Waktu', ylabel='Elevasi Muka Air',
          title=''' Kirana Adhiningtyas_26050120130077
          Perubahan Elevasi Permukaan Air dalam Grid Tertentu di Sepanjang Waktu''')
  ax1.grid()

fig2, ax2 = plt.subplots(figsize=(12,8))
for i in range (1, 16):
  col2 = rand_col_hex_string()
  line, = ax2.plot(hasilu_np[i-1], c=col2, label=f't={i}')
  ax2.legend()

  ax2.set(xlabel='Grid', ylabel='Kecepatan Arus',
          title=''' Kirana Adhiningtyas_26050120130077
          Perubahan Kecepatan Arus dalam Waktu Tertentu di Sepanjang Waktu''')
  ax2.grid()

fig3, ax3 = plt.subplots(figsize=(12,8))
for i in range (1, 16):
  col3 = rand_col_hex_string()
  line, = ax3.plot(hasilz_np[i-1], c=col3, label=f't={i}')
  ax3.legend()

  ax3.set(xlabel='Grid', ylabel='Elevasi Muka Air',
          title=''' Kirana Adhiningtyas_26050120130077
          Perubahan Elevasi Permukaan Air dalam Waktu Tertentu di Sepanjang Waktu''')
  ax3.grid()

plt.show()
```

**Grafik 1**

![Fig0](https://user-images.githubusercontent.com/106046240/169881348-c9697e79-bc0e-470c-b01c-d6fc2319e4f2.png)

**Grafik 2**

![fig1](https://user-images.githubusercontent.com/106046240/169881376-d06a015e-19b0-495b-8398-42f3ae037cb3.png)

**Grafik 3**

![Fig2](https://user-images.githubusercontent.com/106046240/169881396-8a74f51a-46a9-4ffa-9302-daf13f4a16bc.png)

**Grafik 4**

![Fig3](https://user-images.githubusercontent.com/106046240/169881789-b286de83-6424-440a-8aca-bebfd2e4fc2f.png)

Grafik 1 dan 2 menunjukkan pola grafik yang tidak konsisten apabila ditinjau dari besar elevasi. Pada grafik tersebut menunjukan kedalaman berada pada perairan dangkal atau pesisir dengan kondisi batas yang tidak terpenuhi. Grafik 3 dan 4 menunjukkan pola grafik yang konsisten dengan grid elevasi yang semakin besar sehingga nilai kecepatannya semakin meningkat. Pada grafik tersebut terlihat lebih konsisten sehingga dapat diartikan bahwa jenis perairan yang menjadi objek analisis merupakan perairan dalam. Berdasarkan pola pada grafik dan nilai yang didapat antara besar elevasi dengan kecepatan terlihat sinkron sehingga untuk grafik 3 dan 4 tidak diperlukan analisis dengan model 2D atau 3D sedangkan grafik 1 dan 2 memerlukan analisis lanjutan menggunakan pemodelan 2D atau 3D.

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
