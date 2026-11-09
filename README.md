<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Personal Biodata | Rizqika Karisti Arianti</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', sans-serif;
    background: #050d20;
    color: white;
    overflow-x: hidden;
}

/* BACKGROUND ANGKASA */
.space {
    position: fixed;
    inset: 0;
    z-index: -2;
    background:
      radial-gradient(ellipse at 20% 20%, #163d73 0%, transparent 40%),
      radial-gradient(ellipse at 80% 70%, #142d5a 0%, transparent 40%),
      linear-gradient(180deg, #030817, #0b1c3b, #071329);
}

.stars {
    position: fixed;
    inset: 0;
    z-index: -1;
    pointer-events: none;
    background-image:
      radial-gradient(2px 2px at 20px 30px, white, transparent),
      radial-gradient(2px 2px at 100px 150px, #9ed8ff, transparent),
      radial-gradient(1px 1px at 200px 80px, white, transparent),
      radial-gradient(2px 2px at 300px 200px, white, transparent),
      radial-gradient(1px 1px at 400px 100px, #9ed8ff, transparent);
    background-size: 450px 350px;
    animation: stars 8s linear infinite alternate;
}

@keyframes stars {
    from { opacity: .4; }
    to { opacity: 1; }
}

/* PLANET */
.planet {
    position: absolute;
    width: 110px;
    height: 110px;
    border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, #d9f2ff, #659bd5, #18345d);
    box-shadow: 0 0 45px #448bd8;
    top: 130px;
    right: 9%;
}

.saturn {
    position: absolute;
    width: 85px;
    height: 85px;
    border-radius: 50%;
    background: radial-gradient(circle at 30% 30%, #d9efff, #6c9dce, #244a78);
    box-shadow: 0 0 25px #5b9bd8;
    top: 75%;
    left: 7%;
}

.saturn::after {
    content: "";
    position: absolute;
    width: 135px;
    height: 35px;
    border: 5px solid #a9d9ff;
    border-radius: 50%;
    transform: rotate(-25deg);
    top: 25px;
    left: -28px;
}

/* NAVBAR */
nav {
    position: sticky;
    top: 0;
    z-index: 10;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 8%;
    background: rgba(4, 13, 32, .9);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid #294c79;
}

nav h2 {
    color: #a9dfff;
    letter-spacing: 2px;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 25px;
}

nav a {
    color: white;
    text-decoration: none;
    transition: .3s;
}

nav a:hover {
    color: #80caff;
}

/* HERO */
.hero {
    min-height: 90vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 60px 20px;
    position: relative;
}

.hero .moon {
    font-size: 85px;
    color: #d8efff;
    text-shadow: 0 0 35px #9acfff;
    margin-bottom: 20px;
}

.hero h1 {
    font-size: clamp(30px, 5vw, 55px);
    color: #e5f5ff;
    letter-spacing: 3px;
    text-shadow: 0 0 20px #5ca9e8;
}

.hero h3 {
    color: #91caff;
    margin-top: 18px;
    font-weight: 400;
    letter-spacing: 3px;
}

.hero p {
    max-width: 600px;
    line-height: 1.8;
    color: #c4d9f5;
    margin: 25px 0;
}

.btn {
    display: inline-block;
    padding: 13px 30px;
    border: 1px solid #8dccff;
    border-radius: 30px;
    color: white;
    text-decoration: none;
    background: rgba(65, 139, 211, .2);
    transition: .3s;
}

.btn:hover {
    background: #3d83c2;
    box-shadow: 0 0 20px #4ca9ff;
}

/* SECTION */
section {
    padding: 90px 9%;
    position: relative;
}

.section-title {
    text-align: center;
    font-size: 32px;
    color: #bce4ff;
    margin-bottom: 45px;
    letter-spacing: 3px;
}

.section-title span {
    display: block;
    font-size: 15px;
    color: #8baed8;
    margin-top: 10px;
    letter-spacing: 2px;
}

/* CARD */
.card {
    max-width: 850px;
    margin: auto;
    padding: 35px;
    border-radius: 22px;
    background: linear-gradient(
      135deg,
      rgba(24, 55, 100, .85),
      rgba(9, 25, 53, .9)
    );
    border: 1px solid rgba(147, 205, 255, .3);
    box-shadow: 0 0 30px rgba(51, 133, 208, .15);
    transition: .3s;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 0 35px rgba(75, 160, 245, .3);
}

/* BIODATA */
.info {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    padding: 17px 0;
    border-bottom: 1px solid rgba(190, 220, 255, .15);
}

.info:last-child {
    border-bottom: none;
}

.info strong {
    color: #9dd7ff;
}

.info p {
    color: #f1f7ff;
    text-align: right;
}

/* PENDIDIKAN */
.timeline {
    max-width: 750px;
    margin: auto;
    border-left: 3px solid #76bfff;
    padding-left: 30px;
}

.timeline-item {
    position: relative;
    padding: 10px 20px 35px;
}

.timeline-item::before {
    content: "✦";
    position: absolute;
    left: -42px;
    top: 10px;
    color: #a8dcff;
    font-size: 22px;
}

.timeline-item h3 {
    color: #a9dcff;
    margin-bottom: 10px;
}

.timeline-item p {
    color: #d4e4f8;
    line-height: 1.8;
}

/* PENGALAMAN */
.experience-box {
    max-width: 850px;
    margin: auto;
    padding: 35px;
    background: rgba(24, 55, 100, .75);
    border-radius: 20px;
    border: 1px solid #568dc4;
    line-height: 2;
}

.experience-box h3 {
    color: #a8ddff;
    margin-bottom: 15px;
    font-size: 24px;
}

.experience-box strong {
    color: #a8ddff;
}

/* ABOUT */
.about {
    max-width: 850px;
    margin: auto;
    text-align: center;
    line-height: 2;
    padding: 40px;
    background: rgba(20, 48, 89, .7);
    border-radius: 25px;
    border: 1px solid #4d82b6;
    color: #dcecff;
}

.about .symbol {
    font-size: 55px;
    margin-bottom: 20px;
}

/* QUOTE */
.quote {
    text-align: center;
    padding: 80px 20px;
    color: #b5dfff;
    font-size: 23px;
    font-style: italic;
    line-height: 1.8;
}

/* FOOTER */
footer {
    background: #030918;
    text-align: center;
    padding: 40px 20px;
    border-top: 1px solid #315a87;
    color: #9dbde0;
    line-height: 2;
}

footer strong {
    color: #bce5ff;
}

/* RESPONSIVE */
@media(max-width: 700px) {
    nav {
        flex-direction: column;
        gap: 15px;
    }

    nav ul {
        gap: 13px;
        flex-wrap: wrap;
        justify-content: center;
        font-size: 13px;
    }

    .info {
        flex-direction: column;
        gap: 7px;
    }

    .info p {
        text-align: left;
    }

    .card {
        padding: 22px;
    }

    section {
        padding: 65px 6%;
    }

    .planet {
        width: 65px;
        height: 65px;
        right: 5%;
    }
}
</style>
</head>

<body>

<div class="space"></div>
<div class="stars"></div>
<div class="planet"></div>
<div class="saturn"></div>

<!-- NAVIGATION -->
<nav>
    <h2>✦ RIZQIKA</h2>
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#biodata">Biodata</a></li>
        <li><a href="#pendidikan">Pendidikan</a></li>
        <li><a href="#pengalaman">Pengalaman</a></li>
        <li><a href="#about">About</a></li>
    </ul>
</nav>

<!-- HOME -->
<div class="hero" id="home">

    <div class="moon">☾</div>

    <h1>WELCOME TO MY UNIVERSE</h1>

    <h3>RIZQIKA KARISTI ARIANTI</h3>

    <p>
        Selamat datang di website personal saya.
        Sebuah ruang kecil untuk mengenal diri saya,
        perjalanan pendidikan, dan pengalaman yang
        telah saya lalui.
    </p>

    <a href="#biodata" class="btn">
        Explore My Profile ✦
    </a>

</div>

<!-- BIODATA -->
<section id="biodata">

    <h2 class="section-title">
        ✧ PERSONAL BIODATA ✧
        <span>Kenali lebih dekat tentang saya</span>
    </h2>

    <div class="card">

        <div class="info">
            <strong>Nama Lengkap</strong>
            <p>Rizqika Karisti Arianti</p>
        </div>

        <div class="info">
            <strong>Tempat, Tanggal Lahir</strong>
            <p>Pacitan, 11 Januari 2008</p>
        </div>

        <div class="info">
            <strong>Jenis Kelamin</strong>
            <p>Perempuan</p>
        </div>

        <div class="info">
            <strong>Agama</strong>
            <p>Islam</p>
        </div>

        <div class="info">
            <strong>Kewarganegaraan</strong>
            <p>Indonesia</p>
        </div>

        <div class="info">
            <strong>Nomor WhatsApp</strong>
            <p>082139672727</p>
        </div>

    </div>
</section>

<!-- PENDIDIKAN -->
<section id="pendidikan">

    <h2 class="section-title">
        ✧ EDUCATION JOURNEY ✧
        <span>Perjalanan pendidikan saya</span>
    </h2>

    <div class="timeline">

        <div class="timeline-item">
            <h3>SMKN 1 Donorojo</h3>
            <p>
                Pendidikan terakhir sebelum melanjutkan
                ke jenjang perguruan tinggi.
            </p>
        </div>

        <div class="timeline-item">
            <h3>Politeknik Indonusa Surakarta</h3>
            <p>
                Saat ini saya sedang menempuh pendidikan
                di Politeknik Indonusa Surakarta.
            </p>
            <p>
                <strong>Program Studi:</strong>
                Teknologi Rekayasa Perangkat Lunak (TRPL)
            </p>
        </div>

    </div>
</section>

<!-- PENGALAMAN -->
<section id="pengalaman">

    <h2 class="section-title">
        ✧ MY EXPERIENCE ✧
        <span>Pengalaman dan perjalanan kerja</span>
    </h2>

    <div class="experience-box">

        <h3>✦ Praktik Kerja Lapangan (PKL)</h3>

        <p>
            <strong>Tempat:</strong><br>
            Uti Unik Collection and Modiste
        </p>

        <p>
            <strong>Durasi:</strong><br>
            6 Bulan
        </p>

        <p>
            <strong>Periode:</strong><br>
            6 Juli 2025 – 15 Desember 2025
        </p>

        <p>
            Praktik Kerja Lapangan merupakan salah satu
            pengalaman yang memberikan kesempatan
            kepada saya untuk mengenal dunia kerja,
            menambah wawasan, serta memperoleh
            pengalaman secara langsung di lingkungan kerja.
        </p>

    </div>
</section>

<!-- ABOUT ME -->
<section id="about">

    <h2 class="section-title">
        ✧ ABOUT ME ✧
        <span>Sedikit cerita tentang saya</span>
    </h2>

    <div class="about">

        <div class="symbol">🌙</div>

        <p>
            Halo! Nama saya Rizqika Karisti Arianti.
            Saya merupakan mahasiswa Program Studi
            Teknologi Rekayasa Perangkat Lunak (TRPL)
            di Politeknik Indonusa Surakarta.
        </p>

        <p>
            Website ini dibuat sebagai media untuk
            memperkenalkan diri, menampilkan biodata,
            riwayat pendidikan, dan pengalaman yang
            telah saya miliki.
        </p>

        <p>
            Saya percaya bahwa setiap perjalanan
            memiliki proses dan setiap proses
            memberikan pelajaran berharga.
        </p>

    </div>

</section>

<!-- MOTIVASI -->
<div class="quote">

    "Just like the stars, keep shining
    even in the darkest night."

    <p style="font-size:15px; margin-top:15px;">
        ✦ Dream Big • Keep Learning • Never Give Up ✦
    </p>

</div>

<!-- FOOTER -->
<footer>

    <h2>✦ MY LITTLE UNIVERSE ✦</h2>

    <p>
        Personal Website of
        <strong>Rizqika Karisti Arianti</strong>
    </p>

    <p>
        Made with ♡ and dreams
    </p>

    <p style="font-size:12px; margin-top:15px;">
        © 2026 Rizqika Karisti Arianti.
        All Rights Reserved.
    </p>

</footer>

</body>
</html>
