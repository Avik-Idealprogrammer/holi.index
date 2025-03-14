<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Holi!</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(45deg, #ff0000, #ff7300, #ffeb00, #0be881, #0097e6, #9c88ff, #f368e0);
            background-size: 400% 400%;
            animation: gradientBG 10s ease infinite;
            text-align: center;
            overflow: hidden;
            font-family: 'Poppins', sans-serif;
            color: white;
        }
        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        h1 {
            font-size: 60px;
            margin-top: 15vh;
            text-shadow: 3px 3px 10px rgba(255,255,255,0.3);
            animation: fadeIn 2s ease-in-out;
        }
        p {
            font-size: 22px;
            margin: 20px auto;
            width: 80%;
            max-width: 700px;
            text-shadow: 2px 2px 6px rgba(255,255,255,0.3);
            animation: fadeIn 3s ease-in-out;
        }
        .container {
            position: relative;
            z-index: 10;
            padding: 20px;
            border-radius: 15px;
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            display: inline-block;
            margin-top: 50px;
            box-shadow: 0 5px 20px rgba(255,255,255,0.2);
        }
        .splash {
            position: absolute;
            width: 80px;
            height: 80px;
            background: radial-gradient(circle, rgba(255,255,255,0.8), rgba(255,255,255,0));
            border-radius: 50%;
            animation: splash 1.5s linear infinite;
            mix-blend-mode: screen;
        }
        @keyframes splash {
            0% { transform: scale(0.5); opacity: 1; }
            100% { transform: scale(4); opacity: 0; }
        }
        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(-20px); }
            100% { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🎨 Happy Holi! 🌸</h1>
        <p>Holi, the festival of colors, is a joyous celebration of love, unity, and the victory of good over evil. It brings people together, breaking barriers and spreading happiness with vibrant colors and sweets. Wishing you a colorful and delightful Holi!</p>
    </div>
    <script>
        function createSplash(x, y) {
            const splash = document.createElement("div");
            splash.classList.add("splash");
            splash.style.background = `hsl(${Math.random() * 360}, 100%, 70%)`;
            splash.style.left = `${x - 40}px`;
            splash.style.top = `${y - 40}px`;
            document.body.appendChild(splash);
            setTimeout(() => splash.remove(), 1500);
        }
        document.body.addEventListener("click", (e) => {
            createSplash(e.clientX, e.clientY);
        });
    </script>
</body>
</html>

