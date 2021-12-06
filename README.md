# latihan2
Dictionary adalah tipe data pada python yang berfungsi untuk menyimpan kumpulan data/nilai dengan pendekatan key-value. Setiap key dipisahkan dari value-nya oleh titik dua (:), sedangkan item dipisahkan oleh koma, dan semuanya tertutup dalam kurung kurawal {}.
Dictionary sendiri memiliki dua buah komponen inti:

1.Key merupakan nama atribut suatu item pada dictionary.

2.Value adalah nilai yang disimpan pada suatu atribut.
# Program
![image](https://user-images.githubusercontent.com/92682351/144775441-31e67a7f-c71b-42ca-881c-ad51803dc281.png)
![image](https://user-images.githubusercontent.com/92682351/144775469-c8e32239-3841-43cc-bb49-5b9dd8d7e471.png)
1.Membuat dictionary daftar kontak. python s={'Ari': '0895767999', 'Dina': '081288886'}

2.Untuk menampilkan salah satu kontak, gunakan s['Ari']. s adalah variable dictionary, sedangkan ['Ari'] adalah keys dari sebuah dictionary. python print("Menampilkan kontak Ari :", s['Ari'])

3.Jika ingin menambahkan kontak baru gunakan variable_dictionary['keys']=value;. python s['Riko']='081354587';

4.Untuk mengubah kontak yang lama dengan yang baru, gunakan variable_dictionary['keys']=value;. Disini saya akan mengubah valuenya yang semula 'Dina': '081288886' menjadi 'Dina': '088960779'. python s['Dina']='088960779';

5.Untuk menampilkan semua nama kontak, gunakan keys(). python print(s.keys())

6.Jika ingin menampilkan semua nomor kontak, gunakan values(). pyhton print(s.values())

7.Untuk menampilkan daftar kontak beserta nomor teleponnya, gunakan items(). pyhton print(s.items())

8.Untuk menghapus salah satu kontak, gunakan statement del variable_dictionary[keys];. python del s['Dina'];

# Output
![image](https://user-images.githubusercontent.com/92682351/144775755-0cbe1c04-9fb3-4ed4-a622-1cab2e4f50d3.png)


# Tugas praktikum
# program
![image](https://user-images.githubusercontent.com/92682351/144775908-72bfb77d-0829-495d-b4b1-f4caee82d612.png)

![image](https://user-images.githubusercontent.com/92682351/144775934-68b0023d-df6c-4bb3-a57d-18b52c13b8e2.png)

![image](https://user-images.githubusercontent.com/92682351/144775974-20984e1b-9c78-49de-bf33-b4c77b13022c.png)

![image](https://user-images.githubusercontent.com/92682351/144775988-b3713dc1-ca27-4556-9714-071470ba1a47.png)

# penjelasan
1.Membuat dictionary kosong yang nantinya akan diinput dengan data.
data={}

2.Membuat perulangan dengan while dan terdapat pilihan menu untuk menjalankan program.

while True:
print()
a=input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar] :")
print()
Menambahkan data nim, nama, nilai tugas, uts, dan uas. Data yang diinputkan akan masuk ke dalam dictionary data dengan nim sebagai keys sedangkan nama, tugas, uts dan uas sebagai values.

if a=="t" or a=="T":
    print("TAMBAH DATA")
    print("-----------")
    nim=int(input("NIM\t: "))
    nama=input("Nama\t: ")
    tugas=int(input("Tugas\t: ")) 
    uts=int(input("UTS\t: "))
    uas=int(input("UAS\t: "))
    akhir=(int(tugas)*30/100)+(int(uts)*35/100)+(int(uas)*35/100)
    data[nim]=nama, tugas, uts, uas, akhir
    
3.Menampilkan atau melihat data. Jika sebelumnya belum menginput data, maka tampilannya akan "Tidak ada data". Apabila sudah menginput data, maka data yang telah diinput tadi akan ditampilkan.

elif a=="l" or a=="L":
    if data.items():
        print("DAFTAR NILAI")
        print("------------")
        print(72*"=")
        print("| {0:^10} | {1:^10} | {2:^6} | {3:^6} | {4:^6} |   {5:^12}  |".format("NIM", "NAMA", "TUGAS", "UTS", "UAS", "NILAI AKHIR"))
        print(72*"=")
        for item in data.items(): 
            print("| {0:>10} | {1:>10} | {2:>6} | {3:>6} | {4:>6} |   {5:>12}  |".format(nim, nama, tugas, uts, uas, akhir))
            print(72*"=")
        print()
    else:
        print("DAFTAR NILAI")
        print("------------")
        print(72*"=")
        print("| {0:^10} | {1:^10} | {2:^6} | {3:^6} | {4:^6} |   {5:^12}  |".format("NIM", "NAMA", "TUGAS", "UTS", "UAS", "NILAI AKHIR"))
        print(72*"=")
        print("|                             TIDAK ADA DATA                           |")
        print(72*"=")
        print()
        
4.Apabila ingin mengubah data, maka anda akan diminta untuk menginputkan nim terlebih dahulu. Setelah itu input data yang ingin diubah.

 elif a=="u" or a=="U":
    print("UBAH DATA")
    print("---------")
    b=input("Masukkan NIM anda: ")
    print()
    if data.keys():
        tugas=int(input("Tugas\t: ")) 
        uts=int(input("UTS\t: "))
        uas=int(input("UAS\t: "))
        akhir=(int(tugas)*30/100)+(int(uts)*35/100)+(int(uas)*35/100)
        
5.Jika ingin menghapus data, anda akan diminta untuk menginput nim. Lalu data yang telah diinput diawal tadi akan dihapus beserta valuesnya (nama, nilai tugas, nilai uts dan nilai uas).

elif a=="h" or a=="H":
    print("HAPUS DATA")
    print("----------")
    b=input("Masukkan NIM anda: ")
    print()
    if data.keys():
        del data[nim]
6.Apabila ingin mencari data, anda akan diminta untuk menginput nim kemudian data yang anda cari akan muncul berdasarkan nim yang diinput tadi.

elif a=="c" or a=="C":
    print("CARI DATA")
    print("---------")
    b=input("Masukkan NIM anda: ")
    print()
    if data.keys():
        print(72*"=")
        print("| {0:^10} | {1:^10} | {2:^6} | {3:^6} | {4:^6} |   {5:^12}  |".format("NIM", "NAMA", "TUGAS", "UTS", "UAS", "NILAI AKHIR"))
        print(72*"=")
        print("| {0:>10} | {1:>10} | {2:>6} | {3:>6} | {4:>6} |   {5:>12}  |".format(nim, nama, tugas, uts, uas, akhir))
        print(72*"=")
        print()
        
7.Jika data sudah selesai diinput, pilih menu 'k'/'K' maka program akan terhenti.

elif a=="k" or a=="K":
     break
     
     sekian kurang lebihnya mohon maaf, wassalamualaikum warohmatullahiwabarokatuh
