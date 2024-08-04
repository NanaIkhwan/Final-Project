# Program Lirik Lagu

## Deskripsi

Program ini mengelola data lirik lagu dalam format objek JavaScript. Program ini menyertakan data asli tentang lagu dan artis, serta memodifikasi objek tersebut untuk memperbarui informasi lagu. Data awal berisi informasi seperti nama artis, judul lagu, dan liriknya. Modifikasi dilakukan dengan menyebarkan data awal ke objek baru dan memperbarui beberapa nilai.

## Struktur Kode

### 1. Data Awal (`lirik_lagu`)

Objek `lirik_lagu` berisi informasi berikut:

- **`status`**: Boolean yang menunjukkan status data. 
- **`data`**: Objek yang berisi informasi rinci tentang lagu.
  - **`artist`**: Nama artis (Awalnya "Avenged Sevenfold").
  - **`songTitle`**: Judul lagu (Awalnya "Little Piece of Heaven").
  - **`songLyrics`**: Lirik lagu dalam format string panjang.
  - **`songLyricsArr`**: Lirik lagu yang dipecah menjadi array string, setiap baris lirik adalah elemen array.

Contoh data:
```javascript
let lirik_lagu = {
  "status": true,
  "data": {
      "artist": "Avenged Sevenfold",
      "songTitle": "Little Piece of Heaven",
      "songLyrics": "Before the story begins, is it such a sin\nFor me to take what's mine, until the end of time?...",
      "songLyricsArr": [
          "Before the story begins, is it such a sin",
          "For me to take what's mine, until the end of time?",
          ...
      ]
  }
};
```

### 2. Modifikasi Data (`newLirikLagu`)

Objek `newLirikLagu` dibuat dengan menggunakan operator spread (`...`) untuk menduplikasi `lirik_lagu` dan memperbarui beberapa atribut:

- **`artist`**: Diperbarui menjadi "Najwa Ikhwan Maulana".
- **`songTitle`**: Diperbarui menjadi "Masinis".

Kode:
```javascript
let newLirikLagu = {
  ...lirik_lagu,
  data: {
      ...lirik_lagu.data,
      artist: "Najwa Ikhwan Maulana",
      songTitle: "Masinis"
  }
};
```

### 3. Output ke Console

Modifikasi objek `newLirikLagu` dicetak ke console menggunakan `console.log()` untuk menampilkan hasil akhir.

```javascript
console.log(newLirikLagu);
```

## Cara Menggunakan

1. **Salin Kode**:
   - Salin kode JavaScript yang disediakan ke dalam file `.js` (misalnya `lirikLagu.js`).

2. **Jalankan Kode**:
   - Buka file JavaScript di editor teks atau IDE.
   - Jalankan file menggunakan lingkungan pengembangan JavaScript seperti Node.js, atau di konsol browser.

3. **Lihat Hasil**:
   - Periksa hasil yang dicetak ke console untuk melihat objek `newLirikLagu` yang telah dimodifikasi.

## Prerequisites

- **Browser Modern** atau **Node.js**:
  - Untuk menjalankan kode JavaScript dan melihat output.
