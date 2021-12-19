# labspy08

# praktikum 8 
# Buat program sederhana dengan mengaplikasikan penggunaan class. Buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan:

# flowchartnya

![flowchartpraktikum8](https://user-images.githubusercontent.com/81457697/146673454-04f1f286-9dce-4b64-ab5b-ae2ee6446d24.jpg)

-input untuk mengimport untuk mendapatkan clear system pada os
```python
from os import system
```

-input untuk membuat class untuk menampung data mahasiswa beserta atributnya
```python
class mahasiswa:   
    nim=""
    nama=""
    tugas=""
    uts=""
    uas=""
    akhir=""
 ```
-input untuk variabel untuk menampung list dari dari object mahasiswa
```python
pilih=0
datasiswa=[]
```
-input untuk menampilkan daftar menu mahasiswa
```python
def menu():
    system("cls")
    print("Menu Aplikasi Data Mahasiswa");
    print("-"*43)
    print("1. Input Data Mahasiswa")
    print("2. Tampilkan Data Mahasiswa")
    print("3. Update Data Mahasiswa")
    print("4. Hapus Data Mahasiswa")
    print("5. Keluar Aplikasi")
    pilih= int(input("Masukan Pilihan Anda : "))
    if pilih == 1:
        pilih1()
        menu()
    elif pilih == 2:
        tampil()
        input("Kembali Menu Utama")
        menu()
    elif pilih == 3:
        index_update=-1
        tampil()
        id_edit = int(input("Input NIM yang akan diupdate "))
        for a in range(0, len(datasiswa)):
            if id_edit==datasiswa[a].nim:
                index_update=a
                break
        if (index_update > -1):
            print("INPUT DATA YANG DI UPDATE")
            siswa=mahasiswa()
            siswa.nim=(int(input("Msdukan NIM                      : ")))
            siswa.nama=(input("Masukan Nama Mahasiswa          : "))
            siswa.tugas=(float(input("Masukan Nilai Tugas              : ")))
            siswa.uts=(float(input("Masukan Nilai Uts              : ")))
            siswa.uas=(float(input("Masukan Nilai Uas              : ")))
            siswa.akhir=siswa.tugas*0.30+siswa.uts*0.35+siswa.uas*0.35
            datasiswa=[index_update]=siswa
            print("Berhasil Update Data Mahasiswa")
        else : print("NIM Tidak Ditemukan")
        input("Kembali Menu Utama")
        menu()
    elif pilih ==4:
        system("cls")
        tampil()
        index_update=-1
        id_hapus = int(input("Input NIM Yang Akan Dihapus"))
        for a in range (0, len(data)):
            if id_hapus==datasiswa[a].nim:
                index_delete = a
                break
        if(index_delete > -1):
            del datasiswa[index_delete]
            print("Data Telah Dihapus")
        else: 
            print("NIM Tidak Ditemukan")
            input("Kembali Menu Utama")
            menu()
            menu()
    elif pilih ==5 :
        exit()
```
-input untuk menambahkan data mahasiswa
```python
def pilih1():
    ulang = "Y"
    while ulang in("y","Y"):
        system("cls")
        siswabaru=mahasiswa()
        print("INPUT DATA MAHASISWA")
        siswabaru.nim=(int(input("Masukan NIM            : ")))
        siswabaru.nama=(input("Masukan Nama Mahasiswa : "))
        siswabaru.tugas=(float(input("Masukan Nilai Tugas    : ")))
        siswabaru.uts=(float(input("Masukan Nilai UTS      : ")))
        siswabaru.uas=(float(input("Masukan Nilai UAS      : ")))
        siswabaru.akhir=siswabaru.tugas*0.30 + siswabaru.uts*0.35 + siswabaru.uas*0.35
        datasiswa.append(siswabaru)
        ulang=input("Apakah Anda Ingin Mengulang (Y/T)? ")
menu()
```
-input untuk menampilkan data yang sudah tersimpan ,cara mengaksesnya dengan memilih angka yang sudah disedikan di daftar menu
```python
def tampil():
    system("cls")
    print("DATA MAHASISWA")
    for data in datasiswa:
        print("Nim          : "+str(data.nim)) 
        print("Nama         : "+data.nama)
        print("Nilai Tugas  : "+str(data.tugas))
        print("Nilai UTS    : "+str(data.uts))
        print("Nilai UAS    : "+str(data.uas))
        print("Nilai Akhir  : "+str(data.akhir))
        print("-"*18)
```
-input untuk menghapus data mahasiswa yang sudah dimasukan kedalam menu
```python
elif pilih ==4:
        system("cls")
        tampil()
        index_update=-1
        id_hapus = int(input("Input NIM Yang Akan Dihapus"))
        for a in range (0, len(data)):
            if id_hapus==datasiswa[a].nim:
                index_delete = a
                break
        if(index_delete > -1):
            del datasiswa[index_delete]
            print("Data Telah Dihapus")
        else: 
            print("NIM Tidak Ditemukan")
            input("Kembali Menu Utama")
            menu()
            menu()
```
-input untuk keluar dari program
```python
  elif pilih ==5 :
        exit()
```
berikut output dari daftar menu mahasiswa
# output ketika program baru di run

![output1](https://user-images.githubusercontent.com/81457697/146674042-5f4fe184-fe74-4e4e-9de1-250056bbbf0a.png)

# output ketika kita sudah memasukan data mahasiswa

![output2](https://user-images.githubusercontent.com/81457697/146674159-895b2cff-d321-40c1-ac12-dda2fb2946f2.png)

# output untuk menampilkan data mahasiswa siapa saja yang sudah masuk

![output3](https://user-images.githubusercontent.com/81457697/146674169-ada2acd1-6c11-4f64-809d-388d31b68702.png)

# output untuk kembali ke  menu utama dan keluar aplikasi

![output4](https://user-images.githubusercontent.com/81457697/146674219-7cd6a5cd-0314-4689-b0db-2a279695e4a1.png)
