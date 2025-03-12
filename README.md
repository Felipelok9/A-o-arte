<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirecionando...</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background-color: #f4f4f4;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
        img {
            width: 200px; /* Tamanho do logo */
            margin-bottom: 20px;
        }
        #contador {
            font-size: 30px;
            font-weight: bold;
            color: #ff4500;
            margin: 10px 0;
        }
        button {
            background-color: #25D366;
            color: white;
            border: none;
            padding: 12px 20px;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            text-decoration: none;
            display: inline-block;
        }
        button:hover {
            background-color: #1ebe5d;
        }
    </style>
</head>
<body>

    <!-- Logo -->
    <img src="https://i.ibb.co/ycLBKgZ1/Logo-A-o-Arte.png" alt="Logo">
  
    <h1>Você será redirecionado para o grupo do WhatsApp em:</h1>
    <p id="contador">5</p>

    <!-- Botão de Atendimento -->
    <a href="https://wa.me/message/XI6IZ27MI7FFB1" target="_blank">
        <button>Falar com Atendente</button>
    </a>

    <script>
        let tempo = 5; // Tempo em segundos
        let linkWhatsApp = "https://chat.whatsapp.com/G3z12fym25G33YA32svNAC"; // Link do grupo

        function atualizarContador() {
            document.getElementById("contador").textContent = tempo;
            if (tempo <= 0) {
                window.location.href = linkWhatsApp; // Redireciona
            } else {
                tempo--;
                setTimeout(atualizarContador, 1000);
            }
        }

        atualizarContador();
    </script>

</body>
</html>
