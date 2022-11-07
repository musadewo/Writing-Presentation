# Day 1 : React. JS Lanjutan - Proptypes

<p>PropTypes merupakan library untuk menvalidasi props. Ini sangat membantu dalam meminimalkan bugs saat mengembangkan App besar. Jika props tidak benar type nya maka akan muncul warning. <br/>
Pada React PropTypes sudah tidak jadi 1 library dengan React sejak versi 15.5, karena hal itu kita diwajibkan menginstall terlebih dahulu library React PropTypes sebelum digunakan.</p>

<b>Install React PropTypes</b>

<p>Untuk installasinya terbilang cukup mudah, hanya perlu memasukkan perintah 'npm install prop-types' Pada Command Prompt dan tunggu hingga proses installasinya selesai.</p>

```npm
npm install prop-types
```

![](./image/SS-pt.png)

<p>Setelah berhasil terinstall, cek kembali pada package.json</p>

![](./image/SS-pt2.png)

<b>Contoh penggunaan Prop-Types</b>

<p>Disini saya akan membuat contoh program sederhana mengenai PropTypes. Jadi saya akan membuat 1 file bernama Studentsinfo.jsx yang berada didalam folder components dan dipanggil di app.jsx</p>

<p>Studentsinfo.jsx</p>

```jsx
const Studentsinfo = ({ name, age }) => {
  return (
    <div>
      <h2>{name}</h2>
      <h2>{age + 5}</h2>
    </div>
  );
};

export default Studentsinfo;
```

<p>App.jsx</p>

```jsx
import Studentsinfo from "./components/studentsinfo";

function App() {
  return (
    <div className="App">
      <h1>Belajar PropTypes</h1>
      <Studentsinfo name={"Sadewo"} age={"20"} />
    </div>
  );
}

export default App;
```

<p>Output</p>

![](./image/SS-pt3.png)

<p>Kenapa pada output untuk Age yang ditampilkan 205 ? Karena yang kita masukkan di dalam Prop App.jsx itu adalah tipe data String (" "). Disini kegunaan dari Prop-Types, Prop-Types akan mendeteksi tipe data yang digunakan untuk mempermudah proses debugging.</p>

<p>Studentsinfo.jsx</p>

```jsx
import PropTypes from "prop-types";

const Studentsinfo = ({ name, age }) => {
  return (
    <div>
      <h2>{name}</h2>
      <h2>{age + 5}</h2>
    </div>
  );
};

Studentsinfo.propTypes = {
  name: PropTypes.string,
  age: PropTypes.number,
};

export default Studentsinfo;
```

<p>Output</p>

![](./image/SS-pt5.png)

<p>Pada Output diatas kita tahu bahawa Invalid prop `age` of type `string` supplied to `Studentsinfo`, expected `number`. Yang artinya tipe data yang digunakan pada age adalah number bukan string.</p>

<p>Bagaimana cara memperbaikinya ? Cara memperbaikinya adalah mengedit kembali age prop pada App.jsx dengan menghilangkan kutip 2 (" ")</p>

```jsx
import Studentsinfo from "./components/studentsinfo";

function App() {
  return (
    <div className="App">
      <h1>Belajar PropTypes</h1>
      <Studentsinfo name={"Sadewo"} age={20} />
    </div>
  );
}

export default App;
```

<p>Output</p>

![](./image/SS-pt6.png)

<p>Maka Warning akan hilang dari console.</p>

<p>Pada Prop-Types terdapat banyak validasi data, seperti string, number, boolean dan lain - lain.</p>

1. Type data string. <br/>
   ```jsx
   name: PropTypes.string,
   ```
2. Type data number. <br/>
   ```jsx
   age: PropTypes.number,
   ```
3. Type data bebas. <br/>
   ```jsx
   name: PropTypes.any,
   ```
4. Type data array. <br/>
   ```jsx
   data: PropTypes.array,
   ```
5. Type data object. <br/>
   ```jsx
   data: PropTypes.object,
   ```
6. Opsi pada type data. <br/>
   ```jsx
   name: PropTypes.oneOfType([PropTypes.string, PropTypes.number]),
   ```
7. Mengecek value dari props. <br/>
   ```jsx
   data: PropTypes.arrayOf(PropTypes.number),
   ```
8. Mengecek nilai dari object. <br/>
   ```jsx
   info: PropTypes.shape({
       nama: PropTypes.string,
       age: PropTypes.number,
   }),
   ```
9. Function isRequired. <br/>Fungsi isRequired artinya data harus ada. <br/>
   ```jsx
   name: PropTypes.string.isRequired,
   ```

# Day 2 : React Router

<p>Routing adalah proses di mana pengguna diarahkan ke halaman yang berbeda berdasarkan tindakan atau permintaan mereka. Router ReactJS terutama digunakan untuk mengembangkan Aplikasi Web Halaman Tunggal. React Router digunakan untuk menentukan beberapa rute dalam aplikasi. Saat pengguna mengetik URL tertentu ke browser, dan jika jalur URL ini cocok dengan ‘rute’ apa pun di dalam file router, pengguna akan diarahkan ke rute tersebut.</p>

<p>Sebelum menggunakan React Router, kita diharuskan menginstall terlebih dahulu library Router-Dom.</p>

<b>Install React-Router-Dom</b>

<p>Untuk installasi kita hanya perlu memasukkan command 'npm install react-router-dom' pada terminal dan menunggu hingga proses selesai.</p>

![](./image/SS-router.png)

<p>Setelah selesai menginstall, cek kembali apakah sudah terpasang dengan membuka file package.json.</p>

![](./image/SS-router2.png)

<b>Configurasi main.jsx</b>

- BrowserRoute <br/>BrowserRoute adalah Langkah termudah untuk mengatur router. Yang perlu kita lakukan adalah mengimpor router spesifik yang dibutuhkan dan bungkus seluruh aplikasi di router itu. <br/>
  ```jsx
  import React from "react";
  import ReactDOM from "react-dom/client";
  import App from "./App";
  import { BrowserRouter } from "react-router-dom";
  ReactDOM.createRoot(document.getElementById("root")).render(
    <BrowserRouter>
      <App />
    </BrowserRouter>
  );
  ```

<b>Penggunaan Route</b>

<p>Jika kita ingin membuat route, maka kita perlu page untuk berpindah halaman. Disini saya akan menyiapkan 3 file page bernama HomePage.jsx, AboutPage.jsx, dan DetailPage.jsx</p>

<p>App.jsx</p>

```jsx
import { Routes, Route, Link } from "react-router-dom";
import HomePage from "./pages/HomePage";
import AboutPage from "./pages/AboutPage";
import DetailPage from "./pages/DetailPage";

const App = () => {
  return (
    <>
      <nav>
        <Link to={"/"}>Home</Link>
        <Link to={"/about"}>About</Link>
        <Link to={"/detail"}>Detail</Link>
      </nav>

      <Routes>
        <Route path="/" element={<HomePage />} />
        <Route path="/detail/:id" element={<DetailPage />} />
        <Route path="/about" element={<AboutPage />}></Route>
      </Routes>
    </>
  );
};

export default App;
```

<p>HomePage.jsx</p>

```jsx
import { useNavigate, Link } from "react-router-dom";

const HomePage = () => {
  const navigation = useNavigate();
  let data = [
    {
      id: 1,
      nama: "Sadewo",
    },
    {
      id: 2,
      nama: "Dira",
    },
    {
      id: 3,
      nama: "Zahra",
    },
  ];

  const handleDetail = (id) => {
    navigation(`/detail/${id}`);
  };

  return (
    <>
      <h1>Home</h1>

      {data.map((el) => {
        return (
          <div>
            <h2>Nama : {el.nama}</h2>
            <button onClick={() => handleDetail(el.id)}>detail</button>
          </div>
        );
      })}

      <Link to={"about/student"}>About Student</Link>
      <Link to={"about/teacher"}>About Teacher</Link>
    </>
  );
};
export default HomePage;
```

<p><b>Note : </b>Pada HomePage.jsx, saya menggunakan useNavigate agar bisa digunakan pada function handleDetail, dan const handleDetail berfungsi untuk pindah halaman ke page detail sekaligus membawa id params.</p>

<p>Output</p>

![](./image/SS-router3.png)

<p>Dari Output tersebut, link yang menuju about studen dan about teacher sudah ada, tetapi ketika kita klik hanya menampilkan halaman kosong. Hal ini dikarenakan kita belum menambahkan route about student dan about teacher pada app.jsx</p>

<p>App.jsx</p>

<p>DetailPage.jsx</p>

```jsx
import { useParams } from "react-router-dom";

const DetailPage = () => {
  const { id } = useParams();
  console.log(id);

  const detailInfo = [
    {
      id: 1,
      name: "Sadewo",
      address: "Jakarta",
      hobby: "Membaca",
    },
    {
      id: 2,
      name: "Dira",
      address: "Bogor",
      hobby: "Melukis",
    },
    {
      id: 3,
      name: "Zahra",
      address: "Depok",
      hobby: "Menggambar",
    },
  ];

  return (
    <>
      {detailInfo
        .filter((el) => el.id === +id)
        .map((el) => {
          return (
            <div key={el.id}>
              <h2>Name: {el.name}</h2>
              <h2>Address: {el.address}</h2>
              <h2>Hobby: {el.hobby}</h2>
            </div>
          );
        })}
    </>
  );
};

export default DetailPage;
```

<p>AboutPage.jsx</p>

```jsx
import { Outlet, Link } from "react-router-dom";

const AboutPage = () => {
  return (
    <>
      <Outlet />
      <Link to={"student"}>About Student |</Link>
      <Link to={"teacher"}>About Teacher</Link>
    </>
  );
};

export default AboutPage;
```

<p>Jika kita menekan salah satu dari 3 button yang ada, jika menekan button yang bernama Sadewo, maka handleDetail akan memanggil data yang berada di file DetailPage.jsx dan menampilkannya.</p>

<p>Output</p>

<p><img src="./gif/gif-route.gif"></p>

<p><b>Note : </b>Pada DetailPage.jsx,saya menggunakan useParams untuk menangkap id yang kita kirim dari halaman home dengan mencocokkan data yang dikirim dari home dan melakukan Mapping data untuk menampilkan hasil yang sesuai dari data filter.</p>

<b>Membuat Route</b>
