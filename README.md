<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IronSoulAI | kuponAi Strateji Merkezi</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Rajdhani:wght@300;500;700&display=swap');

        :root {
            --neon-blue: #00f2ff;
            --dark-bg: #050a14;
        }

        body {
            background-color: var(--dark-bg);
            color: #e2e8f0;
            font-family: 'Rajdhani', sans-serif;
            margin: 0;
            padding: 0;
        }

        .orbitron { font-family: 'Orbitron', sans-serif; }

        /* Glassmorphism Paneller */
        .glass-panel {
            background: rgba(15, 23, 42, 0.7);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(0, 242, 255, 0.2);
            box-shadow: 0 10px 40px 0 rgba(0, 0, 0, 0.9);
        }

        .neon-text {
            text-shadow: 0 0 12px rgba(0, 242, 255, 0.8);
            color: var(--neon-blue);
        }

        .neon-border-bottom {
            border-bottom: 2px solid var(--neon-blue);
        }

        /* Bot Çerçevesi İçin Özel Efekt */
        .bot-container {
            position: relative;
            background: #000;
            border-radius: 1rem;
            overflow: hidden;
            border: 2px solid rgba(0, 242, 255, 0.1);
        }

        .bot-container::before {
            content: '';
            position: absolute;
            top: -2px; left: -2px; right: -2px; bottom: -2px;
            background: linear-gradient(45deg, transparent, var(--neon-blue), transparent);
            z-index: -1;
            animation: border-glow 4s linear infinite;
        }

        @keyframes border-glow {
            0% { opacity: 0.3; }
            50% { opacity: 0.7; }
            100% { opacity: 0.3; }
        }

        .custom-scroll::-webkit-scrollbar { width: 4px; }
        .custom-scroll::-webkit-scrollbar-thumb { background: var(--neon-blue); border-radius: 10px; }
    </style>
</head>
<body>

    <nav class="p-5 flex justify-between items-center border-b border-cyan-900/30 bg-black/40 sticky top-0 z-50">
        <div class="text-2xl font-bold orbitron neon-text tracking-widest">IRONSOULAI</div>
        <div class="hidden md:flex space-x-8 text-xs uppercase tracking-[0.2em]">
            <a href="#" class="hover:text-cyan-400 transition">Tahmin Paneli</a>
            <a href="#" class="hover:text-cyan-400 transition">İstatistikler</a>
            <a href="#" class="text-cyan-400 border-b border-cyan-400">kuponAi BOT</a>
        </div>
    </nav>

    <main class="container mx-auto px-4 py-10">
        
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 mb-16 items-center">
            <div class="lg:col-span-5 space-y-6">
                <div class="inline-block px-3 py-1 border border-cyan-500/50 rounded text-cyan-400 text-xs orbitron mb-2">AI POWERED ENGINE</div>
                <h1 class="text-6xl font-black orbitron leading-tight tracking-tighter">
                    VERİDEN <br> <span class="neon-text underline decoration
