
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{--teal:#009688;--teal2:#00BFA5;--navy:#0A1628;--card:#0F1E2E;--gold:#F5A623;--muted:#7A9BB0;--white:#E8F4F0}
body{font-family:'Space Grotesk',sans-serif;background:var(--navy);color:var(--white);min-height:100vh;overflow-x:hidden}
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&family=JetBrains+Mono:wght@400;500&display=swap');
.wrap{max-width:680px;margin:0 auto;padding:1.5rem 1rem}

/* HEADER */
.hero{text-align:center;padding:2rem 0 1.5rem;border-bottom:1px solid #1A3048}
.avatar{width:80px;height:80px;border-radius:50%;background:linear-gradient(135deg,var(--teal),#00897B);display:flex;align-items:center;justify-content:center;margin:0 auto 1rem;font-size:2rem;font-weight:700;color:#fff;position:relative}
.online-dot{position:absolute;bottom:4px;right:4px;width:12px;height:12px;background:#34D399;border-radius:50%;border:2px solid var(--navy);animation:pulse 2s ease-in-out infinite}
@keyframes pulse{0%,100%{transform:scale(1);opacity:1}50%{transform:scale(1.4);opacity:.6}}
.hero-name{font-size:1.6rem;font-weight:700;letter-spacing:-.03em;color:#fff;margin-bottom:.25rem}
.hero-name span{color:var(--teal)}
.hero-sub{font-size:.85rem;color:var(--muted);margin-bottom:1rem;font-family:'JetBrains Mono',monospace}
.badge-row{display:flex;flex-wrap:wrap;gap:.4rem;justify-content:center;margin-bottom:1rem}
.badge{display:inline-flex;align-items:center;gap:.35rem;font-size:.72rem;font-weight:500;padding:.28rem .65rem;border-radius:100px;border:1px solid;font-family:'JetBrains Mono',monospace;letter-spacing:.01em}
.b-teal{background:rgba(0,150,136,.12);border-color:rgba(0,150,136,.35);color:var(--teal2)}
.b-gold{background:rgba(245,166,35,.1);border-color:rgba(245,166,35,.3);color:#F5C842}
.b-muted{background:rgba(255,255,255,.05);border-color:#1A3048;color:var(--muted)}

/* STATS TICKER */
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:.6rem;margin:1.2rem 0}
.stat{background:var(--card);border:1px solid #1A3048;border-radius:10px;padding:.9rem;text-align:center;transition:border-color .25s}
.stat:hover{border-color:rgba(0,150,136,.4)}
.stat-n{font-size:1.7rem;font-weight:700;color:#fff;line-height:1;font-family:'Space Grotesk',sans-serif}
.stat-n span{color:var(--teal)}
.stat-l{font-size:.7rem;color:var(--muted);margin-top:.25rem;letter-spacing:.04em}

/* TERMINAL */
.term{background:#050D16;border:1px solid #1A3048;border-radius:10px;overflow:hidden;margin:1rem 0}
.term-bar{display:flex;align-items:center;gap:.4rem;padding:.55rem .85rem;background:#080F18;border-bottom:1px solid #1A3048}
.dot{width:10px;height:10px;border-radius:50%}
.d-r{background:#FF5F57}.d-a{background:#FFBD2E}.d-g{background:#28C840}
.term-ttl{font-size:.68rem;color:var(--muted);margin-left:.3rem;font-family:'JetBrains Mono',monospace;letter-spacing:.04em}
.term-body{padding:1rem 1.1rem;font-family:'JetBrains Mono',monospace;font-size:.78rem;line-height:1.9;min-height:180px}
.p{color:var(--teal)}.o{color:var(--muted)}.s{color:#34D399}.w{color:var(--gold)}.k{color:#C084FC}
.cur{display:inline-block;width:2px;height:.9em;background:var(--teal);vertical-align:text-bottom;animation:blink 1s steps(1) infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}

/* PROJECTS */
.sec-title{font-size:.72rem;color:var(--teal);font-family:'JetBrains Mono',monospace;letter-spacing:.08em;margin:1.4rem 0 .7rem;display:flex;align-items:center;gap:.5rem}
.sec-title::after{content:'';flex:1;height:1px;background:#1A3048}
.projects{display:grid;grid-template-columns:1fr 1fr;gap:.6rem}
.pcard{background:var(--card);border:1px solid #1A3048;border-radius:9px;padding:.9rem;cursor:pointer;transition:border-color .2s,transform .15s;position:relative;overflow:hidden}
.pcard::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--teal),transparent);opacity:0;transition:opacity .3s}
.pcard:hover{border-color:rgba(0,150,136,.45);transform:translateY(-2px)}
.pcard:hover::before{opacity:1}
.p-rank{font-family:'JetBrains Mono',monospace;font-size:.65rem;color:var(--gold);background:rgba(245,166,35,.1);border:1px solid rgba(245,166,35,.2);padding:.15rem .45rem;border-radius:4px;display:inline-block;margin-bottom:.5rem}
.p-name{font-size:.95rem;font-weight:700;color:#fff;letter-spacing:-.01em;margin-bottom:.15rem}
.p-ar{font-size:.78rem;color:var(--muted);direction:rtl;margin-bottom:.5rem;font-family:serif}
.p-desc{font-size:.75rem;color:var(--muted);line-height:1.6}

/* STACK */
.stack{display:grid;grid-template-columns:repeat(4,1fr);gap:.45rem;margin:.6rem 0}
.stk{background:var(--card);border:1px solid #1A3048;border-radius:7px;padding:.55rem .5rem;text-align:center;font-size:.7rem;color:var(--muted);transition:all .2s;cursor:default}
.stk:hover{border-color:rgba(0,150,136,.4);color:var(--white)}
.stk i{display:block;font-size:1.1rem;margin-bottom:.25rem;color:var(--teal)}

/* TIMELINE */
.tl{list-style:none;padding:0;margin:.6rem 0}
.tl-item{display:grid;grid-template-columns:20px 1fr;gap:.7rem;padding-bottom:1.1rem;position:relative}
.tl-item:not(:last-child) .td::after{content:'';position:absolute;left:9px;top:22px;width:1px;bottom:0;background:#1A3048}
.td{width:20px;height:20px;border-radius:50%;background:rgba(0,150,136,.15);border:1.5px solid var(--teal);display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:2px;position:relative}
.td-i{width:7px;height:7px;border-radius:50%;background:var(--teal)}
.tl-yr{font-family:'JetBrains Mono',monospace;font-size:.65rem;color:var(--teal);margin-bottom:.1rem}
.tl-t{font-size:.82rem;font-weight:500;color:#fff}
.tl-s{font-size:.72rem;color:var(--muted)}

/* CONTACT */
.contact{background:var(--card);border:1px solid #1A3048;border-radius:10px;padding:1.1rem;margin:1rem 0;display:flex;flex-direction:column;gap:.55rem}
.c-link{display:flex;align-items:center;gap:.6rem;font-size:.82rem;color:var(--muted);text-decoration:none;padding:.45rem .6rem;border-radius:7px;transition:background .2s,color .2s}
.c-link:hover{background:rgba(0,150,136,.08);color:var(--teal)}
.c-link i{font-size:1rem;color:var(--teal);width:18px;text-align:center}

/* AWARD */
.award{background:linear-gradient(120deg,#0A1F0A,#08180E);border:1px solid rgba(52,211,153,.3);border-radius:10px;padding:1rem;margin:.6rem 0;display:flex;gap:.8rem;align-items:flex-start}
.award-icon{width:36px;height:36px;border-radius:8px;background:rgba(52,211,153,.12);border:1px solid rgba(52,211,153,.25);display:flex;align-items:center;justify-content:center;flex-shrink:0}
.award-icon i{color:#34D399;font-size:1.1rem}
.award-yr{font-family:'JetBrains Mono',monospace;font-size:.65rem;color:#34D399;margin-bottom:.2rem}
.award-t{font-size:.88rem;font-weight:700;color:#fff;margin-bottom:.15rem}
.award-d{font-size:.74rem;color:var(--muted);line-height:1.5}

/* FOOTER */
.footer{text-align:center;padding:1.2rem 0 .5rem;border-top:1px solid #1A3048;margin-top:1rem}
.footer-q{font-family:'JetBrains Mono',monospace;font-size:.75rem;color:var(--teal);margin-bottom:.3rem}
.footer-s{font-size:.7rem;color:var(--muted)}
</style>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/dist/tabler-icons.min.css"/>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet"/>

<div class="wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="avatar">HBS<div class="online-dot"></div></div>
    <div class="hero-name">Hamza <span>Boubakar</span> Seddik</div>
    <div class="hero-sub">Software Engineer · MFEP Algeria · Algiers 🇩🇿</div>
    <div class="badge-row">
      <span class="badge b-gold"><i class="ti ti-trophy" aria-hidden="true"></i>Hackathon #1 · 2026</span>
      <span class="badge b-teal"><i class="ti ti-code" aria-hidden="true"></i>7+ Years Engineering</span>
      <span class="badge b-muted"><i class="ti ti-building-arch" aria-hidden="true"></i>ERP · Microservices · PWA</span>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats">
    <div class="stat">
      <div class="stat-n" id="s1">0<span>+</span></div>
      <div class="stat-l">Years of engineering</div>
    </div>
    <div class="stat">
      <div class="stat-n" id="s2">0</div>
      <div class="stat-l">Major systems</div>
    </div>
    <div class="stat">
      <div class="stat-n"><span id="s3">0</span><span>#</span></div>
      <div class="stat-l">Hackathon rank 2026</div>
    </div>
  </div>

  <!-- TERMINAL -->
  <div class="term">
    <div class="term-bar">
      <div class="dot d-r"></div><div class="dot d-a"></div><div class="dot d-g"></div>
      <div class="term-ttl">hamza@mfep-Algeria ~ portfolio</div>
    </div>
    <div class="term-body" id="tb"></div>
  </div>

  <!-- PROJECTS -->
  <div class="sec-title"><i class="ti ti-folder-code" aria-hidden="true"></i> featured projects</div>
  <div class="projects">
    <div class="pcard">
      <div class="p-rank"><i class="ti ti-trophy" aria-hidden="true"></i> Hackathon Winner</div>
      <div class="p-name">WSAP</div>
      <div class="p-ar">منصة وورلد سكيلز الجزائر</div>
      <div class="p-desc">National vocational competition platform. Automated scoring & digital certificates.</div>
    </div>
    <div class="pcard">
      <div class="p-rank"><i class="ti ti-building-community" aria-hidden="true"></i> National ERP</div>
      <div class="p-name">Tassyir</div>
      <div class="p-ar">نظام ERP المؤسسي</div>
      <div class="p-desc">Unified ERP spanning all training centers across Algeria at scale.</div>
    </div>
    <div class="pcard">
      <div class="p-rank"><i class="ti ti-chart-bar" aria-hidden="true"></i> Government</div>
      <div class="p-name">SGFEP</div>
      <div class="p-ar">المنصة الوطنية للإحصائيات</div>
      <div class="p-desc">Strategic analytics dashboard for MFEP executive decision-making.</div>
    </div>
    <div class="pcard">
      <div class="p-rank"><i class="ti ti-brain" aria-hidden="true"></i> AI-Powered</div>
      <div class="p-name">Tawjih</div>
      <div class="p-ar">محرك التوجيه الذكي</div>
      <div class="p-desc">AI guidance engine — psychometric profiling & career recommendations.</div>
    </div>
  </div>

  <!-- STACK -->
  <div class="sec-title"><i class="ti ti-stack-2" aria-hidden="true"></i> technology stack</div>
  <div class="stack">
    <div class="stk"><i class="ti ti-brand-php" aria-hidden="true"></i>PHP 8</div>
    <div class="stk"><i class="ti ti-brand-laravel" aria-hidden="true"></i>Laravel</div>
    <div class="stk"><i class="ti ti-brand-csharp" aria-hidden="true"></i>C# .NET</div>
    <div class="stk"><i class="ti ti-coffee" aria-hidden="true"></i>Java EE</div>
    <div class="stk"><i class="ti ti-brand-javascript" aria-hidden="true"></i>JavaScript</div>
    <div class="stk"><i class="ti ti-database" aria-hidden="true"></i>MySQL</div>
    <div class="stk"><i class="ti ti-brand-redis" aria-hidden="true"></i>Redis</div>
    <div class="stk"><i class="ti ti-brand-nginx" aria-hidden="true"></i>Nginx</div>
    <div class="stk"><i class="ti ti-brand-google-cloud" aria-hidden="true"></i>G. Cloud</div>
    <div class="stk"><i class="ti ti-device-mobile" aria-hidden="true"></i>PWA</div>
    <div class="stk"><i class="ti ti-brand-linux" aria-hidden="true"></i>Linux</div>
    <div class="stk"><i class="ti ti-api" aria-hidden="true"></i>REST API</div>
  </div>

  <!-- AWARD -->
  <div class="award">
    <div class="award-icon"><i class="ti ti-trophy" aria-hidden="true"></i></div>
    <div>
      <div class="award-yr"><i class="ti ti-calendar" aria-hidden="true"></i> National Recognition · 2026</div>
      <div class="award-t">1st Place — National Digital Transformation Hackathon</div>
      <div class="award-d">Awarded for WSAP — recognized by MFEP for excellence in digital innovation and public-sector engineering at national level.</div>
    </div>
  </div>

  <!-- TIMELINE -->
  <div class="sec-title"><i class="ti ti-timeline" aria-hidden="true"></i> engineering timeline</div>
  <ul class="tl">
    <li class="tl-item"><div class="td"><div class="td-i"></div></div><div><div class="tl-yr">2026</div><div class="tl-t">1st Place · National Hackathon</div><div class="tl-s">WSAP — WorldSkills Algeria Platform</div></div></li>
    <li class="tl-item"><div class="td"><div class="td-i"></div></div><div><div class="tl-yr">2024 – 2026</div><div class="tl-t">Lead Engineer · AI & Analytics</div><div class="tl-s">Tawjih AI Engine · SGFEP Government Platform</div></div></li>
    <li class="tl-item"><div class="td"><div class="td-i"></div></div><div><div class="tl-yr">2021 – 2024</div><div class="tl-t">Senior Engineer · ERP Systems</div><div class="tl-s">Tassyir National ERP · MFEP Algeria</div></div></li>
    <li class="tl-item"><div class="td"><div class="td-i"></div></div><div><div class="tl-yr">2018 – 2021</div><div class="tl-t">Software Engineer · MFEP</div><div class="tl-s">Enterprise systems, REST APIs, server infrastructure</div></div></li>
    <li class="tl-item"><div class="td"><div class="td-i"></div></div><div><div class="tl-yr">2017</div><div class="tl-t">Started software engineering career</div><div class="tl-s">Algiers, Algeria</div></div></li>
  </ul>

  <!-- CONTACT -->
  <div class="sec-title"><i class="ti ti-send" aria-hidden="true"></i> get in touch</div>
  <div class="contact">
    <a class="c-link" href="mailto:boubakarseddikh@gmail.com"><i class="ti ti-mail" aria-hidden="true"></i>boubakarseddikh@gmail.com</a>
    <a class="c-link" href="https://www.linkedin.com/in/hamza-boubakare-seddike" target="_blank"><i class="ti ti-brand-linkedin" aria-hidden="true"></i>linkedin.com/in/hamza-boubakare-seddike</a>
    <a class="c-link" href="https://github.com/Hamza2024-CODE" target="_blank"><i class="ti ti-brand-github" aria-hidden="true"></i>github.com/Hamza2024-CODE</a>
    <a class="c-link" href="https://hamza-boubakare-seddike.gt.tc/?i=1" target="_blank"><i class="ti ti-world" aria-hidden="true"></i>hamza-boubakare-seddike.gt.tc</a>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-q">" Build systems that outlast the sprint. "</div>
    <div class="footer-s"><i class="ti ti-map-pin" aria-hidden="true"></i> Algiers, Algeria · MFEP · 2026</div>
  </div>

</div>

<script>
// Counter animation
function countUp(id, target, suffix) {
  let v = 0;
  const el = document.getElementById(id);
  const step = Math.ceil(target / 30);
  const t = setInterval(() => {
    v = Math.min(v + step, target);
    el.innerHTML = v + (suffix || '');
    if (v >= target) clearInterval(t);
  }, 50);
}
setTimeout(() => {
  countUp('s1', 7, '<span>+</span>');
  countUp('s2', 4, '');
  countUp('s3', 1, '');
}, 400);

// Terminal
const lines = [
  {t:'p',c:'whoami'},
  {t:'o',x:'hamza.boubakar.seddik · MFEP Algeria'},
  {t:'p',c:'cat awards.json'},
  {t:'k',x:'{ "rank": 1, "event": "National Hackathon 2026" }'},
  {t:'p',c:'ls projects/'},
  {t:'s',x:'wsap/    tassyir/    sgfep/    tawjih/'},
  {t:'p',c:'./deploy.sh --env production'},
  {t:'w',x:'▸ Building 4 microservices...'},
  {t:'s',x:'✓ All services deployed successfully'},
  {t:'p',c:''},
];
const tb = document.getElementById('tb');
let li = 0, phase = 'cmd';
function tick() {
  if (li >= lines.length) { tb.innerHTML += '<span class="cur"></span>'; return; }
  const ln = lines[li];
  if (ln.t === 'p') {
    if (phase === 'cmd') {
      const d = document.createElement('div');
      d.innerHTML = `<span class="p">hamza@mfep:~$ </span><span id="ac"></span>`;
      tb.appendChild(d);
      const sp = d.querySelector('#ac');
      const cmd = ln.c; let ci = 0;
      const iv = setInterval(() => {
        if (ci <= cmd.length) { sp.textContent = cmd.slice(0, ci++); }
        else { clearInterval(iv); phase='out'; li++; setTimeout(tick, 400); }
      }, 55);
    }
  } else {
    const cls = {o:'o',s:'s',w:'w',k:'k'}[ln.t]||'o';
    const d = document.createElement('div');
    d.innerHTML = `<span class="${cls}">${ln.x}</span>`;
    tb.appendChild(d);
    li++; setTimeout(tick, 160);
  }
  tb.scrollTop = 9999;
}
setTimeout(tick, 700);
</script>
