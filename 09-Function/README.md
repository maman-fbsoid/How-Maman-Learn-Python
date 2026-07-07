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

### Menerima semua argumen berapapun jumlahnya

Kita bakal coba bikin fungsi yang bikin kita bisa masukin arumen berapapun jumlahnya

Caranya?

```python
def bakso(*isian):
    print(isian)

bakso('daging')
bakso('usus', 'cabai', 'naga')
```

Outputnya?

```python
('daging',)
('usus', 'cabai', 'naga')
```

Jadi kita kek bilang ke python bahwa "Kumpulin semua argumen kedalam satu wadah berapapun jumlahnya"

Jadi fungsi jadi `*` tuh bikin kita bebas berapapun jumlahnya masukin argumen

Sekarang coba kita rapikan dikit

```python
def bakso(*isian):
    print("\nIsian dalam baksomu adalah: ")
    for topping in isian:
        print(f"- {topping}")

bakso('daging')
bakso('usus', 'cabai', 'naga')
```

Outpunya

```python
Isian dalam baksomu adalah:
- daging

Isian dalam baksomu adalah:
- usus
- cabai
- naga
```

Nah jadi rapi dan bagus sekarang

### Mencampurkan argumen

Nah kita bakal coba campur menyampur dan ya tentu saja kodenya bakal seikit ribet kalau dibaca

Jadi kita bakal bikin kode yang sama tapi akan kita variasikan

```python
def bakso(jumlah, *isian):
    print(f"\nMembuat bakso sebanyak {jumlah}, dengan isian: ")
    for topping in isian:
        print(f"- {topping}")

bakso(2, 'daging')
bakso(12, 'cabai', 'daging', 'usus')
```

Outputnya

```pyhon
Membuat bakso sebanyak 2, dengan isian:
- daging

Membuat bakso sebanyak 12, dengan isian:
- cabai
- daging
- usus
```

Nah disini kalo dilihat ya bahwa kita memodifikasi dengan menambahkan `jumlah` dan string baru

That simple

### Menerima jumlah keyword argument yang tidak terbatas

Nah sekarang kita bakal coba dengan function dapat menerima keyword argumen yang tak terbatas

Gimana caraya?

Sini praktek dulu nanti tak jelasin

```python
def build_profile(awal, akhir, **user_info):
    profile = {}
    profile['nama_depan'] = awal
    profile['nama_belakang'] = akhir
    for key, value in user_info.items():
        profile[key] = value
    return profile

user_profile = build_profile('ada', 'lovelace', location='garut', hobi='makan pecel')
print(user_profile)
```

Outputnya

```python
{'nama_depan': 'ada', 'nama_belakang': 'lovelace', 'location': 'garut', 'hobi': 'makan p
ecel'}
```

Nah jadi gini le

Apa sih `**user_info`? itu tuh kwargs

Jadi dia kek bilang ke kalian "Kasih gue nama depan dan belakang, terus kalau ada informasi tambahan apa pun, tampung semuanya"

Nah kenapa pake `location=` dan `hobi=`? kok pake sama dengan?

Jadi kita pake itu tuh karena ya `garut` dan `makan pecel` tuh gabisa di baca pyton masuk mana karena ya parameter lain udah kepake

Jadi kita pake tuh sama dengan biar masuk ke kwargs karena itu keyword arguments

# import

Nah beberapa dari kalian mungkin pernah lihat ini di dalam script python

Jadi apa sih `import` ini?

Jadi ini tuh bisa bikin kita pake kode di tempat lain buat dipake di tempat yang sekarang untuk menghemat ruang dan waktu kalian juga biar ga ribet

Contohnya gimana sih?

Gini loh ya rek

```python
def isi_bakso(jumlah, *isian):
    print(f"\nMembuat bakso sebanyak {jumlah}, dengan isian: ")
    for topping in isian:
        print(f"- {topping}")
```

Anggap kode di atas ada di dalam file `tes_github.py` lalu kita mau salin kode di dalamnya ke file lain

Anggep file kedua namanya `tes_git.py` jadi tinggal pake import

```python
import tes_github

tes_github.isi_bakso(12, 'daging')
tes_github.isi_bakso(90, 'cabai', 'usus', 'naga')
```

Tuh! gimana? faham? outputnya sama loh ya!

### import function spesifik

Nah jadi kita bakal pake import buat dipake di function yang spesifik

Caranya gini

```python
from tes_github import isi_bakso

isi_bakso(12, 'daging')
isi_bakso(90, 'cabai', 'usus', 'naga')
```

Nah jadi kalian alih alih pake `tes_github.isi_bakso` satu persatu, mending langsung tunjuk `from tes_github from isi_bakso` gitu aja

### Alias

Nah buat user linux, kata alias udah ga asing lagi lah ya

Buat yang gak tahu, ini tuh semacam kita kasih nama custom ke sesuatu dan ini dipake di import

Caranya? gini

```python
import tes_github as tg

tg.isi_bakso(12, 'daging')
tg.isi_bakso(90, 'cabai', 'usus', 'naga')
```

Nah alih alih pake `tes_github.isi_bakso` yang panjang, kalian bisa singkat pake `as` jadi `tg` gitu!

Kalo pake function spesifik jadinyya gini

```python
from tes_github import isi_bakso as ib

ib(12, 'daging')
ib(90, 'cabai', 'usus', 'naga')
```

Nah tuh lihat bahwa kita pake `ib` alih alih pake `isi_bakso`

### import semua function

Materi terakhir kita bakal impport semua function jadi satu pake `*`

Gini caranya

```python
from tes_github import *

isi_bakso(12, 'daging')
isi_bakso(90, 'cabai', 'usus', 'naga')
```

Jadi pake ini kalian ga usah nyebut satu persatu function. Tinggal pake tanda petik udah jadi

# Penutup

Baiklah makasih semua yang udah dukung dan baca. Kalo ada kesalahan dan typo mohon maaf

ADIOS!
