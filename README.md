<!DOCTYPE html>
<html>
<body style="margin:0;height:100vh;background:black;position:relative;">
<iframe id="video" src="https://player.vimeo.com/video/1126541722?autoplay=1&loop=1" style="width:100%;height:100%;border:none;" allowfullscreen allow="autoplay"></iframe>
<a href="#" onclick="c(event)" id="btn" style="position:fixed;top:20px;right:20px;z-index:100;font-size:24px;color:white;background:rgba(0,0,0,0.7);padding:10px;border-radius:5px;text-decoration:none;display:block;">кликни</a>
<script>
function c(e){
    e.preventDefault();
    
    let clicks=parseInt(localStorage.btnClicks||0)+1;
    localStorage.btnClicks=clicks;
    
    let messages = [
        '', '', '', '', // 1-4 клика: "о чём видео?"
        'думаешь, это смешно?', // 5
        'не смешно', // 6
        'блаблабла', // 7
        'блаблаблаблабла', // 8
        'а вы упорные', // 9
        'а вы очень упорные', // 10
        'ладно, надоели, камин' // 11
    ];
    
    let message = clicks <= 4 ? 'о чём видео?' : messages[clicks] || 'о чём видео?';
    
    document.body.innerHTML='<div style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">'+message+'</div>';
    
    setTimeout(()=>{
        // Возврат к видео
        document.body.innerHTML='<iframe id="video" src="https://player.vimeo.com/video/1126541722?autoplay=1&loop=1" style="width:100%;height:100%;border:none;" allowfullscreen allow="autoplay"></iframe><a href="#" onclick="c(event)" id="btn" style="position:fixed;top:20px;right:20px;z-index:100;font-size:24px;color:white;background:rgba(0,0,0,0.7);padding:10px;border-radius:5px;text-decoration:none;display:block;">кликни</a>';
    }, 3000);
}
</script>
</body>
</html>
