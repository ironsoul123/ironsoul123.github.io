<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IronSoulAI | VIP Analytics</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&family=Poppins:wght@300;600&display=swap" rel="stylesheet">
    <style>
        :root { --main: #00f2ff; --bg: #0a0a0a; --card: #141414; }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--bg); color: #fff; font-family: 'Poppins', sans-serif; overflow-x: hidden; }

        /* ARKA PLAN GÖRSELİ (BLURLU) */
        .hero-bg {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: url('tema.jpg') center/cover no-repeat;
            filter: brightness(0.2) blur(8px); z-index: -1;
        }

        /* HEADER */
        nav { padding: 30px 8%; display: flex; justify-content: space-between; align-items: center; }
        .logo { font-family: 'Orbitron'; font-size: 1.5rem; letter-spacing: 4px; color: var(--main); }

        /* ANA İÇERİK */
        .content { 
            height: 80vh; display: flex; flex-direction: column; 
            align-items: center; justify-content: center; text-align: center; padding: 0 20px;
        }

        h1 { font-family: 'Orbitron'; font-size: 3.5rem; margin-bottom: 10px; text-shadow: 0 0 20px rgba(0,242,255,0.4); }
        p { color: #888; max-width: 600px; margin-bottom: 40px; font-size: 1.1rem; }

        /* ANALİZ BUTONU */
        .btn-main {
            background: var(--main); color: #000; padding: 20px 50px;
            border-radius: 50px; font-weight: bold; text-decoration: none;
            font-family: 'Orbitron'; font-size: 1.2rem; transition: 0.4s;
            box-shadow: 0 0 30px rgba(0,242,255,0.3);
        }
        .btn-main:hover { transform: scale(1.1); box-shadow: 0 0 60px var(--main); letter-spacing: 2px; }

        /* ALT BİLGİ KARTLARI */
        .stats { 
            display: flex; gap: 30px; margin-top: 60px; 
            flex-wrap: wrap; justify-content: center;
        }
        .stat-box { 
            background: var(--card); border: 1px solid rgba(255,255,255,0.05);
            padding: 20px 40px; border-radius: 20px; min-width: 200px;
        }
        .stat-box h3 { color: var(--main); font-family: 'Orbitron'; margin-bottom: 5px; }
        .stat-box span { font-size: 0.8rem; color: #555; text-transform: uppercase; }

        @media (max-width: 768px) {
            h1 { font-size: 2rem; }
            .stats { gap: 15px; }
        }
    </style>
</head>
<body>

    <div class="hero-bg"></div>

    <nav>
        <div class="logo">İRONSOULAI</div>
        <div style="font-size: 0.7rem; border: 1px solid #333; padding: 5px 10px; border-radius: 5px;">v4.0 STABLE</div>
    </nav>

    <div class="content">
        <h1 style="color: #fff;">KUPON<span style="color: var(--main);">AI</span></h1>
        <p>Dünyanın en gelişmiş yapay zeka spor analiz motoruna bağlanın. <br>İstatistikler, form durumları ve banko tahminler tek bir noktada.</p>
        
        <a href="https://poe.com/kuponAi" target="_blank" class="btn-main">ANALİZİ BAŞLAT</a>

        <div class="stats">
            <div class="stat-box">
                <h3>%91</h3>
                <span>İsabet Oranı</span>
            </div>
            <div class="stat-box">
                <h3>24/7</h3>
                <span>Canlı Tarama</span>
            </div>
            <div class="stat-box">
                <h3>Vip</h3>
                <span>Erişim</span>
            </div>
        </div>
    </div>

    <footer style="position: fixed; bottom: 20px; width: 100%; text-align: center; font-size: 0.7rem; color: #333;">
        &copy; 2026 IRONSOULAI DIGITAL PROTOCOL
    </footer>

</body>
</html>
