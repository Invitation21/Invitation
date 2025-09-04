<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Pernikahan - Rendi & Shobri</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            color: #5a5a5a;
            background-color: #fcf9f6;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header & Cover */
        .cover {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), url('https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            position: relative;
            padding: 0 15px;
        }
        
        .names {
            margin-bottom: 20px;
        }
        
        .bride-name, .groom-name {
            font-family: 'Playfair Display', serif;
            font-size: 2.8rem;
            margin-bottom: 5px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .and {
            font-size: 1.8rem;
            margin: 10px 0;
        }
        
        .date {
            font-size: 1.2rem;
            margin-top: 20px;
            letter-spacing: 2px;
        }
        
        .scroll-down {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 2rem;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateY(0) translateX(-50%);}
            40% {transform: translateY(-20px) translateX(-50%);}
            60% {transform: translateY(-10px) translateX(-50%);}
        }
        
        /* Section Styling */
        section {
            padding: 60px 0;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
            text-align: center;
            font-size: 2rem;
            margin-bottom: 30px;
            color: #a8715c;
        }
        
        /* Couple Section */
        .couple {
            text-align: center;
        }
        
        .couple-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 8px solid #f0e6df;
            margin: 0 auto 25px;
            display: block;
        }
        
        .couple-text {
            max-width: 700px;
            margin: 0 auto;
            font-size: 1rem;
            padding: 0 15px;
        }
        
        /* Event Details */
        .event-details {
            background-color: #f0e6df;
        }
        
        .event-card {
            background: white;
            padding: 25px 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 25px;
            text-align: center;
        }
        
        .event-title {
            font-family: 'Playfair Display', serif;
            color: #a8715c;
            font-size: 1.5rem;
            margin-bottom: 15px;
        }
        
        .event-info {
            margin-bottom: 10px;
            font-size: 0.95rem;
        }
        
        .event-info i {
            margin-right: 10px;
            color: #a8715c;
        }
        
        /* Countdown */
        .countdown {
            text-align: center;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1519225421980-715cb0215aed?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            color: white;
            padding: 50px 0;
        }
        
        .countdown-container {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        .countdown-box {
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 10px;
            min-width: 80px;
            backdrop-filter: blur(5px);
        }
        
        .countdown-number {
            font-size: 2rem;
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .countdown-label {
            font-size: 0.9rem;
        }
        
        /* Gallery */
        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 30px;
        }
        
        .gallery-item {
            height: 180px;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        /* RSVP */
        .rsvp {
            background-color: #f0e6df;
            text-align: center;
        }
        
        .rsvp-form {
            max-width: 100%;
            margin: 0 auto;
            background: white;
            padding: 25px 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
            text-align: left;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            font-size: 0.95rem;
        }
        
        .form-group input, .form-group select, .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Montserrat', sans-serif;
            font-size: 1rem;
        }
        
        .btn {
            background-color: #a8715c;
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
            width: 100%;
        }
        
        .btn:hover {
            background-color: #946652;
        }
        
        /* Footer */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 25px 0;
            font-size: 0.9rem;
        }
        
        .footer-text {
            margin-top: 15px;
        }
        
        /* Navigation for Mobile */
        .mobile-nav {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #a8715c;
            border-radius: 50px;
            padding: 10px 0;
            z-index: 1000;
            display: none;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }
        
        .nav-items {
            display: flex;
            justify-content: space-around;
            width: 280px;
        }
        
        .nav-item {
            color: white;
            text-decoration: none;
            display: flex;
            flex-direction: column;
            align-items: center;
            font-size: 0.8rem;
        }
        
        .nav-item i {
            font-size: 1.2rem;
            margin-bottom: 5px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .bride-name, .groom-name {
                font-size: 2.2rem;
            }
            
            .and {
                font-size: 1.5rem;
            }
            
            .date {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .couple-img {
                width: 180px;
                height: 180px;
            }
            
            .mobile-nav {
                display: block;
            }
            
            .gallery-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 480px) {
            .bride-name, .groom-name {
                font-size: 1.8rem;
            }
            
            .countdown-box {
                min-width: 70px;
                padding: 12px;
            }
            
            .countdown-number {
                font-size: 1.8rem;
            }
            
            .countdown-label {
                font-size: 0.8rem;
            }
            
            .gallery-item {
                height: 150px;
            }
        }
        
        /* Music Player */
        .music-player {
            position: fixed;
            top: 20px;
            right: 20px;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 50%;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            cursor: pointer;
        }
        
        .music-player i {
            font-size: 1.5rem;
            color: #a8715c;
        }
    </style>
</head>
<body>
    <!-- Music Player -->
    <div class="music-player" id="musicToggle">
        <i class="fas fa-music"></i>
    </div>
    <audio id="weddingMusic" loop>
        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    </audio>

    <!-- Cover Section -->
    <header class="cover" id="home">
        <div class="names">
            <h1 class="bride-name">Sarah</h1>
            <div class="and">&</div>
            <h1 class="groom-name">Budi</h1>
        </div>
        <p class="date">28 • 10 • 2023</p>
        <div class="scroll-down">
            <i class="fas fa-chevron-down"></i>
        </div>
    </header>

    <!-- Couple Section -->
    <section class="couple" id="couple">
        <div class="container">
            <h2 class="section-title">Kami Berbahagia</h2>
            <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=80" alt="Pasangan" class="couple-img">
            <p class="couple-text">
                Dengan penuh rasa syukur dan kebahagiaan, kami bermaksud menyelenggarakan pernikahan putra-putri kami. 
                Merupakan suatu kehormatan dan kebahagiaan bagi kami apabila Bapak/Ibu/Saudara/i berkenan hadir untuk 
                memberikan doa restu kepada kedua mempelai.
            </p>
        </div>
    </section>

    <!-- Event Details -->
    <section class="event-details" id="events">
        <div class="container">
            <h2 class="section-title">Acara Pernikahan</h2>
            
            <div class="event-card">
                <h3 class="event-title">Akad Nikah</h3>
                <p class="event-info">
                    <i class="far fa-calendar"></i> Sabtu, 28 Oktober 2023
                </p>
                <p class="event-info">
                    <i class="far fa-clock"></i> Pukul 08:00 - 10:00 WIB
                </p>
                <p class="event-info">
                    <i class="fas fa-map-marker-alt"></i> Masjid Al-Ikhlas, Jl. Merdeka No. 123, Jakarta
                </p>
                <a href="https://maps.google.com" class="btn" style="margin-top: 15px; display: inline-block; width: auto;">
                    <i class="fas fa-map"></i> Lihat Lokasi
                </a>
            </div>
            
            <div class="event-card">
                <h3 class="event-title">Resepsi Pernikahan</h3>
                <p class="event-info">
                    <i class="far fa-calendar"></i> Sabtu, 28 Oktober 2023
                </p>
                <p class="event-info">
                    <i class="far fa-clock"></i> Pukul 11:00 - 15:00 WIB
                </p>
                <p class="event-info">
                    <i class="fas fa-map-marker-alt"></i> Ballroom Hotel Grand Palace, Jl. Sudirman No. 456, Jakarta
                </p>
                <a href="https://maps.google.com" class="btn" style="margin-top: 15px; display: inline-block; width: auto;">
                    <i class="fas fa-map"></i> Lihat Lokasi
                </a>
            </div>
        </div>
    </section>

    <!-- Countdown -->
    <section class="countdown" id="countdown">
        <div class="container">
            <h2 class="section-title">Hitungan Mundur</h2>
            <div class="countdown-container">
                <div class="countdown-box">
                    <div class="countdown-number" id="days">00</div>
                    <div class="countdown-label">Hari</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="hours">00</div>
                    <div class="countdown-label">Jam</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="minutes">00</div>
                    <div class="countdown-label">Menit</div>
                </div>
                <div class="countdown-box">
                    <div class="countdown-number" id="seconds">00</div>
                    <div class="countdown-label">Detik</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery -->
    <section class="gallery" id="gallery">
        <div class="container">
            <h2 class="section-title">Galeri Kami</h2>
            <div class="gallery-container">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1539673394310-9f2c6f31a9e9?ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=80" alt="Foto Prewedding">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1519741497674-611481863552?ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=80" alt="Foto Prewedding">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1511285560929-80c456cbc1d1?ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=80" alt="Foto Prewedding">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1543080853-556086153871?ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=80" alt="Foto Prewedding">
                </div>
            </div>
        </div>
    </section>

    <!-- RSVP -->
    <section class="rsvp" id="rsvp">
        <div class="container">
            <h2 class="section-title">Konfirmasi Kehadiran</h2>
            <form class="rsvp-form">
                <div class="form-group">
                    <label for="name">Nama Lengkap</label>
                    <input type="text" id="name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" required>
                </div>
                <div class="form-group">
                    <label for="phone">Nomor Telepon</label>
                    <input type="tel" id="phone">
                </div>
                <div class="form-group">
                    <label for="attendance">Konfirmasi Kehadiran</label>
                    <select id="attendance" required>
                        <option value="">Pilih opsi</option>
                        <option value="yes">Ya, saya akan hadir</option>
                        <option value="no">Maaf, tidak bisa hadir</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="guests">Jumlah Tamu</label>
                    <input type="number" id="guests" min="1" value="1">
                </div>
                <div class="form-group">
                    <label for="message">Pesan / Doa</label>
                    <textarea id="message" rows="4"></textarea>
                </div>
                <button type="submit" class="btn">Kirim Konfirmasi</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>Terima kasih atas doa dan restunya</p>
            <p class="footer-text">© 2023 Undangan Pernikahan Sarah & Budi</p>
        </div>
    </footer>

    <!-- Mobile Navigation -->
    <nav class="mobile-nav">
        <div class="nav-items">
            <a href="#home" class="nav-item">
                <i class="fas fa-home"></i>
                <span>Home</span>
            </a>
            <a href="#events" class="nav-item">
                <i class="fas fa-calendar-alt"></i>
                <span>Acara</span>
            </a>
            <a href="#gallery" class="nav-item">
                <i class="fas fa-images"></i>
                <span>Galeri</span>
            </a>
            <a href="#rsvp" class="nav-item">
                <i class="fas fa-envelope"></i>
                <span>RSVP</span>
            </a>
        </div>
    </nav>

    <script>
        // Countdown timer
        function updateCountdown() {
            const weddingDate = new Date('October 28, 2023 08:00:00').getTime();
            const now = new Date().getTime();
            const distance = weddingDate - now;
            
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            
            document.getElementById('days').innerText = days.toString().padStart(2, '0');
            document.getElementById('hours').innerText = hours.toString().padStart(2, '0');
            document.getElementById('minutes').innerText = minutes.toString().padStart(2, '0');
            document.getElementById('seconds').innerText = seconds.toString().padStart(2, '0');
        }
        
        setInterval(updateCountdown, 1000);
        updateCountdown();
        
        // Smooth scrolling
        document.querySelector('.scroll-down').addEventListener('click', function() {
            window.scrollBy({
                top: window.innerHeight,
                behavior: 'smooth'
            });
        });
        
        // Form submission
        document.querySelector('.rsvp-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Terima kasih telah mengkonfirmasi kehadiran Anda!');
            this.reset();
        });
        
        // Music player
        const musicToggle = document.getElementById('musicToggle');
        const audio = document.getElementById('weddingMusic');
        
        musicToggle.addEventListener('click', function() {
            if (audio.paused) {
                audio.play();
                musicToggle.innerHTML = '<i class="fas fa-pause"></i>';
            } else {
                audio.pause();
                musicToggle.innerHTML = '<i class="fas fa-music"></i>';
            }
        });
        
        // Mobile navigation
        document.querySelectorAll('.nav-item').forEach(item => {
            item.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                window.scrollTo({
                    top: targetElement.offsetTop,
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
