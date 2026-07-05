# APA itu While Loop

Nah Whlie loop sebenernya mirip sama for loop

Tapi ada bedanya loh

While loop tuh bakal mengulang blok kode selama kondisinya `True`

## Praktek

Kita bakal langsung prakter biar kalian ga berangan angan

```python
angka = 1
while angka <= 5:
    print(angka)
    angka += 1
```

Outputnya

```python
1
2
3
4
5
```

Kalo kalian bingung sedikit soal kodenya itu wajar

Sini tak jelasin

Jadi `while` kita pake buat ngasih tahu. Contoh kek tadi `while <= 5`

Artinya tuh loop terus dari angka yang lebih kecil dari 5 dan berhenti pas sampe 5

Dan kalo `+= 1` tuh kita buang nambahing angka 1 terus. Kalo ga dikasih, while bakal terus nge loop angka 1

### Membuat user bisa berhenti dari loop

Nah ini sekarang gimana biar user bisa keluar dari while loop

```python
kalimat = "\nSelamat datang di sistem Immortal Snake!"
kalimat += "\nSilahkan bilang 'Berhenti!' Untuk menghentikan progam: "

message = ""
while message != 'Berhenti!':
    message = input(kalimat)
    print(message)
```

Outputnya

```python
Selamat datang di sistem Immortal Snake!
Silahkan bilang 'Berhenti!' Untuk menghentikan progam: Halo
Halo

Selamat datang di sistem Immortal Snake!
Silahkan bilang 'Berhenti!' Untuk menghentikan progam: Halo semua
Halo semua

Selamat datang di sistem Immortal Snake!
Silahkan bilang 'Berhenti!' Untuk menghentikan progam: Berhenti!
Berhenti!

[Process exited 0]
```

Bisa di lihat ia akan berhenti saat aku mengetik 'Berhenti!'

Loh caranya gimana?

Jadi gini, kita pertama kan bikin variabel `kalimat` terus kita bikin variabel `message` dengan isi kosong. Lah buat apa? Jadi itu dibuat sebagai tempat menyimpan input yang diketik oleh pengguna

Terus kita pake operator `!=` alias tidak sama dengan

Nah kita bilang `while message != 'Berhenti!'` itu kita bilang "Kalo dia bilang selain kata 'Berhenti!' lanjutkan programnya"

Dan kita pake `print(message)` buat nampilin apa yang kita ketik

### Memakai Flag

Flag? Bendera kah???

Hahahaha

Enggak ya bos!

Flag tuh tipenya kebanyakan `bool` alias `True` dan `False`

Contoh dalam while loop

```python
kalimat = "\nSelamat datang di sistem Immortal Snake!"
kalimat += "\nSilahkan bilang 'Berhenti!' Untuk menghentikan progam: "

aktif = True
while aktif:
    message = input (kalimat)

    if message == 'Berhenti!':
        aktif = False
    else:
        print(message)
```

### Memakai `break`

Oke sekarang kita akan memakai fuction `break`

Fungsinya apa?

Kalo kita pake Flag tuh ya dia bakal ngecek dulu tapi kalo pake break. Dia bakal langsung berhenti tanpa ngecek apapun

Contoh kodenya

```python
kalimat = "\nSebutkan satu makanan!"
kalimat += "\n(Silahkan bilang 'Berhenti!' Untuk menghentikan progam): "

while True:
    makanan = input(kalimat)

    if makanan == 'Berhenti!':
        break
    else:
        print(f"Aku suka {makanan.title()}!")
```

Nah kita pake breaknya di dalam `if`

Outputnya

```python
Sebutkan satu makanan!
(Silahkan bilang 'Berhenti!' Untuk menghentikan progam): Baso
Aku suka Baso!

Sebutkan satu makanan!
(Silahkan bilang 'Berhenti!' Untuk menghentikan progam): Kerikil
Aku suka Kerikil!

Sebutkan satu makanan!
(Silahkan bilang 'Berhenti!' Untuk menghentikan progam): Berhenti!

[Process exited 0]
```

### Memakai Continue while loop

Apa itu `continue`?

Jadi fungsinya adalah menghentikan sisa kode pada iterasi (putaran) saat ini dan langsung memaksa program melompat ke iterasi berikutnya

Kita bakal pake `continue`

Contoh kodenya

```python
angka = 0
while angka < 10:
    angka += 1
    if angka % 2 == 0:
        continue

    print(angka)
```

Nah cara kerjanya gimana?

Pertama `angka = 0` adalah putaran pertama

Nah kita pake `while` dengan bilng `< 10`

Terus di tambah `angka += 1` yang bikin jadi `angka = 1`

Lalu `if angka % 2 == 0`

Nah apakah 1 habis dibagi 2? TIDAK!

Nah di sini `continue` akhirnya dipake sebagai loncatan

Makanya outputnya

```python
1
3
5
7
9
```

## Loop dengan List dan Dictionary

Nah kita bakal coba gabungin dengan List dan Dictionary kedalah while

### Memindah item dari daftar ke daftar lain

Disini kita bakal mencoba memindah item dari daftar satu ke daftar 2

Contohnya

```python
makanan_belum_dipesan = ['tempe', 'baso', 'mie']
makanan_dipesan = []

while makanan_belum_dipesan:
    makanan_dimakan = makanan_belum_dipesan.pop()

    print(f"Makanan dibuat: {makanan_dimakan}")
    makanan_dipesan.append(makanan_dimakan)

print("\nMakanan yang sudah di hitung: ")
for makanan_habis in makanan_dipesan:
    print(makanan_habis.title())
```

Di sini buat yang bingung akan kujelaskan

Pertama kita bikin list `makanan_belum_dipesan` dengan isi daftar makanan lalu `makanan_dipesan` dengan isi kosong

Nah kita bilang ke while dan bikin variabeel `makanan_dimakan` dan juga narik `makanan_belum_dipesan` pake `pop()`

Lalu kita tambahin pake `append()`

Abis itu bikin for loop untuk isi `makanan_dipesan`

Udah gitu aja simpel

### Menghapus nilai tertentu yang spesfik di dalam list

Nah kita bakal pake lagi function `remove()`

Contoh

```python
makanan = ['baso', 'pangsit', 'baso', 'mie', 'baso', 'ayam', 'kambing']
print(makanan)

while 'baso' in makanan:
    makanan.remove('baso')

print(makanan)
```

Outputnya

```python
['baso', 'pangsit', 'baso', 'mie', 'baso', 'ayam', 'kambing']
['pangsit', 'mie', 'ayam', 'kambing']
```

Nah bisa dilihat kalau kehapus kan

### Memakai User Input kedalam While loop

Nah sekarang kita bakal coba pake input

Contoh

```python
respons = {}

hasil_aktif = True

while hasil_aktif:
    nama = input("\nSiapa namamu?: ")
    respon = input("Sebutkan satu makanan yang sangat ingin kamu makan?: ")

    respons[nama] = respon

    repeat = input("Apakah kamu mau mengajak orang lain untuk makan bersamamu?(iya/tidak): ")
    if repeat == 'tidak':
        hasil_aktif = False

print("\n--- Hasil Jawaban ---")
for nama, respon in respons.items():
    print(f"{nama} ingin makan {respon}.")
```

Outputnya

```python
Siapa namamu?: Maman
Sebutkan satu makanan yang sangat ingin kamu makan?: Mie Ayam
Apakah kamu mau mengajak orang lain untuk makan bersamamu?(iya/tidak): iya

Siapa namamu?: Budi
Sebutkan satu makanan yang sangat ingin kamu makan?: Baso
Apakah kamu mau mengajak orang lain untuk makan bersamamu?(iya/tidak): tidak

--- Hasil Jawaban ---
Maman ingin makan Mie Ayam.
Budi ingin makan Baso.

[Process exited 0]
```

Nah cara kerjanya gimana?

Pertama kan kita bikin dictionary kosong bernama `respons`

Lalu bikin Flag `hasil_aktif` dengan nilai `True`

Terus dalam while kita bikin dua input yaitu nama dan respon

Lalu kita simpan ke Dictionary pake `respons[nama] = respon`

Lalu di repeat dengan `if repeat == 'tidak': hasil_aktif = False` Nah kelihatan kan

Nah terus `hasil_akhir` tinggal nunjukin hasilnya

# Penutup

Baiklah sudah selesai dan makasih udah baca dan maaf jika ada kesalah kata maupun kesalahan kode
