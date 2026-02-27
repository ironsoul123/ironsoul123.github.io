<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IronSoulAI | Professional AI Betting Analytics</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #00f2ff;
            --accent: #7000ff;
            --bg: #02050a;
            --glass: rgba(255, 255, 255, 0.03);
            --border: rgba(0, 242, 255, 0.15);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: var(--bg); color: #fff; font-family: 'Inter', sans-serif; overflow-x: hidden; }

        /* CANLI SKOR BANDI (TICKER) */
        .ticker-wrap {
            width: 100%; overflow: hidden; background: rgba(0,0,0,0.8);
            border-bottom: 1px solid var(--primary); padding: 10px 0;
            white-space: nowrap; font-family: 'Orbitron', sans-serif; font-size: 0.8rem;
        }
        .ticker { display: inline-block; animation: ticker 30s linear infinite; }
        .ticker-item { display: inline-block; padding: 0 30px; border-right: 1px solid #333; }
        @keyframes ticker { 0% { transform: translateX(100%); } 100% { transform: translateX(-100%); } }

        /* NAVİGASYON */
        nav {
            display: flex; justify-content: space-between; align-items: center;
            padding: 20px 8%; background: rgba(2, 5, 10, 0.9);
            backdrop-filter: blur(20px); position: sticky; top: 0; z-index: 1000;
        }
        .logo { font-family: 'Orbitron', sans-serif; font-size: 1.6rem; font-weight: 700; background: linear-gradient(to right, var(--primary), var(--accent)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; letter-spacing: 3px; }

        /* PREMIUM HERO SECTION */
        .hero {
            padding: 100px 8% 50px; text-align: center;
            background: radial-gradient(circle at 50% 50%, rgba(0, 242, 255, 0.05) 0%, transparent 70%);
        }
        .hero h1 { font-family: 'Orbitron', sans-serif; font-size: 3rem; margin-bottom: 20px; text-shadow: 0 0 30px rgba(0, 242, 255, 0.3); }
        .hero p { color: #888; max-width: 600px; margin: 0 auto 30px; font-size: 1.1rem; }

        /* DASHBOARD GRID */
        .container { padding: 40px 8%; display: grid; grid-template-columns: 2fr 1fr; gap: 30px; }

        .card {
            background: var(--glass); border: 1px solid var(--border);
            border-radius: 24px; padding: 30px; backdrop-filter: blur(15px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.4); transition: 0.4s;
        }
        .card:hover { border-color: var(--primary); transform: translateY(-5px); }

        .btn-ai {
            display: inline-block; width: 100%; padding: 20px; margin-top: 20px;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            color: #000; font-family: 'Orbitron', sans-serif; font-weight: 700;
            text-decoration: none; border-radius: 12px; text-align: center;
            box-shadow: 0 0 30px rgba(0, 242, 255, 0.4); transition: 0.3s;
        }
        .btn-ai:hover { letter-spacing: 2px; box-shadow: 0 0 50px var(--primary); }

        /* STATS BOX */
        .stat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-bottom: 30px; }
        .stat-card { background: rgba(255,255,255,0.02); padding: 20px; border-radius: 15px; text-align: center; border: 1px solid rgba(255,255,255,0.05); }
        .stat-card h4 { color: var(--primary); font-family: 'Orbitron'; font-size: 1.2rem; }
        .stat-card span { font-size: 0.7rem; color: #555; text-transform: uppercase; }

        /* FLOATING ELEMENT */
        .bot-pulse {
            position: fixed; bottom: 30px; right: 30px; width: 65px; height: 65px;
            background: var(--primary); border-radius: 50%; display: flex;
            align-items: center; justify-content: center; font-size: 1.8rem;
            box-shadow: 0 0 30px var(--primary); cursor: pointer; z-index: 1000;
            animation: float 3s ease-in-out infinite;
        }
        @keyframes float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-15px); } }

        @media (max-width: 968px) {
            .container { grid-template-columns: 1fr; }
            .hero h1 { font-size: 2rem; }
        }
    </style>
</head>
<body>

    <div class="ticker-wrap">
        <div class="ticker">
            <span class="ticker-item">🔴 LIVE: Real Madrid 2 - 1 Man City</span>
            <span class="ticker-item">🟢 SUCCESS: Arsenal - MS 1 ✅</span>
            <span class="ticker-item">🟡 PENDING: G.Saray - Beşiktaş | 2.5 ÜST</span>
            <span class="ticker-item">🔴 LIVE: Milan 0 - 0 Inter</span>
            <span class="ticker-item">🟢 SUCCESS: Fenerbahçe - 1.5 ÜST ✅</span>
        </div>
    </div>

    <nav>
        <div class="logo">İRONSOULAI</div>
        <div style="font-size: 0.8rem; color: var(--primary); font-weight: bold;">[ PREMIUM ACCESS ]</div>
    </nav>

    <header class="hero">
        <h1>KUPONAI INTELLIGENCE</h1>
        <p>Geleceği tahmin etmiyoruz, onu verilerle inşa ediyoruz. Yapay zeka destekli en gelişmiş spor analiz laboratuvarına hoş geldiniz.</p>
        <div class="stat-grid" style="max-width: 500px; margin: 0 auto;">
            <div class="stat-card"><h4>%88.4</h4><span>Başarı Oranı</span></div>
            <div class="stat-card"><h4>2.4k</h4><span>Günlük Analiz</span></div>
        </div>
    </header>

    <div class="container">
        <div class="card">
            <h2 style="font-family: 'Orbitron'; margin-bottom: 20px; color: var(--primary);">🤖 CORE ANALYTICS</h2>
            <div style="position: relative; border-radius: 15px; overflow: hidden; margin-bottom: 25px;">
                <img src="tema.jpg" alt="IronSoulAI Banner" style="width: 100%; display: block; filter: brightness(0.6);">
                <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 100%;">
                    <a href="https://poe.com/kuponAi" target="_blank" class="btn-ai" style="width: 80%; margin: 0 auto;">kuponAi MODÜLÜNÜ ÇALIŞTIR</a>
                </div>
            </div>
            <p style="font-size: 0.9rem; color: #666; text-align: center;">Yapay zeka motoruna bağlanarak kişiselleştirilmiş analiz raporu oluşturun.</p>
        </div>

        <div class="side-panel">
            <div class="card" style="margin-bottom: 20px;">
                <h3 style="font-family: 'Orbitron'; font-size: 1rem; color: var(--accent); margin-bottom: 15px;">TOPLULUK SESİ</h3>
                <div style="font-size: 0.85rem; padding: 10px; background: rgba(255,255,255,0.02); border-radius: 10px; border-left: 2px solid var(--accent);">
                    "AI bugün Dortmund maçını bildi, kasa katlandı!" - <b>User_X</b>
                </div>
            </div>

            <div class="card">
                <h3 style="font-family: 'Orbitron'; font-size: 1rem; color: var(--primary); margin-bottom: 15px;">SİSTEM RAPORU</h3>
                <p style="font-size: 0.8rem; color: #888;"><b>Sunucu:</b> Frankfurt-1</p>
                <p style="font-size: 0.8rem; color: #888;"><b>Versiyon:</b> v4.2 Private</p>
                <div style="margin-top: 15px; height: 2px; background: #111; position: relative;">
                    <div style="position: absolute; width: 88%; height: 100%; background: var(--primary); box-shadow: 0 0 10px var(--primary);"></div>
                </div>
                <p style="font-size: 0.7rem; margin-top: 5px; text-align: right;">GÜVEN ENDEKSİ: 88%</p>
            </div>
        </div>
    </div>

    <a href="https://poe.com/kuponAi" target="_blank" class="bot-pulse">🤖</a>

    <footer style="text-align: center; padding: 60px; color: #222; font-size: 0.7rem; letter-spacing: 2px;">
        İRONSOULAI PROTOCOL &copy; 2026 | SECURED ACCESS ONLY
    </footer>

</body>
</html>
