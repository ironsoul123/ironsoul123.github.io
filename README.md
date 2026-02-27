<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IronSoulAI | kuponAi Terminal</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --neon-blue: #00f2ff;
            --neon-purple: #7000ff;
            --bg: #050505;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(0, 242, 255, 0.2);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background-color: var(--bg); color: #fff; font-family: 'Inter', sans-serif; overflow-x: hidden; }

        /* Arka Plan Görseli */
        .background-overlay {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(rgba(0,0,0,0.8), rgba(0,0,0,0.8)), url('tema.jpg') center/cover no-repeat;
            z-index: -1; filter: blur(5px);
        }

        /* Navigasyon */
        nav {
            padding: 20px 8%; display: flex; justify-content: space-between; align-items: center;
            background: rgba(0,0,0,0.8); border-bottom: 1px solid var(--border);
            position: sticky; top: 0; z-index: 1000; backdrop-filter: blur(10px);
        }
        .logo { font-family: 'Orbitron'; font-size: 1.5rem; color: var(--neon-blue); letter-spacing: 3px; font-weight: bold; }
        .nav-links a { color: #fff; text-decoration: none; margin-left: 20px; font-size: 0.8rem; text-transform: uppercase; transition: 0.3s; }
        .nav-links a:hover { color: var(--neon-blue); }

        /* Hero Bölümü */
        .hero { padding: 100px 8% 60px; text-align: center; }
        .hero h1 { font-family: 'Orbitron'; font-size: 3.5rem; margin-bottom: 20px; background: linear-gradient(to right, #fff, var(--neon-blue)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .hero p { color: #888; max-width: 700px; margin: 0 auto 40px; line-height: 1.6; }

        /* Ana Dashboard Grid */
        .container { padding: 0 8% 80px; display: grid; grid-template-columns: 2fr 1fr; gap: 30px; }

        /* Kartlar */
        .card { background: var(--glass); border: 1px solid var(--border); border-radius: 20px; padding: 30px; backdrop-filter: blur(10px); height: 100%; }
        h2 { font-family: 'Orbitron'; font-size: 1.1rem; margin-bottom: 20px; color: var(--neon-blue); display: flex; align-items: center; gap: 10px; }

        /* Bot Butonu Tasarımı */
        .bot-box { 
            background: rgba(0,0,0,0.5); border-radius: 15px; padding: 40px; text-align: center;
            border: 1px dashed var(--neon-blue); transition: 0.3s;
        }
        .bot-box:hover { background: rgba(0, 242, 255, 0.05); }
        .cta-button {
            display: inline-block; padding: 18px 45px; background: var(--neon-blue); color: #000;
            text-decoration: none; border-radius: 50px; font-family: 'Orbitron'; font-weight: bold;
            box-shadow: 0 0 20px rgba(0, 242, 255, 0.4); transition: 0.3s;
        }
        .cta-button:hover { transform: scale(1.05); box-shadow: 0 0 40px var(--neon-blue); }

        /* Tablolar ve Veriler */
        table { width: 100%; border-collapse: collapse; margin-top: 10px; }
        td { padding: 12px 0; border-bottom: 1px solid rgba(255,255,255,0.05); font-size: 0.85rem; }
        .badge { background: var(--neon-purple); padding: 3px 8px; border-radius: 4px; font-size: 0.7rem; }

        /* Topluluk Paylaşımları */
        .post { background: rgba(255,255,255,0.02); padding: 15px; border-radius: 12px; margin-bottom: 15px; border-left: 3px solid var(--neon-purple); }

        /* Mobil Uyumluluk */
        @media (max-width: 968px) {
            .container { grid-template-columns: 1fr; }
            .hero h1 { font-size: 2.2rem; }
        }
    </style>
</head>
<body>

    <div class="background-overlay"></div>

    <nav>
        <div class="logo">İRONSOULAI</div>
        <div class="nav-links">
            <a href="#analiz">Analiz</a>
            <a href="#topluluk">Topluluk</a>
            <a href="#" style="color: var(--neon-blue);">Giriş Yap</a>
        </div>
    </nav>

    <header class="hero">
        <h1>kuponAi PROTOCOL</h1>
        <p>Yapay zeka odaklı analiz terminali ile spor dünyasındaki verileri kazanca dönüştürün. Hızlı, güvenilir ve tamamen dijital.</p>
        <div style="display: flex; justify-content: center; gap: 20px;">
            <div style="text-align: center;"><h4 style="color: var(--neon-blue); font-family: 'Orbitron';">%92</h4><span style="font-size: 0.7rem; color: #555;">İSABET</span></div>
            <div style="text-align: center;"><h4 style="color: var(--neon-blue); font-family: 'Orbitron';">24/7</h4><span style="font-size: 0.7rem; color: #555;">TARAMA</span></div>
        </div>
    </header>

    <div class="container">
        <div class="main-content">
            <div class="card" id="analiz">
                <h2>🤖 ANALİZ MOTORU</h2>
                <div class="bot-box">
                    <p style="margin-bottom: 25px; color: #ccc;">kuponAi yapay zekasıyla anlık bağlantı kurun, lig analizlerini ve günün kuponlarını hemen alın.</p>
                    <a href="https://poe.com/kuponAi" target="_blank" class="cta-button">BOTU BAŞLAT</a>
                </div>

                <div style="margin-top: 40px;">
                    <h2>👥 TOPLULUK AKIŞI</h2>
                    <div class="post">
                        <div style="font-weight: bold; font-size: 0.8rem; margin-bottom: 5px;">@AnalistKral</div>
                        <p style="font-size: 0.85rem; color: #aaa;">Yapay zekanın Bayern tahmini yine tuttu! Seri devam ediyor.</p>
                    </div>
                    <div class="post">
                        <div style="font-weight: bold; font-size: 0.8rem; margin-bottom: 5px;">@VipBettr</div>
                        <p style="font-size: 0.85rem; color: #aaa;">Gecenin kuponu hazır, kuponAi'ye onaylattım. Bol şans.</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="sidebar">
            <div class="card">
                <h2>🏆 LİG ANALİZLERİ</h2>
                <table>
                    <tr><td>Süper Lig</td><td><span class="badge">AKTİF</span></td></tr>
                    <tr><td>Premier League</td><td><span class="badge">AKTİF</span></td></tr>
                    <tr><td>Bundesliga</td><td><span class="badge">AKTİF</span></td></tr>
                    <tr><td>Champions League</td><td><span class="badge" style="background:var(--neon-blue); color:#000;">KRİTİK</span></td></tr>
                </table>
            </div>

            <div class="card" style="margin-top: 30px;">
                <h2>📢 SİSTEM HABERLERİ</h2>
                <p style="font-size: 0.8rem; color: #777; line-height: 1.6;">
                    • v5.0 güncellemesi ile analiz hızı artırıldı.<br>
                    • Yeni ligler sisteme entegre edildi.<br>
                    • Üyelik sistemi yak
