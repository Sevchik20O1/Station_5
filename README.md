xml
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ссылка 4 клика</title>
    <style>
        body { 
            margin: 0; padding: 20px; height: 100vh; 
            background: white; display: flex; align-items: center; 
            justify-content: center; font-family: sans-serif; 
            font-size: 48px; color: black; flex-direction: column;
        }
        a { color: black; text-decoration: none; }
        a:hover { text-decoration: underline; }
        .counter { font-size: 24px; margin-top: 20px; }
    </style>
</head>
<body>
    <div>
        <a href="#" id="magicLink" onclick="handleClick(event)">кликни</a>
        <div id="clickCounter" class="counter">Кликов: 0/4</div>
    </div>

    <script>
        function handleClick(event) {
            event.preventDefault();
            let clicks = parseInt(localStorage.getItem('kaminClicks') || '0');
            clicks++;
            
            localStorage.setItem('kaminClicks', clicks.toString());
            document.getElementById('clickCounter').textContent = `Кликов: ${clicks}/4`;
            
            if (clicks < 4) {
                // Первые 3 клика: VK видео
                window.open('https://vk.com/video-232836144_456239017', '_blank');
            } else {
                // 4-й клик: камин
                window.open('data:text/html,<html style=\'margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-family:sans-serif;font-size:48px;color:black;\'><body>камин</body></html>');
            }
        }
        
        // Показать текущий счётчик при загрузке
        window.onload = function() {
            let clicks = parseInt(localStorage.getItem('kaminClicks') || '0');
            document.getElementById('clickCounter').textContent = `Кликов: ${clicks}/4`;
        }
    </script>
</body>
</html>
