<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Nitish Belagali — Portfolio</title>
  <meta name="description" content="Portfolio of Nitish Belagali — Data Analytics • AI Agents • Data Engineering" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <script>
    (() => {
      const saved = localStorage.getItem('theme');
      const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
      const on = (saved === 'dark') || (!saved && prefersDark);
      if (on) { document.documentElement.classList.add('dark'); document.body?.classList?.add('dark'); }
    })();
    window.tailwind = window.tailwind || {};
    tailwind.config = { darkMode: 'class' };
  </script>
  <script src="https://cdn.tailwindcss.com"></script>

  <style>
    :root{--brand:#3B82F6;--accent:#F59E0B}
    html{scroll-behavior:smooth}
    body{font-family:Inter,system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif}
    .container{max-width:1100px}
    .glass{backdrop-filter:saturate(180%) blur(10px); background-color:rgba(255,255,255,.7)}
    .dark .glass{background-color:rgba(17,24,39,.6)}
    .chip{display:inline-flex;align-items:center;gap:.5rem;border-radius:999px;padding:.35rem .7rem;border:1px solid rgba(148,163,184,.35)}
    dialog::backdrop{background:rgba(0,0,0,.55)}
    
    /* Animations */
    .card{transition:transform .35s cubic-bezier(.2,.8,.2,1), box-shadow .35s, background .35s}
    .card:hover{transform:translateY(-6px); box-shadow:0 20px 40px -20px rgba(0,0,0,.35)}
    .btn:hover{filter:brightness(110%)}
    .link-underline{background-image:linear-gradient(currentColor,currentColor);background-size:0% 2px;background-repeat:no-repeat;background-position:0 100%;transition:background-size .35s}
    .link-underline:hover{background-size:100% 2px}
    .orb{position:absolute;border-radius:50%;filter:blur(60px);opacity:.35;pointer-events:none}
    .orb--1{width:420px;height:420px;background:radial-gradient(#60a5fa,transparent 60%);top:-80px;left:-120px}
    .orb--2{width:380px;height:380px;background:radial-gradient(#c084fc,transparent 60%);bottom:-120px;right:-80px}
    .reveal{opacity:0;transform:translateY(14px);transition:opacity .7s ease, transform .7s ease}
    .reveal.is-visible{opacity:1;transform:none}
    @media (prefers-reduced-motion: reduce){.card,.reveal{transition:none}.orb{display:none}}
  </style>
</head>

<body class="relative bg-slate-50 text-slate-800 dark:bg-slate-950 dark:text-slate-100">
  <div class="orb orb--1"></div>
  <div class="orb orb--2"></div>

  <header class="sticky top-0 z-50">
    <nav class="glass border-b border-slate-200 dark:border-slate-800">
      <div class="container mx-auto px-4 py-3 flex items-center justify-between">
        <a href="#home" class="font-extrabold text-lg tracking-tight">Nitish<span class="text-[var(--brand)]">.</span></a>
        <div class="hidden md:flex items-center gap-6 text-sm font-medium">
          <a href="#about" class="hover:text-[var(--brand)] link-underline">About</a>
          <a href="#skills" class="hover:text-[var(--brand)] link-underline">Skills</a>
          <a href="#projects" class="hover:text-[var(--brand)] link-underline">Projects</a>
          <a href="#experience" class="hover:text-[var(--brand)] link-underline">Experience</a>
        </div>
        <div class="flex items-center gap-3">
          <button id="themeToggle" class="btn inline-flex items-center gap-2 rounded-2xl border border-slate-300 dark:border-slate-700 px-3 py-1.5 text-xs font-semibold hover:bg-slate-100 dark:hover:bg-slate-800">🌙/☀️</button>
          <a href="#contact" class="btn hidden sm:inline-flex items-center gap-2 rounded-2xl bg-[var(--brand)] text-white px-3 py-1.5 text-xs font-semibold shadow">Hire me</a>
        </div>
      </div>
    </nav>
  </header>

  <section id="home" class="container mx-auto px-4 pt-10 pb-14 reveal">
    <div class="grid md:grid-cols-[260px_1fr] gap-8 items-center">
      <img src="assets/profile.jpg" alt="Nitish Belagali" class="w-56 h-56 object-cover rounded-3xl shadow-xl ring-4 ring-white dark:ring-slate-900" onerror="this.src='https://github.com/nitishbelagali.png';">
      <div>
        <span class="inline-flex items-center gap-2 text-xs font-bold uppercase tracking-widest text-[var(--brand)]">AI Engineering • Data Analytics • BI</span>
        <h1 class="mt-2 text-3xl md:text-5xl font-extrabold leading-tight bg-clip-text text-transparent bg-gradient-to-r from-[var(--brand)] via-[#a78bfa] to-[#22d3ee]">Hi, I’m Nitish Belagali. <br>I build AI systems that solve data problems.</h1>
        <p class="mt-3 text-slate-500 dark:text-slate-300">Graduate Student @ Northeastern • Ex-IBM, Boehringer Ingelheim, Accenture.</p>
        <div class="mt-6 flex flex-wrap gap-3">
          <a href="#projects" class="btn inline-flex items-center rounded-xl bg-[var(--brand)] text-white px-4 py-2 text-sm font-semibold shadow">View Projects</a>
          <a href="https://github.com/nitishbelagali" target="_blank" class="btn inline-flex items-center rounded-xl border border-slate-300 dark:border-slate-700 px-4 py-2 text-sm font-semibold hover:bg-slate-100 dark:hover:bg-slate-800">GitHub</a>
          <a href="assets/Nitish_Resume.pdf" target="_blank" class="btn inline-flex items-center rounded-xl border border-slate-300 dark:border-slate-700 px-4 py-2 text-sm font-semibold hover:bg-slate-100 dark:hover:bg-slate-800">Resume</a>
        </div>
      </div>
    </div>
  </section>

  <section id="about" class="container mx-auto px-4 py-10 reveal">
    <div class="rounded-3xl bg-white/70 dark:bg-slate-900/60 shadow border border-slate-200 dark:border-slate-800 p-6 md:p-8 card">
      <h2 class="text-2xl font-bold">About Me</h2>
      <p class="mt-3 text-slate-600 dark:text-slate-300">I am a data generalist with <b>3.5 years</b> of experience bridging the gap between raw data and business value. While my background is in BI and Data Engineering, my passion lies in <b>AI Engineering</b>—building agents that don't just chat, but <i>do</i> work.</p>
      <p class="mt-3 text-slate-600 dark:text-slate-300">Currently finishing my MS in Information Systems at Northeastern University. When I'm not coding, I'm playing soccer (Chelsea FC fan), lifting, or exploring national parks.</p>
    </div>
  </section>

  <section id="projects" class="container mx-auto px-4 py-10 reveal">
    <div class="flex items-end justify-between mb-6">
      <h2 class="text-2xl font-bold">Featured Projects</h2>
      <a href="https://github.com/nitishbelagali" class="text-sm font-semibold text-[var(--brand)] underline">See all →</a>
    </div>
    
    <div class="grid gap-6 md:grid-cols-2">

      <article class="p-6 rounded-2xl bg-white/70 dark:bg-slate-900/60 border border-slate-200 dark:border-slate-800 card border-l-4 border-l-[var(--brand)]">
        <div class="flex justify-between items-start">
            <h3 class="text-lg font-bold">🛡️ Causal Sentinel v2.0</h3>
            <span class="chip text-[10px] bg-blue-100 dark:bg-blue-900 text-blue-800 dark:text-blue-100">Enterprise AI</span>
        </div>
        <p class="text-sm text-slate-600 dark:text-slate-300 mt-2">An autonomous observability platform that ingests logs (GitHub/Jira/Slack), detects revenue crashes, and uses <b>Causal Inference</b> to prove financial impact.</p>
        <div class="mt-3 flex flex-wrap gap-2 text-xs text-slate-500">
          <span class="chip">Python</span> <span class="chip">DoWhy</span> <span class="chip">OpenAI</span> <span class="chip">Streamlit</span>
        </div>
        <div class="mt-4 flex gap-4 text-sm font-medium">
          <a href="https://github.com/nitishbelagali/causal-sentinel" target="_blank" class="text-[var(--brand)] hover:underline">View Code</a>
          <button onclick="document.getElementById('causalModal').showModal()" class="text-slate-500 hover:text-slate-800 dark:hover:text-slate-200">Read More</button>
        </div>
      </article>

      <article class="p-6 rounded-2xl bg-white/70 dark:bg-slate-900/60 border border-slate-200 dark:border-slate-800 card border-l-4 border-l-purple-500">
        <div class="flex justify-between items-start">
            <h3 class="text-lg font-bold">🕵️‍♂️ Skeptic Analyst Agent</h3>
            <span class="chip text-[10px] bg-purple-100 dark:bg-purple-900 text-purple-800 dark:text-purple-100">AI Agent</span>
        </div>
        <p class="text-sm text-slate-600 dark:text-slate-300 mt-2">A "Human-in-the-Loop" AI Agent that audits dirty data before analyzing it. Uses <b>Polars</b> for high-speed checks to prevent LLM hallucinations.</p>
        <div class="mt-3 flex flex-wrap gap-2 text-xs text-slate-500">
          <span class="chip">LangChain</span> <span class="chip">DuckDB</span> <span class="chip">Polars</span> <span class="chip">GPT-4o</span>
        </div>
        <div class="mt-4 flex gap-4 text-sm font-medium">
          <a href="https://github.com/nitishbelagali/skeptic-analyst" target="_blank" class="text-[var(--brand)] hover:underline">View Code</a>
          <button onclick="document.getElementById('skepticModal').showModal()" class="text-slate-500 hover:text-slate-800 dark:hover:text-slate-200">Read More</button>
        </div>
      </article>

      <article class="p-6 rounded-2xl bg-white/70 dark:bg-slate-900/60 border border-slate-200 dark:border-slate-800 card">
        <h3 class="text-lg font-bold">Spotify Data Pipeline</h3>
        <p class="text-sm text-slate-600 dark:text-slate-300 mt-2">Cloud-native ETL with Spark & Airflow on AWS. Processing millions of rows for analytics in Redshift.</p>
        <div class="mt-3 flex flex-wrap gap-2 text-xs text-slate-500">
          <span class="chip">AWS EMR</span> <span class="chip">Airflow</span> <span class="chip">Spark</span> <span class="chip">Redshift</span>
        </div>
        <div class="mt-4 flex gap-4 text-sm font-medium">
          <a href="https://github.com/nitishbelagali" target="_blank" class="text-[var(--brand)] hover:underline">View Code</a>
          <button onclick="document.getElementById('spotifyModal').showModal()" class="text-slate-500 hover:text-slate-800 dark:hover:text-slate-200">Read More</button>
        </div>
      </article>

      <article class="p-6 rounded-2xl bg-white/70 dark:bg-slate-900/60 border border-slate-200 dark:border-slate-800 card">
        <h3 class="text-lg font-bold">RAG Chatbot for Policy</h3>
        <p class="text-sm text-slate-600 dark:text-slate-300 mt-2">FastAPI + ChromaDB backend for retrieving and citing internal policy documents.</p>
        <div class="mt-3 flex flex-wrap gap-2 text-xs text-slate-500">
          <span class="chip">FastAPI</span> <span class="chip">ChromaDB</span> <span class="chip">Docker</span>
        </div>
        <div class="mt-4 flex gap-4 text-sm font-medium">
          <a href="https://github.com/nitishbelagali" target="_blank" class="text-[var(--brand)] hover:underline">View Code</a>
        </div>
      </article>

    </div>
  </section>

  <section id="experience" class="container mx-auto px-4 py-10 reveal">
    <h2 class="text-2xl font-bold">Experience</h2>
    <div class="mt-6 space-y-6">
      
      <div class="relative pl-8 border-l-2 border-slate-200 dark:border-slate-800">
        <div class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-[var(--brand)]"></div>
        <h3 class="font-bold text-lg">IT Data Analyst Co-op</h3>
        <div class="text-sm text-[var(--brand)] font-semibold">Boehringer Ingelheim • Jan 2025 – Present</div>
        <p class="text-sm text-slate-600 dark:text-slate-400 mt-2">Automating 50M+ row Oracle exports using Python/Redshift. Modularizing R Shiny apps for 5+ scientific domains.</p>
      </div>

      <div class="relative pl-8 border-l-2 border-slate-200 dark:border-slate-800">
        <div class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-slate-300 dark:bg-slate-700"></div>
        <h3 class="font-bold text-lg">Technical Services Specialist</h3>
        <div class="text-sm text-slate-500 font-semibold">IBM • Aug 2021 – Jun 2023</div>
        <p class="text-sm text-slate-600 dark:text-slate-400 mt-2">Optimized Informatica ETL workflows, reducing processing time by 40%. Delivered real-time BigQuery strategies.</p>
      </div>

      <div class="relative pl-8 border-l-2 border-slate-200 dark:border-slate-800">
        <div class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-slate-300 dark:bg-slate-700"></div>
        <h3 class="font-bold text-lg">Associate Software Engineer</h3>
        <div class="text-sm text-slate-500 font-semibold">Accenture • Feb 2021 – Aug 2021</div>
        <p class="text-sm text-slate-600 dark:text-slate-400 mt-2">Built Tableau dashboards for biomedical clients, driving 30% better decision-making accuracy.</p>
      </div>

    </div>
  </section>

  <section id="skills" class="container mx-auto px-4 py-10 reveal">
    <h2 class="text-2xl font-bold">Technical Arsenal</h2>
    <div class="mt-4 flex flex-wrap gap-2">
      <span class="chip">Python</span>
      <span class="chip">SQL</span>
      <span class="chip">Spark</span>
      <span class="chip">Airflow</span>
      <span class="chip">Kafka</span>
      <span class="chip">LangChain</span>
      <span class="chip">OpenAI API</span>
      <span class="chip">DoWhy</span>
      <span class="chip">Polars</span>
      <span class="chip">DuckDB</span>
      <span class="chip">Tableau</span>
      <span class="chip">Power BI</span>
      <span class="chip">Docker</span>
      <span class="chip">AWS (S3, EMR, Redshift)</span>
      <span class="chip">Azure</span>
    </div>
  </section>

  <footer class="py-10 text-center text-sm text-slate-500">
    <p>Built by Nitish Belagali • 2025</p>
    <div class="mt-2 flex justify-center gap-4">
      <a href="mailto:nitish.belagali@gmail.com" class="hover:text-[var(--brand)]">Email</a>
      <a href="https://github.com/nitishbelagali" class="hover:text-[var(--brand)]">GitHub</a>
      <a href="https://linkedin.com/in/nitishbelagali" class="hover:text-[var(--brand)]">LinkedIn</a>
    </div>
  </footer>

  <dialog id="causalModal" class="p-0 rounded-2xl w-[min(900px,92vw)] backdrop:bg-black/60">
    <div class="p-8 bg-white dark:bg-slate-900 text-slate-800 dark:text-slate-100">
      <div class="flex justify-between items-start">
        <h3 class="text-2xl font-bold">🛡️ Causal Sentinel v2.0</h3>
        <button class="chip" onclick="document.getElementById('causalModal').close()">Close</button>
      </div>
      <div class="mt-4 space-y-4">
        <p><b>The Problem:</b> When revenue crashes, engineers struggle to correlate 1,000s of logs with business metrics. Traditional tools (Datadog/Dynatrace) are expensive ($50k+) and only show correlation, not causation.</p>
        <p><b>The Solution:</b> I built an open-source observability platform that ingests logs from GitHub, Jira, and Slack. It uses GPT-4o to classify risk and <b>Microsoft DoWhy</b> to perform counterfactual analysis.</p>
        <div class="p-4 bg-slate-100 dark:bg-slate-800 rounded-xl">
           <code>Impact = E[Revenue | Bug] - E[Revenue | No Bug]</code>
           <p class="text-sm mt-2">It mathematically proves: "This specific bug caused a $572k loss."</p>
        </div>
        <p><b>Tech Stack:</b> Python, Streamlit, Plotly, OpenAI GPT-4o, DoWhy, PyGithub, Slack SDK.</p>
      </div>
    </div>
  </dialog>

  <dialog id="skepticModal" class="p-0 rounded-2xl w-[min(900px,92vw)] backdrop:bg-black/60">
    <div class="p-8 bg-white dark:bg-slate-900 text-slate-800 dark:text-slate-100">
      <div class="flex justify-between items-start">
        <h3 class="text-2xl font-bold">🕵️‍♂️ Skeptic Analyst Agent</h3>
        <button class="chip" onclick="document.getElementById('skepticModal').close()">Close</button>
      </div>
      <div class="mt-4 space-y-4">
        <p><b>The Problem:</b> AI Agents hallucinate SQL when data is dirty (NULLs, mixed types). They blindly trust the user input.</p>
        <p><b>The Solution:</b> A custom ReAct Agent that assumes data is "guilty until proven innocent." It runs a <b>Polars</b> audit first. If errors are found, it <b>HALTS</b> execution using session state and forces the human to make a decision.</p>
        <ul class="list-disc pl-5 space-y-1">
            <li><b>Anti-Hallucination:</b> Sanitizes context before LLM sees it.</li>
            <li><b>Cost Optimized:</b> Uses CPU (Polars) for scanning, saving GPU tokens for reasoning.</li>
        </ul>
        <p><b>Tech Stack:</b> LangChain, Streamlit, DuckDB, Polars, GPT-4o.</p>
      </div>
    </div>
  </dialog>

  <dialog id="spotifyModal" class="p-0 rounded-2xl w-[min(900px,92vw)] backdrop:bg-black/60">
    <div class="p-8 bg-white dark:bg-slate-900 text-slate-800 dark:text-slate-100">
      <div class="flex justify-between items-start">
        <h3 class="text-2xl font-bold">Spotify Data Pipeline</h3>
        <button class="chip" onclick="document.getElementById('spotifyModal').close()">Close</button>
      </div>
      <div class="mt-4 space-y-4">
        <p>An end-to-end cloud data pipeline. Ingests raw data from APIs to S3, transforms using Spark on EMR, and loads into Redshift for analytics.</p>
        <ul class="list-disc pl-5">
            <li>Orchestrated via Apache Airflow.</li>
            <li>Reduced query latency by 50% via dimensional modeling.</li>
        </ul>
      </div>
    </div>
  </dialog>

  <script>
    // Theme Toggle Logic
    const toggle = document.getElementById('themeToggle');
    toggle.addEventListener('click', () => {
      document.documentElement.classList.toggle('dark');
      document.body.classList.toggle('dark');
      localStorage.setItem('theme', document.documentElement.classList.contains('dark') ? 'dark' : 'light');
    });

    // Reveal Animation
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('is-visible');
        }
      });
    }, { threshold: 0.1 });
    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
  </script>
</body>
</html>
