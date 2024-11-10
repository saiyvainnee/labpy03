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
Input Nilai N: Program dimulai dengan meminta pengguna untuk memasukkan nilai n, yang menentukan berapa banyak bilangan acak yang akan dihasilkan. Nilai n ini kemudian dikonversi menjadi tipe data integer menggunakan int(input(...)).

Looping: Program kemudian memasuki sebuah loop yang akan dijalankan sebanyak n kali (dimulai dari 1 hingga n), menggunakan for i in range(1, n + 1).

Generate Bilangan Acak: Pada setiap iterasi dalam loop, program menghasilkan sebuah bilangan acak menggunakan random.uniform(1, 5). Fungsi random.uniform(1, 5) menghasilkan bilangan acak dengan nilai pecahan yang berada di antara 1 dan 5 (inklusif).

Menampilkan Hasil: Setelah bilangan acak dihasilkan, program mencetak hasilnya dalam format:

Menampilkan indeks data ke-i (misalnya "data ke: 1") dan nilai bilangan acak yang dihasilkan.
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
