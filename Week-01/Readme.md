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
- git clone. Command membuat Salinan repository lokal. <br/>
  ![](./image/SS-git-clone.jpg) <br/><br/>

# Day 2 : HTML

<b>Pengenalan HTML</b>

<p>HTML adalah singkatan dari Hypertext Markup Language. HTML digunakan untuk menampilkan konten pada browser. Contoh konten yang dapat ditampilkan seperti Text, Image, Video, Link, dan masih banyak lainnya. Dan HTML bukan sebuah bahasa pemrograman (programming languange), melainkan sebuah markup languange. Karna HTML bukan sebuah bahasa pemrograman HTML tidak bisa dinamis mengelola data karna itu HTML bersifat static, yang hanya menampilkan konten saja.</p>

<b>Tool Pendukung untuk membuat HTML</b>

1. Browser (Chrome, Mozila, Opera, Microsoft Edge dan lain - lain).
1. Code Editor (Visual Studio Code, Sublime Text, Lapce dan lain - lain).
1. Ekstensi Khusus untuk Visual Studio Code (Prettier, Live Server, Auto Rename Tag, Auto Close Tag dan lain - lain).

<b>Membuat HTML / Website Sederhana</b>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>WebsiteKu</title>
  </head>
  <body>
    <h1>Hallo World!</h1>
    <p>Nama Saya Muhammad Sadewo Wicaksono</p>
  </body>
</html>
```

![](./image/SS-html-website.jpg)

<b>Cara menjalankan HTML di Browser</b>

<p>Terdapat 2 cara dalam menjalankan HTML, yaitu secara manual dengan memasukkan direktori file pada search bar browser dan dengan ekstensi live server yang ada di Visual Studio Code.</p>

- Menjalankan secara manual. <br/>
  ![](./image/SS-html-website-manual.jpg) <br/>
  Penjelasan : Pada Search bar kita masukkan lokasi / tempat file html berada.
- Menjalankan dengan Live Server <br/>
  ![](./image/SS-html-website-liveserver.jpg) <br/>
  Note : Diharuskan menginstall ekstension live server terlebih dahulu
  ![](./image/SS-html-website.jpg) <br/>
  Hasil nya sama seperti manual, tetapi tanpa harus mengetikkan lokasi file berada.

<b>Tag Populer dalam HTML</b>

- img (image). Tag tersebut berguna untuk menyisipkan gambar pada HTML.

```html
<img src="./img/koeching.jpg" alt="gambar kucing 1" /> <img src="https://www.greeners.co/wp-content/uploads/2021/03/Kucing-Domestik-3.jpg" alt="gambar kucing 2" />
```

![](./image/SS-html-website-kucing.jpg)

- p (paragraph). Tag tersebut berguna untuk membuat paragraf pada HTML.

```html
<p>Nama Saya Muhammad Sadewo Wicaksono</p>
<p>Saya sedang Stupen di SKilvul</p>
```

![](./image/SS-html-website-p.jpg)

- a (a href). Tag tersebut berguna untuk membuat tulisan menjadi tulisan berlink.

```html
<a href="https://www.google.com/">google</a> ``
```

![](./image/SS-html-website-ahref.jpg)

<b>semantic HTML</b>

<p>Apa itu Semantic HTML? Semantic HTML adalah Tag HTML yang memiliki arti atau makna. <br/>
Contoh Semantic HTML</p>

![](./image/SS-html-semantic.jpg)

<p>Pada Semantic HTML kita tidak perlu lagi footer dibuat di dalam div class.</p>

![](./image/SS-html-semantic2.jpg)

<p>Karna footer terdapat Tag nya sendiri yang mempermudah dalam pembuatan Website.</p>

<b>Mendeploy Website ke Netlify</b>

1. Buka Website Netlify https://app.netlify.com/
2. Login menggunakan GitHub. <br/>
   ![](./image/SS-html-netlify.jpg)
3. Klik tab Sites dan klik Import from Git.
   ![](./image/SS-html-netlify2.jpg)
4. Pilih GitHub. <br/>
   ![](./image/SS-html-netlify3.jpg)
5. Pilih Repository dari GitHub yang ingin di Deploy.
   ![](./image/SS-html-netlify4.jpg)
6. Pada bagian Site Setting bisa di Skip / Scroll saja dan Klik Deploy Site.
   ![](./image/SS-html-netlify5.jpg)
   ![](./image/SS-html-netlify6.jpg)
7. Website sudah di Deploy, selanjutnya tinggal klik Link tersebut dan membuat Website yang sudah di Deploy.
   ![](./image/SS-html-netlify7.jpg)
8. Website sudah bisa dibuka secara Online. https://celebrated-paletas-a17b4a.netlify.app/
   ![](./image/SS-html-netlify8.jpg)

# Day 3 : CSS

<b>Apa itu CSS dan apa Peran CSS dalam HTML ?</b>

<p>CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mendesain halaman website. Seperti pengertiannya, CSS memiliki Peran sebagai mendesain halaman Website menjadi lebih menarik.</p>

<b>Menyisipkan CSS kedalam HTML</b>

<p>Terdapat 3 cara dalam menyisipkan CSS kedalam HTML</p>

1. Internal CSS. CSS dimasukkan langusng di dalam HTML menggunakan tag < style >.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>WebsiteKu</title>
    <style>
      p {
        color: blue;
      }
    </style>
  </head>
  <body>
    <h1>Hallo World!</h1>
    <p>Nama Saya Muhammad Sadewo Wicaksono</p>
    <a href="https://www.google.com/">google</a>
    <p>Saya sedang Stupen di SKilvul</p>
    <img src="./img/koeching.jpg" alt="gambar kucing 1" />
    <img src="https://www.greeners.co/wp-content/uploads/2021/03/Kucing-Domestik-3.jpg" alt="gambar kucing 2" />
  </body>
</html>
```

![](./image/SS-css.jpg)

2. Eksternal CSS. CSS terpisah dengan html, dan mengharuskan membuat file dengan ekstensi .css.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>WebsiteKu</title>
    <style>
      p {
        color: blue;
      }
    </style>
  </head>
  <body>
    <h1>Hallo World!</h1>
    <p>Nama Saya Muhammad Sadewo Wicaksono</p>
    <a href="https://www.google.com/">google</a>
    <p>Saya sedang Stupen di SKilvul</p>
    <img src="./img/koeching.jpg" alt="gambar kucing 1" />
    <img src="https://www.greeners.co/wp-content/uploads/2021/03/Kucing-Domestik-3.jpg" alt="gambar kucing 2" />
  </body>
</html>
```

![](./image/SS-css2.jpg)

3. Inline CSS. CSS langsung disematkan kedalam element HTML.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>WebsiteKu</title>
    <style>
      p {
        color: blue;
      }
    </style>
  </head>
  <body>
    <h1>Hallo World!</h1>
    <p>Nama Saya Muhammad Sadewo Wicaksono</p>
    <p style="color: red">inline css</p>
    <a href="https://www.google.com/">google</a>
    <p>Saya sedang Stupen di SKilvul</p>
    <img src="./img/koeching.jpg" alt="gambar kucing 1" />
    <img src="https://www.greeners.co/wp-content/uploads/2021/03/Kucing-Domestik-3.jpg" alt="gambar kucing 2" />
  </body>
</html>
```

![](./image/SS-css3.jpg)

<b>Tag dasar dan styling pada CSS</b>

1. < link >. Tag link berguna untuk menghubungkan file CSS dengan file HTML.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

2. < style >. Tag style biasanya digunakan langsung didalam file HTML nya.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      p {
        color: red;
      }
    </style>
    <title>Document</title>
  </head>
  <body>
    <p>coba</p>
    <b style="color: blue;">coba 2</b>
  </body>
</html>
```

<b>Flexbox pada CSS</b>

<p>Flexbox adalah cara untuk mengatur layout. Flexbox memiliki kemampuan untuk menyesuaikan layout secara otomatis. Karena hal itu Flexbox direkomendasikan karena penggunaannya yang mudah dan didukung oleh kebanyakan browser.</p>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
  </head>
  <body>
    <div class="container">
      <div class="item">item</div>
      <div class="item">item</div>
      <div class="item">item</div>
      <div class="item">item</div>
      <div class="item">item</div>
    </div>
  </body>
</html>
```

```css
.container {
  display: flex;
  border: 5px solid blue;
}
.item {
  border: 1px solid white;
  width: 100px;
  height: 100px;
  background-color: brown;
}
```

![](./image/SS-css-flexbox.jpg)

# Day 4 : Algorithm & Data Structures dan JS Dasar - Intro JavaScrip

## Algorithm & Data Structures

<b>Apa itu Algorithm & Data Structures? dan apa maanfaat dan perbedaan dari Algorithm & Data Structures?</b>

<p>Algoritma adalah deskripsi berupa step-step yang dibutuhkan untuk menyelesaikan suatu masalah, sedangkan Data Structures mengelola sebuah data.</p>

<b>Algoritma Sederhana dan bahasa pemprograman</b>

```algoritma
Mulai
Masukan bilangan pertama (A)
Masukan Bilangan kedua (B)
Hitung Hasil = A + B;
Tampilkan Hasil
Selesai
```

```javascript
let bilpertama = 20;
let bilkedua = 10;

console.log(bilpertama + bilkedua);
```

![](./image/SS-js.jpg)

<b>Big O Notation</b>

<p>Big O Notation digunakan untuk mengukur tingkat kompleksitas suatu algoritma. Dengan Big O Notation dapat mempercepat proses operasi dan mengurangi pemakaian memori yang berlebihan karena program yang panjang.</p>

## JS Dasar - Intro JavaScript

<p>Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website. Javascript juga dapat membuat website menjadi interaktif dan dinamis </p>

<b>Menjalankan Javascript</b>

1. Pertama buat file .html dan buat file .js
2. Hubungkan kedua file dengan

```html
<script src="script.js"></script>
```

3. Buka Browser, klik kanan kan klik inspect.
4. Klik tab Console disebelah Elements <br/>
   ![](./image/SS-js2.jpg)

<b>Tipe data pada Javascript</b>

<p>Terdapat 6 tipe data fundamental pada Javascript, yaitu number, string, boolean, null, undefined, dan object.</p>

1. number. Tipe data yang mengandung semua angka termasuk angka desimal. <br/>
   ![](./image/SS-js-number.jpg)
2. string. grup karakter yang ada pada keyboard laptop/PC kita yaitu letters (huruf), number (angka), spaces (spasi), symbol, dan lainnya. <br/>
   ![](./image/SS-js-string.jpg) <br/>
   ![](./image/SS-js-string-hasil.jpg)
3. boolean. tipe data yang hanya mempunyai 2 buah nilai. <br/>
   ![](./image/SS-js-boolean.jpg)
4. null. Tipe data yang diartikan bahwa sebuah variable/data tidak memiliki nilai. Null berbeda dengan string kosong. String kosong masih memiliki tipe data string. <br/>
   ![](./image/SS-js-null.jpg) <br/>
   ![](./image/SS-js-null-hasil.jpg)
5. Undefined. Tipe data yang merepresentasikan varibel/data yang tidak memiliki nilai. <br/>
   ![](./image/SS-js-undefined.jpg) <br/>
   ![](./image/SS-js-undefined-hasil.jpg)
6. object. Tipe data yang mengkoleksi data yang saling berhubungan (related). Tipe data pbject dapat menyimpan data dengan tipe data apapun (number, string, boolean, dan lainnya). <br/>
   ![](./image/SS-js-object.jpg)

<b>Operator pada Javascript</b>

- Assignment Operator (=). Assignment operator digunakan untuk menyimpan sebuah nilai pada variabel.

```js
let nama = 'Muhammad Sadewo Wicaksono';
```

- Arithmetic Operator. Arithmetic operator adalah operator yang melibatkan operasi matematika.

```js
consol.log(1 + 1); // Prints 2
consol.log(4 - 2); // Prints 2
consol.log(5 * 3); // Prints 15
consol.log(10 / 2); // Prints 5
consol.log(11 % 3); // Prints 2
```

- Comparison Operator. Comparison operator adalah operator yang membandingkan satu nilai dengan nilai lainnya. Hasil operasi yang melibatkan comparison operator adalah antara true or false

```js
10 > 8; // Prints 'true'
4 > 5; // Prints 'false'
```

- Logical Operator. Logical operator biasa digunakan untuk sebuah CONDITIONAL pada pemograman. Menghasilkan nilai BOOLEAN yaitu TRUE or FALSE.
<p>AND (&&) akan menghasilkan nilai true jika kedua atau semua premis bernilai TRUE.</p>

```js
console.log(true && true); // true
console.log(true && false); // false
console.log(false && true); // false
console.log(false && true && true); // false
console.log(true && true && true); // true
```

<p>OR (||) akan menghasilkan nilai true jika salah satu premis mengandung nilai TRUE</p>

```js
console.log(true || true); // true
console.log(true || false); // true
console.log(false || false || true); // true
console.log(false || false); // false
```

<p>NOT (!) akan membalikkan sebuah nilai BOOLEAN. TRUE menjadi FALSE dan sebaliknya.</p>

```js
let mandi = true;
console.log(!mandi); // false

let main = false;
console.log(!main); // true
```

# Day 5 : JS Dasar - Conditional & Looping

## Conditional

<p>Conditional merupakan statement percabangan yang menggambarkan suatu kondisi. Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut</p>

<b>Contoh Conditional</b>

1. IF Statement

```js
let laper = true;
if (laper) {
  console.log('makan');
}
```

![](./image/SS-js-condition.jpg) 2. IF … ELSE Statement

```js
let laper = false;
if (laper) {
  console.log('makan');
} else {
  console.log('skip, kenyang');
}
```

![](./image/SS-js-condition2.jpg) 3. IF … ELSE IF … Statement

```js
let lampu = 'hijau';
if (lampu === 'merah') {
  console.log('berhenti');
} else if (lampu === 'kuning') {
  console.log('alon - alon');
} else {
  console.log('jalan');
}
```

![](./image/SS-js-condition3.jpg)

## Looping

<p>Looping adalah statement yang mengulang sebuah instruksi hingga kondisi terpenuhi atau jika kondisi stop/berhenti tercapai.</p>

<b>Macam - Macam perulangan pada Javascript</b>

1. Manual Loop

```js
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
```

![](./image/SS-js-looping.jpg)

2. FOR LOOP
<p>Gunakan For Loop bila mengetahui seberapa banyak nilai pasti untuk pengulangan.</p>

```js
let angka = 1;
for (angka; angka <= 5; angka++) {
  console.log(angka);
}
```

![](./image/SS-js-looping2.jpg)

3. WHILE LOOP
<p>Gunakan WHile Loop bila tidak mengetahui seberapa banyak nilai pasti untuk pengulangan.</p>

```js
let angka = 1;
while (angka <= 5) {
  console.log(angka);
  angka++;
}
```