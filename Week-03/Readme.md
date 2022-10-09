# Day 1 : JS Intermediate Array & Multidimensional Array

## JS Intermediate Array

<p>Apa itu Array ? Kenapa dalam 1 Variable Array bisa memuat lebih dari 1 data ? <br/>
Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.</p>

<p>Array itu bisa dibilang sebagai kereta, karena pada array ada yang namanya Index. Index adalah urutan data pada Array, index dimulai dari 0 atau dari data pertama yang terdapat pada Array.</p>

<b>Contoh Struktur Array</b>

```js
// Tanpa Index

let buah = ["Jeruk", "Anggur", "Semangka"];
console.log(buah);
```

```js
// Menggunakan Index

let hewan = ["Kucing", "Kancul", "Kelinci"];
console.log(hewan[2]);
```

![](./image/SS-js-strukturarray.png)

<b>Property & Method Array</b>

- Property Length <br/> Property Length mengembalikan jumlah data / element pada Array.

```js
let buah = ["Jeruk", "Anggur", "Semangka"];
console.log(buah.length);
```

![](./image/SS-js-array.png)

- Method Push <br/> Method push() menambahkan satu atau lebih elemen ke akhir array dan mengembalikan panjang array yang baru.

```js
let buah = ["Jeruk", "Anggur", "Semangka"];
buah.push("Mangga");
console.log(buah);
// Mangga akan muncul diakhir Array
```

![](./image/SS-js-array2.png)

- Method Unshift <br/> Method unshift() menambahkan satu atau lebih elemen ke awal array dan mengembalikan panjang array yang baru.

```js
let buah = ["Jeruk", "Anggur", "Semangka"];
buah.push("Mangga");
buah.unshift("Pepaya");
console.log(buah);
// Pepaya akan muncul di Array paling awal (index - 0)
```

![](./image/SS-js-array3.png)

- Method Pop <br/> Method pop() menghapus elemen terakhir dari array dan mengembalikan elemen tersebut.

```js
let buah = ["Jeruk", "Anggur", "Semangka"];
buah.push("Mangga");
buah.unshift("Pepaya");
// Method Pop
buah.pop(); // Mangga akan hilang dari Array
console.log(buah);
```

![](./image/SS-js-array4.png)

- Method Shift <br/> Method shift() menghapus elemen pertama dari array dan mengembalikan elemen yang dihapus.

```js
let buah = ["Jeruk", "Anggur", "Semangka"];
buah.push("Mangga");
buah.unshift("Pepaya");
// Method Pop
buah.pop(); // Mangga hilang dari Array
// Method Shift
buah.shift(); // Pepaya hilang dari Array
console.log(buah);
```

![](./image/SS-js-array5.png)

- Method Splice <br/> Method splice() mengubah konten array dengan menghapus atau mengganti elemen yang ada dan/atau menambahkan elemen baru di tempatnya.

```js
// Syntax Splice()
splice(start, deleteCount, item1);
```

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
buah.splice(2); // Splice akan menghapus data dari Index 2 keatas.
console.log(buah);
```

![](./image/SS-js-array6.png)

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
buah.splice(2, 1); // Splice hanya akan menghapus data dari Index ke 2 saja.
console.log(buah);
```

![](./image/SS-js-array7.png)

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
buah.splice(2, 1, "Kelapa"); // Splice akan menghapus data pada index 2 dan menggantinya menjadi Kelapa.
console.log(buah);
```

![](./image/SS-js-array9.png)

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
buah.splice(2, 0, "Kelapa"); // Splice akan menyisipkan data Kelapa pada index ke 2 tanpa menghapus index 2 yaitu Semangka.
console.log(buah);
```

![](./image/SS-js-array8.png)

- Method Slice <br/> Method slice() mengembalikan Shallow Copy (Mengambil data dan Mengcopy data tersebut) tanpa mengubah struktur Array.

```js
// Syntax Slice()
slice(start, end);
```

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
let slice = buah.slice(2, 5); // Slice akan mengambil data array dari index 3 sampai index 5.
console.log(slice);
```

![](./image/SS-js-array10.png)

- Method Sort <br/> Method sort() adalah Method untuk mengurutkan secara Ascending atau Descending Alphanumeric.

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
buah.sort(); // Sort akan mengurutkan sesuai dengan Alphabet.
console.log(buah);
```

![](./image/SS-js-array11.png)

```js
let angka = [1, 4, 2, 5, 9];
angka.sort(); // Sort akan mengurutkan sesuai dengan Numeric.
console.log(angka);
```

![](./image/SS-js-array12.png)

- Method Reverse <br/> Method Reverse() membalikkan urutan element dalam array akan berbalik ke arah yang berlawanan dengan yang dinyatakan sebelumnya.

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
buah.reverse(); // Reverse akan membalikkan urutan Array.
console.log(buah);
```

![](./image/SS-js-array13.png)

<b>Array Loop</b>

- For (Looping Classic)

```js
// Ascending
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
for (let i = 0; i < buah.length; i++) {
  console.log(buah[i]);
}

// Descending
for (let i = buah.length - 1; i >= 0; i--) {
  console.log(buah[i]);
}
```

![](./image/SS-js-array14.png)

- For of

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
for (let Buah of buah) {
  console.log(Buah);
}
```

![](./image/SS-js-array15.png)

- ForEach <br/> Method forEach() mengeksekusi fungsi yang disediakan satu kali untuk setiap elemen array.

```js
// Syntax
// Arrow function
forEach((element, index, array) => {
  /* … */
});
// Callback function
forEach(callbackFn, thisArg);
// Inline callback function
forEach(function (element, index, array) {
  /* … */
}, thisArg);
```

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
buah.forEach((item, index) => {
  console.log(index, item); // ForEach tidak bisa return.
});
```

![](./image/SS-js-array16.png)

- Map <br/>

```js
let buah = ["Jeruk", "Anggur", "Semangka", "Pepaya", "Mangga"];
let buahSegar = buah.map((item) => {
  return item + " " + "segar"; // Map dapat mengembalikan return
});
console.log(buahSegar);
```

![](./image/SS-js-array17.png)

<b>Array Multidimensional</b>

<p>Array Multidimensi itu Array di dalam array kayak gerbong kereta, didalam kereta terdapat ruang.</p>

```js
let multiarr = [
  ["Nama", "Sadewo"],
  ["Umur", 21],
  ["Hobi", "Rebahan"],
];
console.log(multiarr[0][1]); // Yang dipanggil adalah Gerbong pertama (index 0) dan Ruang kedua (index 1)
console.log(multiarr[2][1]); // Yang dipanggil adalah Gerbong ketiga (index 2) dan Ruang kedua (index 1)
```

![](./image/SS-js-array18.png)
