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

<img width="1130" alt="Screenshot 2024-02-18 at 13 21 01" src="https://github.com/SchoolBoyJoJo/ajk-jojo-penugasan1/assets/142652941/110deb09-7bc7-4de6-96d1-dd482fcb9d1b">

Pada screenshot diatas kita melakukan git stash dan kita dapat berpindah ke branch development, ketika kita melakukan git stash git akan memberikan id pada stash yang kita lakukan pada screenshot id nya ialah '85fb545' jadi git stash akan menyimpan pekerjaan yang sudah kita lakukan pada branch lana pada id itu. Jika kita telah selesai dengan urusan di develpoment (skenario nya) maka jika kita ingin melanjutkan pekerjaan kita pada branch lana kita harus pindah terlebih dahulu pindah ke branch lana dan melakukan 'git stash pop' disana

<img width="1132" alt="Screenshot 2024-02-18 at 13 23 29" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/6d6b5d73-3403-4420-86f9-152efb2f53d1">

Pada screenshot diatas kita telah melakukan git stash dan bisa kita lihat git memberikan status pada hal yang sedang kita kerjakan sebelumnya dimana pekerjaan kita pada branch lana belum di commit yang pasti status nya masih merah setelah melakukan git stash kita dapat melanjutkan pekerjaan kita

<img width="1440" alt="Screenshot 2024-02-18 at 17 54 56" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/ba630d92-826a-49ae-bd31-bbf9b42b6518">

Pada screenshot perhatikan pada line 21 disitu ialah perubahan yang kita lakukan 

<img width="1132" alt="Screenshot 2024-02-18 at 17 55 58" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/a7f178fe-09e3-4861-ab7f-75740d845a1a">

Pada screenshot itu kita telah melakukan commit pada perubahan yang kita lakukan, bisa diliat pada git log yang ditampilkan, anggap saja skenario kita telah melakukan kesalahan pada commit yang kita lakukan sehingga kita perlu kembali ke commit sebelumnya disitu lah kita akan menggunakan 'git reset'

<img width="1440" alt="Screenshot 2024-02-18 at 17 57 45" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/c3084b88-9201-4eea-b70a-1330c6a634d3">

Pada screenshot kita telah melakukan git reset pada id commit sebelumnya (kita bisa kembali ke commit mana pun asal tau id nya, cari id nya bisa dengan 'git log') saat melalukan git reset memang perubahan yang kita lakukan tidak lah hilang (line 21) jika skenario nya kita ingin menghapus total commit dan perubahan yang kita buat itu melakukan perintah 'git reset <id_commit> --hard'

<img width="1440" alt="Screenshot 2024-02-18 at 17 59 52" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/b9185e14-20fa-42a1-9016-3be96c700f5e">

Pada screenshot itu saya menunjukkan hasil dari melakukan 'git reset <id_commit> --hard' dimana perubahan (line 21) menghilang sepenuhnya

<img width="1440" alt="Screenshot 2024-02-18 at 13 55 51" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/1c7e4529-fbfb-482b-b24a-527a2c1b423d">

Pada screenshot diatas ialah perubahan yang kita lakukan (line 17-20)

<img width="584" alt="Screenshot 2024-02-18 at 13 55 31" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/69b77be4-8a38-45ea-9d48-1d78fea53497">

Pada screenshot diatas kita melakukan perintah 'git diff' perintah ini akan melakukan perbandingan pada file yang sedang kita kerjakan dengan file ada di repo, jika hanya melakukan git diff ini tidak akan menunjukkan perbedaan yang telah kita masukkan ke staging area

<img width="582" alt="Screenshot 2024-02-18 at 13 57 28" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/40be588c-2546-4f27-ad96-41c443e3e2b3">

Jika ingin membandingkan perbedaan file yang berada di staging area dan repo maka kita perlu melakukan 'git diff --cached'

<img width="1118" alt="Screenshot 2024-02-18 at 01 08 58" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/49797786-f160-472c-a3c9-270964ed2dae">

Pada screenshot diatas kita melakukan merge pada branch featureA dengan development, tentunya diatas kita telah membuat branch development, featureA, featureB. Dimana struktur nya branch master direct-path ke branch development; branch development direct-path ke branch featureA dan featureB. Pada screenshot tujuan kita ialah melakukan merge pada branch featureA ke development dimana jika kita ingin melakukan itu kita perlu berada di branch development setelah itu kita bisa menjalankan command 'git merge featureA'. Seperti yang kita lihat pesan yang diberikan pada gitbash ialah "Fast-forward" dimana hal ini akan terjadi jika kita melakukan merge pada branch yang memiliki jalur direct-path

# 4. Menangani conflict pada saat melakukan merge

<img width="1440" alt="Screenshot 2024-02-18 at 01 12 54" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/ee5a808f-90ee-4857-84ac-02ab7ab85e82">

Pada screenshot diatas dapat kita lihat bahwa ketika kita ingin melakukan merge pada featureB ke development terjadi conflict karna sebelumnya kita telah melakukan merge pada featureA dimana featureA dan featureB melakukan perubahan pada line yang sama sehingga ketika terjadi conflict kita harus menyelesaikan nya terlebih dahulu sebelum di merge. Kita dapat memilih perubahan yang ingin kita pakai antara featureA dan featureB tentu saja kita bisa memilih perubahan dari kedua branch jadi conflict ini dapat diselesaikan cukup mudah, hanya dengan mengedit file pada code editor seperti biasanya dan setelah melakukan edit kita harus memasukkan perubahan yang telah kita lakukan pada staging area dan melakukan commit

<img width="1132" alt="Screenshot 2024-02-18 at 01 18 38" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/914f40dc-a5f1-460e-af15-226584976fab">

Pada graph itu dapat kita lihat, pada commit id ed5783 kita telah melakukan merge featureB ke development, sebenarnya merge yang kita lakukan itu bukannlah merge Fast-forward melainkan Three-way merge. Kenapa Three-way merge? karna featureA dan featureB tidak direct-path, sebelumnya kita telah melakukan merge pada featureA dan development sehingga membuat development tidak direct-path lagi dengan featureB jika kita melakukan Three-way merge biasanya gitbash akan menyebut sebagai recursive merge

# 5. Merge no Fast-forward

<img width="1139" alt="Screenshot 2024-02-18 at 01 30 44" src="https://github.com/arsitektur-jaringan-komputer/modul-git/assets/142652941/ec3610c3-d53b-4b46-89bf-472c57fda387">

Pada screenshot diatas kita bisa lihat, bahwa kita melakukan recursive merge, serupa dengan kasus conflict sebelumnya ini terjadi karna kita melakukan merge pada branch yang tidak direct-path
