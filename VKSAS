<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Calculator Hub -- All‑in‑One</title>
  <style>
    :root{
      --bg:#0f172a;        /* slate-900 */
      --panel:#111827;     /* gray-900 */
      --muted:#1f2937;     /* gray-800 */
      --text:#e5e7eb;      /* gray-200 */
      --accent:#22c55e;    /* green-500 */
      --accent-2:#60a5fa;  /* blue-400 */
      --card:#0b1225;
      --shadow:0 10px 30px rgba(0,0,0,.35);
    }
    *{box-sizing:border-box}
    body{margin:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,Inter,Arial,sans-serif;background:linear-gradient(180deg,#0b1225,#0f172a 20%);color:var(--text)}
    header{position:sticky;top:0;z-index:50;background:rgba(17,24,39,.7);backdrop-filter:blur(8px);border-bottom:1px solid #1f2937}
    .wrap{max-width:1100px;margin:0 auto;padding:18px 20px;display:flex;align-items:center;gap:14px}
    .logo{display:flex;align-items:center;gap:10px;font-weight:800;font-size:1.25rem;letter-spacing:.3px}
    .logo .dot{width:10px;height:10px;border-radius:50%;background:var(--accent)}
    .pill{margin-left:auto;display:flex;gap:8px}
    .pill button{background:var(--muted);border:1px solid #374151;color:var(--text);padding:8px 12px;border-radius:999px;cursor:pointer}
    .container{max-width:1100px;margin:22px auto 60px;padding:0 20px;display:grid;grid-template-columns:280px 1fr;gap:20px}
    @media (max-width:900px){.container{grid-template-columns:1fr}}
    .sidebar{position:sticky;top:74px;background:var(--panel);border:1px solid #1f2937;border-radius:16px;padding:14px 12px;box-shadow:var(--shadow)}
    .search{display:flex;gap:8px;margin:8px 8px 12px}
    .search input{flex:1;background:#0b1225;border:1px solid #1f2937;border-radius:10px;color:var(--text);padding:10px 12px}
    .group-title{font-size:.8rem;opacity:.8;margin:12px 10px 6px}
    .nav{display:flex;flex-direction:column;gap:6px}
    .nav button{width:100%;text-align:left;background:#0b1225;border:1px solid #1f2937;color:var(--text);padding:10px 12px;border-radius:10px;cursor:pointer}
    .nav button.active{border-color:var(--accent);outline:2px solid rgba(34,197,94,.2)}.main{display:flex;flex-direction:column;gap:16px}
.card{background:var(--panel);border:1px solid #1f2937;border-radius:18px;box-shadow:var(--shadow)}
.card h2{margin:0;padding:18px 18px 0;font-size:1.2rem}
.card .content{padding:18px}
.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
@media (max-width:700px){.grid{grid-template-columns:1fr}}
label{font-size:.9rem;opacity:.9}
input,select{width:100%;margin-top:6px;background:#0b1225;border:1px solid #1f2937;color:var(--text);padding:10px 12px;border-radius:12px}
.btn{background:linear-gradient(90deg,var(--accent),#16a34a);border:none;color:white;padding:12px 16px;border-radius:12px;cursor:pointer}
.btn.secondary{background:#0b1225;border:1px solid #334155}
.row{display:flex;gap:10px;flex-wrap:wrap;align-items:center}
.result{background:#0b1225;border:1px dashed #334155;padding:12px 14px;border-radius:12px;word-break:break-word}
.muted{opacity:.7;font-size:.9rem}
footer{max-width:1100px;margin:30px auto 60px;padding:0 20px;text-align:center;opacity:.8}

  </style>
</head>
<body>
  <header>
    <div class="wrap">
      <div class="logo"><span class="dot"></span> Calculator Hub <span class="muted">-- All‑in‑One</span></div>
      <div class="pill"><button id="clearAll">Reset All</button><button id="copyLink">Share Page</button></div>
    </div>
  </header>  <div class="container">
    <!-- Sidebar -->
    <aside class="sidebar">
      <div class="search">
        <input id="filter" placeholder="Search calculators…" />
      </div>
      <div class="group">
        <div class="group-title">Math</div>
        <div class="nav">
          <button data-target="basic">Basic Calculator</button>
          <button data-target="scientific">Scientific (Lite)</button>
          <button data-target="percentage">Percentage / Discount</button>
          <button data-target="emi">Loan EMI</button>
        </div>
      </div>
      <div class="group">
        <div class="group-title">Converters</div>
        <div class="nav">
          <button data-target="temperature">Temperature</button>
          <button data-target="length">Length / Distance</button>
          <button data-target="weight">Weight / Mass</button>
          <button data-target="time">Time</button>
          <button data-target="currency">Currency*</button>
        </div>
      </div>
      <div class="group">
        <div class="group-title">Daily Life</div>
        <div class="nav">
          <button data-target="bmi">BMI</button>
          <button data-target="age">Age</button>
          <button data-target="fuel">Fuel Cost</button>
          <button data-target="screentime">Screen Time</button>
        </div>
      </div>
      <div class="muted" style="margin:10px 12px 0">* Offline demo rates. For live rates, add an API later.</div>
    </aside><!-- Main -->
<main class="main">
  <!-- BASIC CALC -->
  <section id="basic" class="card">
    <h2>Basic Calculator</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Expression (e.g., 12 + 3 * 4)</label>
          <input id="basicExp" placeholder="Type expression" />
        </div>
        <div class="row" style="align-items:flex-end">
          <button class="btn" onclick="calcBasic()">Calculate</button>
          <div id="basicOut" class="result">Result: --</div>
        </div>
      </div>
    </div>
  </section>

  <!-- SCIENTIFIC LITE -->
  <section id="scientific" class="card" hidden>
    <h2>Scientific (Lite)</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Value</label>
          <input id="sciVal" type="number" placeholder="Enter number" />
        </div>
        <div>
          <label>Function</label>
          <select id="sciFn">
            <option value="sqrt">√ Square Root</option>
            <option value="pow2">x²</option>
            <option value="pow3">x³</option>
            <option value="sin">sin(x)</option>
            <option value="cos">cos(x)</option>
            <option value="tan">tan(x)</option>
            <option value="log">log₁₀(x)</option>
            <option value="ln">ln(x)</option>
          </select>
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="calcSci()">Compute</button>
        <div id="sciOut" class="result">Result: --</div>
      </div>
      <div class="muted" style="margin-top:8px">Trigonometric inputs use radians for precision.</div>
    </div>
  </section>

  <!-- PERCENTAGE / DISCOUNT -->
  <section id="percentage" class="card" hidden>
    <h2>Percentage / Discount</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Original Price</label>
          <input id="price" type="number" placeholder="e.g., 1499" />
        </div>
        <div>
          <label>Discount %</label>
          <input id="discount" type="number" placeholder="e.g., 28" />
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="calcDiscount()">Calculate</button>
        <div id="discOut" class="result">Final: -- | You save: --</div>
      </div>
    </div>
  </section>

  <!-- EMI -->
  <section id="emi" class="card" hidden>
    <h2>Loan EMI</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Principal (₹)</label>
          <input id="emiP" type="number" placeholder="e.g., 200000" />
        </div>
        <div>
          <label>Annual Interest (%)</label>
          <input id="emiR" type="number" step="0.01" placeholder="e.g., 10.5" />
        </div>
        <div>
          <label>Tenure (months)</label>
          <input id="emiN" type="number" placeholder="e.g., 36" />
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="calcEMI()">Compute EMI</button>
        <div id="emiOut" class="result">EMI: -- | Total Interest: -- | Total: --</div>
      </div>
    </div>
  </section>

  <!-- TEMPERATURE CONVERTER -->
  <section id="temperature" class="card" hidden>
    <h2>Temperature Converter</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Value</label>
          <input id="tempVal" type="number" placeholder="e.g., 36.6" />
        </div>
        <div>
          <label>From</label>
          <select id="tempFrom"><option>Celsius</option><option>Fahrenheit</option><option>Kelvin</option></select>
        </div>
        <div>
          <label>To</label>
          <select id="tempTo"><option>Fahrenheit</option><option>Celsius</option><option>Kelvin</option></select>
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="convertTemp()">Convert</button>
        <div id="tempOut" class="result">--</div>
      </div>
    </div>
  </section>

  <!-- LENGTH CONVERTER -->
  <section id="length" class="card" hidden>
    <h2>Length / Distance</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Value</label>
          <input id="lenVal" type="number" placeholder="e.g., 1" />
        </div>
        <div>
          <label>From</label>
          <select id="lenFrom"><option>meter</option><option>kilometer</option><option>centimeter</option><option>mile</option><option>foot</option></select>
        </div>
        <div>
          <label>To</label>
          <select id="lenTo"><option>kilometer</option><option>meter</option><option>centimeter</option><option>mile</option><option>foot</option></select>
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="convertLength()">Convert</button>
        <div id="lenOut" class="result">--</div>
      </div>
    </div>
  </section>

  <!-- WEIGHT CONVERTER -->
  <section id="weight" class="card" hidden>
    <h2>Weight / Mass</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Value</label>
          <input id="wtVal" type="number" placeholder="e.g., 5" />
        </div>
        <div>
          <label>From</label>
          <select id="wtFrom"><option>kilogram</option><option>gram</option><option>pound</option><option>ounce</option></select>
        </div>
        <div>
          <label>To</label>
          <select id="wtTo"><option>gram</option><option>kilogram</option><option>pound</option><option>ounce</option></select>
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="convertWeight()">Convert</button>
        <div id="wtOut" class="result">--</div>
      </div>
    </div>
  </section>

  <!-- TIME CONVERTER -->
  <section id="time" class="card" hidden>
    <h2>Time Converter</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Value</label>
          <input id="timeVal" type="number" placeholder="e.g., 3600" />
        </div>
        <div>
          <label>From</label>
          <select id="timeFrom"><option>second</option><option>minute</option><option>hour</option><option>day</option></select>
        </div>
        <div>
          <label>To</label>
          <select id="timeTo"><option>minute</option><option>second</option><option>hour</option><option>day</option></select>
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="convertTime()">Convert</button>
        <div id="timeOut" class="result">--</div>
      </div>
    </div>
  </section>

  <!-- BMI -->
  <section id="bmi" class="card" hidden>
    <h2>BMI Calculator</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Height (cm)</label>
          <input id="bmiH" type="number" placeholder="e.g., 165" />
        </div>
        <div>
          <label>Weight (kg)</label>
          <input id="bmiW" type="number" placeholder="e.g., 55" />
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="calcBMI()">Calculate</button>
        <div id="bmiOut" class="result">BMI: --</div>
      </div>
    </div>
  </section>

  <!-- AGE -->
  <section id="age" class="card" hidden>
    <h2>Age Calculator</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Date of Birth</label>
          <input id="dob" type="date" />
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="calcAge()">Find Age</button>
        <div id="ageOut" class="result">--</div>
      </div>
    </div>
  </section>

  <!-- FUEL COST -->
  <section id="fuel" class="card" hidden>
    <h2>Fuel Cost</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Distance (km)</label>
          <input id="fuelD" type="number" placeholder="e.g., 120" />
        </div>
        <div>
          <label>Mileage (km/l)</label>
          <input id="fuelM" type="number" placeholder="e.g., 18" />
        </div>
        <div>
          <label>Fuel Price (₹/l)</label>
          <input id="fuelP" type="number" placeholder="e.g., 105" />
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="calcFuel()">Calculate</button>
        <div id="fuelOut" class="result">--</div>
      </div>
    </div>
  </section>

  <!-- SCREEN TIME -->
  <section id="screentime" class="card" hidden>
    <h2>Screen Time</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Daily average (hours)</label>
          <input id="scrH" type="number" placeholder="e.g., 3.5" />
        </div>
        <div>
          <label>Days</label>
          <input id="scrD" type="number" placeholder="e.g., 7" />
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="calcScreen()">Compute</button>
        <div id="scrOut" class="result">--</div>
      </div>
    </div>
  </section>

  <!-- CURRENCY -->
  <section id="currency" class="card" hidden>
    <h2>Currency Converter (Offline Demo)</h2>
    <div class="content">
      <div class="grid">
        <div>
          <label>Amount</label>
          <input id="curVal" type="number" placeholder="e.g., 100" />
        </div>
        <div>
          <label>From</label>
          <select id="curFrom"><option>INR</option><option>USD</option><option>EUR</option></select>
        </div>
        <div>
          <label>To</label>
          <select id="curTo"><option>USD</option><option>INR</option><option>EUR</option></select>
        </div>
      </div>
      <div class="row" style="margin-top:10px">
        <button class="btn" onclick="convertCurrency()">Convert</button>
        <div id="curOut" class="result">--</div>
      </div>
      <div class="muted" style="margin-top:8px">Rates are for demo only (e.g., 1 USD ≈ 83 INR, 1 EUR ≈ 90 INR). Replace with a live API later.</div>
    </div>
  </section>

</main>

  </div>  <footer>
    © 2025 Calculator Hub • Made with ❤ by Vaibhav • Tip: Press <kbd>/</kbd> to jump to search
  </footer><script>
  // ---------- Sidebar navigation ----------
  const buttons=[...document.querySelectorAll('.sidebar .nav button')];
  const sections=[...document.querySelectorAll('main section.card')];
  function show(id){sections.forEach(s=>{s.hidden = s.id!==id});buttons.forEach(b=>{b.classList.toggle('active', b.dataset.target===id)});location.hash = id}
  buttons.forEach(b=>b.addEventListener('click',()=>show(b.dataset.target)));
  if(location.hash){const id=location.hash.slice(1);const b=buttons.find(x=>x.dataset.target===id);(b?show(id):show('basic'))}else{show('basic')}

  // Search filter
  const filter=document.getElementById('filter');
  filter.addEventListener('input',()=>{
    const q=filter.value.toLowerCase();
    buttons.forEach(b=>{
      const ok=b.textContent.toLowerCase().includes(q);
      b.style.display = ok? 'block':'none';
    });
  });
  window.addEventListener('keydown',e=>{if(e.key==='/' && document.activeElement.tagName!=='INPUT'){e.preventDefault();filter.focus()}});

  // Utility helpers
  const fmt = n=> (Number.isFinite(n)? new Intl.NumberFormat(undefined,{maximumFractionDigits:6}).format(n):'--');

  // ---------- Basic Calculator ----------
  function calcBasic(){
    const exp=document.getElementById('basicExp').value;
    try{
      // very small, safe evaluator: allow digits + ops only
      if(!/^[-+/*()% .\d]+$/.test(exp)) throw Error('Invalid characters');
      // eslint-disable-next-line no-new-func
      const val = Function('return ('+exp+')')();
      document.getElementById('basicOut').textContent='Result: '+fmt(val);
    }catch(err){document.getElementById('basicOut').textContent='Error: check expression';}
  }

  // ---------- Scientific (Lite) ----------
  function calcSci(){
    const x=parseFloat(document.getElementById('sciVal').value);
    const fn=document.getElementById('sciFn').value;
    let y=NaN;
    switch(fn){
      case 'sqrt': y=Math.sqrt(x); break;
      case 'pow2': y=x**2; break;
      case 'pow3': y=x**3; break;
      case 'sin': y=Math.sin(x); break;
      case 'cos': y=Math.cos(x); break;
      case 'tan': y=Math.tan(x); break;
      case 'log': y=Math.log10(x); break;
      case 'ln': y=Math.log(x); break;
    }
    document.getElementById('sciOut').textContent='Result: '+fmt(y);
  }

  // ---------- Discount ----------
  function calcDiscount(){
    const p=+document.getElementById('price').value;
    const d=+document.getElementById('discount').value;
    const save = p*d/100; const final=p-save;
    document.getElementById('discOut').textContent=`Final: ${fmt(final)} | You save: ${fmt(save)}`;
  }

  // ---------- EMI ----------
  function calcEMI(){
    const P=+document.getElementById('emiP').value;
    const R=+document.getElementById('emiR').value/12/100; // monthly rate
    const N=+document.getElementById('emiN').value;
    if(!P||!R||!N){document.getElementById('emiOut').textContent='Please enter all values';return}
    const emi = P*R*( (1+R)**N ) / ( (1+R)**N - 1 );
    const total = emi*N; const interest = total-P;
    document.getElementById('emiOut').textContent=`EMI: ₹${fmt(emi)} | Total Interest: ₹${fmt(interest)} | Total: ₹${fmt(total)}`;
  }

  // ---------- Temperature ----------
  function toC(val,unit){
    if(unit==='Celsius') return val;
    if(unit==='Fahrenheit') return (val-32)*5/9;
    if(unit==='Kelvin') return val-273.15;
  }
  function fromC(val,unit){
    if(unit==='Celsius') return val;
    if(unit==='Fahrenheit') return val*9/5+32;
    if(unit==='Kelvin') return val+273.15;
  }
  function convertTemp(){
    const v=+document.getElementById('tempVal').value;
    const a=document.getElementById('tempFrom').value;
    const b=document.getElementById('tempTo').value;
    const c=fromC(toC(v,a),b);
    document.getElementById('tempOut').textContent=`${fmt(v)} ${a} = ${fmt(c)} ${b}`;
  }

  // ---------- Length ----------
  const L={ meter:1, kilometer:1000, centimeter:0.01, mile:1609.344, foot:0.3048 };
  function convertLength(){
    const v=+document.getElementById('lenVal').value;
    const a=document.getElementById('lenFrom').value; const b=document.getElementById('lenTo').value;
    const m=v*L[a]; const out=m/L[b];
    document.getElementById('lenOut').textContent=`${fmt(v)} ${a} = ${fmt(out)} ${b}`;
  }

  // ---------- Weight ----------
  const W={ kilogram:1, gram:0.001, pound:0.45359237, ounce:0.028349523125 };
  function convertWeight(){
    const v=+document.getElementById('wtVal').value;
    const a=document.getElementById('wtFrom').value; const b=document.getElementById('wtTo').value;
    const kg=v*W[a]; const out=kg/W[b];
    document.getElementById('wtOut').textContent=`${fmt(v)} ${a} = ${fmt(out)} ${b}`;
  }

  // ---------- Time ----------
  const T={ second:1, minute:60, hour:3600, day:86400 };
  function convertTime(){
    const v=+document.getElementById('timeVal').value;
    const a=document.getElementById('timeFrom').value; const b=document.getElementById('timeTo').value;
    const s=v*T[a]; const out=s/T[b];
    document.getElementById('timeOut').textContent=`${fmt(v)} ${a}s = ${fmt(out)} ${b}s`;
  }

  // ---------- BMI ----------
  function calcBMI(){
    const hCm=+document.getElementById('bmiH').value; const w=+document.getElementById('bmiW').value;
    const hM=hCm/100; const bmi=w/(hM*hM);
    let cat='--';
    if(bmi<18.5) cat='Underweight'; else if(bmi<25) cat='Normal'; else if(bmi<30) cat='Overweight'; else cat='Obese';
    document.getElementById('bmiOut').textContent=`BMI: ${fmt(bmi)} (${cat})`;
  }

  // ---------- Age ----------
  function calcAge(){
    const dobVal=document.getElementById('dob').value; if(!dobVal){document.getElementById('ageOut').textContent='Please pick a date';return}
    const dob=new Date(dobVal); const now=new Date();
    let y=now.getFullYear()-dob.getFullYear();
    let m=now.getMonth()-dob.getMonth();
    let d=now.getDate()-dob.getDate();
    if(d<0){ m--; const prevMonth=new Date(now.getFullYear(), now.getMonth(), 0).getDate(); d += prevMonth; }
    if(m<0){ y--; m += 12; }
    const daysLived=Math.floor((now-dob)/86400000);
    document.getElementById('ageOut').textContent=`${y} years, ${m} months, ${d} days (≈ ${fmt(daysLived)} days)`;
  }

  // ---------- Fuel ----------
  function calcFuel(){
    const D=+document.getElementById('fuelD').value; const M=+document.getElementById('fuelM').value; const P=+document.getElementById('fuelP').value;
    if(!D||!M||!P){document.getElementById('fuelOut').textContent='Please enter all values';return}
    const liters=D/M; const cost=liters*P;
    document.getElementById('fuelOut').textContent=`Fuel needed: ${fmt(liters)} L | Cost: ₹${fmt(cost)}`;
  }

  // ---------- Screen Time ----------
  function calcScreen(){
    const h=+document.getElementById('scrH').value; const d=+document.getElementById('scrD').value;
    const totalH=h*d; const mins=totalH*60; const secs=mins*60;
    document.getElementById('scrOut').textContent=`Total: ${fmt(totalH)} hours = ${fmt(mins)} minutes = ${fmt(secs)} seconds`;
  }

  // ---------- Currency (demo static rates) ----------
  const RATES={ INR:1, USD:83, EUR:90 }; // 1 unit in INR (approx demo)
  function convertCurrency(){
    const v=+document.getElementById('curVal').value; const a=document.getElementById('curFrom').value; const b=document.getElementById('curTo').value;
    if(!v){document.getElementById('curOut').textContent='Enter an amount';return}
    const inINR=v*RATES[a]; const out=inINR/RATES[b];
    document.getElementById('curOut').textContent=`${fmt(v)} ${a} ≈ ${fmt(out)} ${b}`;
  }

  // Header actions
  document.getElementById('clearAll').onclick=()=>{document.querySelectorAll('input').forEach(i=>i.value='');document.querySelectorAll('.result').forEach(r=>r.textContent='--');document.getElementById('basicOut').textContent='Result: --';};
  document.getElementById('copyLink').onclick=()=>{navigator.clipboard.writeText(location.href).then(()=>{alert('Link copied!')});};
</script></body>
</html>
