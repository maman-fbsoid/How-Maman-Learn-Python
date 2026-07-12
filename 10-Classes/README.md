# APA itu Class?

Jadi kita anggap saja bahwa Class adalah blueprint untuk membuat objek

Lebih tepatnya, Class menggabungkan data dan function di satu tempat

### Membuat Class

Baiklah kita langsung masuk ke materi dengan kita membuat kode simpel

```python
class Anjing():
    def __init__(self, nama, umur):
        self.nama = nama
        self.umur = umur

    def duduk(self):
        print(f"{self.nama.title()} sekarang sedang duduk")

    def makan(self):
        print(f"{self.nama.title()} sedang makan")

my_dog = Anjing('Cookie', '6')

print(f"Nama anjingku adalah {my_dog.nama.title()}")
print(f"Umur anjingku adalah {my_dog.umur} tahun")
```

Outputnya

```python
Nama anjingku adalah Cookie
Umur anjingku adalah 6 tahun
```

Nah bisa dilihat bahwa Class dapat menyimpan banyak `def` sekaligus di dalamnya

### APA itu `__init__()`

`__init__()` atau dibaca dunder init adalah function spesial yang otomatis dipanggil ketika sebuah objek dibuat

Kenapa kita harus pake `__init__()`?

Supaya objek punya data awal

### Calling Method

Nah sekarang coba kita panggil function lain

```python
class Anjing():
    def __init__(self, nama, umur):
        self.nama = nama
        self.umur = umur

    def duduk(self):
        print(f"{self.nama.title()} sekarang sedang duduk")

    def makan(self):
        print(f"{self.nama.title()} sedang makan")

my_dog = Anjing('Cookie', '6')

print(f"Nama anjingku adalah {my_dog.nama.title()}")
print(f"Umur anjingku adalah {my_dog.umur} tahun")
my_dog.duduk()
my_dog.makan()
```

Jadi kalian cuman tinggal nambahin `my_dog.duduk()` dan `my_dog.makan()`

Sekarang coba kita variasikan class ini agar lebih bagus

```python
class Anjing():
    def __init__(self, nama, umur):
        self.nama = nama
        self.umur = umur

    def duduk(self):
        print(f"{self.nama.title()} sekarang sedang duduk")

    def makan(self):
        print(f"{self.nama.title()} sedang makan")

my_dog = Anjing('Cookie', '6')
your_dog = Anjing('Sandvich', '2')

print(f"Nama anjingku adalah {my_dog.nama.title()}")
print(f"Umur anjingku adalah {my_dog.umur} tahun")
my_dog.duduk()
my_dog.makan()

print(f"\nNama anjingmu adalah {your_dog.nama.title()}")
print(f"Umur anjingmu {your_dog.umur}")
your_dog.duduk()
your_dog.makan()
```

Nah disini kita nambahin `your_dog` sebagai tambahan
