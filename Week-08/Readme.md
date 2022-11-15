# Day 1 : React Context

<p><b>Context</b> membuat kita bisa mengirim data dari satu component ke component lain baik itu parent, child atau sibling component tanpa harus menambahkan props di setiap component yang 'dilewati'.</p>

<p>Kenapa dibuat Context ? kan kita bisa menggunakan props. Karena Context dapat menghindari masalah seperti props drilling.</p>

<p>Context berbeda dengan Redux. Redux state management data dalam 1 tempat, sedangkan Context bukan state management, Context hanya membuat data state yang diinginkan bersifat global agar dapat digunakan oleh component lain.</p>

<b>Penjelasan props drilling.</b>

<p>Semisalnya dalam sebuah React App memiliki beberapa Component seperti gambar dibawah.</p>

![](./image/SS-context.png)

<p>Jika kita ingin mengirim data dari component A ke component E, maka kita harus menambahkan props di component C dan D dan manambahkan props lagi di component D dan E. Yang membuat kita diharuskan membuat props disetiap component yang dilewati. Yang akan menyebabkan props drilling..</p>

![](./image/SS-context2.png)

<p>Hal tersebut tidak akan terjadi jika React App hanya memiliki sedikit component.</p>

<b>Contoh penggunaan React Context</b>

<p>Saya akan membuat Program sederhana menggunakan Context. Saya akan membuat folder context, didalam folder context terdapat file bernama UserProvider.jsx, di file tersebut state disimpan dan menunggu dipanggil.</p>

<p>UserProvider.jsx</p>

```jsx
import React, { createContext, useState } from "react";

export const UserContext = createContext();

function UserProvider({ children }) {
  const [user, setUser] = useState({
    name: "Sadewo",
    email: "dewo@gmail.com"
  })

  return (
    // Value akan berisikan data berupa object
    <UserContext.Provider value={{ user, setUser }}>
      {children}
    </UserContext.Provider>
  )
}

export default UserProvider;
```

<p>Setelah membuat file UserProvider.jsx, selanjutnya mengedit file App.jsx dan Main.jsx.</p>

<p>App.jsx</p>

```jsx
// Import useContext dari react dan UserContext dari UserProvider.
import { useContext } from "react";
import { UserContext } from "./context/UserProvider";

function App() {
    // Destructur dan yang kita ambil hanya data user saja
    const { user } = useContext(UserContext);

  return (
    <div className="App">
    {/* Memanggil const user dan data yang diinginkan */}
      <h1>{user.name}</h1>
      <h2>{user.email}</h2>
    </div>
  );
}

export default App;
```

<p>Main.jsx</p>

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
// Impoer UserProvider dari UserProvider
import UserProvider from "./context/UserProvider";

ReactDOM.createRoot(document.getElementById("root")).render(
    // Memanggil UserProvider
  <UserProvider>
  <App />
  </UserProvider>
);
```

<p>Output</p>

![](./image/SS-context3.png)

# Day 2 : React Context with useReducer

# Day 3 : React Testing (Jest & RTL)
