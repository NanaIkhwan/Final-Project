### Penjelasan Kode JavaScript

Berikut adalah penjelasan mendetail untuk kode JavaScript yang Anda berikan:

```javascript
"use strict";

function getGrade(score) {
    if (score >= 90 && score <= 100)
        return 'A';
    if (score >= 80 && score < 90)
        return 'B';
    if (score >= 70 && score < 80)
        return 'C';
    if (score >= 60 && score < 70)
        return 'D';
    return 'E';
}

function calculateAverageAndGrade(webProgramming, computerProgramming, statistics, databaseSystems) {
    const average = (webProgramming + computerProgramming + statistics + databaseSystems) / 4;
    const grade = getGrade(average);
    return { average, grade };
}

try {
    const webProgramming = 85;
    const computerProgramming = 90;
    const statistics = 78;
    const databaseSystems = 88;
    const result = calculateAverageAndGrade(webProgramming, computerProgramming, statistics, databaseSystems);
    console.log(`Average: ${result.average.toFixed(2)}`);
    console.log(`Grade: ${result.grade}`);
}
catch (error) {
    console.error(error.message);
}
```

### Penjelasan Fungsional

1. **`"use strict";`**
   - Perintah ini mengaktifkan mode ketat (strict mode) di JavaScript, yang membantu dalam menangkap kesalahan dan mempromosikan praktik coding yang lebih baik.

2. **Fungsi `getGrade(score)`**
   - **Input**: `score` (angka antara 0 hingga 100).
   - **Output**: Huruf nilai berdasarkan rentang nilai.
   - **Logika**:
     - Mengembalikan `'A'` untuk nilai antara 90 hingga 100.
     - Mengembalikan `'B'` untuk nilai antara 80 hingga kurang dari 90.
     - Mengembalikan `'C'` untuk nilai antara 70 hingga kurang dari 80.
     - Mengembalikan `'D'` untuk nilai antara 60 hingga kurang dari 70.
     - Mengembalikan `'E'` untuk nilai kurang dari 60.

3. **Fungsi `calculateAverageAndGrade(webProgramming, computerProgramming, statistics, databaseSystems)`**
   - **Input**: Empat parameter yang masing-masing mewakili nilai dari mata pelajaran.
   - **Output**: Objek yang berisi `average` dan `grade`.
   - **Logika**:
     - Menghitung rata-rata dari keempat nilai.
     - Menggunakan fungsi `getGrade` untuk menentukan huruf nilai berdasarkan rata-rata.
     - Mengembalikan objek yang berisi rata-rata (`average`) dan nilai huruf (`grade`).

4. **Blok `try...catch`**
   - **`try`**:
     - Menginisialisasi nilai-nilai untuk mata pelajaran.
     - Memanggil `calculateAverageAndGrade` untuk mendapatkan rata-rata dan nilai huruf.
     - Mencetak hasil rata-rata dan nilai huruf ke konsol. `toFixed(2)` digunakan untuk membatasi tampilan rata-rata hingga dua angka desimal.
   - **`catch`**:
     - Menangkap dan mencetak pesan kesalahan jika terjadi error selama eksekusi kode dalam blok `try`.

### Cara Kerja

1. **Inisialisasi Nilai**:
   - Nilai untuk `webProgramming`, `computerProgramming`, `statistics`, dan `databaseSystems` diatur.

2. **Menghitung Rata-Rata dan Nilai**:
   - Fungsi `calculateAverageAndGrade` menghitung rata-rata dari nilai-nilai mata pelajaran dan menentukan nilai huruf berdasarkan rata-rata tersebut.

3. **Menampilkan Hasil**:
   - Rata-rata (dibulatkan hingga dua desimal) dan nilai huruf dicetak ke konsol.

4. **Penanganan Kesalahan**:
   - Jika ada error dalam proses, pesan kesalahan akan dicetak.

### Output Contoh

Jika nilai-nilai yang diberikan adalah:
- `webProgramming = 85`
- `computerProgramming = 90`
- `statistics = 78`
- `databaseSystems = 88`

Outputnya akan menjadi:
```
Average: 85.25
Grade: B
```

**Penjelasan Output**:
- Rata-rata nilai dari keempat mata pelajaran adalah 85.25.
- Berdasarkan rata-rata tersebut, nilai huruf yang sesuai adalah `'B'`.
