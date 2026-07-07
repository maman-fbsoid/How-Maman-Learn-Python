# APA itu Function

Function adalah sekumpulan kode yang diberi nama agar bisa dipakai berkali kali

Nah jadi simpelnya kita bisa pakai satu kode untuk digunakan berkali kalo

### Def

Pertama kita bakal pake `def`

Gunanya apa?

Untuk membuat Function itu

Gimana caranya?

Gini

```python
def sapa():
    print("Halo")

sapa()
```

Nah alih alih pake `print()` biasa, kita bisa pake `def` agar bisa print lebih mudah untuk digunakan berkali kali

Contoh lagi

```python
def sapa(nama):
    print(f"Halo, {nama.title()}")

sapa('maman')
```

Nah daripada pake `print("Halo, maman")` terus kita mau sapa nama lain, mending pake def biar ga nulis print terus terusan

Cara kerja kode di atas simpel

`def` pertama bikin Function `sapa(nama)` terus di dalamnya di isi pake `print(f"Halo, {nama.title()}")` yang kita fahami bahwa di situ kita pake `nama` buat nanti bikin `sapa('maman')`

### Membuat argumen

Nah sekarang kita masuk lebih jauh

```python
def hewan(tipe_hewan, nama_hewan):
    print(f"\nAku punya {tipe_hewan}.")
    print(f"Nama {tipe_hewan}ku adalah {nama_hewan.title()}.")

hewan('kucing', 'Viktor')
```

Outputnya

```python
Aku punya kucing.
Nama kucingku adalah Viktor.
```

Kalo bingung wajar, jadi cara kerjanya gini

Dibuat Function `hewan(tipe_hewan, nama_hewan)`

Terus di dalamnya di isi pake `print()` dengan string berisi `tipe_hewan` dan `nama_hewan`

Dan akhirnya kita keluarkan semuanya dengan bikin ya jenis hewannya dan nama hewannya

### Return

Sekarang coba kita pake `return`

`return` adalah keyword yang digunakan untuk mengembalikan hasil dari sebuah function kepada bagian program yang memanggilnya

Langsung ke contohnya aja ya kita

```python
def nama_orang(nama_depan, nama_belakang):
    nama_lengkap = f"{nama_depan} {nama_belakang}"
    return nama_lengkap.title()

programmer = nama_orang('ada', 'lovelace')
print(programmer)
```

Nah

Pertama `def` bikin function nama orang dengan isi nama depan dan belakang

Lalu di dalamnya di isi `nama_orang` dan di dalamnya di isi 2 parameter yaitu `nama_depan` dan `nama_belakang`

Terus kita return tuh

Nah yang masing bingung return tuh kek gimana sih caranya

Dia tuh kek bilang "Oke, gw udah `jadiin nama_lengkap` huruf depannya kapital. Nih hasilnya: `Ada Lovelace`. Ambil"

Gitu loh ya

### Gabungin if else

Nah kita bakal gabungin sama if else dan juga kita bakal bikin argumen opsional

Hah argumen opsiopnal?

Iya

Jadi bebas mau di isi sama enggak gitu loh

Contoh

```python
def nama_orang(nama_depan, nama_belakang, nama_tengah=''):
    if nama_tengah:
        nama_lengkap = f"{nama_depan} {nama_tengah} {nama_belakang}"
    else:
        nama_lengkap = f"{nama_depan} {nama_belakang}"
    return nama_lengkap.title()

programmer = nama_orang('ada', 'lovelace')
print(programmer)

programmer = nama_orang('terry', 'davis', 'a.')
print(programmer)
```

Nah kan pake `nama_tengah=''` itu adalah Default Parameter alias parameter bawaan. Nah juga ini fungsinya bilang ke python "Kalo inputnya kosong di kosongin aja jangan di eror-in"

Lalu kita biki 2 kondisi bahwa kalo nanti muncul 3 nama kita pake yang if dan ya kalo 2 sebaliknya

Simpel kan logikanya

Oh iya ini outputnya

```python
Ada Lovelace
Terry A. Davis
```

Gitu

### Kombinasi dengan while loop

Nah sekarang kita bakal gabungin pake while loop bikin infinity loop

```python
def nama_orang(nama_depan, nama_belakang):
    nama_lengkap = f"{nama_depan} {nama_belakang}"
    return nama_lengkap.title()

while True:
    print("\nMohon masukan namamu")
    n_depan = input("Nama depan: ")
    n_belakang = input("Nama belakang: ")

    nama_lengkap = nama_orang(n_depan, n_belakang)
    print(f"\nHalo, {nama_lengkap}!")
```

Outputnya

```python
Mohon masukan namamu
Nama depan: Maman
Nama belakang: Fungky

Halo, Maman Fungky!

Mohon masukan namamu
Nama depan: Budi
Nama belakang: Utomo

Halo, Budi Utomo!

Mohon masukan namamu
Nama depan: 
```

Nah dia abakal loop terus tanpa henti nanyain namamu

Sekarang coba kita bikin biar bisa keluar

```python
def nama_orang(nama_depan, nama_belakang):
    nama_lengkap = f"{nama_depan} {nama_belakang}"
    return nama_lengkap.title()

while True:
    print("\nMohon masukan namamu")
    print("(Ketik 'q' untuk keluar kapan saja")
    
    n_depan = input("Nama depan: ")
    if n_depan == 'q':
        break
    
    n_belakang = input("Nama belakang: ")
    if n_belakang == 'q':
        break

    nama_lengkap = nama_orang(n_depan, n_belakang)
    print(f"\nHalo, {nama_lengkap}!")
```

Nah kalo kalian lihat, kalo kuketi q bakal bikin program berhenti pake `break`

### Melewati list

Nah kita bakal ngelewatin list agar muncul urut satu per satu elemen

Caranya kita bakal gabungin `def` dan for loop

Contoh

```python
def user_terbaik(namanya):
    for nama in namanya:
        menyapa = f"Halo, {nama.title()}!"
        print(menyapa)

username = ['budi', 'epan', 'bambang']
user_terbaik(username)
```

Outputnya

```python
Halo, Budi!
Halo, Epan!
Halo, Bambang!
```

Nah cara kerjanya juga simpel dengan `def` bikin function, terus kam isi pake for loop

### Modifikasi list dalam Function

Jadi di sini kita bakal belajar cara mdifikasi list yang ada di dalam function

Ini agak ribet sih cara kerjanya tapi tetap bakal kujelaskan

Contoh kodenya

```python
def model_3d(model_belum_jadi, model_jadi):
    while model_belum_jadi:
        model_sekarang = model_belum_jadi.pop()

        print(f"Membuat model: {model_sekarang}")
        model_jadi.append(model_sekarang)

def menunjukkan_model_jadi(model_jadi):
    print("\nModelnya lagi di buat ya: ")
    for model_selesai in model_jadi:
        print(model_jadi)

model_belum_jadi = ['bus', 'truk', 'kereta']
model_jadi = []
model_3d(model_belum_jadi, model_jadi)
menunjukkan_model_jadi(model_jadi)
```

Jadi ini bekerja tuh

Program ini bekerja dengan cara mengambil satu per satu model dari daftar model_belum_jadi menggunakan pop(), menampilkan proses pembuatannya, lalu memindahkannya ke daftar model_jadi menggunakan append() hingga daftar model_belum_jadi kosong, kemudian function menunjukkan_model_jadi() menampilkan semua model yang sudah selesai dibuat

Gituuu

# TO BE CONTINUED
