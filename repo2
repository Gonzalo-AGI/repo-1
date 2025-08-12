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

  #bar-legendaria { background: #0169a7; }
  #bar-renacida { background: #dfeb05; }
  #bar-visionaria { background: #049109; }
  #bar-constructora { background: #db1304; }

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
    background-image: linear-gradient(135deg, #0169a7, #005181);
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
    background: linear-gradient(135deg, #5079ab, #5079ab);
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
  <h1>Your Animal Personality Breakdown!</h1>
  <h3 id="greeting" class="greeting-text"></h3> <!-- First name greeting here -->
  <h2 id="result-title"></h2> <!-- Dynamic personality type -->
  <p id="result-description" class="summary-text"></p> <!-- Description -->

  <!-- Scores -->
  <p>🐑 Sheep Personality: <span id="score-legendaria">0%</span></p>
  <div class="bar-bg"><div class="bar" id="bar-legendaria"></div></div>

  <p>🦜 Love Bird Personality: <span id="score-renacida">0%</span></p>
  <div class="bar-bg"><div class="bar" id="bar-renacida"></div></div>

  <p>🦉 Owl Personality: <span id="score-visionaria">0%</span></p>
  <div class="bar-bg"><div class="bar" id="bar-visionaria"></div></div>

  <p>🦏 Rhino Personality: <span id="score-constructora">0%</span></p>
  <div class="bar-bg"><div class="bar" id="bar-constructora"></div></div>

<!-- ✅ Buttons -->
<div class="cta-wrapper">
  <a href="javascript:void(0)" id="cta-btn" class="btn alt-btn animated-cta">GET YOUR 30-DAY PLAN</a>
</div>

<!-- ✅ Script -->
<script>
document.addEventListener("DOMContentLoaded", function () {
  const params = new URLSearchParams(window.location.search);
  const Sheep = parseInt(params.get("Sheep")) || 0;
  const Love Bird = parseInt(params.get("Love Bird")) || 0;
  const Owl = parseInt(params.get("Owl")) || 0;
  const Rhino = parseInt(params.get("Rhino")) || 0;
  const firstName = params.get("first_name");

  // Calculate total
  const total = Sheep + Love Bird + Owl + Rhino;

  // Calculate percentages
  const legendPercent = total ? Math.round((Sheep / total) * 100) : 0;
  const renaPercent = total ? Math.round((Love Bird / total) * 100) : 0;
  const visioPercent = total ? Math.round((Owl / total) * 100) : 0;
  const constrPercent = total ? Math.round((Rhino / total) * 100) : 0;

  // Update bars and scores
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
  let ctaText = "GET YOUR 30-DAY PLAN";

  if (highest === legendaria) {
    resultText = "🔥 You’re the Legendary Chingona!";
    resultDesc = "You’ve done what others only dream of. Now it’s time to multiply.";
    ctaLink = "https://www.adrianagallardo.com/pages/legendaria";
  } else if (highest === renacida) {
    resultText = "💥 You’re the Reborn Chingona!";
    resultDesc = "You’ve risen stronger than ever. Now it’s your time to dominate.";
    ctaLink = "https://www.adrianagallardo.com/pages/renacida";
  } else if (highest === visionaria) {
    resultText = "💡 You’re the Visionary Chingona!";
    resultDesc = "You have the vision. Now you need the structure to execute it.";
    ctaLink = "https://www.adrianagallardo.com/pages/visionaria";
  } else if (highest === constructora) {
    resultText = "📐 You’re the Builder Chingona!";
    resultDesc = "You’re already building. Now do it your way.";
    ctaLink = "https://www.adrianagallardo.com/pages/constructora";
  } else if (highest === encaminada) {
    resultText = "🚀 You’re the Chingona On the Way!";
    resultDesc = "You don’t want to start over again. Now it’s time to finish!";
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
    document.getElementById("greeting").innerHTML =
      `Hi <span class="highlight-name">${firstName}</span>, here’s your Chingona power 👇`;
  }
});

</script>

<div style="max-width: 900px; margin: auto; padding: 2rem 1rem; font-family: 'Helvetica Neue', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; background: linear-gradient(to bottom, #f7f7f7, #ffffff);">
 
  <!-- Title -->
  <div style="text-align: center; margin-bottom: 3rem;">
    <h2 style="font-size: 2.3rem; font-weight: 700; color: #005181;">THE ANIMAL PERSONALITY QUIZ</h2>
    <p style="font-size: 1.2rem; color: #333; max-width: 700px; margin: auto;">You’ve already achieved what others only dream of. But legends don’t stagnate—they multiply!</p>
  </div>
 
  <!-- Cards -->
  <div style="display: flex; flex-direction: column; gap: 2rem;">
 
    <div style="background:#D6ECFA
 ; backdrop-filter:blur(8px); border-radius:20px; padding:2rem; box-shadow:0 8px 20px rgba(0,0,0,0.06);">
      <h3 style="color:#1a325d; font-size:1.5rem; font-weight:700;">The harsh reality</h3>
      <p>You’ve built the life, the brand, and the identity. You’ve overcome things that would have broken most people—and you did it while carrying others along the way.</p>
      <p>But now? You’re looking for something deeper. More real. More aligned.  
 You’re powerful—but you’re bored.  
 Respected—but restless.  
 You reached success… and now you’re wondering if this is it.</p>
      <p>It’s not.</p>
      <p>Chingona Circle is where women leaders like you stop settling, stop running on autopilot, and challenge themselves again. It’s not about “achieving more”—it’s about growth and purpose. Deep roots. Sharp clarity. Clean energy. A new level of personal power!</p>
    </div>
 
    <div style="background:#D6ECFA
 ; backdrop-filter:blur(8px); border-radius:20px; padding:2rem; box-shadow:0 8px 20px rgba(0,0,0,0.06);">
      <h3 style="color:#1a325d; font-size:1.5rem; font-weight:700;">Your strengths</h3>
      <ul>
        <li>You have the receipts, the scars, and the wins—you earned your place!</li>
        <li>Your standards are high—for you and for everyone around you.</li>
        <li>The ability to lead, teach, build, and command attention.</li>
      </ul>
    </div>
 
    <div style="background:#D6ECFA
 ; backdrop-filter:blur(8px); border-radius:20px; padding:2rem; box-shadow:0 8px 20px rgba(0,0,0,0.06);">
      <h3 style="color:#1a325d; font-size:1.5rem; font-weight:700;">What’s draining your energy:</h3>
      <ul>
        <li>You’re still doing too much alone.</li>
        <li>You outgrew your previous circle, but you haven’t replaced it yet.</li>
        <li>You don’t feel challenged—and that’s making you slip.</li>
      </ul>
    </div>
 
    <div style="background:#D6ECFA
 ; backdrop-filter:blur(8px); border-radius:20px; padding:2rem; box-shadow:0 8px 20px rgba(0,0,0,0.06);">
      <h3 style="color:#1a325d; font-size:1.5rem; font-weight:700;"> 
 Personal revelations</h3>
      <ul>
        <li>You don’t need more noise. You need more cleanliness/clarity.</li>
        <li>If you don’t find a bigger room, you’ll shrink to fit the one you’re in.</li>
        <li>You’re not stuck—you’re under-challenged.</li>
      </ul>
    </div>
 
    <div style="background:#D6ECFA
 ; backdrop-filter:blur(8px); border-radius:20px; padding:2rem; box-shadow:0 8px 20px rgba(0,0,0,0.06);">
      <h3 style="color:#1a325d; font-size:1.5rem; font-weight:700;">Revelations to take control of your life:</h3>
      <ul>
        <li>Having control of your emotions is no longer optional—it’s your edge.</li>
        <li>People are watching you—and what you tolerate, they will repeat.</li>
        <li>You build a legacy when you raise your internal standards, not just the external ones.</li>
      </ul>
    </div>
 
    <div style="background:#D6ECFA
 ; backdrop-filter:blur(8px); border-radius:20px; padding:2rem; box-shadow:0 8px 20px rgba(0,0,0,0.06);">
      <h3 style="color:#1a325d; font-size:1.5rem; font-weight:700;"> 
 Personal development plan – 30 days</h3>
 
      <h4 style="margin-top:1rem; font-weight:600;">Week 1 – Audit like a CEO</h4>
      <ul>
        <li>Review your energy, schedule, habits, and relationships.</li>
        <li>Eliminate 2 things that aren’t aligned with the woman you say you are.</li>
        <li>Choose ONE personal growth goal you’ve been ignoring—and focus on it every day.</li>
      </ul>
 
      <h4 style="margin-top:1rem; font-weight:600;">Week 2 – Get Your Edge Back</h4>
      <ul>
        <li>Do something that makes you nervous (again).</li>
        <li>Join or create a space where you’re not the woman at the highest level.</li>
        <li>Say what you’ve been holding back—in life, in your business, or with your boundaries.</li>
      </ul>
 
      <h4 style="margin-top:1rem; font-weight:600;">WEEK 3 – CREATE HABITS THAT LEAVE A LEGACY</h4>
      <ul>
        <li>Teach again or mentor—that’s how your power multiplies!</li>
        <li>Level up—multiply your income x10 = multiply your peace x10.</li>
        <li>Organize your day according to your energy, not just your productivity.</li>
      </ul>
 
      <h4 style="margin-top:1rem; font-weight:600;">Week 4 – Activate Expansion</h4>
      <ul>
        <li>Make a move that puts you back in growth mode—hire, fire, invest, or say NO.</li>
        <li>Review your vision for the next 90 days and recommit.</li>
        <li>Surround yourself with women who challenge you—not just applaud you.</li>
      </ul>
    </div>
 
    <!-- CTA + Buttons -->
    <div style="text-align:center; padding:3rem 1rem;">
      <style>
         .bounce-button-xl {
           display:inline-block;
           padding:24px 64px;
           margin:1rem;
           font-size:1.4rem;
           font-weight:800;
           text-decoration:none;
           border-radius:999px;
           box-shadow:0 10px 35px rgba(0,0,0,0.15);
           transition:transform 0.3s ease, box-shadow 0.3s ease;
           animation:pulseGradient 5s infinite linear;
           background-size:200% 200%;
           color:white;
           background-image:linear-gradient(270deg, #1a325d, #1a325d, #1a325d);
         }
 
        .bounce-button-xl:hover {
           transform:scale(1.07) translateY(-6px);
           box-shadow:0 16px 50px rgba(0,0,0,0.2);
         }
 
        .bounce-button-xl.gray {
           background-image:linear-gradient(270deg, #bbbbbb, #dddddd, #bbbbbb);
           color:#333;
         }
 
        @keyframes pulseGradient {
           0% { background-position: 0% 50%; }
           50% { background-position: 100% 50%; }
           100% { background-position: 0% 50%; }
         }
 
        @media (max-width: 500px) {
           .bounce-button-xl {
             font-size: 1.1rem;
             padding: 18px 36px;
           }
         }
      </style>
 
      <h3 style="color:#1a325d; font-size:1.5rem; font-weight:700;"> 
        Lead from abundance, not exhaustion
      </h3>
      <p style="font-size:1.2rem; color:#444; max-width:700px; margin:0 auto 2rem auto; line-height:1.6;">
        In Chingona Circle, strong women become even stronger.  
 This is your space to keep growing without having to lead alone. 
      </p>
 
      <a href="https://calendly.com/d/crsw-3zj-2w5/haz-tu-cita-para-una-sesion-de-negocios-gratis" class="bounce-button-xl">
        BOOK YOUR FREE CONSULTATION
      </a>
 
      <a href="https://cdn.shopify.com/s/files/1/0524/7326/6329/files/Chingona_Legendaria.pdf?v=1747440726" class="bounce-button-xl gray">
        ACCESS THE FULL PLAN
      </a>
    </div>
 
  </div>
</div>
