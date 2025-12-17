<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Клик</title>
    <style>
        body { 
            margin: 0; padding: 20px; height: 100vh; 
            background: white; display: flex; align-items: center; 
            justify-content: center; font-family: sans-serif; 
            font-size: 48px; color: black; 
        }
        a { color: black; text-decoration: none; }
        a:hover { text-decoration: underline; }
    </style>
</head>
<body>
    <a href="#" onclick="handleClick(event)">кликни</a>

    <script>
        function handleClick(event) {
            event.preventDefault();
            let clicks = parseInt(localStorage.getItem('kaminClicks') || '0');
            clicks++;
            localStorage.setItem('kaminClicks', clicks.toString());
            
            if (clicks < 4) {
                window.location.href = 'https://vk.com/video-232836144_456239017';
            } else {
                window.location.href = 'data:text/html,<html style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-family:sans-serif;font-size:48px;color:black;"><body>камин</body></html>';
            }
        }
    </script>
</body>
</html>
