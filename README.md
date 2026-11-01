<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Sanjeev Kumar Patel, CS student learning ML the slow way</title>
<meta name="description" content="Portfolio of Sanjeev Kumar Patel: CS undergrad at NIT Srinagar working on DSA, full-stack and machine learning.">
<meta property="og:title" content="Sanjeev Kumar Patel, CS student learning ML the slow way">
<meta property="og:description" content="DSA in C++, full-stack, and machine learning from the math up. Portfolio of a CS undergrad at NIT Srinagar.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://sanjeev-kumar-patel.github.io/">
<meta name="theme-color" content="#1F6FEB">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400;12..96,600;12..96,800&family=Caveat:wght@500;700&display=swap" rel="stylesheet">
<style>
:root{--paper:#EBF0F7;--ink:#14213D;--muted:#4A5878;--pen:#1F6FEB;--red:#C2255C;--grid:rgba(31,111,235,.10);--line:rgba(20,33,61,.2);--code:#E1E8F3;color-scheme:light;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--paper:#0D1424;--ink:#E6ECF7;--muted:#9AA8C6;--pen:#6FA8FF;--red:#FF7AA8;--grid:rgba(111,168,255,.09);--line:rgba(230,236,247,.2);--code:#16213A;color-scheme:dark}}
:root[data-theme="dark"]{--paper:#0D1424;--ink:#E6ECF7;--muted:#9AA8C6;--pen:#6FA8FF;--red:#FF7AA8;--grid:rgba(111,168,255,.09);--line:rgba(230,236,247,.2);--code:#16213A;color-scheme:dark}
*,*::before,*::after{box-sizing:inherit}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background-color:var(--paper);background-image:linear-gradient(var(--grid) 1px,transparent 1px),linear-gradient(90deg,var(--grid) 1px,transparent 1px);background-size:28px 28px;color:var(--ink);font:400 1.0625rem/1.65 "Bricolage Grotesque",system-ui,-apple-system,"Segoe UI",sans-serif}
.page{position:relative;max-width:46rem;margin:0 auto;padding:4rem 1.4rem 3rem 2rem}
.page::before{content:"";position:absolute;left:.7rem;top:0;bottom:0;width:2px;background:var(--red);opacity:.45}
h1,h2{font-weight:800;letter-spacing:-.02em;line-height:1.05;margin:0}
h1{font-size:clamp(2.8rem,10vw,5rem)}
h2{font-size:clamp(1.7rem,5vw,2.3rem);margin-bottom:1rem}
section{margin-top:5rem}
p{margin:0 0 1rem;max-width:62ch}
a{color:var(--pen);text-underline-offset:3px}
a:focus-visible,button:focus-visible,input:focus-visible,canvas:focus-visible{outline:3px solid var(--pen);outline-offset:3px;border-radius:4px}
.note{font-family:Caveat,"Bradley Hand","Segoe Script",cursive;font-weight:700;font-size:1.35rem;line-height:1.2;color:var(--red);display:inline-block;transform:rotate(-2deg)}
.lede{font-size:1.25rem;margin-top:1.4rem}
/* playground */
.lab{margin-top:2.4rem;border:2px solid var(--ink);border-radius:6px;background:var(--paper)}
.lab canvas{display:block;width:100%;height:230px;cursor:crosshair;touch-action:none}
.lab .bar{display:flex;flex-wrap:wrap;gap:.6rem 1.4rem;align-items:center;padding:.7rem 1rem;border-top:2px solid var(--ink);font-size:.95rem}
.lab label{display:flex;gap:.6rem;align-items:center}
.lab input{accent-color:var(--pen);width:9rem}
#st{flex:1 1 14rem;color:var(--muted)}
/* rows */
.row{border-left:3px solid var(--pen);padding:.2rem 0 .2rem 1rem;margin-bottom:1.6rem}
.row h3{margin:0;font-size:1.25rem}
.row p{margin:.2rem 0}
pre{background:var(--code);border-radius:6px;padding:1rem 1.1rem;overflow-x:auto;font:.9rem/1.55 ui-monospace,"SF Mono",Menlo,Consolas,monospace;margin:1rem 0 .4rem}
dl{margin:0}
dt{font-weight:800;margin-top:1rem}
dd{margin:0;color:var(--muted)}
ol.path{list-style:none;margin:0;padding:0;counter-reset:s}
ol.path li{counter-increment:s;position:relative;padding:0 0 1.6rem 3rem}
ol.path li::before{content:counter(s);position:absolute;left:0;top:0;width:2.1rem;height:2.1rem;border-radius:50%;border:2px solid var(--ink);display:grid;place-items:center;font-weight:800;font-size:.95rem;background:var(--paper)}
ol.path li::after{content:"";position:absolute;left:1rem;top:2.3rem;bottom:.2rem;width:2px;background:var(--line)}
ol.path li:last-child::after{display:none}
ol.path li.now::before{background:var(--pen);border-color:var(--pen);color:var(--paper)}
ol.path b{display:block;font-size:1.15rem}
ol.path span{color:var(--muted)}
.links{display:flex;flex-wrap:wrap;gap:.7rem;margin-top:1.4rem}
.links a,.links button{font:inherit;font-weight:600;color:var(--ink);background:transparent;border:2px solid var(--ink);border-radius:6px;padding:.55rem 1rem;text-decoration:none;cursor:pointer}
.links a:hover,.links button:hover{background:var(--ink);color:var(--paper)}
footer{margin-top:4rem;color:var(--muted);font-size:.9rem}
/* loader */
#loader{position:fixed;inset:0;z-index:50;background:#070B16;color:#DCE8FF;display:grid;place-items:center;align-content:center;gap:1.6rem;text-align:center;cursor:pointer;transition:opacity .5s}
#loader.out{opacity:0;pointer-events:none}
.holo{font:800 clamp(2.4rem,11vw,4.6rem)/1 "Bricolage Grotesque",system-ui,sans-serif;letter-spacing:.06em;position:relative;transform:perspective(700px) rotateX(16deg);text-shadow:0 0 22px rgba(80,160,255,.6)}
.holo::before,.holo::after{content:attr(data-t);position:absolute;inset:0;mix-blend-mode:screen}
.holo::before{color:#18E0FF;transform:translate(-3px,0);opacity:.55}
.holo::after{color:#FF3FA4;transform:translate(3px,0);opacity:.45;animation:fl 2.4s steps(1) infinite}
@keyframes fl{0%,100%{transform:translate(3px,0)}50%{transform:translate(2px,1px)}}
.ring{position:relative;width:8rem;height:8rem}
.ring svg{width:100%;height:100%;transform:rotate(-90deg)}
.ring circle{fill:none;stroke-width:5}
.ring .bg{stroke:#1B2742}
.ring .fg{stroke:#58A6FF;stroke-linecap:round;stroke-dasharray:326.7;stroke-dashoffset:326.7}
#pct{position:absolute;inset:0;display:grid;place-items:center;font-weight:800;font-size:1.5rem}
#steps{list-style:none;margin:0;padding:0;text-align:left;font-size:.98rem}
#steps li{opacity:.35;padding:.12rem 0 .12rem 1.4rem;position:relative}
#steps li.now{opacity:1}
#steps li.done{opacity:.7}
#steps li.done::before{content:"\2713";position:absolute;left:0;color:#58A6FF}
#steps li.now::before{content:"\203A";position:absolute;left:.3rem;color:#FF3FA4}
.skip{font-size:.85rem;opacity:.5}
@media (prefers-reduced-motion:reduce){.holo::after{animation:none}#loader{transition:none}}
</style>
<noscript><style>#loader{display:none}</style></noscript>
</head>
<body>
<div id="loader" role="status" aria-label="Loading portfolio">
  <div class="holo" data-t="SANJEEV">SANJEEV</div>
  <div class="ring"><svg viewBox="0 0 120 120"><circle class="bg" cx="60" cy="60" r="52"/><circle class="fg" id="fg" cx="60" cy="60" r="52"/></svg><div id="pct">0%</div></div>
  <ol id="steps">
    <li>Compiling the C++ I trust</li>
    <li>Re-deriving the gradient by hand</li>
    <li>Counting problems (still not the point)</li>
    <li>Breaking one small thing on purpose</li>
    <li>Putting it back together</li>
  </ol>
  <div class="skip">Tap anywhere to skip</div>
</div>

<main class="page">
  <header>
    <h1>Hi, I’m Sanjeev.</h1>
    <p class="lede">I’m a CS student at NIT Srinagar (class of 2028), and I learn best when something is actually broken.</p>
    <p>I don’t trust a model until I’ve seen the math. So here is the smallest version of one: a ball rolling down a loss curve.</p>
    <div class="lab">
      <canvas id="gd" tabindex="0" role="img" aria-label="Loss curve with two valleys. Click or tap to drop a point and watch gradient descent roll it downhill."></canvas>
      <div class="bar">
        <label>Learning rate <input id="lr" type="range" min="0.02" max="0.9" step="0.01" value="0.12"> <output id="lrv">0.12</output></label>
        <span id="st" aria-live="polite">Click or tap the curve to drop a point.</span>
      </div>
    </div>
    <span class="note" style="margin-top:.8rem">try the right side, then crank the learning rate up</span>
  </header>

  <section id="about">
    <h2>What I’m like</h2>
    <p>Give me a slow query, a weird bug or a half-working schema and I’ll happily lose a weekend to it. The projects where the answer is sitting in a tutorial three tabs over don’t teach me much.</p>
    <p>Right now I’m pulled toward machine learning and data science, but I’m doing it the slow way: the probability, the linear algebra and the statistics most tutorials skip. It takes longer. It’s also the only way I end up believing the number at the end.</p>
    <p>If something in one of my repos is useful, take it and run. If it’s broken, even better. Tell me why.</p>
  </section>

  <section id="building">
    <h2>Things I’m building</h2>
    <div class="row">
      <h3>GitHub bug scanner</h3>
      <p>Watches pushes and pull requests, looks for bugs, posts what it finds to GitHub and a dashboard, then tracks whether they get fixed.</p>
      <span class="note">still on paper</span>
    </div>
    <div class="row">
      <h3>Dining Philosophers</h3>
      <p>The classic OS synchronisation problem, written in C++17 for my operating systems coursework.</p>
      <span class="note">coursework, but it’s a good bug magnet</span>
    </div>
    <p>The rest lives on <a href="https://github.com/sanjeev-kumar-patel">GitHub</a>.</p>
  </section>

  <section id="dsa">
    <h2>How I read a problem</h2>
    <p>I’m past 400 problems on LeetCode and GeeksforGeeks, mostly in C++. The count was never the point. What I track is how quickly I can look at something new and see its shape: graphs, DP, greedy, binary search, and always the complexity.</p>
<pre><code>// Smallest speed that still finishes in time.
// The question I ask first: is the answer monotonic?
int lo = 1, hi = *max_element(a.begin(), a.end());
while (lo &lt; hi) {
    int mid = lo + (hi - lo) / 2;
    if (canFinish(a, mid, h)) hi = mid;
    else lo = mid + 1;
}
return lo;</code></pre>
    <span class="note">if yes, binary search the answer</span>
    <p style="margin-top:1rem"><a href="https://leetcode.com/u/sanjeev-kumar-patel/">My LeetCode profile</a></p>
  </section>

  <section id="toolbox">
    <h2>What I reach for</h2>
    <dl>
      <dt>For problem solving</dt><dd>C++ first, C when I want to be closer to the machine.</dd>
      <dt>For the web</dt><dd>JavaScript, React, Node.js, Express, HTML and CSS, with MySQL or MongoDB behind it.</dd>
      <dt>Day to day</dt><dd>Git and GitHub, Linux and Bash, VS Code, Postman.</dd>
      <dt>Still learning</dt><dd>Python, NumPy, pandas, scikit-learn and Jupyter, properly, not just the API.</dd>
    </dl>
  </section>

  <section id="path">
    <h2>The roadmap, mistakes included</h2>
    <ol class="path">
      <li class="now"><b>DSA and C++</b><span>Graphs and DP. I’m not rushing past this; everything else sits on top of it.</span></li>
      <li class="now"><b>Math and statistics</b><span>Probability and linear algebra, the parts tutorials skip.</span></li>
      <li><b>ML fundamentals</b><span>Build from scratch first, then reach for the library.</span></li>
      <li><b>Data science</b><span>Real datasets and honest results.</span></li>
    </ol>
  </section>

  <section id="contact">
    <h2>Say hello</h2>
    <p>I’m up for talking about DSA, backend design, debugging stories, or how to learn ML without just calling <code>.fit()</code>. If you found a bug in one of my repos, I especially want to hear from you.</p>
    <div class="links">
      <button type="button" id="copy" data-email="sanjeev2005p.05@gmail.com">Copy email</button>
      <a href="mailto:sanjeev2005p.05@gmail.com">Write an email</a>
      <a href="https://www.linkedin.com/in/sanjeev-kumar-patel/">LinkedIn</a>
      <a href="https://github.com/sanjeev-kumar-patel">GitHub</a>
    </div>
    <span id="cs" class="note" aria-live="polite" style="margin-top:.8rem"></span>
  </section>

  <footer>Built by hand, on graph paper. Stars on a repo are noticed.</footer>
</main>

<script>
(function(){
  var $=function(s){return document.querySelector(s)};
  /* loader */
  var L=$('#loader'),fg=$('#fg'),pct=$('#pct'),li=[].slice.call(document.querySelectorAll('#steps li')),t0=performance.now(),D=2800,gone=false;
  function finish(){if(gone)return;gone=true;L.classList.add('out');setTimeout(function(){L.remove()},550)}
  function tick(n){if(gone)return;var p=Math.min(1,(n-t0)/D),i=Math.min(4,Math.floor(p*5));
    fg.style.strokeDashoffset=326.7*(1-p);pct.textContent=Math.round(p*100)+'%';
    li.forEach(function(e,j){e.className=p===1||j<i?'done':j===i?'now':''});
    p<1?requestAnimationFrame(tick):setTimeout(finish,250)}
  L.addEventListener('click',finish);
  if(matchMedia('(prefers-reduced-motion:reduce)').matches){finish()}else{requestAnimationFrame(tick)}

  /* gradient descent */
  var cv=$('#gd'),cx=cv.getContext('2d'),W=0,H=0,X0=-2.4,X1=2.4,Y0=-.6,Y1=3.6;
  var f=function(x){return .2*x*x*x*x-.9*x*x+.35*x+1.2},g=function(x){return .8*x*x*x-1.8*x+.35};
  var lr=.12,x=null,trail=[],n=0,timer=null,msg=$('#st'),down=false;
  var px=function(v){return (v-X0)/(X1-X0)*W},py=function(v){return H-14-(v-Y0)/(Y1-Y0)*(H-28)};
  var css=function(k){return getComputedStyle(document.documentElement).getPropertyValue(k).trim()};
  function fit(){var r=cv.getBoundingClientRect(),d=window.devicePixelRatio||1;W=r.width;H=r.height;cv.width=W*d;cv.height=H*d;cx.setTransform(d,0,0,d,0,0);draw()}
  function draw(){
    cx.clearRect(0,0,W,H);
    cx.strokeStyle=css('--pen');cx.lineWidth=3;cx.beginPath();
    for(var i=0;i<=200;i++){var v=X0+(X1-X0)*i/200;i?cx.lineTo(px(v),py(f(v))):cx.moveTo(px(v),py(f(v)))}
    cx.stroke();
    cx.fillStyle=css('--muted');
    trail.forEach(function(v){cx.globalAlpha=.5;cx.beginPath();cx.arc(px(v),py(f(v)),2.5,0,7);cx.fill()});cx.globalAlpha=1;
    if(x!==null&&Math.abs(x)<=X1+3){
      var s=g(x),a=x-.55,b=x+.55;
      cx.strokeStyle=css('--red');cx.lineWidth=1.5;cx.beginPath();cx.moveTo(px(a),py(f(x)+s*(a-x)));cx.lineTo(px(b),py(f(x)+s*(b-x)));cx.stroke();
      cx.fillStyle=css('--red');cx.beginPath();cx.arc(px(x),py(f(x)),7,0,7);cx.fill()}
  }
  function stop(t){clearInterval(timer);timer=null;msg.textContent=t;draw()}
  function step(){
    x-=lr*g(x);n++;trail.push(x);if(trail.length>60)trail.shift();
    if(Math.abs(x)>6){x=null;return stop('Learning rate too high. It overshot and left the page.')}
    if(Math.abs(g(x))<.003||n>500){return stop(x>0?'Settled at x = '+x.toFixed(2)+', loss '+f(x).toFixed(2)+'. That is a local minimum, not the best valley. Try the left side.':'Settled at x = '+x.toFixed(2)+', loss '+f(x).toFixed(2)+'. This is the deepest valley.')}
    msg.textContent='Step '+n+': x = '+x.toFixed(2)+', loss = '+f(x).toFixed(2);draw()}
  function drop(e){var r=cv.getBoundingClientRect();x=X0+(e.clientX-r.left)/r.width*(X1-X0);trail=[];n=0;draw();clearInterval(timer);timer=setInterval(step,70)}
  cv.addEventListener('pointerdown',function(e){down=true;cv.setPointerCapture(e.pointerId);drop(e)});
  cv.addEventListener('pointermove',function(e){if(down)drop(e)});
  cv.addEventListener('pointerup',function(){down=false});
  cv.addEventListener('keydown',function(e){if(e.key==='Enter'||e.key===' '){e.preventDefault();var r=cv.getBoundingClientRect();drop({clientX:r.left+r.width*(.65+Math.random()*.25)})}});
  $('#lr').addEventListener('input',function(e){lr=+e.target.value;$('#lrv').textContent=lr.toFixed(2)});
  addEventListener('resize',fit);
  matchMedia('(prefers-color-scheme:dark)').addEventListener('change',draw);
  if(document.fonts&&document.fonts.ready)document.fonts.ready.then(fit);
  fit();

  /* copy email */
  $('#copy').addEventListener('click',function(){
    var m=this.dataset.email,out=$('#cs');
    (navigator.clipboard?navigator.clipboard.writeText(m):Promise.reject()).then(function(){out.textContent='Email copied.'},function(){out.textContent='Copy failed. It is '+m})
  });
})();
</script>
</body>
</html>
