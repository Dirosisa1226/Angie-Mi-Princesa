<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Angie Nikol</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            text-align: center;
            background-color: #478a8f; /* Amarillo pastel */
            margin: 0;
            padding: 0;
            position: relative; /* Para el posicionamiento absoluto del botón */
        }
        h1 {
            color: #000000; /* Verde pastel */
            font-size: 50px; /* Tamaño de la fuente aumentado */
        }
        p {
            color: #000000; /* Azul pastel más oscuro */
            font-size: 30px;
            margin-bottom: 30px;
        }
        #Image {
            width: 600px; /* Tamaño del Monster Inc */
            height: 600px;
            margin-bottom: 20px;
            border-radius: 50%;
            animation: bounce 1s infinite alternate; /* MonsterInc */
        }
        @keyframes bounce {
            0% { transform: translateY(0); }
            100% { transform: translateY(-10px); }
        }
        button {
            padding: 15px 30px;
            font-size: 20px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s ease;
            position: absolute; /* Posicionamiento absoluto */
        }
        #btnYes {
            background-color: rgb(174, 0, 255); /* Naranja pastel */
            color: white;
            top: 50%;
            left: 50%;
            transform: translate(-200%, 270%);
        }
        #btnNo {
            background-color:rgb(174, 0, 255); /* Rojo pastel */
            color: white;
        }
        button:hover {
            transform: scale(1.5);
        }
        .move {
            animation: moveButton 1s infinite alternate;
        }
        @keyframes moveButton {
            0% {
                top: calc(10% + 90vh * random());
                left: calc(10% + 90vw * random());
            }
            100% {
                top: calc(10% + 90vh * random());
                left: calc(10% + 90vw * random());
            }
        }
    </style>
</head>
<body>
    <h1>¡Me haces muy feliz, perdoname cofa!</h1>
    <p>Sabes lo feliz que me haces? No quiero perderte!!</p>
    <img id="Image" src="Monster inc.gif" alt="MonsterInc">
    <br>
    <button id="btnYes" onclick="aceptar()">¡Shí!</button>
    <button id="btnNo" onmouseover="startMove()" onmouseout="stopMove()">¡No!</button>

    <script>
        let moveInterval;

        function startMove() {
            moveInterval = setInterval(moveButton, 500); // Inicia el movimiento del botón
        }

        function stopMove() {
            clearInterval(moveInterval); // Detiene el movimiento del botón
        }

        function moveButton() {
            let btnNo = document.getElementById('btnNo');
            let randomX = Math.random() * window.innerWidth;
            let randomY = Math.random() * window.innerHeight;
            btnNo.style.left = randomX + 'px';
            btnNo.style.top = randomY + 'px';
        }

        function aceptar() {
            alert('No lo vuelvo a hacer mi corazon de melon, Graciaaaaaaaas, MUAAAAAAAAAAK');
        }
    </script>
</body>
</html>
