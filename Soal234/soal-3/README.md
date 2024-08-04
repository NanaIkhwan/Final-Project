### Penjelasan Fungsi

**Fungsi `printTriangle(height)`**:
- **Parameter `height`**: Merupakan tinggi segitiga yang akan dicetak. Nilai ini menentukan berapa banyak baris yang akan dicetak.

#### Cara Kerja:
1. **Loop Baris**: 
   - Loop pertama (`for (let i = 1; i <= height; i++)`) iterasi dari 1 hingga `height`, di mana `i` merepresentasikan nomor baris saat ini.

2. **Membuat Baris**:
   - Di dalam loop baris, variabel `row` diinisialisasi sebagai string kosong. Variabel ini akan menyimpan string yang merepresentasikan baris saat ini.
   - Loop kedua (`for (let j = 1; j <= i; j++)`) iterasi dari 1 hingga `i`, di mana `j` digunakan untuk menambahkan karakter `*` ke string `row`.

3. **Mencetak Baris**:
   - Setelah loop dalam baris selesai, `row` berisi string yang diisi dengan `*` sebanyak `i` kali. Fungsi `console.log(row)` digunakan untuk mencetak baris ke konsol.

### Contoh Keluaran

Jika `height` adalah 5, maka output dari fungsi ini akan berupa:

```
*
**
***
****
*****
```

### Kode Lengkap

Berikut adalah kode lengkap dari fungsi `printTriangle(height)`:

```javascript
function printTriangle(height) {
    for (let i = 1; i <= height; i++) {
        let row = '';
        for (let j = 1; j <= i; j++) {
            row += '*';
        }
        console.log(row);
    }
}

printTriangle(10);
```

**Cara Menjalankan Kode**:
1. **Di Browser**: Tempelkan kode ke konsol JavaScript di developer tools di browser.
2. **Di Node.js**: Simpan kode dalam file JavaScript (misalnya `triangle.js`) dan jalankan dengan perintah `node triangle.js`.

### Penjelasan Output

- **Baris Pertama**: `*` - Satu karakter `*`.
- **Baris Kedua**: `**` - Dua karakter `*`.
- **Baris Ketiga**: `***` - Tiga karakter `*`.
- Dan seterusnya, hingga mencapai jumlah `height` karakter `*` pada baris terakhir.
