# adriana
Un pequeño detalle para recordarte cuánto te amo y lo importante que eres para mí. Espero que te guste esta sorpresa, mi amor. ❤️✨"
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Adriana ❤️</title>
    <style>
        body {
            text-align: center;
            font-family: 'Arial', sans-serif;
            background-color: #ffe6e6;
            color: #ff4081;
            overflow-y: auto;
            max-height: 100vh;
        }
        h1 {
            font-size: 36px;
            margin-top: 50px;
            animation: fadeIn 2s ease-in-out;
        }
        p {
            font-size: 20px;
            margin-top: 20px;
            animation: fadeIn 3s ease-in-out;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .yes {
            background-color: #4CAF50;
            color: white;
        }
        .no {
            background-color: #f44336;
            color: white;
            position: absolute;
        }
        .tulip {
            width: 50px;
            height: 50px;
            background: url('https://upload.wikimedia.org/wikipedia/commons/thumb/6/68/Tulip_-_floriade_canberra.jpg/640px-Tulip_-_floriade_canberra.jpg') no-repeat center;
            background-size: cover;
            display: inline-block;
            margin: 5px;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 24px;
            animation: floatUp 4s infinite ease-in-out;
        }
        @keyframes floatUp {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100px); opacity: 0; }
        }
    </style>
</head>
<body>
    <h1>Adriana, ¿Me amas? ❤️</h1>
    <button class="yes" onclick="goToMessage()">Sí</button>
    <button class="no" onclick="moveNo()" id="noButton">No</button>
    <div id="message" style="display: none; overflow-y: auto; max-height: 80vh; padding: 10px;">
        <h1>Para mi hermosa Adriana ❤️</h1>
        <p>El día que te conocí, llegaste a mi trabajo buscando ayuda con un adres y una copia de tu tarjeta de identidad. Desde ese momento, quedé prendado de tu belleza, tu dulzura y esa mirada que me cautivó.</p>
        <p>Después de ese día no pude sacarte de mi mente, y supe que algo especial estaba ocurriendo. Me enteré que fuiste un domingo a la papelería solo con la excusa de verme, aunque no trabajaba ese día. Eso me hizo sonreír y sentirme afortunado.</p>
        <p>Te escribí un "hola" el lunes y cuando respondiste casi al instante, mi corazón saltó de emoción. Desde ahí nuestra historia comenzó a escribirse sola, con cada conversación y cada encuentro.</p>
        <h2>🌷 Para ti, tulipanes porque sé que te encantan 🌷</h2>
        <div class="tulip"></div>
        <div class="tulip"></div>
        <div class="tulip"></div>
        <div class="tulip"></div>
        <div class="tulip"></div>
        <p>Mi amor, a pesar de no haber sido el hombre más detallista con flores y regalos, sé que he llenado tu pancita de muchas delicias. 😂
           Me encanta compartir momentos contigo, verte sonreír, llevarte a conocer lugares hermosos en Medellín.</p>
        <p>Te debo muchas cosas: 🌻 Flores amarillas, 🌷 Tulipanes y muchas más sorpresas.</p>
        <p>Pero lo más importante que quiero que sepas es que te amo con todo mi corazón. Quiero que seas feliz, que siempre sonrías y que nunca dudes de mi amor por ti. Eres lo mejor que me ha pasado en la vida y siempre estaré aquí para ti.</p>
    </div>
    <script>
        function goToMessage() {
            document.querySelector("h1").style.display = "none";
            document.querySelector("button.yes").style.display = "none";
            document.querySelector("button.no").style.display = "none";
            document.getElementById("message").style.display = "block";
            createHearts();
        }
        
        function moveNo() {
            let button = document.getElementById("noButton");
            let newX = Math.random() * (window.innerWidth - 100);
            let newY = Math.random() * (window.innerHeight - 50);
            button.style.left = newX + "px";
            button.style.top = newY + "px";
        }
        
        function createHearts() {
            for (let i = 0; i < 30; i++) {
                let heart = document.createElement("div");
                heart.className = "heart";
                heart.innerHTML = "❤️";
                heart.style.left = Math.random() * window.innerWidth + "px";
                heart.style.top = Math.random() * window.innerHeight + "px";
                heart.style.animationDuration = (Math.random() * 2 + 2) + "s";
                document.body.appendChild(heart);
                setTimeout(() => heart.remove(), 4000);
            }
        }
    </script>
</body>
</html>
