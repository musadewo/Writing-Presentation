# Day 1 : Unix Command Line & Git & Git Hub Dasar

## Unix Command Line

- Shell adalah sebuah program yang menerima perintah (Command) untuk di eksekusi oleh system.
- Command Line Interface (CLI) atau Antarmuka Baris Perintah berfungsi untuk memasukkan perintah (Command) pada Sistem.
- Terminal Emulator Program atau Aplikasi untuk mengakses CLI, contoh Terminal Emulator di windows adalah Command Prompt (CMD) , Terminal, dan Windows PowerShell.

<b>Mengakses CLI pada Windows.</b>

<p>Untuk mengakses CLI pada Windows bisa menggunakan Git Bash, CMD, PowerShell atau Terminal. Untuk Git Bash diharuskan mendownload dan menginstall terlebih dahulu, tetapi untuk CMD, PowerShell dan Terminal sudah ada dari Windows.</p>

<b>File System Structure</b>

<p>File System Structure berfungsi untuk mengatur data yang disimpan didalam sebuah system.</p>

<b>Command pada CLI</b>

- pwd (Print working directory). Command untuk melihat current working directory. <br/>
  ![](./image/SS-pwd.jpg)
- ls (lists). Command untuk melihat isi file yang ada di sebuah direktori. <br/>
  ![](./image/SS-ls.jpg)
- cd (change directory). Command untuk berpindah direktori. <br/>
  ![](./image/SS-cd.jpg)
- cat (concatenate). Command untuk melihat seluruh isi sebuah file. <br/>
  ![](./image/SS-cat.jpg)
- head. Command untuk melihat beberapa line awal dari sebuah file.
  ![](./image/SS-head.jpg)
- tail. Command untuk melihat beberapa line akhir dari sebuah file.
  ![](./image/SS-tail.jpg)
- touch. Command untuk membuat sebuah file. <br/>
  ![](./image/SS-touch.jpg)
- mkdir (make directory). Command untuk membuat sebuah direktori
  ![](./image/SS-mkdir.jpg)
- cp (copy). Command untuk mengcopy (menyalin) file. <br/>
  ![](./image/SS-cp.jpg)
- cp -r (recursive copy). Command untuk mengcopy (menyalin) directory.
  ![](./image/SS-cp-r.jpg)
- mv (move). Command untuk memindahkan file dan direktori.
  ![](./image/SS-mv.jpg)
- mv (rename). Command mv juga bisa untuk mengganti nama file atau direktori.
  ![](./image/SS-mv-rename.jpg)
- rm (remove). Command untuk menghapus file. <br/>
  ![](./image/SS-rm.jpg)
- rm -r (recursive remove). Command untuk menghapus direktori. <br/>
  ![](./image/SS-rm-r.jpg)

## Git & GitHub Dasar

<b>Apa itu Git & GitHub? Kenapa Git & GitHub menjadi tool yang wajib digunakan?</b>

<p><b>Git</b> adalah adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file. <br/> <b>GitHub</b> adalah tempat atau platform untuk menyimpan source code suatu proyek dan melacak riwayat lengkap semua perubahan. Dan GitHub sebagai tempat berkaloborasi projects dalam sebuah team yang sama tanpa harus copy paste folder.</p>

<b>Perbedaan antara Git dan GitHub</b>

<p><b>Git</b> merupakan software berbasis Version Control System (VCS) yang bertugas untuk mencatat perubahan seluruh file atau repository suatu project. Sedangkan <b>GitHub</b> merupakan layanan cloud yang berguna untuk menyimpan dan mengelola sebuah project yang dinamakan repository (repo git).</p>

<b>Alur kerja Git dan GitHub</b>

<p><b>Git</b> sebagai Version Control System berguna untuk mencatat setiap perubahan dalam seluruh file atau respository, sedangkan <b>GitHub</b> tempat upload project yang telah dibuat secara local.</p>

<b>Membuat Repository pada GitHub</b>

- Buka Website GitHub dan Login.
- klik tab Repositories dan klik New.
  ![](./image/SS-repo-1.jpg)
- Masukkan nama untuk repository nya dan pilih Public bila ingin dilihat oleh orang lain. Jika tidak ingin dilihat orang lain, pilih Private
  ![](./image/SS-repo-2.jpg)
- centang Add a README File bila ingin langsung membuat file Readme didalam repository dan Create repository.
  ![](./image/SS-repo-3.jpg)

<b>Command atau Perintah pada Git</b>

- git add. Command yang digunakan untuk menambahkan file baru di repository yang dipilih.
  ![](./image/SS-git-add.jpg)
- git commit. Command untuk menyimpan perubahan yang sudah dilakukan, namun tidak ada perubahan yang terjadi pada remote repository.
  ![](./image/SS-git-commit.jpg)
- git push. Command untuk mengirimkan perubahan file yang dilakukan setelah di commit ke remote repository.
  ![](./image/SS-git-push.jpg)
- git clone. Command membuat Salinan repository lokal.
  ![](./image/SS-git-clone.jpg)
