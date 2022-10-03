# Day 1 : Js Dasar-Scope & Function

## Js Dasar - Scope

<b>Apa itu Scope dalam Javascript ? Ada berapa macam Scope pada Javascript ?</b>

<p>Scope adalah  konsep yang digunakan untuk membatasi pengaksesan suatu variabel. Scope berfungsi untuk Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.</p>
<p>Analogi Sederhana Scope : <br/>
Bayangkan sebuah kaleng berisikan biskuit. Kita bisa memasukkan biskuit tersebut ke dalam tiap kaleng yang berbeda, dan suatu saat kita lapar, kita bisa tahu ke kaleng mana yang harus kita cari.</p>
<p>Pada analogi diatas kita bisa tahu bahwa, Variable adalah biskuit dan scope adalah kaleng. Kesimpulan : scope adalah tempat yang mengurung / menyimpan variable yang ada didalamnya.</p>

<p>Scope pada Javascript terdapat 3 tipe, yaitu Block Scope, Global Scope, dan Local / Function Scope</p>

1. Block Scope <br/> Blocks adalah code yang berada didalam curly braces {}. Pada Block Scope, jika kita melakukan console.log diluar curly braces / kurung kurawal, hanya variable var saja yang bisa terpanggil sedangkan untuk variable let dan const tidak bisa terpanggil.

```js
{
  var i = 5;
  let x = 2;
  const y = 3;
}
console.log(i);
console.log(x);
console.log(y);
```

![](./image/SS-js-block-scope.jpg)

2. Global Scope <br/> Variable yang dideklarasikan secara global (diluar function apa pun) disebut Global Scope. Global Scope dapat mendeklerasikan dengan var, let dan const ketika dideklarasikan diluar block.

```js
let nama = 'sadewo';

function orang() {
  return nama;
}

console.log(orang());
console.log(nama);
```

![](./image/SS-js-global-scope.jpg)

3. Local / Function Scope <br/> Seperti namanya, Local / Function Scope hanya dapat diakses didalam Function saja. Jika mendeklarasikan variable didalam Function, hanya Function tersebut yang dapat mengaksesnya. Bisa dibilang Local / Function Scope kebalikan dari Global yang bisa diakses dari mana saja selama masih dalam Program Javascript.

```js
function orang() {
  var nama = 'Sadewo';
  return nama;
}

console.log(orang());
console.log(nama);
```

![](./image/SS-js-local-scope.jpg)

## Js Dasar - Function

<b>Apa itu Function ? Kenapa kita membutuhkan Function pada Javascript ?</b>

<p>Function adalah sebuah blok kode yang dirancang untuk melakukan tugas / task tertentu. Function pada Javascript berfungsi untuk mempersingkat dan mempermudah programmer dalam penulisan kode atau program yang sama tidak tertulis secara berulang kali. Jadi kita hanya membuat 1 function, tetapi function tersebut dapat digunakan atau dipanggil kembali.</p>

```js
function hallow() {
  return 'Hellow~';
}
```

![](./image/SS-js-function.jpg)

<p>Memanggil Function bisa dengan cara memanggil nama function nya, dan dengan console.log(namafunction());</p>

```js
hallow(); // memanggil dengan nama function
console.log(hallow()); // memanggil dengan console.log
```

### Parameter dan Argumen

<b>Parameter Function</b>

<p>Parameter Function dapat menerima sebuah inputan data dan memproses data tersebut untuk melakukan task / tugas. Saat membuat Function, harus memperhatikan data yang dibutuhkan. Misalnya mau membuat function pengurangan dengan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.</p>

![](./image/SS-js-parameterfunction.jpg)

```js
function pengurangan(a, b) {
  return a - b;
}
```

<b>Argumen Function</b>

<p>Argumen adalah nilai yang digunakan saat memanggil function. Jumlah argumen harus sama dengan jumlah parameternya. Jadi jika di function penambahan ada 2 parameter nilai saat membuat function. Saat memanggil function gunakan 2 buah nilai argumen.</p>

![](./image/SS-js-argument2.jpg)

```js
function pengurangan(a, b) {
  return a - b;
}

console.log(pengurangan(10, 5));
```

![](./image/SS-js-argument.jpg)

<b>Default Parameters</b>

<p>Default paramaters digunakan untuk memberikan nilai awal/default pada parameter function. Default parameters bisa digunakan jika ingin menjaga function agar tidak error (undefined) saat dipanggil tanpa argumen.</p>

```js
// Default Parameter pada Reguler Function
function hellow(name = 'Stranger', greet = 'Hello') {
  console.log(`${greet} ${name}!`);
}

hellow('Sadewo', 'Hai');
hellow();
```

```js
// Default Parameter pada Arrow Function
const hellow = (name = 'Stranger', greet = 'Hello') => console.log(`${greet} ${name}!`);

hellow('Sadewo', 'Hai');
hellow();
```

![](./image/SS-js-defaultparameters.jpg)

<b>Arrow Function</b>

<p>Arrow function adalah cara lain menuliskan function. Ini adalah fitur terbaru yang ada pada ES6 (Javascript Version)</p>

```js
const pengurangan = (a, b) => {
  return a - b;
};
console.log(pengurangan(4, 2));
```

![](./image/SS-js-arrowfunction.jpg)

# Day 2 : Js Dasar - Data Type Built in Prototype & Method

<p>JavaScript adalah bahasa dinamis dengan tipe dinamis. Variabel dalam JavaScript tidak secara langsung terkait dengan jenis nilai tertentu, dan variabel apa pun dapat diberi (dan ditetapkan ulang) nilai dari semua jenis.</p>

```js
let i = 42; // i sekarang adalah tipe data number
i = 'bar'; // i sekarang adalah tipe data string
i = true; // i sekarang adalah tipe data boolean
```

<p>JavaScript juga merupakan bahasa yang diketik dengan lemah, yang berarti memungkinkan konversi tipe implisit saat operasi melibatkan tipe yang tidak cocok, alih-alih melempar kesalahan tipe.</p>

<b>JavaScript types</b>

<p>Pada JavaScript terdapat 2 jenis tipe data, yaitu tipe data primitif dan tipe data object (non primitif).</p>
<p>Tipe data primitif : </p>

1. String
2. Number
3. BigInt
4. Boolean
5. Null
6. Undefined
7. Symbol

<p>Tipe data object (non primitif)</p>

1. Array
2. Object
3. Map
4. Date
5. Masih banyak lagi

<b>Menemukan jenis tipe data menggunakan typeof</b>

```js
let buah = 'mangga';

console.log(typeof buah);
```

![](./image/SS-js-typeof.jpg)

```js
let angka = 123218;

console.log(typeof angka);
```

![](./image/SS-js-typeof2.jpg)

<b>Memeriksa berapa banyak karakter dalam 1 kata menggunkan length.</b>

```js
let buah = 'mangga';

console.log(buah.length);
```

![](./image/SS-js-length.jpg)

## String

<p>Objek String digunakan untuk mewakili dan memanipulasi urutan karakter. <br/>
String berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk teks. Beberapa operasi yang paling sering digunakan pada string adalah memeriksa panjangnya, membangun dan menggabungkannya menggunakan operator string + dan +=, memeriksa keberadaan atau lokasi substring dengan metode indexOf(), atau mengekstrak substring dengan substring () metode.</p>

<b>Membuat string menjadi huruf kapital dengan method toUpperCase() dan menjadi huruf kecil dengan method toLowerCase()</b>

<p>toUpperCase()</p>

```js
let buah = 'mangga';

console.log(buah.toUpperCase());
```

![](./image/SS-js-toUpperCase.jpg)

<p>Metode toUpperCase() mengembalikan nilai string panggilan yang dikonversi menjadi huruf besar.</p>
<br/>

<p>toLowerCase()</p>

```js
let buah = 'JeRuK';

console.log(buah.toLowerCase());
```

![](./image/SS-js-toLowerCase.jpg)

<p>Metode toLowerCase() mengembalikan nilai string panggilan yang dikonversi ke huruf kecil.</p>
<br/>

<b>Mencari / Mengembalikan 1 karakter dalam string menggunakan method charAt()</b>

```js
let buah = 'JeRuK';

console.log(buah.charAt(2));
```

![](./image/SS-js-charat.jpg)

<p>Kenapa pada hasil yang ditampilkan adalah R ? kenapa bukan e yang ditampilkan ? <br/>
Karena Method CharAt() mengembalikan 1 karakter sesuai dengan Array jadinya indexnya dimulai dari 0 bukan 1, karena itulah yang dikembalikan adalah R.</p>

<b>Mencari 1 karakter atau 1 kata dalam sebuah string menggunakan method includes()</b>

```js
let buah = 'JeRuK';

console.log(buah.includes('R'));
```

![](./image/SS-js-includes.jpg)

<p>Pada method includes(), ketika karakter / kata yang ingin dicari dalam string ketemu maka akan menampilkan nilainya true, bila tidak menemukannya maka nilainya false</p>

<b>Method split() memisahkan data dan mengubahnya menjadi data array</b>

```js
let kalimat = 'dengan menggunakan split(), kita dapat memisahkan sebuah string menjadi data array';
console.log('BEFORE', kalimat);
console.log('AFTER', kalimat.split(' '));
```

![](./image/SS-js-split.jpg)

<p>Pada codingan diatas, method split membutuhkan pola dan membagi string yang dituju, dan mengubahnya menjadi array.</p>

<b>Method Number.isNan / isNan</b>

![](./image/SS-js-NaN.jpg)

<p>Method Number.isNaN() menentukan apakah nilai yang diteruskan adalah NaN dan tipenya adalah Number. Sedangakan Method isNaN() menentukan apakah nilai yang diteruskan adalah NaN (NaN = Not A Number).</p>

<b>Method toString()</b>

![](./image/SS-js-toString.jpg)

<p>Method toString berfungsi untuk merubah Number / angka menjadi String.</p>

<b>Method toFixed()</b>

![](./image/SS-js-tofixed.jpg)

<p>Method toFixed berfungsi untuk mengambil atau menampilkan angka dibelakang koma (,) atau titik (.)</p>

<b>Math : Properti</b>

- Math.E <br/> Properti Math.E mewakili bilangan Euler, basis logaritma natural, e, yang kira-kira 2,718. <br/>
  ![](./image/SS-js-math.e.jpg)

- Math.PI <br/> Properti Math.PI mewakili rasio keliling lingkaran dengan diameternya, kira-kira 3,14159 <br/>
  ![](./image/SS-js-mathpi.jpg)

<b>Math : Method</b>

- Math.abs() <br/> Function Math.abs() mengembalikan nilai absolut dari sebuah angka. <br/>
  ![](./image/SS-js-mathabs.jpg)

- Math.ceil() <br/> Function Math.ceil() selalu membulatkan dan mengembalikan bilangan bulat yang lebih kecil yang lebih besar dari atau sama dengan angka yang diberikan. <br/>
  ![](./image/SS-js-mathceil.jpg)

- Math.floor() <br/> Function Math.floor() selalu membulatkan ke bawah dan mengembalikan bilangan bulat terbesar yang kurang dari atau sama dengan angka tertentu. <br/>
  ![](./image/SS-js-mathfloor.jpg)

- Math.round() <br/> Function Math.round() mengembalikan nilai angka yang dibulatkan ke bilangan bulat terdekat. <br/>
  ![](./image/SS-js-mathround.jpg)

- Math.random() <br/> Function Math.random () mengembalikan angka acak antara 0 (inklusif), dan 1 (eksklusif).
  <br/>
  ![](./image/SS-js-mathrandom.jpg)

<b>Prototype</b>

```js
function Person(first, middle, last, age) {
  this.firstName = first;
  this.middleName = middle;
  this.lastName = last;
  this.age = age;
}

const Saya = new Person('Muhammad', 'Sadewo', 'Wicaksono', 50);
document.getElementById('p').innerHTML = 'Nama Saya ' + Saya.middleName;
```

![](./image/SS-js-prototype.jpg)

# Day 3 : Js Dasar - DOM Introduction, Selecting Elements, dan DOM Traversing Elements

## JS Dasar - DOM Introduction

<p>Document Object Model (DOM) adalah representasi data dari objek yang terdiri dari struktur dan konten dokumen di web. Panduan ini akan memperkenalkan DOM, melihat bagaimana DOM merepresentasikan dokumen HTML di memori dan bagaimana menggunakan API untuk membuat konten web dan aplikasi.</p> 
<p>Document Object Model (DOM) adalah antarmuka pemrograman untuk dokumen web. Ini mewakili halaman sehingga program dapat mengubah struktur, gaya, dan konten dokumen.</p> 
<p>DOM bukan bagian dari bahasa JavaScript, melainkan Web API yang digunakan untuk membangun situs web.</p>
<p>DOM adalah jembatan atau penghubung supaya bahasa pemrogramaan dapat berinteraksi dengan dokumen HTML. Dengan DOM, JavaScript (JS) dapat memanipulasi HTML.</p> <br/>

## JS Dasar - Selecting Elements & Traversing Elements

<b>Macam - macam Selector Elements pada JS</b>

- getElementById(); <br/> getElementById digunakan untuk menyeleksi elemen dengan menggunakan ID pada element tersebut. Element ID harus unik tidak boleh ada yang sama dalam satu web. Jika ada yang sama, maka salah satunya tidak akan di perses.

```js
document.getElementById('saya');
```

```js
let title = document.getElementById('title');
console.log(title);
```

![](./image/SS-js-byid.jpg)

- getElementsByClassName() <br/> getElementByClassName digunakan untuk menyeleksi elemen dengan menggunakan Class pada suatu elemen.

```js
document.getElementsByClassName('kelas');
```

```js
let items = document.getElementsByClassName('item');
console.log(items[2]);
```

![](./image/SS-js-byclass.jpg)

- getElementsByName() <br/> getElementByName digunakan untuk menyeleksi elemen berdasarkan attribute name pada elemen/tag (name=”name_value“).

```js
document.getElementsByName('nama');
```

- getElementsByTagName() <br/> getElementByTagName digunakan untuk menyeleksi elemen berdasarkan nama tag/elemen pada HTML.

```js
document.getElementsByTagName('tagname');
```

```js
let itemByTag = document.getElementsByTagName('li');
console.log(itemByTag[1]);
console.log(itemByTag.item(1));
console.log(itemByTag.length);
```

![](./image/SS-js-bytagname.jpg)

- querySelector() <br/> querySelector menyeleksi elemen dengen menggunakan CSS Selector.

```js
document.querySelector('css');
```

```js
let listQuery = document.querySelector('.list');
console.log(listQuery);
```

![](./image/SS-js-query.jpg)

```js
console.log(itemQuery.parentElement);
console.log(itemQuery.closest('.list'));
```

![](./image/SS-js-query2.jpg)

- querySelectorAll() <br/> querySelectorAll menyeleksi semua elemen menggunakan CSS selector yang digunakan.

```js
document.querySelectorAll('css');
```

# Day 4 : JS Dasar - DOM Manipulating Elements & Styles

## JS Dasar - DOM Manipulating Elements

<b>Macam - macam DOM Manipulating Elements</b>

- innerHTML <br/> innerHTML adalah properti dari Elemen yang memungkinkan Anda untuk mendapatkan atau mengatur markup HTML yang terkandung di dalam elemen.

```html
<ul id="menu">
  <li>Home</li>
  <li>Services</li>
</ul>
```

```js
let menu = document.getElementById('menu');
console.log(menu.innerHTML);
```

![](./image/SS-js-innerHTML.jpg)

- CreateElement <br/> CreateElement berfungsi untuk menambahkan Element tanpa harus membuat di file HTML.

```js
let p = document.createElement('p');
p.innerText = 'ini adalah paragraf';
```

- append <br/> append() menyisipkan satu set objek Node atau objek DOM String. append() dilakukan setelah CreateElement().

```js
app.append(p);
```

![](./image/SS-js-append.jpg)

- appendChild <br/> apeendChild() menambahkan simpul (elemen) sebagai anak terakhir dari sebuah elemen.

```js
let p2 = document.createElement('p');
p2.innerText = 'paragraf ke-2';
app.appendChild(p2);
```

![](./image/SS-js-appendchild.jpg)

- remove <br/> remove() menghapus elemen (atau node) dari dokumen.

```js
let end = document.getElementById('end');
end.remove();
```

![](./image/SS-js-remove.jpg)

<b>Attribute</b>

```js
console.log(link.attributes); // [] list attribute
console.log(link.getAttribute('href')); // ambil isi attribute
link.setAttribute('id', 'google'); // add attribute
```

## JS Dasar - DOM Styles

<b>Memberikan Style dari Element</b>

```js
let link = document.getElementsByClassName('link')[0];

link.style.color = 'black';
link.style.border = '1px solid black';
link.style.padding = '5px 20px';
link.style.backgroundColor = 'cyan';
link.style.removeProperty('border'); // menghapus style property
```

![](./image/SS-js-style.jpg)

# Day 5 : JS Dasar - DOM Events & Forms

## JS Dasar - DOM Events

<p>Events adalah Kejadian/kegiatan/interaksi yang terjadi pada website.</p>

<p>Terdapat 3 cara dalam memberikan event</p>

1. Menambahkan di HTML Attribute nya <br/>

```js
<h1 onclick="alert('Hallow')">Hallow</h1>
```

2. Menambahkan Event Property <br/>

```js
let kalimat = document.getElementById('kalimat');
kalimat.onclick = function () {
  alert('ini dari kalimat');
};
```

3. Menambahkan addEventListener() <br/>

```js
let button = document.getElementById('btn');
button.addEventListener('click', function (event) {
  console.log(event.target);
  alert('ini dari button');
});
```

<b>Counter menggunakan Selecting Element dan addEventListener</b>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>

    <script src="./script.js" defer></script>
  </head>
  <body>
    <!-- Buat counter -->
    <div>
      <button id="decrement">-</button>
      <span id="counter">0</span>
      <button id="increment">+</button>
    </div>
  </body>
</html>
```

```js
let btnDecrement = document.getElementById('decrement');
let btnIncrement = document.getElementById('increment');
let counter = document.getElementById('counter');

let angka = 0;

btnIncrement.addEventListener('click', function () {
  angka = angka + 1;
  counter.innerText = angka;
});

btnDecrement.addEventListener('click', function () {
  angka--;
  counter.innerText = angka;
});
```

![](./image/SS-js-counter.jpg) <br/>
![](./image/SS-js-counter2.jpg) <br/>
![](./image/SS-js-counter3.jpg)

## JS Dasar - DOM Forms

<b>Membuat Form Login</b>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>

    <script src="./script.js" defer></script>
  </head>
  <body>
    <div class="container">
      <form id="sign-in">
        <h1>Sign In</h1>

        <div class="field">
          <label for="username">username</label>
          <input type="text" id="username" name="username" />
        </div>

        <div class="field">
          <label for="password">password</label>
          <input type="text" id="password" name="password" />
        </div>

        <button type="submit">login</button>
      </form>
    </div>
  </body>
</html>
```

```js
let loginForm = document.querySelector('#sign-in');
let inputUsername = document.querySelector('#username');
let inputPassword = document.querySelector('#password');

let user = {
  username: 'sadewo',
  password: '123',
};

loginForm.addEventListener('submit', (event) => {
  event.preventDefault();

  let userLogin = {
    username: inputUsername.value,
    password: inputPassword.value,
  };

  console.log(userLogin);

  let login = userLogin.username == user.username && userLogin.password == user.password;

  if (login) {
    console.log('selamat anda berhasil login');
  } else {
    console.log('username dan password anda salah');
  }

  loginForm.reset();
});
```

![](./image/SS-js-form.jpg)
