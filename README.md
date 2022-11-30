# Tugas Praktikum {Pertemuan ke 11} ![gambar](https://camo.githubusercontent.com/1cf226ebd63b65195652984b96e56db54bfaa9a41690b6da6c138a40e4137393/68747470733a2f2f75706c6f61642e77696b696d656469612e6f72672f77696b6970656469612f636f6d6d6f6e732f302f30612f507974686f6e2e737667) 

|**Nama**|**NIM**|**Kelas**|**Matkul**|
|----|---|-----|------|
|Muhammad Ikhsan Fakhrudin|312210019|TI.22.A2|Pemrograman|

# Latihan 1

![gambar 9](screenshot/ss9.png)

# Kode Program

![gambar1](screenshot/ss1.png)

# Output

Maka hasil nya akan seperti ini :

![gambar 2](screenshot/ss2.png)

# Tugas Praktikum

![gambar 10](screenshot/ss10.png)

# Kode Program

![gambar 3](screenshot/ss3.png)

![gambar 4](screenshot/ss4.png)

# Penjelasan

`Membuat dictionary` yang akan diinput dengan data.

```
data = {}
```

`Membuat perulangan` dan keterangan untuk pilihan menu.

```
while True:
    header="PROGRAM INPUT NILAI MAHASISWA"
    header2=("MENU UTAMA")
    print(header.center(97,"="))
    print()
    print(header2.center(97,"_"))
    c = input("\n(L)ihat, (T)ambah, (U)bah), (H)apus, (C)ari, (K)eluar: ")
```

`Menambahkan data` yang akan diinput kemudian masuk ke dalam dictionary.

```
if c.lower() == 't':
        print("Tambah Data")
        nama = input("Nama\t\t: ")
        nim = int(input("NIM\t\t: "))
        uts = int(input("Nilai UTS\t: "))
        uas = int(input("Nilai UAS\t: "))
        tugas = int(input("Nilai Tugas\t: "))
        akhir = tugas*30/100 + uts*35/100 + uas*35/100
        data[nama] = nim, uts, uas, tugas, akhir
```

**Output Menambahkan data.**

![gambar 5](screenshot/ss5.png)

Jika ingin `Menampilkan/Melihat data` , dapat menggunakan :

```
elif c.lower() == 'l':
        if data.items():
            print("="*88)
            print("|                               Daftar Mahasiswa                             |")
            print("="*88)
            print("|No. | Nama                      |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*88)
            i = 0
            for z in data.items():
                i += 1
                print("| {no:2d} | {0:15s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                      .format(z[0][:25], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
            print("=" *88)
        else:
            print("="*78)
            print("|                               Daftar Mahasiswa                             |")
            print("="*78)
            print("|No. | Nama            |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*78)
            print("|                                TIDAK ADA DATA                              |")
            print("="*78)
```

**Output Tampilan data yg sudah berhasil di input.**

![gambar 6](screenshot/ss6.png)

Jika ingin `Mengubah data` dapat menggunakan :

```
elif c.lower() == 'u':
        print("Ubah Data")
        nama = input("Masukkan Nama   : ")
        if nama in data.keys():
            nim = int(input("NIM\t\t: "))
            uts = int(input("Nilai UTS\t: "))
            uas = int(input("Nilai UAS\t: "))
            tugas = int(input("Nilai Tugas\t: "))
            akhir = tugas*30/100 + uts*35/100 + uas*35/100
            data[nama] = nim, uts, uas, tugas, akhir
        
        else:
            print("Nama {0} tidak ditemukan".format(nama))
```

**Output Mengubah data.**

![gambar 7](screenshot/ss7.png)


Jika ingin `Mencari data` dapat menggunakan :

```
elif c.lower() == 'c':
        print("Cari Data")
        nama = input("Masukkan Nama : ")
        if nama in data.keys():
            print("="*88)
            print("|                             Daftar Mahasiswa                          |")
            print("="*88)
            print("| Nama                      |       NIM       |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*88)
            print("| {0:20s} | {1:15d} | {2:5d} | {3:5d} | {4:7d} | {5:7.2f} |"
                  .format(nama, nim, uts, uas, tugas, akhir))
            print("="*88)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
```

**Output data yg ingin di cari.**

![gambar 11](screenshot/ss11.png)


Jika ingin `Menghapus data` dapat menggunakan :

```
elif c.lower() == 'h':
        print("Hapus Data")
        nama = input("Masukkan Nama  : ")
        if nama in data.keys():
            del data[nama]
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
```

**Output data yg telah di hapus.**

![gambar 8](screenshot/ss8.png)


**Sekian Tugas Praktikum di Pertemuan kali ini.**

**Jika Ada yg Salah Sama Minta Maaf.**

**Wassalamualaikum wr.wb.**


