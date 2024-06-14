
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mensaje de Amor</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f5d626;
        }
        .message-box {
            text-align: center;
            background-color: #8952f0;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 80%;
            max-width: 500px;
        }
        .message-box h1 {
            color: #360a5a;
        }
        .message-box p {
            color: #360a5a;
        }
        .message-box button {
            margin-top: 20px;
            padding: 10px 20px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .message-box button.si {
            background-color: #98fb98;
            color: #008000;
        }
        .message-box button.no {
            background-color: #ff9999;
            color: #cc0000;
            margin-left: 10px;
        }
        .message-box button:hover {
            filter: brightness(90%);
        }

        @media (max-width: 600px) {
            .message-box {
                width: 90%;
            }
        }
    </style>
</head>
<body>
    <div class="message-box">
        <h1>🖤</h1>
        <p>Soy la serpiente que se traga el ratón</p>
        <p>¿Quieres leer el mensaje oculto?</p>
        <button class="si" onclick="aceptarMensaje()">Sí</button>
        <button class="no" onclick="rechazarMensaje()">No</button>
        <p id="mensaje-advertencia" style="display: none; color: rgb(255, 255, 255);">¡Inténtelo de nuevo!</p>
    </div>

    <script>
        function aceptarMensaje() {
            alert('¡ME GUSTAS! 😍');
        }

        function rechazarMensaje() {
            document.getElementById('mensaje-advertencia').style.display = 'block';
        }

        // No permitir que el usuario rechace el mensaje haciendo clic derecho
        document.addEventListener('contextmenu', function(event) {
            event.preventDefault();
            alert('No puedes rechazar este mensaje de amor ❤️');
        });
    </script>
</body>
</html>
