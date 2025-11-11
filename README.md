[A2 Store.html](https://github.com/user-attachments/files/23475495/A2.Store.html)
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A2 Digital Store</title>
    
    <link rel="stylesheet" href="stye2.css" />
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <script src="https://unpkg.com/@phosphor-icons/web"></script>

    <style>
        /* ============================= */
        /* === CSS RESET & VARIABLES === */
        /* ============================= */
        :root {
            --bg-dark: #121212;
            --bg-light: #1e1e1e;
            --text-primary: #f0f0f0;
            --text-secondary: #aaaaaa;
            --accent-gradient: linear-gradient(90deg, #6a11cb 0%, #2575fc 100%);
            --accent-blue: #2575fc;
            --card-border: rgba(255, 255, 255, 0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-primary);
            line-height: 1.6;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        h1, h2, h3 {
            font-weight: 600;
        }
        
        a {
            text-decoration: none;
            color: var(--text-primary);
        }

        img {
            max-width: 100%;
        }

        /* ============================= */
        /* ========= HEADER / NAV ======== */
        /* ============================= */
        header {
            background-color: var(--bg-light);
            border-bottom: 1px solid var(--card-border);
            padding: 20px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(5px);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: var(--accent-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--text-secondary);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover, .nav-links a.active {
            color: var(--text-primary);
        }
        
        .btn-login {
            background: var(--accent-gradient);
            color: white;
            padding: 8px 20px;
            border-radius: 50px;
            font-weight: 500;
            transition: transform 0.3s ease;
        }

        .btn-login:hover {
            transform: scale(1.05);
        }

        .mobile-menu-toggle {
            display: none;
            font-size: 2rem;
            cursor: pointer;
        }

        /* ============================= */
        /* ========= HERO SECTION ======== */
        /* ============================= */
        .hero {
            padding: 80px 0;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero h1 span {
            background: var(--accent-gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--text-secondary);
            margin-bottom: 30px;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .search-bar {
            position: relative;
            max-width: 500px;
            margin: 0 auto;
        }
        
        .search-bar input {
            width: 100%;
            padding: 15px 20px 15px 50px;
            border-radius: 50px;
            border: 1px solid var(--card-border);
            background-color: var(--bg-light);
            color: var(--text-primary);
            font-size: 1rem;
        }
        
        .search-bar input::placeholder {
            color: var(--text-secondary);
        }
        
        .search-bar i {
            position: absolute;
            left: 20px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--text-secondary);
            font-size: 1.2rem;
        }

        /* ============================= */
        /* ======= PRODUCT SECTION ======= */
        /* ============================= */
        main {
            padding: 60px 0;
        }

        .section-title {
            font-size: 2rem;
            margin-bottom: 30px;
            text-align: center;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
        }

        .product-card {
            background-color: var(--bg-light);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            overflow: hidden;
            text-align: center;
            padding: 20px 15px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .product-card img {
            width: 80px;
            height: 80px;
            object-fit: cover;
            border-radius: 12px;
            margin-bottom: 15px;
        }

        .product-card h3 {
            font-size: 1rem;
            font-weight: 500;
            color: var(--text-primary);
        }

        /* ============================= */
        /* ======= FOOTER SECTION ======== */
        /* ============================= */
        footer {
            background-color: var(--bg-light);
            border-top: 1px solid var(--card-border);
            padding: 40px 0;
            margin-top: 60px;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;
        }

        .footer-logo {
            font-size: 1.3rem;
            font-weight: 700;
        }
        
        .social-links a {
            margin-left: 15px;
            font-size: 1.5rem;
            color: var(--text-secondary);
            transition: color 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--accent-blue);
        }

        .copyright {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* ============================= */
        /* ======== RESPONSIVE ========= */
        /* ============================= */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                width: 100%;
                position: absolute;
                top: 70px;
                left: 0;
                background-color: var(--bg-light);
                padding: 20px 0;
                text-align: center;
            }
            
            .nav-links.active {
                display: flex;
            }

            .nav-links li {
                margin: 10px 0;
            }

            .mobile-menu-toggle {
                display: block;
            }
            
            .btn-login {
                display: none; /* Sembunyikan di nav, bisa ditambah di menu mobile jika mau */
            }

            .hero h1 {
                font-size: 2.2rem;
            }
            
            .footer-content {
                flex-direction: column;
                text-align: center;
            }
        }

    </style>
</head>
<body>

    <header>
        <nav class="container">
            <a href="#" class="logo">A2 Store</a>
            
            <ul class="nav-links" id="nav-links">
                <li><a href="#" class="active">Beranda</a></li>
                <li><a href="#">Apk premium</a></li>
                <li><a href="#">Game</a></li>
                <li><a href="#">Top up</a></li>
                <li><a href="#">Masukan</a></li>
            </ul>
            
            <a href="#" class="btn-login">Customer Service</a>
            
            <div class="mobile-menu-toggle" id="mobile-menu-toggle">
                <i class="ph-fill ph-list"></i>
            </div>
        </nav>
    </header>

    <section class="hero">
        <div class="container">
            <h1>Top Up Game & Pulsa <span>#Termurah</span></h1>
            <p>Layanan top up game, pulsa, dan produk digital instan 24 jam. Cepat, aman, dan terpercaya.</p>
            
            <div class="search-bar">
                <i class="ph ph-magnifying-glass"></i>
                <input type="text" placeholder="Cari layanan favoritmu...">
            </div>
        </div>
    </section>

    <main class="container">
        <h2 class="section-title">Daftar Layanan</h2>
        
        <div class="product-grid">
            <a href="#" class="product-card">
                <img src="logo-ml.png" alt="Mobile Legends">
                <h3>Mobile Legends</h3>
            </a>
            
            <a href="#" class="product-card">
                <img src="logo-wallet.png" alt="Free Fire">
                <h3>Dompet Digital</h3>
            </a>
            
            <a href="#" class="product-card">
                <img src="pulsa.jpeg" alt="Pulsa">
                <h3>Pulsa</h3>
            </a>
            
            <a href="#" class="product-card">
                <img src="kuota.jpeg" alt="Kuota">
                <h3>Kuota</h3>
            </a>
            
            <a href="#" class="product-card">
                <img src="canva.jpeg" alt="Canva pro">
                <h3>Canva Pro</h3>
            </a>
            
            <a href="#" class="product-card">
                <img src="CapCut.jpeg" alt="Capcut pro">
                <h3>CapCut Pro</h3>
            </a>
        </div>
    </main>

    <footer>
        <div class="container footer-content">
            <div class="footer-logo">
                A2 Store
            </div>
            <div class="copyright">
                &copy; 2025 A2 Store. All rights reserved.
            </div>
            <div class="social-links">
                <a href="#"><i class="ph-fill ph-instagram-logo"></i></a>
                <a href="#"><i class="ph-fill ph-tiktok-logo"></i></a>
                <a href="#"><i class="ph-fill ph-youtube-logo"></i></a>
            </div>
        </div>
    </footer>

    <script>
        // Script sederhana untuk toggle menu mobile
        const menuToggle = document.getElementById('mobile-menu-toggle');
        const navLinks = document.getElementById('nav-links');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            
            // Mengganti ikon buka/tutup
            const icon = menuToggle.querySelector('i');
            if (navLinks.classList.contains('active')) {
                icon.classList.remove('ph-list');
                icon.classList.add('ph-x');
            } else {
                icon.classList.remove('ph-x');
                icon.classList.add('ph-list');
            }
        });

        // Script untuk tombol-tombol layanan di daftar layanan (tanpa konfirmasi)
document.addEventListener('DOMContentLoaded', function() {
    const serviceButtons = document.querySelectorAll('.btn-login'); // Selektor untuk semua tombol layanan (ganti dengan class/id yang sesuai)
    
    serviceButtons.forEach(function(button) {
        button.addEventListener('click', function(event) {
            event.preventDefault(); // Mencegah navigasi default
            
            // Buka WhatsApp Catalog di tab baru langsung
            const whatsappUrl = 'https://wa.me/6289602602626'; // URL WhatsApp Catalog dengan nomor Anda
            window.open(whatsappUrl, '_blank'); // '_blank' membuka di tab baru
            
            // Opsional: Tambahkan tracking atau logika lain jika diperlukan
            console.log('Layanan WhatsApp Catalog dibuka langsung untuk nomor 089602602626');
        });
    });
});

// Script untuk tombol-tombol layanan di daftar layanan (tanpa konfirmasi)
document.addEventListener('DOMContentLoaded', function() {
    const serviceButtons = document.querySelectorAll('.product-card'); // Selektor untuk semua tombol layanan (ganti dengan class/id yang sesuai)
    
    serviceButtons.forEach(function(button) {
        button.addEventListener('click', function(event) {
            event.preventDefault(); // Mencegah navigasi default
            
            // Buka WhatsApp Catalog di tab baru langsung
            const whatsappUrl = 'https://www.whatsapp.com/catalog/6289602602626/?app_absent=0'; // URL WhatsApp Catalog dengan nomor Anda
            window.open(whatsappUrl, '_blank'); // '_blank' membuka di tab baru
            
            // Opsional: Tambahkan tracking atau logika lain jika diperlukan
            console.log('Layanan WhatsApp Catalog dibuka langsung untuk nomor 089602602626');
        });
    });
});

    </script>

</body>
</html>
