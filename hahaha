<!DOCTYPE html>
<html>
<body style="margin:0;height:100vh;background:black;position:relative;">
<iframe src="https://player.vimeo.com/video/1126541722?autoplay=1&muted=1&loop=1" style="width:100%;height:100%;border:none;" allowfullscreen></iframe>
<a href="#" onclick="c(event)" style="position:fixed;top:20px;right:20px;z-index:100;font-size:24px;color:white;background:rgba(0,0,0,0.7);padding:10px;border-radius:5px;text-decoration:none;">кликни</a>
<script>
function c(e){
e.preventDefault();
let x=parseInt(localStorage.kaminClicks||0)+1;
localStorage.kaminClicks=x;
if(x<4){
window.location.href='https://vimeo.com/1126541722?fl=pl&fe=sh';
}else{
document.body.innerHTML='<div style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">камин</div>';
}
}
</script>
</body>
</html>
