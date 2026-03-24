<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Misbah ❤️</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #fecfef 100%);
            background-attachment: fixed;
            color: #fff;
            overflow-x: hidden;
            cursor: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32"><path fill="%23ff69b4" d="M16 0c-8.8 0-16 7.2-16 16s7.2 16 16 16 16-7.2 16-16-7.2-16-16-16zm0 28c-6.6 0-12-5.4-12-12s5.4-12 12-12 12 5.4 12 12-5.4 12-12 12zm4-16c0 2.2-1.8 4-4 4s-4-1.8-4-4 1.8-4 4-4 4 1.8 4 4z"/></svg>'), auto;
            min-height: 100vh;
        }

        /* Floating Hearts Background */
        .hearts-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .heart {
            position: absolute;
            color: #ff69b4;
            font-size: 20px;
            animation: float 6s infinite linear;
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 0; }
            10% { opacity: 1; }
            90% { opacity: 1; }
            100% { transform: translateY(-100px) rotate(360deg); opacity: 0; }
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 10;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        /* Welcome Screen */
        .welcome {
            text-align: center;
            padding: 100px 20px;
            animation: fadeInUp 1s ease-out;
        }

        .welcome h1 {
            font-family: 'Dancing Script', cursive;
            font-size: clamp(2.5rem, 8vw, 5rem);
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 30px;
            text-shadow: 0 0 30px rgba(255, 105, 180, 0.5);
        }

        .welcome-btn {
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            border: none;
            padding: 15px 40px;
            font-size: 1.2rem;
            color: white;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(255, 107, 157, 0.4);
            font-weight: 600;
        }

        .welcome-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(255, 107, 157, 0.6);
        }

        /* Sections */
        .section {
            display: none;
            padding: 80px 20px;
            text-align: center;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .section.active {
            display: flex;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Typing Animation */
        .typing-name {
            font-family: 'Dancing Script', cursive;
            font-size: clamp(3rem, 10vw, 6rem);
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 20px;
            overflow: hidden;
            border-right: 3px solid #ff69b4;
            white-space: nowrap;
            animation: typing 3s steps(40) forwards, blink 0.75s infinite;
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }

        @keyframes blink {
            50% { border-color: transparent; }
        }

        /* Love Message */
        .love-message {
            font-size: 1.3rem;
            line-height: 1.8;
            max-width: 800px;
            margin: 0 auto 40px;
            text-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        /* Shayari */
        .shayari {
            font-family: 'Poppins', sans-serif;
            font-size: 1.4rem;
            line-height: 2;
            max-width: 900px;
            margin: 0 auto;
            background: rgba(255,255,255,0.1);
            padding: 40px;
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { box-shadow: 0 0 20px rgba(255,105,180,0.3); }
            to { box-shadow: 0 0 40px rgba(255,105,180,0.6); }
        }

        .shayari-line {
            opacity: 0;
            transform: translateY(30px);
            animation: slideInUp 0.8s ease forwards;
        }

        .shayari-line:nth-child(1) { animation-delay: 0.2s; }
        .shayari-line:nth-child(2) { animation-delay: 0.4s; }
        .shayari-line:nth-child(3) { animation-delay: 0.6s; }
        .shayari-line:nth-child(4) { animation-delay: 0.8s; }

        @keyframes slideInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Memory Section */
        .memories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 40px;
        }

        .memory-card {
            background: rgba(255,255,255,0.1);
            border-radius: 20px;
            overflow: hidden;
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
            border: 1px solid rgba(255,255,255,0.2);
        }

        .memory-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
        }

        .memory-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        /* Interaction */
        .interaction-btn {
            background: linear-gradient(45deg, #ff9a8b, #ff6b9d);
            border: none;
            padding: 20px 50px;
            font-size: 1.3rem;
            color: white;
            border-radius: 50px;
            cursor: pointer;
            margin: 40px 0;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(255, 154, 139, 0.4);
        }

        .interaction-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(255, 154, 139, 0.6);
        }

        /* Popup */
        .popup {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0);
            background: linear-gradient(45deg, #ff6b9d, #c44569);
            padding: 40px 60px;
            border-radius: 30px;
            text-align: center;
            font-size: 1.5rem;
            font-weight: 600;
            z-index: 1000;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            transition: all 0.4s ease;
        }

        .popup.show {
            transform: translate(-50%, -50%) scale(1);
        }

        /* Final Surprise */
        .surprise {
            font-size: clamp(2rem, 8vw, 4rem);
            font-family: 'Dancing Script', cursive;
            background: linear-gradient(45deg, #ffd700, #ffed4e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 30px rgba(255, 215, 0, 0.5);
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        /* Nav Button */
        .nav-btn {
            position: fixed;
            top: 30px;
            right: 30px;
            background: rgba(255,255,255,0.2);
            border: none;
            color: white;
            padding: 15px 20px;
            border-radius: 50px;
            cursor: pointer;
            backdrop-filter: blur(10px);
            z-index: 100;
            transition: all 0.3s ease;
        }

        .nav-btn:hover {
            background: rgba(255,255,255,0.3);
            transform: scale(1.1);
        }

        /* Responsive */
        @media (max-width: 768px) {
            .container { padding: 10px; }
            .section { padding: 40px 10px; }
            .shayari { padding: 20px; font-size: 1.1rem; }
            .popup { padding: 30px 40px; font-size: 1.2rem; }
        }

        /* Smooth Scroll */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <!-- Background Hearts -->
    <div class="hearts-bg" id="heartsBg"></div>

    <!-- Navigation -->
    <button class="nav-btn" onclick="goHome()">🏠 Home</button>

    <!-- Audio -->
    <audio id="bgMusic" loop>
        <source src="data:audio/wav;base64,UklGRnoGAABXQVZFZm10IBAAAAABAAEAQB8AAEAfAAABAAgAZGF0YQoGAACBhYqFbF1fdJivrJBhNjVgodDbq2EcBj+a2/LDciUFLIHO8tiJNwgZaLvt559NEAxQp+PwtmMcBjiR1/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHfH8N2QQAoUXrTp66hVFApGn+DyvmwhBSxFz/LMeSwFJHf
