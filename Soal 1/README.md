### HTML

1. **Deklarasi Dokumen dan Informasi Meta**:
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Web Profile</title>
        <link rel="stylesheet" type="text/css" href="styles.css">
        <link rel="icon" href="images/favicon.png" type="image/png">
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    </head>
    ```
    - `<!DOCTYPE html>` mendeklarasikan tipe dokumen dan versi HTML.
    - Tag `<meta>` digunakan untuk mengatur encoding karakter dan pengaturan viewport agar desain responsif.
    - Tag `<title>` menentukan judul halaman yang ditampilkan di tab browser.
    - `<link rel="stylesheet" href="styles.css">` menghubungkan file CSS eksternal untuk gaya.
    - `<link rel="icon">` menetapkan favicon untuk halaman web.
    - `<link rel="stylesheet" href="https://cdnjs.cloudflare.com/...">` menghubungkan Font Awesome untuk ikon.

2. **Header**:
    ```html
    <header>
        <h1 class="typing-effect">Welcome to My Web Profile</h1>
    </header>
    ```
    - Berisi heading dengan kelas `typing-effect` untuk animasi teks yang seolah-olah sedang diketik.

3. **Navigasi**:
    ```html
    <nav class="main-nav">
        <ul>
            <li><a href=""><i class="fas fa-home"></i> Home</a></li>
            <li class="dropdown">
                <a href="" class="dropbtn"><i class="fas fa-code"></i> Skills</a>
                <div class="dropdown-content">
                    <a href="#html"><i class="fab fa-html5"></i> HTML</a>
                    <a href="#css"><i class="fab fa-css3-alt"></i> CSS</a>
                </div>
            </li>
            <li class="dropdown">
                <a href="" class="dropbtn"><i class="fas fa-project-diagram"></i> Projects</a>
                <div class="dropdown-content">
                    <a href="https://github.com/NanaIkhwan/tugas1.git" target="_blank" rel="noopener noreferrer"><i class="fas fa-folder"></i> Project 1</a>
                    <a href="https://github.com/NanaIkhwan/pertemuan-week2-3.git" target="_blank" rel="noopener noreferrer"><i class="fas fa-folder"></i> Project 2</a>
                    <a href=""><i class="fas fa-folder"></i> Project 3</a>
                </div>
            </li>
        </ul>
    </nav>
    ```
    - `main-nav` berisi daftar tautan dengan ikon Font Awesome.
    - Kelas `dropdown` menunjukkan bahwa item menu ini dapat diturunkan (dropdown) dan ditampilkan saat hover.

4. **Konten Utama**:
    ```html
    <main class="container">
        <div class="content-wrapper">
            <article class="card" data-tilt>
                <img src="images/Profile.png" alt="Profile Picture">
                <h2 id="about">Najwa Ikhwan M</h2>
                <p>Hello, My name is Nana, and I'm a Web Developer.</p>
                <section id="hobbies">
                    <h3>Hobbies:</h3>
                    <ul>
                        <li>Playing Game</li>
                        <li>Photography</li>
                        <li>Videography</li>
                    </ul>
                </section>
                <aside class="links">
                    <h3>Connect with me:</h3>
                    <a href="https://instagram.com" target="_blank" rel="noopener noreferrer"><img src="images/instagram.png" alt="Instagram"></a>
                    <a href="https://facebook.com" target="_blank" rel="noopener noreferrer"><img src="images/facebook.png" alt="Facebook"></a>
                    <a href="https://youtube.com" target="_blank" rel="noopener noreferrer"><img src="images/youtube.png" alt="YouTube"></a>
                </aside>
                <a href="" class="btn" rel="noopener noreferrer">Follow</a>
            </article>

            <aside class="additional-info">
                <h3>Additional Information</h3>
                <ul>
                    <li>I really enjoy learning to create interactive and responsive websites that can enhance my personal experience.</li>
                    <li>I also enjoy learning about new technologies.</li>
                    <li>In my spare time, I enjoy my hobby outside of Informatics, which is photography.</li>
                </ul>
            </aside>
        </div>
    </main>
    ```
    - `container` adalah pembungkus utama dengan latar belakang gambar.
    - Di dalam `content-wrapper`, terdapat dua bagian utama: `card` (informasi profil) dan `additional-info` (detail tambahan).
    - `card` berisi informasi profil, hobi, dan tautan ke media sosial dengan gambar.

5. **Footer**:
    ```html
    <footer>
        <p>&copy; 2024 Najwa Ikhwan M. All rights reserved.</p>
    </footer>
    ```
    - Menampilkan catatan hak cipta.

### CSS

1. **Gaya Global**:
    ```css
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Poppins', sans-serif;
    }
    ```
    - Mengatur margin dan padding menjadi 0, menggunakan box-sizing border-box, dan menerapkan font Poppins pada semua elemen.

2. **Body dan Header**:
    ```css
    body {
        background-color: #f0f0f0;
        color: #333;
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    header {
        background-color: #333;
        color: #fff;
        padding: 20px;
        text-align: center;
    }
    ```
    - Mengatur latar belakang dan warna teks body, serta mengatur layout agar memenuhi tinggi viewport.
    - Header memiliki latar belakang gelap dan teks putih yang terpusat.

3. **Gaya Navigasi**:
    ```css
    .main-nav {
        background-color: #444;
        padding: 10px 0;
        border: 1px solid #4b4b4b;
        border-radius: 1px;
        box-shadow: 0 2px px rgba(0, 0, 0, 0.3);
    }

    .main-nav ul {
        list-style-type: none;
        display: flex;
        justify-content: center;
        margin: 0;
        padding: 0;
    }
    ```
    - Menata bilah navigasi dengan warna latar belakang, border, dan bayangan.

4. **Menu Dropdown**:
    ```css
    .dropdown-content {
        display: none;
        position: absolute;
        background-color: #d755ff;
        min-width: 160px;
        box-shadow: 0px 8px 16px rgba(0,0,0,0.2);
        z-index: 1;
        border: 2px solid #ff01cf;
        border-radius: 8px;
    }
    .dropdown:hover .dropdown-content {
        display: block;
    }
    ```
    - Menyembunyikan konten dropdown secara default dan menampilkannya saat hover.

5. **Card dan Informasi Tambahan**:
    ```css
    .card {
        width: 90%;
        max-width: 440px;
        color: #fff;
        text-align: center;
        padding: 50px 35px;
        background: rgba(255, 255, 255, 0.2);
        border-radius: 16px;
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(5px);
        margin-bottom: 20px;
        transition: transform 0.5s ease-in-out, box-shadow 0.5s ease-in-out;
    }

    .additional-info {
        width: 90%;
        max-width: 300px;
        color: #fff;
        text-align: left;
        padding: 20px;
        background: rgba(255, 255, 255, 0.2);
        border-radius: 16px;
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(5px);
        margin-bottom: 20px;
        transition: transform 0.5s ease-in-out, box-shadow 0.5s ease-in-out;
    }
    ```
    - Menata `card` dengan latar belakang transparan, sudut membulat, bayangan, dan efek transisi saat di-hover.
    - `additional-info` memiliki gaya serupa dengan efek transisi.

6. **Tombol**:
    ```css
    .btn {
        text-decoration: none;
        display: inline-block;
        font
