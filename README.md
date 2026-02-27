<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IronSoulAI | Profesyonel Bahis Analiz Platformu</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Inter:wght@300;500;700&display=swap" rel="stylesheet">
    <style>
        :root { --neon-blue: #00f2ff; --neon-purple: #7000ff; --dark-bg: #03080f; --glass: rgba(255, 255, 255, 0.05); }
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background-color: var(--dark-bg); color: #ffffff; font-family: 'Inter', sans-serif; scroll-behavior: smooth; }
        
        /* Navigasyon */
        nav { display: flex; justify-content: space-between; align-items: center; padding: 15px 8%; background: rgba(3, 8, 15, 0.95); border-bottom: 1px solid rgba(0,242,255,0.2); position: sticky; top: 0; z-index: 1000; }
        .logo { font-family: 'Orbitron', sans-serif; font-size: 1.4rem; background: linear-gradient(to right, var(--neon-blue), var(--neon-purple)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-weight: bold; }
        .nav-links a { color: #ccc; text-decoration: none; margin-left: 20px; font-size: 0.85rem; font-weight: 500; transition: 0.3s; }
        .nav-links a:hover { color: var(--neon-blue); }
        .btn-login { background: var(--neon-blue); color: #000 !important; padding: 8px 18px; border-radius: 20px; font-weight: bold !important; }

        /* Ortak Konteyner */
        .section { padding: 60px 8%; }
        .grid { display: grid; grid-template-columns: 2fr 1fr; gap: 30px; }
        .card { background: var(--glass); border: 1px solid rgba(255,255,255,0.1); border-radius: 20px; padding: 25px; backdrop-filter: blur(10px); }
        h2 { font-family: 'Orbitron', sans-serif; font-size: 1.2rem; margin-bottom: 20px; color: var(--neon-blue); display: flex; align-items: center; gap: 10px; }

        /* Poe Analiz Paneli */
        .iframe-container { width: 100%; height: 650px; border-radius: 15px; overflow: hidden; background: #000; border: 1px solid var(--neon-blue); }
        iframe { width: 100%; height: 100%; border: none; }

        /* Haber Kartları */
        .news-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 20px; }
        .news-item { background: rgba(255,255,255,0.02); border-radius: 12px; overflow: hidden; transition: 0.3s; border: 1px solid rgba(255,255,255,0.05); }
        .news-item:hover { transform: translateY(-5px); border-color: var(--neon-blue); }
        .news-img { width: 100%; height: 120px; background: #111; object-fit: cover; }
        .news-content { padding: 12px; }
        .news-content h4 { font-size: 0.9rem; margin-bottom: 5px; }
        .news-content p { font-size: 0.75rem; color: #888; }

        /* Takım Analiz Tablosu */
        table { width: 100%; border-collapse: collapse; margin-top: 10px; }
        th { text-align: left; font-size: 0.8rem; color: #555; padding: 10px; }
        td { padding: 12px; font-size: 0.85rem; border-bottom: 1px solid rgba(255,255,255,0.05); }
        .power-bar { height: 6px; background: #222; border-radius: 3px; overflow: hidden; width: 100px; }
        .power-fill { height: 100%; background: var(--neon-blue); box-shadow: 0 0 10px var(--neon-blue); }

        /* Giriş Modalı */
        #loginModal { display:none; position:fixed; top:50%; left:50%; transform:translate(-50%, -50%); background:#0a0f18; padding:40px; border-radius:25px; border:1px solid var(--neon-blue); z-index:2000; width:350px; box-shadow: 0 0 50px rgba(0,0,0,0.9); }
        input { width:100%; margin:10px 0; padding:12px; background:#111; border:1px solid #333; color:white; border-radius:8px; }

        /* Mobil */
        @media (max-width: 968px) { .grid { grid-template-columns: 1fr; } .news-grid { grid-template-columns: 1fr; } .hero h1 { font-size: 2rem; } }
    </style>
</head>
<body>

    <div id="loginModal">
        <h2 style="text-align:center">GİRİŞ YAP</h2>
        <input type="email" placeholder="E-posta Adresi">
        <input type="password" placeholder="Şifre">
        <button onclick="alert('Henüz Veritabanı Bağlanmadı!')" style="width:100%; padding:12px; background:var(--neon-blue); border:none; border-radius:8px; font-weight:bold; cursor:pointer; margin-top:10px;">OTURUM AÇ</button>
        <p style="font-size:0.7rem; text-align:center; margin-top:15px; color:#555;">Hesabınız yok mu? <a href="#" style="color:var(--neon-blue)">Kayıt Ol</a></p>
        <button onclick="document.getElementById('loginModal').style.display='none'" style="background:none; color:#ff4d4d; border:none; width:100%; margin-top:10px; cursor:pointer;">Vazgeç</button>
    </div>

    <nav>
        <div class="logo">İRONSOULAI</div>
        <div class="nav-links">
            <a href="#analiz">AI Analiz</a>
            <a href="#haberler">Haberler</a>
            <a href="#takimlar">Takımlar</a>
            <a href="javascript:void(0)" onclick="document.getElementById('loginModal').style.display='block'" class="btn-login">GİRİŞ YAP</a>
        </div>
    </nav>

    <section class="section" id="analiz">
        <div class="grid">
            <div class="card">
                <h2>📊 YAPAY ZEKA TAHMİN MERKEZİ</h2>
                <div class="iframe-container">
                    <iframe src="https://poe.com/chat/4rp9vtaqqutnolld3k"></iframe>
                </div>
            </div>

            <div>
                <div class="card" id="haberler">
                    <h2>🔥 SON DAKİKA</h2>
                    <div class="news-grid">
                        <div class="news-item">
                            <img src="https://images.unsplash.com/photo-1574629810360-7efbbe195018?w=300" class="news-img">
                            <div class="news-content">
                                <h4>Derbi Analizi Yayında</h4>
                                <p>AI, akşamki derbi için %89 isabetli bir skor tahmini yaptı...</p>
                            </div>
                        </div>
                        <div class="news-item">
                            <img src="https://images.unsplash.com/photo-1508098682722-e99c43a406b2?w=300" class="news-img">
                            <div class="news-content">
                                <h4>Kritik Eksik!</h4>
                                <p>Yıldız oyuncu antrenmanda sakatlandı. Oranlar değişiyor...</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="card" id="takimlar" style="margin-top:20px;">
                    <h2>🛡️ TAKIM GÜÇ ANALİZİ</h2>
                    <table>
                        <tr><th>TAKIM</th><th>GÜÇ</th><th>FORM</th></tr>
                        <tr><td>G.Saray</td><td><div class="power-bar"><div class="power-fill" style="width:96%"></div></div></td><td style="color:#00ff00">●●●●○</td></tr>
                        <tr><td>F.Bahçe</td><td><div class="power-bar"><div class="power-fill" style="width:92%"></div></div></td><td style="color:#00ff00">●●●●●</td></tr>
                        <tr><td>Beşiktaş</td><td><div class="power-bar"><div class="power-fill" style="width:85%"></div></div></td><td style="color:#ffae00">●●●○○</td></tr>
                    </table>
                </div>
            </div>
        </div>
    </section>

    <footer style="padding:40px; text-align:center; border-top:1px solid #111; font-size:0.8rem; color:#444;">
        <p>İRONSOULAI &copy; 2026 - Yapay Zeka ile Geleceği Öngör. +18 Sorumlu Bahis.</p>
    </footer>

</body>
</html>
<style>
    /* Topluluk Paneli Özel Stilleri */
    .community-post {
        background: rgba(255, 255, 255, 0.02);
        border-radius: 12px;
        padding: 15px;
        margin-bottom: 15px;
        border-left: 3px solid var(--neon-purple);
        transition: 0.3s;
    }
    .community-post:hover {
        background: rgba(255, 255, 255, 0.05);
        transform: translateX(5px);
    }
    .user-info {
        display: flex;
        align-items: center;
        gap: 10px;
        margin-bottom: 10px;
    }
    .user-avatar {
        width: 30px;
        height: 30px;
        background: var(--neon-purple);
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 0.7rem;
        font-weight: bold;
    }
    .post-coupon {
        background: #000;
        padding: 10px;
        border-radius: 8px;
        font-size: 0.8rem;
        border: 1px dashed #444;
        margin: 10px 0;
    }
    .post-actions {
        display: flex;
        gap: 15px;
        font-size: 0.75rem;
        color: #666;
    }
    .post-actions span:hover {
        color: var(--neon-blue);
        cursor: pointer;
    }
    .share-input {
        width: 100%;
        background: #111;
        border: 1px solid #333;
        color: white;
        padding: 10px;
        border-radius: 8px;
        margin-bottom: 10px;
        resize: none;
    }
</style>

<div class="card" id="topluluk" style="margin-top:20px;">
    <h2>👥 TOPLULUK KUPONLARI</h2>
    
    <div style="margin-bottom: 25px; padding-bottom: 20px; border-bottom: 1px solid #222;">
        <textarea class="share-input" placeholder="Günün kuponunu veya düşüncelerini paylaş..."></textarea>
        <button onclick="alert('Paylaşmak için giriş yapmalısınız!')" style="background:var(--neon-purple); color:white; border:none; padding:8px 15px; border-radius:5px; font-weight:bold; cursor:pointer; float:right;">PAYLAŞ</button>
        <div style="clear:both;"></div>
    </div>

    <div class="community-feed">
        <div class="community-post">
            <div class="user-info">
                <div class="user-avatar">AD</div>
                <span style="font-size: 0.85rem; font-weight: bold;">AnalizDehası_34</span>
                <span style="font-size: 0.7rem; color: #555;">• 12dk önce</span>
            </div>
            <p style="font-size: 0.85rem;">Yapay zekanın Dortmund tercihi mantıklı, yanına şunu ekledim:</p>
            <div class="post-coupon">
                ⚽ Milan - Napoli | MS 1 | 1.85<br>
                ⚽ Lyon - Nice | 2.5 Üst | 1.65
            </div>
            <div class="post-actions">
                <span>🔥 24 Beğeni</span>
                <span>💬 5 Yorum</span>
            </div>
        </div>

        <div class="community-post" style="border-left-color: var(--neon-blue);">
            <div class="user-info">
                <div class="user-avatar" style="background:var(--neon-blue)">BK</div>
                <span style="font-size: 0.85rem; font-weight: bold;">BahisKralı</span>
                <span style="font-size: 0.7rem; color: #555;">• 45dk önce</span>
            </div>
            <p style="font-size: 0.85rem;">IronSoulAI bugün yine döktürüyor, kasa %20 arttı! 🚀</p>
            <div class="post-actions">
                <span>🔥 56 Beğeni</span>
                <span>💬 12 Yorum</span>
            </div>
        </div>
    </div>
</div>
