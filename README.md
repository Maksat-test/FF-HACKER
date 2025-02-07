<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Password Cracker v1.0</title>
    <style>
        body {
            background-color: #000;
            color: #0f0;
            font-family: 'Courier New', monospace;
            padding: 20px;
        }
        
        .container {
            border: 2px solid #0f0;
            padding: 20px;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .title {
            text-align: center;
            font-size: 24px;
            text-transform: uppercase;
            margin-bottom: 30px;
        }
        
        .section {
            margin: 15px 0;
            padding: 10px;
            border-left: 3px solid #0f0;
        }
        
        button {
            background: #000;
            color: #0f0;
            border: 1px solid #0f0;
            padding: 10px 20px;
            cursor: pointer;
            margin-top: 20px;
        }
        
        button:hover {
            background: #0f0;
            color: #000;
        }
        
        .console {
            background: #002200;
            padding: 15px;
            margin-top: 20px;
            height: 150px;
            overflow-y: auto;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="title">Взломник паролей</div>
        
        <div class="section">
            <h3>Вопросы паролей (Стоимость: 5,00 руб.)</h3>
            <div class="sub-section">
                <p>Сборка: 1,00 руб.</p>
                <p>Проверка: 0,00 руб.</p>
            </div>
        </div>

        <div class="section">
            <h3>Баллы данных:</h3>
            <p>▸ Основной балл: 1000 руб.</p>
            <p>▸ Сборка: 50 руб.</p>
            <p>▸ Резервный балл: 200 руб.</p>
            <p>▸ Консоль программы: 500 руб.</p>
        </div>

        <div class="console" id="console">
            > Система инициализирована<br>
            > Готово к работе
        </div>

        <button onclick="startHack()">НАЧАТЬ ВЗЛОМ</button>
    </div>

    <script>
        function startHack() {
            const consoleElem = document.getElementById('console');
            consoleElem.innerHTML += '<br>> Начата процедура взлома...';
            
            const messages = [
                'Анализ структуры пароля...',
                'Подбор хэш-ключей...',
                'Обход защиты... 23%',
                'Перехват пакетов...',
                'Дешифровка завершена!',
                'Доступ получен!'
            ];

            let delay = 2000;
            messages.forEach((msg, index) => {
                setTimeout(() => {
                    consoleElem.innerHTML += `<br>> ${msg}`;
                    consoleElem.scrollTop = consoleElem.scrollHeight;
                }, delay * index);
            });
        }
    </script>
</body>
</html>
