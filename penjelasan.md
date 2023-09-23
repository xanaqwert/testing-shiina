# Kodingan

## Ringkasan

Shiina.js adalah sebuah fungsi JavaScript yang menangani pengiriman formulir dan menampilkan percakapan chat antara user dan shiina. Ini mencakup fungsi untuk menampilkan indikator loading, animasi, menghasilkan unique ID, dan membuat garis pada chat.

## Contoh kodingan

```javascript
import bot from "./assets/bot.svg";
import user from "./assets/user.svg";

const form = document.querySelector("form");
const chatContainer = document.querySelector("#chat_container");

// ...

form.addEventListener("submit", handleSubmit);
form.addEventListener("keyup", (e) => {
  if (e.keyCode === 13) {
    handleSubmit(e);
  }
});
```

## Analisis kodingan

### Input

- Elemen formulir dan elemen kontainer chat dipilih menggunakan `document.querySelector`.
- Input dari pengguna diperoleh dari formulir menggunakan `FormData` dan nilai dari field "prompt".

---

### Alur/Flow

1. When the form is submitted or the enter key is pressed, the `handleSubmit` function is called.
2. The user's input is extracted from the form using `FormData`.
3. The user's chat stripe is displayed in the chat container.
4. The form input is cleared.
5. A unique ID is generated for the bot's chat stripe.
6. The bot's chat stripe is displayed in the chat container.
7. The chat container is scrolled to the bottom.
8. The loading indicator is displayed in the bot's chat stripe.
9. A request is made to a server endpoint with the user's input as the payload.
10. The loading indicator is cleared.
11. If the response is successful, the bot's response is displayed with a typing effect.
12. If the response is not successful, an error message is displayed.

### Indonesia

    Ketika formulir dikirimkan atau tombol "enter" ditekan, fungsi handleSubmit dipanggil.
    Input dari pengguna diekstraksi dari formulir menggunakan FormData.
    Garis chat pengguna ditampilkan dalam kontainer chat.
    Input formulir dikosongkan.
    ID unik dibuat untuk garis chat bot.
    Garis chat bot ditampilkan dalam kontainer chat.
    Kontainer chat digulirkan ke bagian bawah.
    Indikator loading ditampilkan dalam garis chat bot.
    Permintaan dikirimkan ke titik akhir server dengan input pengguna sebagai payload.
    Indikator loading dihapus.
    Jika tanggapan berhasil, tanggapan dari bot ditampilkan dengan efek mengetik.
    Jika tanggapan tidak berhasil, pesan kesalahan ditampilkan.

---

### Outputs

- The chat conversation between the user and the bot is displayed in the chat container.
- The bot's responses are displayed with a typing effect.

### Indonesia

    Percakapan chat antara pengguna dan bot ditampilkan dalam kontainer chat.
    Tanggapan dari bot ditampilkan dengan efek mengetik.

---
