# 1. Membuat repository

<img width="1122" alt="Screenshot 2024-02-18 at 00 14 13" src="https://github.com/SchoolBoyJoJo/ajk-jojo-penugasan1/assets/142652941/cd314fe7-f33d-4d56-906b-9e09d61fd134">

Pertama kita akan membuat folder pada local mechine kita, sebaiknya nama folder disesuaikan dengan nama repo yang akan kita buat. Selanjutnya kita akan membuat repo tanpa membuat readme.md (jadi repo nya benar-benar kosong) lalu kita menghubungkan repo yang ada pada GitHub dengan command yang ada pada screenshot diatas

# 2. Membuat branch

Kita akan membuat branch, dimana branch default kita saat ini ialah master dan kita akan membuat branch development. Dari branch development kita akan membuat branch featureA dan featureB

<img width="1115" alt="Screenshot 2024-02-18 at 00 24 02" src="https://github.com/SchoolBoyJoJo/ajk-jojo-penugasan1/assets/142652941/438e4b02-56f8-4e9f-95e0-eb70f8b2f093">

Seperti yang dapat kita lihat di screenshot diatas kita menggunakan perintah 'git branch <nama_branch>' untuk membuat branch baru

# 3. Implementasi berbagai command git

<img width="1118" alt="Screenshot 2024-02-18 at 12 37 47" src="https://github.com/SchoolBoyJoJo/ajk-jojo-penugasan1/assets/142652941/84d0d57b-3fe9-43ed-ab69-ef1cd48a3cde">

Pada screenshot diatas ialah implementasi dari 'git push' git push sendiri bermanfaat untuk melakukan upload pada perubahan yang sudah kita lakukan pada local machine kita. Pada kasus ini kita melakukan upload pada GitHuh, untuk melakukan push ini kita memerlukan remote repo pada github di dalam gitbash local kita dimana kita sudah melakukan itu pada saat membuat repository dengan command 'git remote add'

<img width="1115" alt="Screenshot 2024-02-18 at 00 18 25" src="https://github.com/SchoolBoyJoJo/ajk-jojo-penugasan1/assets/142652941/d7b8c7a0-715e-4a48-bb77-ba064af8a3fa">

Pada screenshot diatas ialah implementasi dari 'git pull' command ini berfungsi untuk mengambil perubahan yang telah terjadi pada repo origin kita (perubahan pada github) jadi kondisinya repo origin memiliki commit lebih banyak dari pada repo local machine kita, jika kita melakukan git pull maka semua perubahan yang sudah di commited pada repo origin akan diterapkan juga pada repo local kita


<img width="1134" alt="Screenshot 2024-02-18 at 13 19 17" src="https://github.com/SchoolBoyJoJo/ajk-jojo-penugasan1/assets/142652941/de34512e-af9a-4e7d-8362-980fbf72242e">

Pada screenshot diatas bisa kita lihat kita memiliki 3 branch yaitu development, master, lana. Anggap saja kasusnya kita sedang sibuk dalam mengerjakan branch lana namun team kita atau orang lain butuh bantuan kita segera pada branch development namun pengerjaan kita pada branch lana belum selesai sehingga kita belum ingin untuk melakukan commit, tentu saja jika kita belum melakukan commit kita tidak bisa pindah branch. Seperti pada screenshot ketika kita mencoba 'git checkout development' terdapat pesan error dan kita diminta untuk melakukan stash atau commit, disini lah 'git stash' memiliki peran
