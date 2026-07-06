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

Gitu

Lalu kita biki 2 kondisi bahwa kalo nanti muncul 3 nama kita pake yang if dan ya kalo 2 sebaliknya

Simpel kan logikanya

Oh iya ini outputnya

```python
Ada Lovelace
Terry A. Davis
```

# TO BE CONTINUED
