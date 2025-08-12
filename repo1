<!-- ✅ Move styles to the top -->
<style>

   .quiz-results {

     max-width: 600px;

     margin: 50px auto;

     padding: 30px;

     font-family: 'Helvetica Neue', sans-serif;

     text-align: center;

   }
 
  h1 {

     font-size: 28px;

     font-weight: 700;

     margin-bottom: 20px;

   }
 
  h2 {

     font-size: 24px;

     margin-bottom: 20px;

     color: #111;

   }
 
  h3#greeting {

     font-size: 20px;

     margin-bottom: 30px;

     color: #555;

   }

   .bar-bg {

     background: #eee;

     border-radius: 20px;

     height: 16px;

     margin: 10px auto 10px;

     overflow: hidden;

     width: 100%;

   }

   .bar {

     height: 100%;

     transition: width 1s ease-in-out;

   }

 #bar-legendaria { background: #f25c3c; }

 #bar-renacida { background: #ff7a59; }

 #bar-visionaria { background: #f2cc3c; }

 #bar-constructora { background: #3c9df2; }

 #bar-encaminada { background: #a68dff; }
 
  .summary-text {

     margin-top: 10px;

     font-size: 16px;

     line-height: 1.5;

     color: #444;

   }
 
  .cta-wrapper {

   margin-top: 10px; /* 👈 was 60px */

   display: flex;

   justify-content: center;

   gap: 20px;

   flex-wrap: wrap;

 }
 
  .alt-btn {

     background-color: #3c82f6;

     color: white;

     font-weight: 600;

     text-transform: uppercase;

     letter-spacing: 2px;

     padding: 14px 28px;

     border-radius: 12px;

     text-decoration: none;

     transition: all 0.3s ease;

     box-shadow: 0 4px 10px rgba(0,0,0,0.1);

   }
 
  .alt-btn:hover {

     background-color: #d43b68;

     transform: translateY(-2px);

   }

   @media (max-width: 640px) {

   .cta-wrapper {

     flex-direction: column;

     align-items: center;

   }
 
  .alt-btn {

     width: 100%;

     max-width: 280px;

     margin-bottom: 12px; /* optional spacing between stacked buttons */

   }

     .greeting-text {

   font-size: 18px;

   line-height: 1.6;

   margin-bottom: 20px;

 }

 }

   .quiz-results {

   padding-bottom: 10px; /* reduce space under the bars */

   margin-bottom: 0px;

 }

 @keyframes gradientShift {

   0%   { background-position: 0% 50%; }

   50%  { background-position: 100% 50%; }

   100% { background-position: 0% 50%; }

 }
 
@keyframes bounceLoop {

   0%, 100% { transform: translateY(0); }

   50% { transform: translateY(-4px); }

 }
 
.animated-cta {

   background-color: #e94e77; /* fallback base color */

   background-image: linear-gradient(135deg, #e94e77, #9b5de5);

   background-size: 200% 200%;

   animation: gradientShift 6s ease infinite, bounceLoop 1.5s ease-in-out infinite;

   color: white;

   font-weight: 600;

   text-transform: uppercase;

   letter-spacing: 2px;

   padding: 14px 28px;

   border-radius: 12px;

   text-decoration: none;

   transition: transform 0.3s ease, box-shadow 0.3s ease;

   box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);

   -webkit-tap-highlight-color: transparent;

   user-select: none;

   outline: none;

   border: none;

 }
 
.animated-cta:focus,

 .animated-cta:active {

   transform: scale(0.97);

   animation: gradientShift 6s ease infinite, bounceLoop 1.5s ease-in-out infinite;

   background: linear-gradient(135deg, #e94e77, #9b5de5);

   outline: none;

   box-shadow: none;

 }

 .animated-cta:hover {

   transform: scale(1.02);

   animation: gradientShift 6s ease infinite, bounceLoop 1.5s ease-in-out infinite;

   background: linear-gradient(135deg, #e94e77, #9b5de5);

   color: white;

 }
 
 
/* Bounce effect */

 @keyframes bounce {

   0%, 100% { transform: translateY(0); }

   50% { transform: translateY(-6px); }

 }
 
/* Gradient animation */

 @keyframes gradientShift {

   0% { background-position: 0% 50%; }

   50% { background-position: 100% 50%; }

   100% { background-position: 0% 50%; }

 }
 
.highlight-name {

   font-weight: 800;

   background: linear-gradient(to right, #ffe8ec, #ffe8ec);

   padding: 2px 6px;

   border-radius: 6px;

   color: #e94e77;

 }
</style>
 
<!-- ✅ Content starts after all styles -->
<div class="quiz-results">
<h1> Your Chingona Power Breakdown</h1>
<h3 id="greeting" class="greeting-text"></h3> <!-- First name greeting here -->
<h2 id="result-title"></h2> <!-- Dynamic personality type -->
<p id="result-description" class="summary-text"></p> <!-- Description -->
<!-- Scores -->
<p>🔥 Chingona Legendaria: <span id="score-legendaria">0%</span></p>
<div class="bar-bg"><div class="bar" id="bar-legendaria"></div></div>
 
  <p>💥 Chingona Renacida: <span id="score-renacida">0%</span></p>
<div class="bar-bg"><div class="bar" id="bar-renacida"></div></div>
 
  <p>💡 Chingona Visionaria: <span id="score-visionaria">0%</span></p>
<div class="bar-bg"><div class="bar" id="bar-visionaria"></div></div>
 
  <p>📐 Chingona Constructora: <span id="score-constructora">0%</span></p>
<div class="bar-bg"><div class="bar" id="bar-constructora"></div></div>
 
  <p>🚀 Chingona en Camino: <span id="score-encaminada">0%</span></p>
<div class="bar-bg"><div class="bar" id="bar-encaminada"></div></div>
</div>
 
<!-- ✅ Buttons -->
<div class="cta-wrapper">
<a href="javascript:void(0)" id="cta-btn" class="btn alt-btn animated-cta">RECIBE TU PLAN DE 30 DÍAS</a>
</div>
 
 
<!-- ✅ Script -->
<script>

 document.addEventListener("DOMContentLoaded", function () {

 const params = new URLSearchParams(window.location.search);

 const legendaria = parseInt(params.get("legendaria")) || 0;

 const renacida = parseInt(params.get("renacida")) || 0;

 const visionaria = parseInt(params.get("visionaria")) || 0;

 const constructora = parseInt(params.get("constructora")) || 0;

 const encaminada = parseInt(params.get("encamino")) || 0;

 const firstName = params.get("first_name");
 
// Calculate total

 const total = legendaria + renacida + visionaria + constructora + encaminada;
 
// Calculate percentages

 const legendPercent = total ? Math.round((legendaria / total) * 100) : 0;

 const renaPercent = total ? Math.round((renacida / total) * 100) : 0;

 const visioPercent = total ? Math.round((visionaria / total) * 100) : 0;

 const constrPercent = total ? Math.round((constructora / total) * 100) : 0;

 const encamPercent = total ? Math.round((encaminada / total) * 100) : 0;
 
 
  // Update bars and scores (you must create these IDs in HTML)

   document.getElementById("score-legendaria").textContent = legendPercent + "%";

   document.getElementById("bar-legendaria").style.width = legendPercent + "%";
 
  document.getElementById("score-renacida").textContent = renaPercent + "%";

   document.getElementById("bar-renacida").style.width = renaPercent + "%";
 
  document.getElementById("score-visionaria").textContent = visioPercent + "%";

   document.getElementById("bar-visionaria").style.width = visioPercent + "%";
 
  document.getElementById("score-constructora").textContent = constrPercent + "%";

   document.getElementById("bar-constructora").style.width = constrPercent + "%";
 
  document.getElementById("score-encaminada").textContent = encamPercent + "%";

   document.getElementById("bar-encaminada").style.width = encamPercent + "%";
 
  // Determine the highest score

   const highest = Math.max(legendaria, renacida, visionaria, constructora, encaminada);

   let resultText = "";

   let resultDesc = "";

   let ctaLink = "";

   let ctaText = "RECIBE TU PLAN DE 30 DÍAS";
 
if (highest === legendaria) {

   resultText = "🔥 Eres La Chingona Legendaria!";

   resultDesc = "Has hecho lo que otras solo sueñan. Pero ahora, es momento de multiplicar.";

   ctaLink = "https://www.adrianagallardo.com/pages/legendaria";

 } else if (highest === renacida) {

   resultText = "💥 Eres La Chingona Renacida!";

   resultDesc = "Has renacido más fuerte que nunca. Ahora te toca dominar.";

   ctaLink = "https://www.adrianagallardo.com/pages/renacida";

 } else if (highest === visionaria) {

   resultText = "💡 Eres La Chingona Visionaria!";

   resultDesc = "Tienes la visión. Ahora necesitas la estructura para ejecutarla.";

   ctaLink = "https://www.adrianagallardo.com/pages/visionaria";

 } else if (highest === constructora) {

   resultText = "📐 Eres La Chingona Constructora!";

   resultDesc = "Ya estás construyendo. Ahora hazlo a tu manera.";

   ctaLink = "https://www.adrianagallardo.com/pages/constructora";

 } else if (highest === encaminada) {

   resultText = "🚀 Eres La Chingona En Camino!";

   resultDesc = "Ya no quieres empezar de nuevo. ¡Ahora es momento de terminar!";

   ctaLink = "https://www.adrianagallardo.com/pages/camino";

 }
 
  document.getElementById("result-title").textContent = resultText;

   document.getElementById("result-description").textContent = resultDesc;
 
  const cta = document.getElementById("cta-btn");

   if (cta) {

     cta.href = ctaLink;

     cta.textContent = ctaText;

   }
 
  if (firstName) {

     document.getElementById("greeting").innerHTML = `Hola <span class="highlight-name">${firstName}</span>, este es tu poder Chingona 👇`;

   }

 });
</script>
