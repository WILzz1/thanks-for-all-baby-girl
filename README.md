# thanks-for-all-baby-girl

<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Happy 3 Months ❤️</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            background: linear-gradient(135deg, #ff758c, #ff7eb3);
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            font-family: 'Segoe UI', sans-serif;
            color: white;
        }

        .container {
            text-align: center;
            z-index: 2;
        }

        h1 {
            font-size: 3em;
            animation: fadeIn 2s ease-in-out;
        }

        p {
            font-size: 1.3em;
            margin-top: 10px;
            animation: fadeIn 3s ease-in-out;
        }

        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background: red;
            transform: rotate(45deg);
            animation: float 6s linear infinite;
        }

        .heart::before,
        .heart::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            background: red;
            border-radius: 50%;
        }

        .heart::before {
            top: -10px;
            left: 0;
        }

        .heart::after {
            left: -10px;
            top: 0;
        }

        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(45deg);
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh) rotate(45deg);
                opacity: 0;
            }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Happy 3 Months 💕</h1>
        <p>Terima kasih sudah hadir dan menemani hari-hariku.<br>
        Semoga kita selalu bersama 🤍</p>
    </div>

    <script>
        function createHeart() {
            const heart = document.createElement('div');
            heart.className = 'heart';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 3 + 3) + 's';

            document.body.appendChild(heart);

            setTimeout(() => {
                heart.remove();
            }, 6000);
        }

        setInterval(createHeart, 300);
    </script>

</body>
</html>
