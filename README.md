<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IronSoulAI | kuponAi Terminal v5.0</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;900&family=Plus+Jakarta+Sans:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --neon: #00f2ff;
            --purple: #7000ff;
            --bg: #020408;
            --card: rgba(255, 255, 255, 0.03);
            --border: rgba(0, 242, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--bg); color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; overflow-x: hidden; }

        /* Dinamik Arka Plan */
        .bg-overlay {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(rgba(2,4,8,0.9), rgba(2,4,8,0.9)), url('tema.jpg') center/cover no-repeat;
            z-index: -1; filter: saturate(1.2);
        }

        /* Navigasyon */
        nav {
            padding: 20px 8%; display: flex; justify-content: space-between; align-items: center;
            background: rgba(0,0,0,0.8); border-bottom: 1px solid var(--border);
            backdrop-filter: blur(15px); position: sticky; top: 0; z-index: 1000;
        }
        .logo { font-family: 'Orbitron'; font-weight: 900; letter-spacing: 4px; color: var(--neon); font-size: 1.4rem; }
        .nav-links a { color: #fff; text-decoration: none; margin-left: 25px; font-size: 0.8rem; font-weight: bold; transition: 0.3s; opacity: 0.7; }
        .nav-links a:hover { opacity: 1; color: var(--neon); }

        /* Hero */
        header { padding: 80px 8% 40px; text-align: center; }
        header h1 { font-family: 'Orbitron'; font-size: clamp(2rem, 6vw, 4rem); margin-bottom: 15px; letter-spacing: -2px; }
        header span { color: var(--neon); }
        header p { color: #888; max-width: 600px; margin: 0 auto; font-size: 1.1rem; }

        /* Dashboard Grid */
        .main-container { padding: 40px 8%; display: grid; grid-template-columns: 1fr 350px; gap: 30px; }

        .card { 
            background: var(--card); border: 1px solid var(--border); 
            border-radius: 24px; padding: 30px; backdrop-filter: blur(20px);
            transition: 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .card:hover { border-color: var(--neon); transform: translateY(-5px); }

        /* Bot Alanı */
        .bot-zone { 
            background: rgba(0,0,0,0.4); border: 2px dashed var(--border); 
            border-radius: 20px; padding: 50px; text-align: center; margin-top: 20px;
        }
        .btn-connect {
            display: inline-block; padding: 20px 50px; background: #fff; color: #000;
            text-decoration: none; border-radius: 15px; font-family: 'Orbitron';
            font-weight: 900; font-size: 1.1rem; transition: 0.3s;
            box-shadow: 0 10px 30px rgba(0, 242, 255, 0.2);
        }
        .btn-connect:hover { background: var(--neon); transform: scale(1.05); box-shadow: 0 15px 45px rgba(0, 242, 255, 0.4); }

        /* Sidebar Verileri */
        .side-item { padding: 15px 0; border-bottom: 1px solid rgba(255,255,255,0.05); }
        .side-item b { color: var(--neon); display: block; font-size: 0.7rem; text-transform: uppercase; margin-bottom: 5px; }

        /* Topluluk */
        .post { background: rgba(255,255,255,0.02); padding: 15px; border-radius: 12px; margin-top: 15px; border-left: 4px solid var(--purple); }

        @media (max-width: 1000px) { .main-container { grid-template-columns: 1fr; } }
    </style>
</head>
<body>

    <div class="bg-overlay"></div>

    <nav>
        <div class="logo">İRONSOUL</div>
        <div class="nav-links">
            <a href="#analiz">kuponAi</a>
            <a href="#topluluk">Topluluk</a>
            <a href="javascript:void(0)" onclick="alert('Üyelik Sistemi Çok Yakında!')" style="background:var(--neon); color:#000; padding:8px 15px; border-radius:8px;">GİRİŞ YAP</a>
        </div>
    </nav>

    <header>
        <h1>İRONSOUL<span>AI</span></h1>
        <p>Yapay zeka odaklı veri işleme terminali. İstatistikleri kazanca dönüştürmek için kuponAi modülüne bağlanın.</p>
    </header>

    <div class="main-container">
        <div class="content">
            <div class="card" id="analiz">
                <h2 style="font-family:'Orbitron'; font-size: 1.2rem; color: var(--neon); margin-bottom: 10px;">CORE ENGINE</h2>
                <p style="color:#666; font-size: 0.9rem;">Sistem durumu: <span style="color:#00ff00">ONLINE</span> | Versiyon: v5.0 Stable</p>
                
                <div class="bot-zone">
                    <div style="font-size: 3rem; margin-bottom: 20px;">🤖</div>
                    <h3 style="font-family:'Orbitron'; margin-bottom: 15px;">kuponAi BAĞLANTISI</h3>
                    <p style="color:#aaa; margin-bottom: 30px; font-size: 0.9rem;">Analizler, sakatlık raporları ve günün banko tahminleri için terminali başlatın.</p>
                    <a href="https://poe.com/kuponAi" target="_blank" class="btn-connect">ANALİZİ BAŞLAT</a>
                </div>

                <div id="topluluk" style="margin-top: 40px;">
                    <h2 style="font-family:'Orbitron'; font-size: 1rem;">TOPLULUK ANALİZLERİ</h2>
                    <div class="post">
                        <b style="font-size: 0.8rem; color:var(--neon)">@Analiz_Ustasi:</b>
                        <p style="font-size: 0.85rem; color:#ccc; margin-top:5px;">kuponAi'nin Dortmund tahmini kusursuz çalıştı. Akşam için hazırız!</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="sidebar">
            <div class="card">
                <h2 style="font-family:'Orbitron'; font-size: 1rem; margin-bottom: 20px;">SİSTEM VERİLERİ</h2>
                
                <div class="side-item">
                    <b>BAŞARI ORANI</b>
                    <div style="font-size: 1.2rem; font-weight: 900;">%91.4</div>
                </div>
                
                <div class="side-item">
                    <b>AKTİF LİGLER</b>
                    <p style="font-size: 0.85rem; color:#888;">Tüm Avrupa Ligleri, Türkiye Süper Ligi, NBA</p>
                </div>

                <div class="side-item">
                    <b>GÜVEN ENDEKSİ</b>
                    <div style="height: 6px; background:#111; border-radius: 3px; margin-top: 10px;">
                        <div style="width: 88%; height: 100%; background:var(--neon); box-shadow: 0 0 15px var(--neon);"></div>
                    </div>
                </div>

                <div class="side-item" style="border:none; margin-top: 20px;">
                    <p style="font-size: 0.7rem; color:#444; line-height: 1.4;">
                        *Bu platform bir yatırım tavsiyesi vermez. Yapay zeka verileri ihtimaller üzerine kuruludur.
                    </p>
                </div>
            </div>
        </div>
    </div>

    <footer style="text-align:center; padding: 40px; color:#222; font-size: 0.7rem; letter-spacing: 2px;">
        DESIGNED BY IRONSOULAI PROTOCOL &copy; 2026
    </footer>

</body>
</html>
