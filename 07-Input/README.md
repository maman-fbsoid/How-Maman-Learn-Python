# APA itu Input

Sekarang kita masuk ke materi baru yaitu Input

Sejauh ini kita hanya belajar mengenai Output. Nah kita sekarang akanbelajar Input

Memang agak telat ku ajarin tapiya sudahlah

Bedanya apa?

Jadi gini le

Kalo Output itu menampilkan/mengeluarkan sesuatu 

Kalo Input memasukan sesuatu

Bisa kan faham?

## Menggunakan `input()`

Ya, cara kita menggunakan input itu kita bakal paket function `input()`

Contoh

```python
message = input("Sebutkan namamu: ")
print(message)
```

Nah nanti bakal muncul

```python
Sebutkan namamu:
```

Kalian masukin sesuatu

Contoh aku masukin

```python
Sebutkan namamu: Maman
```

Nanti bakal

```python
Sebutkan namamu: Maman
Maman
```

Nah gitu

### Clear Prompt

Nah sekarang kita coba rapikan dikit inputnya biar kelihatan bagus

```python
prompt = "Halo, senang bertemu denganmu"
prompt += "\nAh, siapa nama anda tuan?: "

nama = input(prompt)
print(f"\nHalo {nama}")
```

Gimana nanti yang muncul?

```python
Halo, senang bertemu denganmu
Ah, siapa nama anda tuan?:
```

Ya kalian tinggal masukan nama dan dia bakal munculin hasilnya

Nah kita kenalan dulu sama operator baru. Aku lupa mau jelasin ini jadi yasudah sekarang aja

`+=` Ini gunanya apa sih?

Simpelnya

Kegunaan utama `+=` adalah untuk menyingkat kode saat kamu ingin menambah nilai suatu variabel dengan nilai lain, lalu menyimpan hasilnya kembali ke variabel itu sendiri

### Memakai `int()`

Nah gunaya `int()` buat apa sih?

Sama aja kayak `input()` tapi ini khsus buat angka

Jadi kayak dibuat khusus aja buat angka

Contoh

```python
gorengan = input("Berapa gorengan yang kau makan? ")
gorengan = int(gorengan)

if gorengan >= 5:
  print("\nBayar 5000")
else:
  print("Gratis aja")
```

Nah bisa di lihat kan input itu simpel (cuman gw aja yang telat jelasin harusnya dari awal)

Nah sekarang kita bakal lanjut

Sekarang sedikit rumit tapi masih easy lahh

```python
angka = input("Sebutkan sebuah angka maka aku akan beritahu angka itu genap atau ganjil: ")
angka = int(angka)

if angka % 2 == 0:
  print("\nAngka {angka} adalah Genap!")
else;
  print("\nAngka {angka} adalah Ganjil!")
```

Gimana kok bisa bekerja?

Karena `if` di situ pake `%` jadi kayak kita bilang ke python "Angkanya nanti dibagi 2 kalo bisa berarti genap kalo enggak berarti ganjil"

# Penutup

Baiklah materi input sampe sini saja karena memang sedikit dan kalian harusnya faham jadi makasih dan ADIOS!
