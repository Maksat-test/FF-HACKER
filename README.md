<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Алмаз Генератор</title>
    <style>
        body {
            background-color: black;
            color: lime;
            text-align: center;
            font-family: Arial, sans-serif;
        }
        .container {
            margin-top: 50px;
        }
        input {
            background: black;
            color: lime;
            border: 1px solid lime;
            padding: 10px;
            font-size: 18px;
            text-align: center;
        }
        #randomNumbers {
            font-size: 20px;
            margin-top: 20px;
        }
        .diamond {
            width: 100px;
            height: 100px;
        }
        .link {
            margin-top: 20px;
            font-size: 18px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Алмаз Генератор</h1>
    <p>ID енгізіңіз (12 сан):</p>
    <input type="text" id="idInput" maxlength="12" placeholder="ID">
    <p>Қосымша 5 сан:</p>
    <input type="text" id="extraInput" maxlength="5" placeholder="5 сан">
    
    <p><img src="https://cdn-icons-png.flaticon.com/512/1820/1820899.png" class="diamond"></p>
    
    <p id="randomNumbers">Сандар генерациясы күтілуде...</p>
    
    <p class="link">
        <a href="https://www.tiktok.com/@ff_sns22?_t=ZS-8tiOHTkfb5G&_r=1" target="_blank">
            Осы сілтемеге тіркеліңіз
        </a>
    </p>
    
    <p>⚠️ Алмаз 12 сағат ішінде түседі!</p>
</div>

<script>
    function generateRandomNumbers() {
        let numbers = [];
        for (let i = 0; i < 6; i++) {
            numbers.push(Math.floor(Math.random() * 10000));
        }
        document.getElementById("randomNumbers").innerText = "Генерация: " + numbers.join(" - ");
    }

    setInterval(generateRandomNumbers, 3000);
</script>

</body>
</html>
