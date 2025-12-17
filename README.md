<!DOCTYPE html>
<html>
<body style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">
<a href="#" onclick="c(event)">кликни</a>
<script>
function c(e){
e.preventDefault();
let x=parseInt(localStorage.kaminClicks||0)+1;
localStorage.kaminClicks=x;
if(x<4){
window.location.href='https://vimeo.com/1126541722?fl=pl&fe=sh'
}else{
document.body.innerHTML='<div style="margin:0;padding:20px;height:100vh;background:white;display:flex;align-items:center;justify-content:center;font-size:48px;font-family:sans-serif;color:black;">камин</div>'
}
}
</script>
</body>
</html>
