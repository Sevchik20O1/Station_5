<!DOCTYPE html>
<html>
<body style="margin:0;height:100vh;background:black;position:relative;">
<iframe id="video" src="https://player.vimeo.com/video/1126541722?autoplay=1&loop=1" style="width:100%;height:100%;border:none;" allowfullscreen allow="autoplay"></iframe>
<a href="#" onclick="c(event)" id="btn" style="position:fixed;top:20px;right:20px;z-index:100;font-size:24px;color:white;background:rgba(0,0,0,0.7);padding:10px;border-radius:5px;text-decoration:none;display:block;">кликни</a>
<script>
let x=parseInt(localStorage.kaminClicks||0)+1;
localStorage.kaminClicks=x;

// 10-й заход = камин
if(x>=10){
    document.body.innerHTML='<div style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">камин</div>';
}

function c(e){
    e.preventDefault();
    // Кнопка ТОЛЬКО показывает "о чём видео?" → возврат к видео
    document.body.innerHTML='<div style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">о чём видео?</div>';
    
    setTimeout(()=>{
        // Возврат к ЧЁРНОМУ ЭКРАНУ С ВИДЕО
        document.body.innerHTML='<iframe id="video" src="https://player.vimeo.com/video/1126541722?autoplay=1&loop=1" style="width:100%;height:100%;border:none;" allowfullscreen allow="autoplay"></iframe><a href="#" onclick="c(event)" id="btn" style="position:fixed;top:20px;right:20px;z-index:100;font-size:24px;color:white;background:rgba(0,0,0,0.7);padding:10px;border-radius:5px;text-decoration:none;display:block;">кликни</a>';
    }, 3000);
}
</script>
</body>
</html>
