    /* --- CSS RESET & VARIABLES --- */
    :root {
        --bg-body: #050505;       
        --bg-surface: #141414;    
        --primary: #E50914;       
        --text-main: #ffffff;
        --text-muted: #a3a3a3;
        --nav-blur: rgba(20, 20, 20, 0.85); /* Efek Kaca */
    }

    * { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
    
    body {
        margin: 0; padding: 0;
        background-color: var(--bg-body);
        color: var(--text-main);
        font-family: 'Outfit', sans-serif;
        padding-top: 60px; /* Space untuk Header Fixed */
        padding-bottom: 40px;
    }

    /* --- UI: HEADER (APP BAR) --- */
    .app-header {
        position: fixed; top: 0; left: 0; right: 0;
        height: 60px;
        background: var(--nav-blur);
        backdrop-filter: blur(12px); /* Efek Blur Premium */
        -webkit-backdrop-filter: blur(12px);
        display: flex; align-items: center; justify-content: space-between;
        padding: 0 20px;
        z-index: 1000;
        border-bottom: 1px solid rgba(255,255,255,0.05);
    }

    .logo {
        font-size: 20px; font-weight: 800;
        letter-spacing: -0.5px;
        color: var(--primary);
        text-transform: uppercase;
    }
    .logo span { color: #fff; }

    /* --- UI: HOME GRID (NETFLIX STYLE) --- */
    #home-view {
        padding: 20px;
        display: none; /* Logic JS akan mengaturnya */
        animation: fadeIn 0.5s ease;
    }

    .section-title {
        font-size: 16px; font-weight: 600; color: var(--text-main);
        margin-bottom: 15px; display: flex; align-items: center; gap: 8px;
    }

    .video-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr); /* 2 Kolom di HP */
        gap: 16px;
    }

    /* Kartu Video */
    .v-card {
        background: var(--bg-surface);
        border-radius: 12px;
        overflow: hidden;
        cursor: pointer;
        transition: transform 0.2s, box-shadow 0.2s;
        border: 1px solid rgba(255,255,255,0.05);
    }

    .v-card:active { transform: scale(0.96); } /* Efek klik membal */

    .thumb-box {
        position: relative;
        width: 100%;
        padding-bottom: 56.25%; /* Rasio 16:9 */
        background: #000;
    }

    .thumb-box img {
        position: absolute; top: 0; left: 0; width: 100%; height: 100%;
        object-fit: cover;
        transition: opacity 0.3s;
    }

    /* Overlay Icon Play saat hover/tampil */
    .play-overlay {
        position: absolute; top: 0; left: 0; width: 100%; height: 100%;
        background: rgba(0,0,0,0.3);
        display: flex; align-items: center; justify-content: center;
        opacity: 0; transition: opacity 0.3s;
    }
    .v-card:hover .play-overlay { opacity: 1; }
    .play-icon-big {
        background: rgba(255, 255, 255, 0.2);
        backdrop-filter: blur(4px);
        border-radius: 50%; width: 40px; height: 40px;
        display: flex; align-items: center; justify-content: center;
        color: #fff;
    }

    .card-info { padding: 12px; }
    .card-title {
        font-size: 13px; font-weight: 500; line-height: 1.4;
        color: #ddd;
        display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; overflow: hidden;
    }

    /* --- UI: PLAYER VIEW --- */
    #player-view { display: none; animation: slideUp 0.4s cubic-bezier(0.2, 0.8, 0.2, 1); }

    .sticky-player {
        position: sticky; top: 60px; /* Di bawah header */
        z-index: 900;
        background: #000;
        width: 100%; padding-bottom: 56.25%;
        box-shadow: 0 20px 50px rgba(0,0,0,0.5);
    }
    
    .sticky-player iframe {
        position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;
    }

    .player-body { padding: 20px; max-width: 800px; margin: 0 auto; }

    .video-main-title {
        font-size: 18px; font-weight: 700; line-height: 1.3; margin-bottom: 8px;
    }
    
    .video-meta {
        font-size: 12px; color: var(--text-muted); margin-bottom: 20px;
        display: flex; gap: 10px;
    }
    .badge { background: #222; padding: 2px 6px; border-radius: 4px; border: 1px solid #333; }

    /* Tombol Aksi (Pill Shape) */
    .action-row {
        display: flex; gap: 10px; margin-bottom: 25px;
    }
    
    .btn-pill {
        flex: 1;
        display: flex; align-items: center; justify-content: center; gap: 8px;
        padding: 12px;
        border-radius: 50px;
        border: none; font-family: inherit; font-size: 14px; font-weight: 600;
        cursor: pointer; transition: 0.2s;
    }
    
    .btn-primary { background: var(--text-main); color: #000; }
    .btn-secondary { background: #262626; color: var(--text-main); }
    .btn-primary:active, .btn-secondary:active { transform: scale(0.95); opacity: 0.8; }

    /* Area Iklan (Dotted Border) */
    .ad-container {
        width: 100%; min-height: 250px;
        background: #0a0a0a;
        border: 2px dashed #222; border-radius: 12px;
        display: flex; flex-direction: column;
        align-items: center; justify-content: center;
        color: #444; font-size: 12px; letter-spacing: 1px;
    }

    /* --- TOAST NOTIFICATION (Custom Alert) --- */
    #custom-toast {
        visibility: hidden;
        min-width: 250px;
        background-color: #222;
        color: #fff;
        text-align: center;
        border-radius: 50px;
        padding: 14px 24px;
        position: fixed;
        z-index: 2000;
        left: 50%;
        bottom: 30px;
        transform: translateX(-50%) translateY(20px);
        opacity: 0;
        transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        font-weight: 500;
        border: 1px solid #333;
        display: flex; align-items: center; justify-content: center; gap: 10px;
    }

    #custom-toast.show {
        visibility: visible;
        transform: translateX(-50%) translateY(0);
        opacity: 1;
    }

    
    @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    @keyframes slideUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }

    /* Responsive Desktop */
    @media (min-width: 768px) {
        .video-grid { grid-template-columns: repeat(4, 1fr); gap: 20px; }
        .player-body { padding: 30px 0; }
    }
