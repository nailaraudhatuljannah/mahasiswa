RINGKASAN MATERI PYTHON OOP (OBJECT-ORIENTED PROGRAMMING)
1. Pengertian Python OOP
OOP (Object-Oriented Programming) adalah konsep pemrograman yang berorientasi pada objek. OOP digunakan untuk menyusun program dengan menggabungkan data dan fungsi ke dalam suatu objek.

Python mendukung konsep OOP sehingga program lebih terstruktur, mudah dikembangkan, dan dapat digunakan kembali.

Contoh penerapan OOP:
- Sistem data mahasiswa.
- Sistem pembayaran.
- Sistem perpustakaan.
- Sistem penjualan.
2. Konsep Dasar OOP
Ada beberapa istilah penting dalam OOP yang harus dipahami.
A. Class
Class adalah cetakan atau blueprint untuk membuat objek. Class berisi atribut dan method.

Contoh:
class Mahasiswa:    nama = "Rizka"    jurusan = "Agroteknologi"


B. Object
Object adalah hasil atau bentuk nyata dari sebuah class.

Contoh:
class Mahasiswa:    passmhs1 = Mahasiswa()mhs2 = Mahasiswa()


Keterangan:
- Mahasiswa = Class.
- mhs1 dan mhs2 = Object.
C. Attribute
Attribute adalah variabel yang terdapat di dalam class atau objek untuk menyimpan data.

Contoh:
class Mahasiswa:    def __init__(self, nama, nim):        self.nama = nama        self.nim = nim


D. Method
Method adalah fungsi yang berada di dalam class dan digunakan untuk menjalankan suatu tindakan.

Contoh:
class Mahasiswa:    def belajar(self):        print("Mahasiswa sedang belajar")


3. Constructor (init)
Constructor adalah method khusus yang otomatis dijalankan ketika objek dibuat.

Contoh:
class Mahasiswa:    def __init__(self, nama, umur):        self.nama = nama        self.umur = umurmhs1 = Mahasiswa("Rizka", 20)print(mhs1.nama)print(mhs1.umur)


Output:
Rizka
20

Fungsi self: Digunakan untuk mengakses atribut dan method milik objek itu sendiri.
4. Empat Pilar Utama OOP
Ini bagian yang paling penting untuk dipahami karena sering muncul dalam ujian.
A. Encapsulation (Enkapsulasi)
Encapsulation adalah konsep membungkus data dan method dalam satu class serta mengatur akses terhadap data tersebut.

Contoh:
class Bank:    def __init__(self):        self.__saldo = 100000    def lihat_saldo(self):        return self.__saldobank = Bank()print(bank.lihat_saldo())


Keterangan:
- __saldo merupakan atribut private.
- lihat_saldo() digunakan untuk mengakses saldo.
B. Inheritance (Pewarisan)
Inheritance adalah konsep pewarisan atribut dan method dari class induk (parent) ke class anak (child).

Contoh:
class Hewan:    def makan(self):        print("Hewan sedang makan")class Kucing(Hewan):    passkucing = Kucing()kucing.makan()


Output:
Hewan sedang makan

Kucing dapat menggunakan method dari class Hewan.
C. Polymorphism (Polimorfisme)
Polymorphism adalah kemampuan beberapa objek untuk menggunakan method dengan nama yang sama tetapi memiliki perilaku berbeda.

Contoh:
class Kucing:    def suara(self):        print("Meong")class Anjing:    def suara(self):        print("Guk guk")k1 = Kucing()a1 = Anjing()k1.suara()a1.suara()


Output:
Meong
Guk guk

D. Abstraction (Abstraksi)
Abstraction adalah konsep menyembunyikan proses atau detail yang rumit dan hanya menampilkan fungsi penting kepada pengguna.

Contoh:
from abc import ABC, abstractmethodclass Kendaraan(ABC):    @abstractmethod    def berjalan(self):        passclass Mobil(Kendaraan):    def berjalan(self):        print("Mobil berjalan")mobil = Mobil()mobil.berjalan()


Output:
Mobil berjalan

5. Perbedaan Class, Object, Attribute, dan Method
Istilah	Pengertian
Class	Cetakan objek
Object	Hasil dari class
Attribute	Data atau karakteristik objek
Method	Fungsi atau tindakan objek
Constructor	Method untuk inisialisasi objek
Self	Referensi ke objek itu sendiri


6. Access Modifier
Access modifier digunakan untuk mengatur tingkat akses atribut dan method.
Jenis	Penulisan	Keterangan
Public	nama	Dapat diakses secara umum
Protected	_nama	Ditujukan untuk penggunaan internal dan pewarisan
Private	__nama	Menggunakan name mangling untuk membatasi akses langsung


7. Contoh Program Python OOP Sederhana
Contoh penerapan OOP dalam sistem data mahasiswa.
class Mahasiswa:    def __init__(self, nama, jurusan, nilai):        self.nama = nama        self.jurusan = jurusan        self.nilai = nilai    def tampilkan_data(self):        print("Nama:", self.nama)        print("Jurusan:", self.jurusan)        print("Nilai:", self.nilai)    def cek_kelulusan(self):        if self.nilai >= 70:            print("Status: Lulus")        else:            print("Status: Tidak Lulus")mhs1 = Mahasiswa("Rizka", "Agroteknologi", 85)mhs1.tampilkan_data()mhs1.cek_kelulusan()


Output:
Nama: Rizka
Jurusan: Agroteknologi
Nilai: 85
Status: Lulus

8. Kelebihan dan Kekurangan OOP
Kelebihan:
1. Program lebih terstruktur.
2. Kode dapat digunakan kembali.
3. Mudah diperbaiki dan dikembangkan.
4. Memudahkan pengelolaan program besar.
5. Keamanan data dapat diatur melalui encapsulation.
Kekurangan:
1. Membutuhkan pemahaman konsep lebih dalam.
2. Struktur program bisa lebih kompleks.
3. Kurang efisien untuk program yang sangat sederhana jika dibandingkan pendekatan prosedural.
9. Poin Penting untuk Menghadapi Ujian
Hafalan cepat OOP
Konsep	Kata kunci
Class	Cetakan
Object	Hasil cetakan
Attribute	Data
Method	Fungsi
__init__	Constructor
self	Objek itu sendiri
Encapsulation	Membungkus data
Inheritance	Pewarisan
Polymorphism	Banyak bentuk
Abstraction	Menyembunyikan detail
