<!--========================== README ANIMADO (HTML + JS) ===========================-->
<div style="text-align:center;font-family:'Fira Code',monospace;color:#00c9ff">
  <h1 id="titleText"></h1>
  <p style="margin-top:-10px;font-size:18px;">Full Stack Developer & AI Enthusiast</p>

  <img src="https://github.com/Victor00128/Chatbot-Vortex/blob/main/Imagen/Chatbot-Vortex.png?raw=true" width="70%" style="border-radius:20px; box-shadow:0 0 25px #00c9ff55"/>

  <h2 style="margin-top:30px">Impacto</h2>
  <p><span id="projectsCount">0</span> Proyectos desarrollados</p>
  <p><span id="interCount">0</span> Interacciones registradas (Vortex)</p>
  <p><span id="clientsCount">0</span> Colaboraciones completadas</p>

  <br />

  <a href="https://github.com/Victor00128/Chatbot-Vortex" style="padding:10px 18px;border-radius:12px;border:2px solid #00c9ff;text-decoration:none;transition:0.3s">
    Ver Código
  </a>
  <a href="https://vortex-ia.netlify.app/" style="padding:10px 18px;border-radius:12px;border:2px solid #00c9ff;margin-left:8px;text-decoration:none;transition:.3s">
    Probar Demo
  </a>
</div>

<script>
// typing effect
const text = "Victor";
let i = 0;
function typing(){
  if(i < text.length){
    document.getElementById("titleText").innerHTML += text.charAt(i);
    i++;
    setTimeout(typing, 140);
  }
}
typing();

// counters
function animateValue(id, end, duration){
  let start = 0;
  let range = end - start;
  let current = start;
  let increment = end > start? 1 : -1;
  let stepTime = Math.abs(Math.floor(duration / range));
  let obj = document.getElementById(id);
  let timer = setInterval(function(){
    current += increment;
    obj.innerHTML = current;
    if (current == end){
      clearInterval(timer);
    }
  }, stepTime);
}
setTimeout(()=> {
   animateValue("projectsCount", 15, 1200);
   animateValue("interCount", 1500, 1800);
   animateValue("clientsCount", 10, 1000);
}, 1000);
</script>
<!--==================================================================================-->
