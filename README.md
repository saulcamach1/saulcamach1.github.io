
<html>
<head>
    <title>Sorpresa Romántica</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #f0e8ff;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
        }

        #surpriseButton {
            padding: 15px 30px;
            font-size: 20px;
            color: white;
            background-color: #e85577;
            border: none;
            border-radius: 15px;
            cursor: pointer;
            box-shadow: 3px 3px 15px rgba(0, 0, 0, 0.3);
        }

        #message {
            display: none;
            font-size: 26px;
            color: #d6336c;
            text-align: center;
            position: absolute;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        .heart {
            position: fixed;
            bottom: -100px;
            height: 60px;
            width: 60px;
            font-size: 35px;
            opacity: 0.7;
        }

        @keyframes floating {
            0% { bottom: 100vh; opacity: 0.7; }
            100% { bottom: -100vh; opacity: 0; }
        }
    </style>
</head>
<body>
    <button id="surpriseButton">Para Mi Mildred bella</button>
    <div id="message">
        <p>¡Te quiero, te adoro, te amo demasiado Mi Pollito hermoso, eres mi amor de siempre, espero que le haya gustado mucho este detallito con mucho amorcito escribiendole cositas para usted con mucho sentimiento, pase una muy bonita tarde mi amor bello 🥰!</p>
    </div>

    <script>

        const confeti = '❤️'; //Sustituir por el emoticono que quieras que llueva (yo uso esta pagina https://emojipedia.org/es)

        document.getElementById("surpriseButton").addEventListener("click", function() {
            this.style.display = 'none';
            document.getElementById("message").style.display = "block";
            startHearts();
        });

        function startHearts() {
            for (let i = 0; i < 150; i++) {
                const heart = document.createElement('div');
                heart.classList.add('heart');
                heart.style.left = Math.random() * window.innerWidth + 'px';
                heart.style.animation = 'floating ' + (2 + Math.random() * 3) + 's ease-in infinite';
                heart.innerText = confeti;
                heart.style.transform= 'rotate(' + 360 * Math.random() + 'deg)';
                document.body.appendChild(heart);
            }
        }
    </script>
</body>
</html>‎ 
