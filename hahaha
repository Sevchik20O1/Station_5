<!DOCTYPE html>
<html>
<body style="margin:0;height:100vh;background:black;position:relative;">
<iframe id="video" src="https://player.vimeo.com/video/1126541722?autoplay=1&loop=1" style="width:100%;height:100%;border:none;" allowfullscreen allow="autoplay"></iframe>
<a href="#" onclick="c(event)" id="btn" style="position:fixed;top:20px;right:20px;z-index:100;font-size:24px;color:white;background:rgba(0,0,0,0.7);padding:10px;border-radius:5px;text-decoration:none;display:none;">кликни</a>
<div id="patience" style="display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:white;z-index:200;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;"></div>
<script>
function resetCounter() {
    localStorage.setItem('kaminClicks', '0');
    localStorage.setItem('kaminLastActivity', Date.now());
}

function checkReset() {
    let lastActivity = parseInt(localStorage.getItem('kaminLastActivity') || '0');
    let now = Date.now();
    if (now - lastActivity > 120000) {
        resetCounter();
    }
}

let x=parseInt(localStorage.kaminClicks||0)+1;
localStorage.kaminClicks=x;
localStorage.setItem('kaminLastActivity', Date.now());
checkReset();

if(x<4){
    document.getElementById('btn').style.display='block';
}else{
    document.body.innerHTML='<div style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">камин</div>';
}

function c(e){
    e.preventDefault();
    localStorage.setItem('kaminLastActivity', Date.now());
    
    // Показываем "о чём видео?" поверх видео
    document.getElementById('patience').textContent='о чём видео?';
    document.getElementById('patience').style.display='flex';
    
    setTimeout(()=>{
        // Возвращаем видео (скрываем надпись)
        document.getElementById('patience').style.display='none';
        
        setTimeout(()=>{
            let clicks=parseInt(localStorage.kaminClicks||0)+1;
            localStorage.kaminClicks=clicks;
            if(clicks<4){
                window.location.href='https://vimeo.com/1126541722?fl=pl&fe=sh';
            }else{
                document.body.innerHTML='<div style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">камин</div>';
            }
        }, 1000); // 1 сек видео перед переходом
    }, 3000);
}

setInterval(checkReset, 30000);
</script>
</body>
</html>
