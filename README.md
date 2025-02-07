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
        .hacker {
            width: 150px;
            height: auto;
        }
        .link {
            margin-top: 20px;
            font-size: 18px;
        }
        #diamondMessage {
            display: none; /* Бастапқыда көрсетілмейді */
            font-size: 18px;
            color: red;
            margin-top: 20px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Алмаз Генератор</h1>
    <p>ID енгізіңіз :</p>
    <input type="text" id="idInput" maxlength="12" placeholder="ID">
    <p> количество алмазов:</p>
    <input type="text" id="extraInput" maxlength="5" placeholder="5 сан">
    
    <p><img src="https://cdn-icons-png.flaticon.com/512/3076/3076746.png" class="hacker"></p>
    
    <p id="randomNumbers">Сандар генерациясы күтілуде...</p>
    
    <button onclick="startRandom()">Генерацияны бастау</button>

    <p class="link">
        <a href="https://www.tiktok.com/@ff_sns22?_t=ZS-8tiOHTkfb5G&_r=1" target="_blank" id="registerLink">
            Осы сілтемеге тіркеліңіз
        </a>
    </p>
    
    <button onclick="confirmRegistration()">Тіркелдім</button>

    <p id="diamondMessage">⚠️ Алмаз 12 сағат ішінде түседі!</p>
</div>

<script>
    function startRandom() {
        let counter = 0;
        let interval = setInterval(() => {
            let numbers = [];
            for (let i = 0; i < 6; i++) {
                numbers.push(Math.floor(Math.random() * 10000));
            }
            document.getElementById("randomNumbers").innerText = "Генерация: " + numbers.join(" - ");
            
            counter++;
            if (counter > 30) { // 3 секундтан кейін тоқтайды
                clearInterval(interval);
            }
        }, 100);
    }

    function confirmRegistration() {
        document.getElementById("diamondMessage").style.display = "block"; // Жазуды көрсету
    }
</script>

</body>
</html>
