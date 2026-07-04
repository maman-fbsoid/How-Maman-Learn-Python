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

# TO BE CONTINUED
