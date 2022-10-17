# Day 1 : JS Intermediate Asynchronous Fetch & Async Await

## JS Intermediate Asynchronous Fetch

<p>Fetch adalah proses untuk mengakses dan memanipulasi protokol server. Fetch melakukan permintaan / request terhadap server berupa API, server mengirim ke database, kembali lagi keserver dan diberikan ke website berupa data JSON untuk ditampilkan.</p>

<p>Fetch menggantikan XMLHttpRequst untuk proses request.</p>

```js
// Bentuk umum fetch
fetch("http://example.com/movies.json") // Fetch mengambil data / Request data dari Link.
  .then((response) => response.json()) // Setelah data diterima, kemudian diubah / diekstrak data tersebut menjadi data Array of Object agar dapat terbaca.
  .then((data) => console.log(data)); // Yang terakhir menampilkannya di Console.log.
```

```js
// Demo fetch 1
// Short Syntax (promise) fetch
fetch("https://digimon-api.vercel.app/api/digimon") // Fetch mengirim Request ke Server.
  // .then menangkap Request tersebut dan merubahnya menjadi Array of Obejct menggunakan .json().
  .then((result) => result.json())
  // Selanjutnya menampilkan data tersebut di console.log.
  .then((result) => {
    console.log(result);
  });
```

![](./image/SS-fetch.png)

```js
// Demo fetch 2
// async await fetch
let fetchdata = async () => {
  let response = await fetch("https://digimon-api.vercel.app/api/digimon");
  let result = await response.json();
  console.log(result);
};
fetchdata();
```

![](./image/SS-fetch2.png)

```html
// Demo fetch 3 // Menampilkan data dengan async await + ForEach // File
index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>

    <script src="script.js" defer></script>
  </head>
  <body>
    <div id="list-data"></div>
  </body>
</html>
```

```js
// File script.js
listData = document.getElementById("list-data");

let fetchdata = async () => {
  let URL = "https://digimon-api.vercel.app/api/digimon";
  let response = await fetch(URL);
  let data = await response.json();
  console.log(data);

  // menampilkan 5 data
  data.slice(0, 5).forEach((item, index) => {
    listData.innerHTML += `<div>
        <img src="${item.img}" alt="" width="200">
        <h3>${item.name}</h3>
      </div>`;
  });
};

fetchdata();
```

![](./image/SS-fetch3.png)

## JS Intermediate Asynchronous Async Await

<p>Async Await adalah proses untuk menangkap API dan merubahnya menjadi JSON agar dapat terbaca oleh JavaScript.</p>

<p>Pada Async Await terdapat 2 model function yang dapat digunakan : </p>

```js
// async function
// async terletak pada depan function
async function asyncawait() {
  // isi function
}

// async arrow
// async terletak setelah function / depan parameter
let asyncawait = async () => {
  // isi function
};
```

```js
// Demo Async Await dengan Async Function
let pergi = (kondisi) => {
  return new Promise((resolve, reject) => {
    if (kondisi == "jalan") {
      resolve("Jalan");
    }
    reject("Ga Jadi");
  });
};

async function asyncjalan() {
  // try catch berfungsi untuk handler error.
  try {
    let result = await pergi("jalan"); // pada asycn function, tidak memerlukan .then pada functionnya.
    console.log(result);
  } catch (error) {
    console.log(error);
  }
}
asyncjalan();
```

![](./image/SS-await.png)

# Day 2 : Git & Github Lanjutan
