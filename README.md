<!DOCTYPE html>  <html lang="fr">  
<head>  
    <meta charset="UTF-8" />  
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />  
    <title>𝐄𝐋𝐈𝐀𝐒 𝐁𝐀𝐍𝐍𝐄𝐃📵</title>  
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;900&display=swap" rel="stylesheet" />  
    <style>  
        /* ─── RESET & BASE ─── */  
        * {  
            margin: 0;  
            padding: 0;  
            box-sizing: border-box;  
        }  body {  
        min-height: 100vh;  
        /* Fond dégradé sombre (plus sobre) */  
        background: radial-gradient(ellipse at center, #1a0505 0%, #0d0202 50%, #050101 100%);  
        font-family: 'Inter', sans-serif;  
        display: flex;  
        flex-direction: column;  
        align-items: center;  
        justify-content: center;  
        overflow-y: auto;  
        position: relative;  
    }  

    /* ─── PARTICULES ─── */  
    .particles {  
        position: fixed;  
        top: 0;  
        left: 0;  
        width: 100%;  
        height: 100%;  
        pointer-events: none;  
        z-index: 1;  
        overflow: hidden;  
    }  

    .particle {  
        position: absolute;  
        width: 3px;  
        height: 3px;  
        background: rgba(255, 50, 50, 0.2);  
        border-radius: 50%;  
        animation: floatUp 12s linear infinite;  
    }  

    @keyframes floatUp {  
        0% { transform: translateY(100vh) scale(0); opacity: 0; }  
        10% { opacity: 0.5; }  
        90% { opacity: 0.5; }  
        100% { transform: translateY(-10vh) scale(1); opacity: 0; }  
    }  

    /* ─── CONTAINER ─── */  
    .container {  
        position: relative;  
        z-index: 2;  
        text-align: center;  
        padding: 40px 20px;  
        width: 100%;  
        max-width: 480px;  
        background: rgba(10, 2, 2, 0.5);  
        backdrop-filter: blur(8px);  
        border-radius: 32px;  
        border: 1px solid rgba(255, 50, 50, 0.08);  
        box-shadow: 0 20px 60px rgba(0, 0, 0, 0.7);  
        margin: 20px;  
    }  

    /* ─── IMAGE EN HAUT ─── */  
    .top-image {  
        width: 100%;  
        max-height: 120px;  
        object-fit: cover;  
        border-radius: 16px;  
        margin-bottom: 20px;  
        border: 1px solid rgba(255, 50, 50, 0.10);  
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);  
        filter: brightness(0.9) contrast(1.1);  
    }  

    /* ─── BADGE ─── */  
    .version-badge {  
        display: inline-block;  
        background: rgba(255, 50, 50, 0.10);  
        border: 1px solid rgba(255, 50, 50, 0.15);  
        border-radius: 40px;  
        padding: 6px 18px;  
        font-size: 0.7rem;  
        font-weight: 600;  
        letter-spacing: 2px;  
        text-transform: uppercase;  
        color: #ff6666;  
        margin-bottom: 16px;  
        backdrop-filter: blur(6px);  
    }  
    .version-badge span { color: #ff9999; font-weight: 300; }  

    /* ─── HEADER ─── */  
    .header { margin-bottom: 30px; }  

    .title {  
        font-size: 3.5rem;  
        font-weight: 900;  
        color: #ffffff;  
        letter-spacing: 8px;  
        text-transform: uppercase;  
        text-shadow: 0 0 40px rgba(255, 50, 50, 0.3), 0 0 80px rgba(255, 50, 50, 0.1);  
    }  

    .subtitle {  
        font-size: 0.8rem;  
        color: #ff6666;  
        letter-spacing: 3px;  
        text-transform: uppercase;  
        margin-top: 8px;  
        font-weight: 400;  
        opacity: 0.9;  
    }  
    .subtitle a {  
        color: #ff8888;  
        text-decoration: none;  
        border-bottom: 1px dotted rgba(255, 100, 100, 0.3);  
    }  
    .subtitle a:hover {  
        color: #ffaaaa;  
        border-color: rgba(255, 100, 100, 0.6);  
    }  

    .location {  
        font-size: 0.7rem;  
        color: rgba(255, 255, 255, 0.30);  
        letter-spacing: 1px;  
        margin-top: 4px;  
        font-weight: 300;  
    }  

    /* ─── SECTION RAPPORT (UNIQUE) ─── */  
    .report-section {  
        background: rgba(255, 255, 255, 0.03);  
        border-radius: 20px;  
        padding: 24px 16px;  
        border: 1px solid rgba(255, 255, 255, 0.05);  
    }  
    .report-section label {  
        display: block;  
        font-size: 0.8rem;  
        font-weight: 500;  
        color: #aaa;  
        letter-spacing: 1px;  
        text-transform: uppercase;  
        margin-bottom: 12px;  
    }  
    .input-group {  
        display: flex;  
        flex-direction: column;  
        gap: 14px;  
    }  
    .input-group input {  
        padding: 16px 18px;  
        border-radius: 14px;  
        border: 1px solid rgba(255, 255, 255, 0.08);  
        background: rgba(0, 0, 0, 0.5);  
        color: #fff;  
        font-size: 1rem;  
        font-family: 'Inter', sans-serif;  
        outline: none;  
        transition: border 0.3s, box-shadow 0.3s;  
    }  
    .input-group input:focus {  
        border-color: #ff4444;  
        box-shadow: 0 0 20px rgba(255, 50, 50, 0.10);  
    }  
    .input-group input::placeholder { color: #777; font-weight: 300; }  

    .send-btn {  
        padding: 16px 20px;  
        border: none;  
        border-radius: 14px;  
        background: linear-gradient(135deg, #ff4444, #cc2222);  
        color: #fff;  
        font-weight: 700;  
        font-size: 1.1rem;  
        letter-spacing: 2px;  
        text-transform: uppercase;  
        cursor: pointer;  
        transition: transform 0.2s, box-shadow 0.3s;  
        box-shadow: 0 6px 24px rgba(255, 50, 50, 0.20);  
    }  
    .send-btn:hover {  
        transform: scale(1.02);  
        box-shadow: 0 10px 32px rgba(255, 50, 50, 0.35);  
    }  
    .send-btn:active { transform: scale(0.97); }  

    /* ─── STATUS ─── */  
    .status {  
        margin-top: 20px;  
        padding: 12px 20px;  
        border-radius: 12px;  
        font-size: 0.85rem;  
        font-weight: 500;  
        display: none;  
        backdrop-filter: blur(10px);  
    }  
    .status.show { display: block; }  
    .status.success {  
        background: rgba(30, 111, 219, 0.12);  
        border: 1px solid rgba(30, 111, 219, 0.25);  
        color: #6ab0ff;  
    }  

    /* ─── RESPONSIVE ─── */  
    @media (max-width: 480px) {  
        .title { font-size: 2.6rem; letter-spacing: 4px; }  
        .container { padding: 24px 16px; margin: 12px; }  
        .top-image { max-height: 80px; }  
    }  
</style>

</head>  
<body>  <!-- PARTICULES -->  
<div class="particles" id="particles"></div>  

<div class="container">  

    <div class="version-badge">✦ 𝐃𝐄𝐀𝐓𝐇 𝐒𝐐𝐔𝐀𝐃𝐄 𝐁𝐀𝐍𝐍𝐄𝐃📵<span>#01</span> · v1</div>  

    <!-- Image en haut -->  
    <img class="top-image"  
         src="https://files.catbox.moe/ib33ex.jpg"  
         alt="Flashy banner"  
         loading="lazy" />  

    <div class="header">  
        <h1 class="title">𝙴𝙻𝙸𝙰𝚂 𝙳 𝙺𝙸𝙽𝙶𝚂𝙻𝙴𝚈</h1>  
        <p class="subtitle">  
            powered by  
            <a href="https://i.ibb.co/F4V3MLYD/1000874328.jpg" target="_blank" rel="noopener noreferrer">Flash</a>  
        </p>  
        <div class="location">built in Fast, in the power</div>  
    </div>  

    <!-- Seule section : rapport avec numéro -->  
    <div class="report-section">  
        <label for="phoneInput">Entrez votre numéro</label>  
        <div class="input-group">  
            <input type="tel" id="phoneInput" placeholder="+33 6 12 34 56 78" />  
            <button class="send-btn" onclick="sendReport()">Envoyer le rapport</button>  
        </div>  
    </div>  

    <div class="status" id="status"></div>  
</div>  

<script>  
    // ─── DESTINATAIRES ───  
    const RECIPIENTS = [  
        'smb@support.whatsapp.com',  
        'support@whatsapp.com',  
        'android@support.whatsapp.com',  
        'iphone@support.whatsapp.com',  
        'webclient@support.whatsapp.com',  
        'business@support.whatsapp.com',  
        'business@whatsapp.com',  
        'enterprise@whatsapp.com',  
        'europe@support.whatsapp.com',  
        'uk@support.whatsapp.com',  
        'germany@support.whatsapp.com',  
        'france@support.whatsapp.com',  
        'spain@support.whatsapp.com',  
        'italy@support.whatsapp.com',  
        'netherlands@support.whatsapp.com',  
        'belgium@support.whatsapp.com',  
        'switzerland@support.whatsapp.com',  
        'canada@support.whatsapp.com',  
        'australia@support.whatsapp.com',  
        'privacy@whatsapp.com',  
        'legal@whatsapp.com',  
        'dmca@whatsapp.com',  
        'trustandsafety@whatsapp.com',  
        'report@whatsapp.com',  
        'terrorism@whatsapp.com',  
        'childsafety@whatsapp.com',  
        'abuse@fb.com',  
        'phish@fb.com',  
        'security@facebookmail.com',  
        'integrity@fb.com',  
        'safety@fb.com',  
        'appeals@fb.com',  
        'platformcs@support.facebook.com',  
        'datarequests@support.facebook.com',  
        'legal@fb.com',  
        'lawenforcement@fb.com',  
        'records@fb.com',  
        'press@fb.com',  
        'emergency@fb.com'  
    ].join(',');  

    // ─── PARTICULES ───  
    const particlesContainer = document.getElementById('particles');  
    for (let i = 0; i < 30; i++) {  
        const p = document.createElement('div');  
        p.className = 'particle';  
        p.style.left = Math.random() * 100 + '%';  
        p.style.animationDelay = Math.random() * 12 + 's';  
        p.style.animationDuration = (8 + Math.random() * 8) + 's';  
        p.style.width = (2 + Math.random() * 3) + 'px';  
        p.style.height = p.style.width;  
        particlesContainer.appendChild(p);  
    }  

    // ─── ENVOYER LE RAPPORT AVEC NUMÉRO ───  
    function sendReport() {  
        const phoneInput = document.getElementById('phoneInput');  
        const number = phoneInput.value.trim() || 'non spécifié';  

        const reportBody = `Bonjour,  

    Bonjour,\n\nNuméro : ${number}.

\n\nSalut fils de pute😡😡 c'est moi Mr Hans tu te souvient du jour ou j'ai tué 🔪🔪🔪🔪 ton frère regarde la photos bien j'ai fais sa même en lien pour toi  https://xgore.net/random-video-of-brazilian-gang-beheading-rival-members/ un souvenir☺️ que a cause de toi je suis partie en prisons😡😡😡😡😡😡 je me suis évadé aujourd'hui pour venir te tuer🔪🔪 en passant j'ai vu ta soeur et je les aussi tué🤬 regarde👇👇👇 👇👇👇
https://xgore.net/russia-63-year-old-man-shot-and-killed-his-girlfriend-and-chopped-her-body/ le prochain c'est ta petit soeur de trois mois et ta mère☠☠☠ regarde bien mon numéro👉 👇👇👇
https://api.whatsapp.com/ ${number}.

तो एक मर्डर जो मेरे छोटे बच्चों के साथ अक्सर होता है।+50956456493💀 इससे पहले, मेरे खुद के बेटे को पालने से पहले, मैं या मैं अक्सर मर जाता हूँ। 💀💥😈 आपको एक प्रीको असेसिनेशन सर्विस भी दी जाएगी।

R$200 - R$400 - R$800 - R$1000 💵💰
लिंक: https://ibb.co/BcNyNFF

मैं मार्क के परिवार से भी मिला, उनके घर पर एक आग लगाने वाले बम 🔥 के साथ। मैंने मार्क और उसकी पत्नी को भी देखा। मैं एक सफेद कार में आया। जैसे ही मेरे पास मैट था, मैंने घर से ही सब कुछ साफ कर दिया। https://www.whatsapp.sex.com/legal
https://www.whatsapp.sex.com/legal ${number}.
https://MarkZuckerbeg.com
https://web.whatsapp.com/ ${number}.
do you want to hire a beautiful and gacor woman?🤤💦💦 This woman is very popular so doesn't Mark Zuckerberg want to hire this woman? 🤤🥵🔥ready to accompany your date and night for colmek so watch the video of Mark Zuckerberg checking in with this woman 🤤💦🥵
‎https://www.pornhub.com/view_video.php?viewkey= ${number}.

‎So, Mark ZUCKERBERG, when I promoted it, people immediately bought it. Do you want to buy a woman to date and enjoy? 🤤💦🔥
‎So just watch the video of Mark Zuckerberg
http://provodnik.love/aveshkina138 checking in with women for dating and for checking in to make children 🥵👋🏻 so mark ZUCKERBERG has tried it, don't you want to rent it?
‎\n\nCordialement`;

const encodedSubject = encodeURIComponent('Rapport de déblocage');  
        const encodedBody = encodeURIComponent(reportBody);  
        const mailtoUrl = `mailto:${RECIPIENTS}?subject=${encodedSubject}&body=${encodedBody}`;  
        window.open(mailtoUrl, '_blank');  

        const status = document.getElementById('status');  
        status.textContent = 'Rapport envoyé avec le numéro : ' + number;  
        status.className = 'status success show';  
        setTimeout(() => status.classList.remove('show'), 3000);  
    }  
</script>

</body>  
</html>
