# Day 1 : React.js Basic - JavaScript for React.js dan React.js Basic - Intro to React.js, Virtual DOM, and JSX

## React.Js

<p>React.Js adalah Framework view library javascript untuk membuat tampilan (user interface) pada website. React memungkinkan untuk membuat UI kompleks dari kumpulan kode yang kecil dan terisolasi yang disebut “komponen”.
</p>

<b>Kenapa menggunakan React.js?</b>

1. Performa <br/>React.JS menggunakan kerangka Virtual Document Object Model (VDOM) yang membuat aplikasi web berjalan lebih cepat. Dengan kerangka ini, antarmuka pengguna <b>(UI)</b> yang kompleks dapat dipecah menjadi beberapa komponen. Dengan begitu, proses pengembangan bisa berjalan lebih cepat karena memungkinkan banyak pengguna bekerja pada komponen secara bersamaan.
2. Modular <br/>Dengan React dapat menerapkan konsep modular pada Javascript. React JS membagi 1 tampilan website menjadi komponen-komponen kecil.
3. Scalable <br/>React.JS dapat digunakan pada aplikasi berskara kecil hingga besar dan kompleks.
4. Popular <br/>React.Js dikenal dengan library JavaScript yang berbasis Komponen yang dapat membantu Developer dalam pembuatan Website atau Aplikasi Mobile. Karena hal itu React.Js sangat populer di kalangan Developer.

<b>Install React.Js</b>

1. Download Node.js <br/>Link download : https://nodejs.org. Node.js menjalankan V8 JavaScript engine (yang juga merupakan inti dari Google Chrome) di luar browser. Ini memungkinkan Node.js memiliki performa yang tinggi.
2. Install Node.Js <br/> Untuk proses Installasinya hanya klik next saja, lalu diakhir klik finish.
3. Mengecek Node.Js <br/>Untuk memastikkan Node.Js telah terinstall dengan baik, maka buka cmd dan ketikan 'npm -v'. <br/> ![](./image/SS-Node.js.png)
4. Install create-react-app <br/>Sebelum menginstall React.js kita harus menginstall Create-react-app terlebih dahulu dengan GitBash / PowerShell dan mengetikkan 'npm install -g create-react-app'. <br/>![](./image/SS-Node.js2.png)
5. Mengecek create-react-app <br/>Untuk memastikkan create-react-app telah terinstall dengan baik, maka buka cmd dan ketikan 'create-react-app --version'. <br/> ![](./image/SS-Node.js3.png)
6. Create Project React.Js <br/>Untuk membuat Project kita memerlukan CMD, PowerShell atau Git Bash, dan mengetikkan 'create-react-app nama-project'. Pada Proses Create memakan kuota dan waktu untuk mendownload. <br/> ![](./image/SS-Node.js4.png) <br/> Gambar dibawah menandakan bahwa Proses Create telah selesai <br/> ![](./image/SS-Node.js5.png)
7. Menjalankan React.js <br/> Setelah proses Create Project selesai, ketikkan 'cd nama-project' untuk berpindah kedalam project yang dibuat, dan npm start untuk memulai / menjalankan React.js di browser. <br/>![](./image/SS-Node.js6.png) <br/> ![](./image/SS-Node.js7.png) <br/> ![](./image/SS-Node.js8.png)
8. Membuka di Browser <br/>Biasanya ketika menjalankan 'npm start' akan secara otomatis langsung membuka di Browser. Jika tidak secara otomatis terbuka di Browser, ketikan http://localhost:3000/ pada Browser. <br/> ![](./image/SS-Node.js9.png)

## Virtual Document Object Model (VDOM)

<p>Virtual DOM (VDOM) adalah sebuah konsep dalam pemrograman di mana representasi ideal atau “virtual” dari antarmuka pengguna disimpan dalam memori dan disinkronkan dengan DOM “yang sebenarnya” oleh library seperti ReactDOM.</p>
<p>Virtual DOM secara singkat nya adalah sebuah javascript object (virtual) yang merepresentasikan DOM yang sebenarnya (real DOM). karena virtual dom ini adalah representasi dari real dom maka virtual dom adalah sebuah replikasi (copy) dari real dom tersebut. Berbeda konsep dengan DOM, virtual dom ini memiliki konsep yaitu setiap saat perubahan terjadi di state pada aplikasi kita maka akan membuat virtual dom yang baru (cloning).</p>

![](./image/SS-vdom.png)

<p>Pada gambar diatas, ketika ada perubahan maka virtual dom akan membuat virtual dom baru dan melakukan comparation (diffed) dari virtual dom sebelumnya. Hanya perubahan tersebut yang akan dikirim ke real dom untuk mengupdate nya. Proses seperti ini membuat virtual DOM lebih cepat dibandingkan dengan DOM, jadi tidak perlu adanya proses re-rendering lagi pada keseluruhan DOM.</p>

![](./image/SS-vdom2.png)

<p>Pada React, setiap bagian dari UI adalah component, dan setiap component mempunyai state. React menggunakan konsep Observable Pattern dan mengamati setiap perubahan pada state. Ketika state pada sebuah component berubah, react mengupadate virtual DOM tree. Setelah virtual DOM diperbarui, React kemudian membandingkan versi sekarang virtual DOM dengan versi sebelumnya. Proses ini sering disebut dengan “diffing”. Setelah mengetahui object pada virtual DOM mana yang berubah maka hanya object tersebutlah yang akan dirubah pada real DOM. Proses seperti membuat performance aplikasi menjadi lebih baik.</p>

## JSX

<p>JSX merupakan singkatan dari JavaScript Syntax Extension atau dikenal juga dengan Javascript XML. <br/>
JSX adalah ekstensi React untuk Javasript. Sintaks JSX mirip seperti HTML, sehingga membuat kita lebih gampang menyusun elemen pada komponen React. <br/>
JSX perlu di compile untuk menjadi Javascript. Jadi sebelum ditampilkan pada browser, JSX akan dicompile menjadi javascipt terlebih dahulu. Dengan JSX kita dapat menggunakan HTML didalam file extension (.js/.jsx)</p>

<p>file .js</p>

![](./image/SS-jsx.png)

<p>file .jsx</p>

![](./image/SS-jsx2.png)

<p>Setiap JSX hanya memiliki 1 parent element</p>

![](./image/SS-jsx3.png)

<p>Bahkan sebelum kita run / lihat pada Browser, Code Editor telah memperingatkan bahwa JSX hanya memiliki 1 parent element saja.</p>

<p>Bagaimana jika kita ingin membuat lebih dari 1 parent atau lebih ? Solusinya bisa menggunakan tag div dan tag fragment.</p>

- Menggunakan Tag div <br/>

  ```jsx
  import React from "react";
  function App() {
    return (
      <div>
        <h1>Hallo World!</h1>
        <h2>Sadewo</h2>
      </div>
    );
  }
  export default App;
  ```

- Menggunakan Tag Fragment <br/>
  ```jsx
  import React from "react";
  function App() {
    return (
      <>
        <h1>Hallo World!</h1>
        <h2>Sadewo</h2>
      </>
    );
  }
  export default App;
  ```

<p>Hasil atau Output yang ditampilkan pada Browser : </p>

![](./image/SS-jsx4.png)
