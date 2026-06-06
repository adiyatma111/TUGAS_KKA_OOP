1.Apa yang terjadi jika kamu mengubah hero1.hp menjadi 500 setelah baris hero1 = Hero...? Coba lakukan print(hero1.hp).
hero1.hp = 500akan mengubah nilai attributehpdari objecthero1 output hp layla jadi 500

2.Perhatikan parameter lawan pada method serang. Parameter tersebut menerima sebuah objek utuh, bukan hanya string nama. Mengapa ini penting? Parameter lawan menerima objek utuh agar bisa mengakses attribute (lawan.name, lawan.hp) dan memanggil method (lawan.diserang()) untuk mengurangi HP lawan—jika hanya string nama, kita tidak bisa mengubah data atau memanggil method lawan sehingga pertarungan tidak berfungsi.

3.Eksperimen Fungsi super(): Pada class Mage, coba hapus (atau jadikan komentar #) baris kode super().init(name, hp, attack_power). Kemudian jalankan programnya.

4.Pertanyaan: Error apa yang muncul saat kamu mencoba melihat info Eudora (eudora.info())? Mengapa error tersebut mengatakan Mage object has no attribute 'name', padahal kita sudah mengirim nama "Eudora" saat pembuatan objek?AttributeError: 'Mage' object has no attribute 'name' Tanpa super().init(), constructor class Hero tidak dipanggil, sehingga attribute name, hp, dan attack_power tidak dibuat—data "Eudora" yang dikirim tidak tersimpan karena proses inisialisasi tidak berjalan.

5.Jelaskan peran fungsi super() dalam menghubungkan data dari class Anak ke class Induk! super() memanggil constructor class induk untuk membuat attribute dasar (name, hp, attack_power) yang dibutuhkan class anak—tanpa super(), attribute dari class induk tidak akan ada di class anak.

6.Apakah nilai HP muncul atau Error? Nilai HP muncul (tidak error). Output: Mencoba akses paksa: 0

7.Apa yang terjadi pada data HP Hero? Jelaskan mengapa keberadaan method Setter sangat penting untuk menjaga integritas data dalam game!HP Hero menjadi -100 (nilai negatif yang tidak valid dalam game).Method Setter penting untuk memvalidasi data sebelum disimpan—tanpa validasi, HP bisa menjadi negatif atau nilai tidak wajar yang menyebabkan bug dalam game (seperti karakter tidak bisa mati atau HP tampil aneh). Dengan Setter yang memiliki validasi if-elif, kita bisa memastikan HP selalu dalam rentang yang valid (contoh: 0-9999), sehingga integritas data game terjaga dan gameplay berjalan normal.
