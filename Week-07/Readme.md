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
       hobby: PropTypes.string,
       class: PropTypes.number,
   }),
   ```
9. Function isRequired. <br/>Fungsi isRequired artinya data harus ada. <br/>
   ```jsx
   name: PropTypes.string.isRequired,
   ```
