<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IronSoulAI | Neural Analysis Terminal</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=JetBrains+Mono:wght@300;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --neon: #00f2ff;
            --purple: #bc13fe;
            --dark: #050505;
            --card-bg: rgba(15, 15, 15, 0.8);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; cursor: crosshair; }
        
        body { 
            background: var(--dark); 
            color: #fff; 
            font-family: 'JetBrains+Mono', monospace;
            overflow: hidden; /* Scroll yerine terminal hissi */
            height: 100vh;
        }

        /* ARKA PLAN EFEKTİ */
        .bg-grid {
            position: fixed; top: 0; left: 0; width: 100%; height: 100%;
            background-image: linear-gradient(rgba(0, 242, 255, 0.05) 1px, transparent 1px),
                              linear-gradient(90deg, rgba(0, 242, 255, 0.05) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: -1;
            animation: gridMove 20s linear infinite;
        }
        @keyframes gridMove { from { transform: translateY(0); } to { transform: translateY(50px); } }

        /* ANA YAPI */
        .wrapper { display: grid; grid-template-columns: 280px 1fr 320px; height: 100vh; gap: 10px; padding: 10px; }

        /* SIDEBAR */
        aside { 
            background: var(--card-bg); border: 1px solid rgba(0,242,255,0.1); 
            border-radius: 15px; padding: 30px; display: flex; flex-direction: column; gap: 20px;
        }

        .status-light { width: 10px; height: 10px; background: #00ff00; border-radius: 50%; display: inline-block; box-shadow: 0 0 10px #00ff00; }

        /* ANA PANEL */
        main { display: grid; grid-template-rows: auto 1fr; gap: 10px; }
        
        .header-bar { 
            background: var(--card-bg); border: 1px solid rgba(0,242,255,0.1);
            border-radius: 15px; padding: 20px; display: flex; justify-content: space-between; align-items: center;
        }

        .main-display {
            background: rgba(0,0,0,0.5); border: 1px solid var(--neon);
            border-radius: 15px; position: relative; overflow: hidden;
            display: flex; flex-direction: column; align-items: center; justify-content: center;
            background-image: url('tema.jpg'); background-size: cover; background-position: center;
        }

        .overlay { 
            position: absolute; top:0; left:0; width:100%; height:100%; 
            background: rgba(0,0,0,0.7); backdrop-filter: blur(2px); 
        }

        /* BUTONLAR */
        .cyber-btn {
            position: relative; z-index: 10; padding: 20px 40px;
            background: transparent; border: 2px solid var(--neon);
            color: var(--neon); font-family: 'Orbitron'; font-weight: bold;
            text-transform: uppercase; letter-spacing: 5px; transition: 0.3s;
            text-decoration: none; overflow: hidden;
        }
        .cyber-btn:hover { background: var(--neon); color: #000; box-shadow: 0 0 50px var(--neon); }

        /* SAĞ PANEL: VERİ AKIŞI */
        .data-panel { 
            background: var(--card-bg); border: 1px solid rgba(0,242,255,0.1);
            border-radius: 15px; padding: 20px; display: flex; flex-direction: column; gap: 15px;
        }

        .data-row { font-size: 0.75rem; border-bottom: 1px solid rgba(255,255,255,0.05); padding-bottom: 5px; }
        .data-row span { color: var(--neon); }

        /* LOGO */
        .logo { font-family: 'Orbitron'; font-size: 1.5rem; color: var(--neon); text-shadow: 0 0 10px var(--neon); }

        @media (max-width: 1000px) {
            .wrapper { grid-template-columns: 1fr; overflow-y: auto; }
            aside, .data-panel { display: none; }
            .main-display { height: 400px; }
        }
    </style>
</head>
<body>

    <div class="bg-grid"></div>

    <div class="wrapper">
        <aside>
            <div class="logo">IRON SOUL</div>
            <div style="font-size: 0.8rem; color: #555;">NEURAL TERMINAL v4.0</div>
            
            <nav style="margin-top: 40px; display: flex; flex-direction: column; gap: 15px;">
                <div class="data-row">SYSTEM STATUS: <span class="status-light"></span></div>
                <div class="data-row">AI CORE: <span>READY</span></div>
                <div class="data-row">UPTIME: <span>99.9%</span></div>
            </nav>

            <div style="margin-top: auto; font-size: 0.7rem; color: #333;">
                ACCESS LEVEL: <span style="color: var(--purple)">ADMINISTRATOR</span>
            </div>
        </aside>

        <main>
            <div class="header-bar">
                <div style="font-family: 'Orbitron'; font-size: 0.9rem;">MARKET ANALYZER</div>
                <div style="color: #666; font-size: 0.8rem;" id="clock">19:34:02</div>
            </div>

            <div class="main-display">
                <div class="overlay"></div>
                <h2 style="font-family: 'Orbitron'; z-index: 10; margin-bottom: 30px; letter-spacing: 10px; text-align: center;">kuponAi ENGINE</h2>
                <a href="https://poe.com/kuponAi" target="_blank" class="cyber-btn">BAĞLANTIYI KUR</a>
            </div>
        </main>

        <div class="data-panel">
            <h3 style="font-family: 'Orbitron'; font-size: 0.8rem; margin-bottom: 10px; color: var(--purple);">LIVE STREAM</h3>
            <div class="data-row">SCANNING: <span>PREMIER LEAGUE...</span></div>
            <div class="data-row">MATCH: <span>ARS vs LIV</span></div>
            <div class="data-row">PRO
