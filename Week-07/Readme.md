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

<p>Dari Output tersebut, link yang menuju about studen dan about teacher sudah ada, tetapi ketika kita klik hanya menampilkan halaman kosong. Hal ini dikarenakan kita belum menambahkan route about student dan about teacher pada App.jsx</p>

<p>App.jsx</p>

```jsx
import { Routes, Route, Link } from "react-router-dom";
import HomePage from "./pages/HomePage";
import AboutPage from "./pages/AboutPage";
import DetailPage from "./pages/DetailPage";
import AboutStudent from "./pages/AboutStudent";
import AboutSchool from "./pages/AboutSchool";
import AboutTeacher from "./pages/AboutTeacher";

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
        <Route path="/about" element={<AboutPage />}>
          <Route path="student" element={<AboutStudent />} />
          <Route path="teacher" element={<AboutTeacher />} />
          <Route index element={<AboutSchool />} />
        </Route>
      </Routes>
    </>
  );
};

export default App;
```

<p>Pada Codingan diatas, saya membuat parent route dengan index defaultnya AboutSchool. Jika kita mengklik link about, maka akan langsung ke halaman AboutSchool dengan menambahkan outlet pada file AboutPage.jsx</p>

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

peran `<Outlet/>` mirip dengan `<children/>`, bedanya hasil render dari `<Outlet/>` ini akan dinamis berdasarkan path URL yang terdaftar. dari contoh diatas, terdapat Route parent dengan path='/about' yang memiliki children dengan path='student' dan path='teacher', `<Outlet/>` akan merender children tersebut sebagai `<AboutPage />` saat akses URL-nya /student (/ sebagai parent + student sebagai children), dan akan merender `<DashboardTasks />` saat akses URL-nya /teacher (/ sebagai parent + teacher sebagai children). nah pada kali ini saya memberikan AboutSchool sebagai index. maka yang akan dirender ketika mengklik about adalah AboutSchool.

<p>Output</p>

<p><img src="./gif/gif-route2.gif"></p>

<p>Berikutnya kita akan membuat DetailPage.jsx. Fungsi dari DetailPage.jsx adalah ketika kita mengklik button detail pada HomePage.jsx, Data yang berupa ID dari HomePage.jsx akan ditampilkan pada DetailPage.jsx</p>

<p>Jika kita menekan salah satu dari 3 button yang ada, jika menekan button yang bernama Sadewo, maka handleDetail akan memanggil data yang berada di file DetailPage.jsx dan menampilkannya.</p>

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

<p>Output</p>

<p><img src="./gif/gif-route.gif"></p>

<p><b>Note : </b>Pada DetailPage.jsx,saya menggunakan useParams untuk menangkap id yang kita kirim dari halaman home dengan mencocokkan data yang dikirim dari home dan melakukan Mapping data untuk menampilkan hasil yang sesuai dari data filter.</p>

# Day 3 & 4: State Management React Redux

<p>State management library adalah library yang digunakan untuk mengelola state pada suatu aplikasi JavaScript.</p>

<b>Kenapa kita menggunakan Redix ? </b>

<p>Redux akan mempermudah dalam mengelola state dimana mengubah state di child-child component tanpa harus membuat bantuan dengan props didalam component didalam props component. Dalam hal ini, redux menggunakan state yang bisa dishare diseluruh aplikasi, menggunakan middleware.</p>

<b>Bagaimana cara kerja Redux ? </b>

![](./image/SS-redux.png)

<p>Alur kerja Redux : </p>

1. Pertama akan ada triger dari UI
2. Kemudian akan ke action
3. Dari action reducer akan mengubah state yang sesuai dengan
4. type dari action tadi
5. Terahir update UI lagi

<p>Terdapat 4 Faktor Utama : </p>

1. UI (Tampilan Website / Aplikasi)
2. Action <br/>Sebuah function yang mereturn sebuah objek. Objek tersebut memiliki sebuah property wajib yaitu type. Type inilah yang menentukan bagaimana statenya akan diubah.
3. Reducer <br/> Sebuah function yang tugasnya untuk mengolah state yang ada di store. Misal menambah data, menghapus data, mengambil data, dsb. Ada 2 parameter wajib dari reducer, yaitu state dan action.
4. Store <br/> Store adalah tempat untuk menampung state. Store dalam Front-End dibilang sebagai database untuk Front-End.

<b>Install React Redux</b>

<p>Sebelum menggunakan Redux, kita diwajibkan menginstall terlebih dahulu. Pastika kita menggunakan React versi 16.8.3 keatas, karena versi tersebut yang support dengan React Redux 8.x.</p>

<p>Untuk Installasinya mirip dengan react router, kita hanya memasukkan command 'npm install redux react-redux' kedalam terminal.</p>

![](./image/SS-redux2.png)

<p>Setelah selesai menginstall, cek kembali apakah sudah terpasang dengan membuka file package.json.</p>

![](./image/SS-redux3.png)

<b>Membuat React Redux dengan Contoh Kasus Counter</b>

<p>Yang pertama saya lakukan adalah membuat components terlebih dahulu.</p>

![](./image/SS-redux4.png)

<p>Selanjutnya saya akan membuat komponen Redux</p>
