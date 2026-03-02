<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para Karol ❤️</title>

<style>
body{
    margin:0;
    padding:0;
    background:#000;
    color:white;
    font-family: 'Segoe UI', sans-serif;
    text-align:center;
    overflow-x:hidden;
}

.container{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    width:90%;
}

button{
    padding:15px 30px;
    font-size:18px;
    border:none;
    border-radius:30px;
    background:#ff2e63;
    color:white;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    background:#ff4d6d;
}

.hidden{
    display:none;
}

.fade{
    animation:fade 2s ease-in-out;
}

@keyframes fade{
    from{opacity:0;}
    to{opacity:1;}
}

section{
    padding:80px 20px;
}

h1,h2,p{
    margin:20px 0;
}

.corazon{
    position:fixed;
    top:-10px;
    font-size:20px;
    animation:caer 6s linear infinite;
}

@keyframes caer{
    to{
        transform:translateY(110vh);
    }
}
</style>
</head>
<body>

<div class="container" id="inicio">
<h1>Mi niña...</h1>
<p>Si estás viendo esto es porque hay algo que mi corazón no podía guardarse.</p>
<button onclick="mostrar()">Toca aquí ❤️</button>
</div>

<div class="hidden" id="contenido">

<section class="fade">
<h2>Karol, 17 de marzo</h2>
<p>
No eres solo una fecha en el calendario.
Eres el día en que el mundo se volvió más bonito.
</p>
</section>

<section class="fade">
<p>
Desde que llegaste a mi vida,
las cosas simples tienen más sentido.
Tu risa, tu mirada,
tu forma de ser…
</p>
</section>

<section class="fade">
<p>
No sé qué nos depare el destino,
pero siempre voy a agradecer
el día en que llegaste a mi mundo.
</p>
</section>

<section class="fade">
<h2>Feliz cumpleaños, mi niña ❤️</h2>
<p>
Que este nuevo año te abrace bonito.
Que la vida te devuelva todo lo que das.
Y que nunca olvides lo especial que eres y cuanto te amo.
<img src="19205.jpeg" style="width:250px;border-radius:20px;margin:10px;">
</p>
</section>

</div>

<script>
function mostrar(){
document.getElementById("inicio").classList.add("hidden");
document.getElementById("contenido").classList.remove("hidden");
crearCorazones();
}

function crearCorazones(){
setInterval(()=>{
const corazon=document.createElement("div");
corazon.classList.add("corazon");
corazon.innerHTML="❤️";
corazon.style.left=Math.random()*100+"vw";
corazon.style.fontSize=(Math.random()*20+10)+"px";
document.body.appendChild(corazon);

setTimeout(()=>{
corazon.remove();
},6000);

},500);
}
</script>

</body>
</html> 
