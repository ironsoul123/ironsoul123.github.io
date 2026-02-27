<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IronSoulAI | kuponAi Analiz Merkezi</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Inter:wght@300;500;700&display=swap" rel="stylesheet">
    <style>
        :root { --neon-blue: #00f2ff; --neon-purple: #7000ff; --dark-bg: #03080f; --glass: rgba(255, 255, 255, 0.05); }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background-color: var(--dark-bg); color: #ffffff; font-family: 'Inter', sans-serif; scroll-behavior: smooth; }
        
        nav { display: flex; justify-content: space-between; align-items: center; padding: 15px 8%; background: rgba(3, 8, 15, 0.95); border-bottom: 1px solid rgba(0,242,255,0.2); position: sticky; top: 0; z-index: 1000; }
        .logo { font-family: 'Orbitron', sans-serif; font-size: 1.4rem; background: linear-gradient(to right, var(--neon-blue), var(--neon-purple)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-weight: bold; }
        .nav-links a { color: #ccc; text-decoration: none; margin-left: 20px; font-size: 0.85rem; font-weight: 500; transition: 0.3s; }
        .btn-login { background: var(--neon-blue); color: #000 !important; padding: 8px 18px; border-radius: 20px; font-weight: bold !important; }

        .section { padding: 40px 8%; }
        .grid { display: grid; grid-template-columns: 2fr 1fr; gap: 30px; }
        .card { background: var(--glass); border: 1px solid rgba(255,255,255,0.1); border-radius: 20px; padding: 25px; backdrop-filter: blur(10px); height: fit-content; }
        h2 { font-family: 'Orbitron', sans-serif; font-size: 1.2rem; margin-bottom: 20px; color: var(--neon-blue); }

        /* Bot Tanıtım Alanı */
        .bot-placeholder {
            width: 100%; height: 500px; border-radius: 15px; 
            background: linear-gradient(45deg, #000, #05101a);
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            border: 2px dashed var(--neon-blue); text-align: center; padding: 20px;
        }

        .btn-ai {
            background: linear-gradient(to right, var(--neon-blue), var(--neon-purple));
            color: white; padding: 15px 40px; border-radius: 50px;
            font-family: 'Orbitron', sans-serif; text-decoration: none; font-weight: bold;
            box-shadow: 0 0 20px rgba(0, 242, 255, 0.5); transition: 0.3s; margin-top: 20px;
        }
        .btn-ai:hover { transform: scale(1.05); box-shadow: 0 0 40px var(--neon-blue); }

        /* Takım Tablosu */
        table { width: 100%; border-collapse: collapse; }
        td { padding: 12px; font-size: 0.85rem; border-bottom: 1px solid rgba(255,255,255,0.05); }
        .power-bar { height: 6px; background: #222; border-radius: 3px; width: 80px; }
        .power-fill { height: 100%; background: var(--neon-blue); }

        /* Floating Bot Icon */
        .floating-bot {
            position: fixed; bottom: 30px; right: 30px; width: 60px; height: 60px;
            background: var(--neon-blue); border-radius: 50%; display: flex;
            align-items: center; justify-content: center; font-size: 1.5rem;
            box-shadow: 0 0 20px var(--neon-blue); text-decoration: none; z-index: 1000;
            animation: pulse 2s infinite;
        }

        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }
        @media (max-width: 968px) { .grid { grid-template-columns: 1fr; } }
    </style>
</head>
<body>

    <nav>
        <div class="logo">İRONSOULAI</div>
        <div class="nav-links">
            <a href="#analiz">kuponAi</a>
            <a href="#topluluk">Topluluk</a>
            <a href="javascript:void(0)" class="btn-login">GİRİŞ YAP</a>
        </div>
    </nav>

    <section class="section" id="analiz">
        <div class="grid">
            <div class="card">
                <h2>🤖 KUPONAI ANALİZ MOTORU</h2>
                <div class="bot-placeholder">
                    <div style="font-size: 4rem; margin-bottom: 20px;">🧠</div>
                    <h3 style="font-family: 'Orbitron'; margin-bottom: 10px;">Yapay Zeka Bağlantısı Hazır</h3>
                    <p style="color: #aaa; max-width: 400px; font-size: 0.9rem;">
                        Analizleri gerçekleştirmek, sakatlıkları kontrol etmek ve banko tahminleri almak için kuponAi modülünü başlatın.
                    </p>
                    <a href="https://poe.com/kuponAi" target="_blank" class="btn-ai">ANALİZİ BAŞLAT</a>
                </div>
                
                <p style="margin-top: 20px; font-size: 0.8rem; color: #555; text-align: center;">
                    *Not: Analizler yapay zeka tarafından sağlanır, yatırım tavsiyesi değildir.
                </p>
            </div>

            <div>
                <div class="card">
                    <h2>📊 SİSTEM DURUMU</h2>
                    <table>
                        <tr><td>Bot Durumu:</td><td style="color:var(--neon-blue)">AKTİF</td></tr>
                        <tr><td>İsabet Oranı:</td><td style="color:#00ff00">%88.2</td></tr>
                        <tr><td>Gecikme:</td><td>1.2ms</td></tr>
                    </table>
                </div>

                <div class="card" style="margin-top: 20px;">
                    <h2>🔥 GÜNÜN ANALİZİ</h2>
                    <div style="background: rgba(0,0,0,0.3); padding: 15px; border-radius: 10px;">
                        <p style="font-weight: bold; color: var(--neon-blue);">Fenerbahçe - Kasımpaşa</p>
                        <p style="font-size: 0.8rem; margin-top: 5px;">AI Tahmini: MS 1 & 2.5 Üst</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <a href="https://poe.com/kuponAi" target="_blank" class="floating-bot" title="Botu Aç">
        🤖
    </a>

    <footer style="text-align: center; padding: 40px; color: #333; font-size: 0.8rem;">
        &copy; 2026 IronSoulAI. Powered by kuponAi.
    </footer>

</body>
</html>
