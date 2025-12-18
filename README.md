<!DOCTYPE html>
<html>
<body style="margin:0;height:100vh;background:black;">
<iframe src="https://player.vimeo.com/video/1126541722?autoplay=1&muted=1&loop=1" style="width:100%;height:100%;border:none;" allowfullscreen></iframe>
<script>
let x=parseInt(localStorage.kaminClicks||0)+1;
localStorage.kaminClicks=x;
if(x>=4){
document.body.innerHTML='<div style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">камин</div>'
}else{
setTimeout(()=>{window.location.href='https://vimeo.com/1126541722?fl=pl&fe=sh'},1000)
}
</script>
</body>
</html>
