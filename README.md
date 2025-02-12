<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi San Valentín?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #ffccd5; 
            text-align: center;
            margin: 0;
            padding: 0;
            overflow: hidden;
        }
        .container {
            position: relative;
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .kuromi, .spiderman {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 200px;
        }
        .kuromi { left: 10%; }
        .spiderman { right: 10%; }
        .heart {
            width: 150px;
            animation: heartbeat 1s infinite alternate;
        }
        @keyframes heartbeat {
            0% { transform: scale(1); }
            100% { transform: scale(1.2); }
        }
        .question {
            font-size: 24px;
            font-weight: bold;
            color: #d1006c;
            margin-top: 20px;
        }
        .buttons {
            margin-top: 20px;
        }
        .btn {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: 0.3s;
        }
        .yes {
            background-color: #ff4081;
            color: white;
        }
        .yes:hover {
            background-color: #d1006c;
        }
        .no {
            background-color: #999;
            color: white;
            position: absolute;
        }
    </style>
</head>
<body>
    <div class="container">
        <img src="kuromi.jpg" class="kuromi" alt="Kuromi">
        <img src="spiderman.png" class="spiderman" alt="Spider-Man">
        <div class="content">
            <img src="corazon.jpg" class="heart" alt="Heart">
            <div class="question">¿Quieres ser mi San Valentín?</div>
            <div class="buttons">
                <button class="btn yes" onclick="alert('¡Sabía que dirías que sí! ❤ TE AMO MUCHO MI CHAPARRITA HERMOSA ;^')">Sí</button>
                <button class="btn no" id="noButton" onmouseover="moveNoButton()">No</button>
            </div>
        </div>
    </div>

    <script>
        function moveNoButton() {
            let noButton = document.getElementById('noButton');
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 50);
            noButton.style.left = ${x}px;
            noButton.style.top = ${y}px;
        }
    </script>
</body>
</html>
