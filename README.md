## TUGAS UAS PEMROGRAMAN
NAMA: RAHMANTA NOVRIZON

NIM:  312210213

KELAS:TI.22.A.2

LINK YOUTUBE:

_______________________________________________________________________________________________________________________________________________________________________
- Pertama buat folder yang berisikan daftar nilai, input nilai, view nilai
![Screenshot (121)](https://user-images.githubusercontent.com/115687740/211341011-9f54f7df-a17a-4eac-adfa-9bf597f81ed1.png)

- setelah bikin terlebih dahulu dictionary
```
data = {}
```

- lalu setelah itu buat class data menggunakan program```def```
```
class Data():
    def _init_(self,nama,nim,uts,uas,tugas,total):
        print("Tambah Data")

```

- buat definisi tambah untuk menambahkan data mengunakan magic word```self```
```
def tambah(self):
        self.nama = input("Nama           : ")
        self.nim = int(input("NIM            : "))
        self.uts = int(input("Nilai UTS      : "))
        self.uas = int(input("Nilai UAS      : "))
        self.tugas = int(input("Nilai Tugas    : "))
        self.total = self.uts*35/100 + self.uas*35/100 + self.tugas*30/100
        data[self.nama] = self.nim, self.uts, self.uas, self.tugas, self.total
        
```

![Screenshot (106)](https://user-images.githubusercontent.com/115687740/211334937-66af9007-b3b6-42cc-b294-9213628a0755.png)

- setelah itu buat class turunan dengan variable Mahasiswa

```
class Mahasiswa(Data):

```
- masukan def tambah untuh menambahkan daftar mahasiswa

```
def tampilkan(self):
        print("Tampilkan Data")
        if data.items():
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            i = 0
            for z in data.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                    .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
            print("=" * 78)
        else:
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            print("|                                TIDAK ADA DATA                              |")
            print("="*78)
        return
        
```

![Screenshot (104)](https://user-images.githubusercontent.com/115687740/211337431-b720dec6-6603-48cd-a31c-1dc728542963.png)

- setalah itu masukkan def hapus untuk menghapus data yang sudah ada dengan memasukan nama yang ingin di hapus
```
def hapus(self):
        print("Hapus Data")
        self.nama = input("Masukkan Nama  : ")
        if self.nama in data.keys():
            del data[self.nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(self.nama))
        return
```
![Screenshot (101)](https://user-images.githubusercontent.com/115687740/211339217-a9987c7d-a7fa-4a92-8068-80be68a5ea74.png)

- masukkan def ubah untuk mengubah data yang sudah di buat
```
def ubah(self):
        print("Ubah Data")
        self.nama = input("Masukkan Nama  : ")
        if self.nama in data.keys():
            self.nim = int(input("NIM            : "))
            self.uts = int(input("Nilai UTS      : "))
            self.uas = int(input("Nilai UAS      : "))
            self.tugas = int(input("Nilai Tugas    : "))
            self.total = self.uts*35/100 + self.uas*35/100 + self.tugas*30/100
            data[self.nama] = self.nim, self.uts, self.uas, self.tugas, self.total
        else:
            print("Nama {0} tidak ditemukan".format(self.nama))
        return
```
![Screenshot (103)](https://user-images.githubusercontent.com/115687740/211338972-8b89af32-4158-4706-a4cb-358f4af16b25.png)

- masukan varieabel untuk memanggil perintah input nama,nim,uts,uas,dan nilai tugas secara otomatis tanpa harus memanggil dengan menambahkan variable lagi
![Screenshot (110)](https://user-images.githubusercontent.com/115687740/211339778-29de95d2-77ab-45be-8f3d-4e62f7ead29d.png)





