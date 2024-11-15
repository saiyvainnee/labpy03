## Latihan 1 Data

````python
import random

# Meminta pengguna memasukkan nilai n
n = int(input("Masukkan nilai N: "))

# Looping untuk menghasilkan n bilangan acak
for i in range(1, n + 1):
    # Menghasilkan bilangan acak antara 1 dan 5
    bilangan_acak = random.uniform(1, 5)

    # Menampilkan data ke-i dan nilai bilangan acak
    print(f"data ke: {i} => {bilangan_acak}")
    print("Selesai")
````
## Hasil
````python
Masukkan nilai N: 4
data ke: 1 => 4.34496385888319
Selesai
data ke: 2 => 2.204136526526117
Selesai
data ke: 3 => 4.449889657248039
Selesai
data ke: 4 => 4.317895572151588
Selesai
PS C:\Users\SAYIDINA RAMADHAN\Desktop\vscode sayi>
````
## Alur algoritma Program
-Input Nilai N: Program dimulai dengan meminta pengguna untuk memasukkan nilai n, yang menentukan berapa banyak bilangan acak yang akan dihasilkan. Nilai n ini kemudian dikonversi menjadi tipe data integer menggunakan int(input(...)).

-Looping: Program kemudian memasuki sebuah loop yang akan dijalankan sebanyak n kali (dimulai dari 1 hingga n), menggunakan for i in range(1, n + 1).

-Generate Bilangan Acak: Pada setiap iterasi dalam loop, program menghasilkan sebuah bilangan acak menggunakan random.uniform(1, 5). Fungsi random.uniform(1, 5) menghasilkan bilangan acak dengan nilai pecahan yang berada di antara 1 dan 5 (inklusif).

-Menampilkan Hasil: Setelah bilangan acak dihasilkan, program mencetak hasilnya dalam format:

-Menampilkan indeks data ke-i (misalnya "data ke: 1") dan nilai bilangan acak yang dihasilkan.
Setelah itu, mencetak "Selesai" untuk menandakan bahwa proses untuk data tersebut telah selesai.
Ulangi Proses: Langkah ini diulang hingga semua n data bilangan acak dihasilkan dan ditampilkan.

## Latihan 2

``` python
# Inisialisasi laba per bulan
laba = 0
total_laba = 0

# Loop untuk bulan 1 sampai 9
for bulan in range(1, 9):
    # Menentukan laba berdasarkan bulan
    if bulan in [1, 2]:  # Bulan 1 dan 2
        laba = 0
    elif bulan in [3, 4]:  # Bulan 3 dan 4
        laba = 1000000.0
    elif bulan in [5,6,7]:  # Bulan 5, 6, dan 7
        laba = 5000000.0
    elif bulan in [8]:  # Bulan 8
        laba = 20000000.0
    elif bulan == 9: # Bulan 9
        laba = 1000000000.0
    
    # Menampilkan laba per bulan
    print(f"laba bulan ke- {bulan} sebesar: {laba}")
    
    # Menambahkan laba ke total laba
    total_laba += laba

# Menampilkan total laba
print(f"Total laba adalah: {total_laba}")
````
````python
laba bulan ke- 1 sebesar: 0
laba bulan ke- 2 sebesar: 0
laba bulan ke- 3 sebesar: 1000000.0
laba bulan ke- 4 sebesar: 1000000.0
laba bulan ke- 5 sebesar: 5000000.0
laba bulan ke- 6 sebesar: 5000000.0
laba bulan ke- 7 sebesar: 5000000.0
laba bulan ke- 8 sebesar: 20000000.0
Total laba adalah: 37000000.0
````
## Alur Algoritma Program
Inisialisasi:

laba = 0 (untuk menyimpan laba per bulan).
total_laba = 0 (untuk menghitung total laba).
Looping Bulan 1-8:

Program menghitung laba berdasarkan bulan:
Bulan 1-2: laba = 0
Bulan 3-4: laba = 1 juta
Bulan 5-7: laba = 5 juta
Bulan 8: laba = 20 juta
Bulan 9: laba = 1 miliar (meskipun tidak digunakan di sini).
Menampilkan Laba: Program menampilkan laba tiap bulan.

Menghitung Total Laba: Total laba dihitung dengan menjumlahkan laba tiap bulan.

Output: Program menampilkan total laba setelah 8 bulan.

## latihan 3
````python
def atm():
  saldo = 1000000

  while True:
    print("Saldo saat ini: Rp", saldo)
    print("1. Tarik Uang")
    print("2. Keluar")
    pilihan = int(input("Pilih menu (1/2): "))

    if pilihan == 1:
      jumlah_tarik = int(input("Masukkan jumlah penarikan: "))
      if jumlah_tarik <= saldo:
        saldo -= jumlah_tarik
        print("Penarikan berhasil!")
      else:
        print("Saldo tidak mencukupi!")
    elif pilihan == 2:
      print("Terima kasih telah menggunakan ATM!")
      break
    else:
      print("Pilihan tidak valid!")

atm()
````
````python
Saldo saat ini: Rp 1000000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Masukkan jumlah penarikan: 50000
Penarikan berhasil!
Saldo saat ini: Rp 950000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Masukkan jumlah penarikan: 1500000
Saldo tidak mencukupi!
Saldo saat ini: Rp 950000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 1
Masukkan jumlah penarikan: 150000
Penarikan berhasil!
Saldo saat ini: Rp 800000
1. Tarik Uang
2. Keluar
Pilih menu (1/2): 2
Terima kasih telah menggunakan ATM!
PS C:\Users\SAYIDINA RAMADHAN\Desktop\vscode sayi>
````
## Alur algoritma
-Inisialisasi Saldo: Saldo awal diatur menjadi 1 juta.

-Menu Utama (Loop): Program menampilkan menu dengan dua pilihan:

1. Tarik Uang: Meminta jumlah penarikan, dan memeriksa apakah saldo cukup. Jika cukup, saldo dikurangi, jika tidak, menampilkan pesan saldo tidak mencukupi.
2. Keluar: Program berhenti dan mencetak pesan terima kasih.
Validasi Pilihan: Jika pengguna memilih selain 1 atau 2, program menampilkan pesan "Pilihan tidak valid".

-Loop Berulang: Program terus mengulang hingga pengguna memilih untuk keluar.
