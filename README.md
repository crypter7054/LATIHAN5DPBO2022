# LATIHAN5DPBO2022
## Identitas
- Nama : Yosafat
- NIM  : 2009929
- Prodi : Ilmu Komputer C2

## Janji
Saya Yosafat (2009929) mengerjakan evaluasi Latihan 5 dalam mata kuliah Desain dan Pemrograman Berorientasi Objek untuk keberkahanNya maka saya tidak melakukan kecurangan seperti yang telah dispesifikasikan. Aamiin.

## Soal
Pada bagian ini, kita akan menggunakan program GUI DataMahasiswa yang bisa kalian download disini. Pada program ini, kalian bisa lihat beberapa fitur masih belum berjalan dengan baik dan beberapa style juga belum terlihat baik. Disini kalian perlu memperbaiki masalah tersebut berdasarkan poin yang dijabarkan di bawah ini:
a. Mengganti font dan ukuran teks
b. Mengubah nama variabel setiap komponen (misal komponen input NIM diberi nama variabel txtNim)
c. Menambahkan validasi ketika inputan tidak lengkap, seperti memunculkan pesan error menggunakan class JOptionPane
d. Menghapus data pada label inputan ketika sudah selesai add, update, delete, maupun ketika menekan tombol cancel
e. Mengupdate tabel setiap kali ada perubahan pada data hasil add, update dan delete

Bonus:
Menambahkan atribut inputan baru selain yang sudah ada pada form, namun tetap berkaitan dengan data mahasiswa. Pastikan penambahan ini ditampilkan juga di tabel


### Screenshot
#### Poin-a
![poin-a](https://user-images.githubusercontent.com/77567907/159034385-44b02559-fd0d-4b8a-a07d-57eb091656e2.jpg)

Untuk mengganti font dan ukuran teks dapat dilakukan dengan membuka menu properties dari Label, Button, Textfield, dan Swing Control lainnya.


#### Poin-b
![poin-b](https://user-images.githubusercontent.com/77567907/159034394-9450e727-47d3-4602-a3a1-6b0434b9a9e8.jpg)

Mengubah nama variabel setiap komponen dapat dilakukan dengan membuka menu properties, pada sub bagian code dengan nama Variable name.


#### Poin-c
![poin-c](https://user-images.githubusercontent.com/77567907/159034396-a74352e4-77a8-49de-9ca5-2824f77d442a.jpg)

Untuk menambahkan validasi ketika inputan tidak lengkap dapat dilakukan dengan menambahkan kondisi pada prosedur insertData yaitu jika nim, nama, dan nilai kosong maka akan menampilkan dialog message, untuk mengecek apakah nim, nama, dan nilai kosong dapat dilakukan dengan menggunakan fungsi isBlank. Jika memenuhi kondisi isBlank maka panggil JOptionPane fungsi showMessageDialog kemudian tambahkan pesan validasi pada fungsi tersebut. Sedangkan untuk kondisi jika inputan nim, nama, dan nilai terisi maka dapat langsung membuat objek list kemudian menampilkan data.


#### Poin-d
![poin-d](https://user-images.githubusercontent.com/77567907/159034400-127db5f4-e757-48a6-824a-6d5b97ba22ba.jpg)

Untuk menghapus data pada label inputan ketika sudah selesai add, update, delete, dan menekan cancel dapat dilakukan dengan menambahkan value dari syntax setText menjadi null, misal inputNama.setText(null) <- ini untuk menghapus data pada label nama. deklarasi syntax tersebut dilakukan pada setiap prosedur yang akan digunakan yaitu insertData(), updateData(), deleteData(), dan CancelButtonActionPerfomed().


#### Poin-e
![poin-e](https://user-images.githubusercontent.com/77567907/159034375-b048160d-29e3-4979-966c-8106970b8077.jpg)

Untuk mengupdate tabel setiap kali ada perubahan data hasil add, update dan delete dapat dilakukan dengan memanggil fungsi setModel pada Tabel yang kemudian value dari fungsi setModel tersebut diisi dengan fungsi setTable (dimana fungsi setTable ini digunakan untuk mengisi dan menampilkan data tabel). Contoh deklarasinya -> Table.setModel(setTable()). Fungsi ini dipanggil pada masing-masing prosedur antara lain, insertData, updateData, dan deleteData. Kondisi khusus untuk perintah delete terdapat sedikit perbedaan yaitu sebelum memanggil fungsi setModel maka harus terlebih dahulu memodifikasi objek listMhs. Modifikasi list ini dilakukan agar data pada listMhs berubah ketika ditampilkan. Modifikasi pada listMhs dapat dilakukan dengan menggunakan fungsi remove misal : listMhs.remove(). Kemudian untuk mengisi parameter dari fungsi remove, terlebih dahulu harus membuat selector yang digunakan untuk memilih row yang akan dihapus. Perintah tersebut dapat dilakukan dengan menggunakan getSelectedRow() yang akan ditampung pada varibel temp. Dengan demikian, parameter dari fungsi remove dapat diisi dengan variabel temp sehingga menjadi listMhs.remove(temp).
