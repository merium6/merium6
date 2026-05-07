<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Maryam Ali – Software Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *{margin:0;padding:0;box-sizing:border-box;}
  body{font-family:'DM Sans',sans-serif;background:#030a1a;color:#c9d8f0;padding:0 0 60px;}

  /* HERO */
  .hero{position:relative;text-align:center;padding:60px 24px 48px;background:linear-gradient(180deg,#000d2e 0%,#030a1a 100%);border-bottom:1px solid rgba(0,140,255,0.15);overflow:hidden;}
  .hero::before{content:'';position:absolute;top:-80px;left:50%;transform:translateX(-50%);width:600px;height:400px;background:radial-gradient(ellipse,rgba(0,100,255,0.12) 0%,transparent 70%);pointer-events:none;}
  .grid-bg{position:absolute;inset:0;opacity:0.05;background-image:linear-gradient(rgba(0,140,255,0.8) 1px,transparent 1px),linear-gradient(90deg,rgba(0,140,255,0.8) 1px,transparent 1px);background-size:40px 40px;}
  .avatar{display:inline-flex;align-items:center;justify-content:center;width:90px;height:90px;border-radius:50%;background:linear-gradient(135deg,#0050cc,#00bfff);margin-bottom:20px;box-shadow:0 0 0 4px rgba(0,140,255,0.15),0 0 30px rgba(0,140,255,0.25);font-family:'Space Mono',monospace;font-size:28px;font-weight:700;color:#fff;position:relative;z-index:1;}
  .hero-name{font-family:'Space Mono',monospace;font-size:38px;font-weight:700;color:#fff;letter-spacing:-1px;position:relative;z-index:1;margin-bottom:8px;}
  .hero-name span{color:#00bfff;}
  .hero-title{font-size:13px;font-weight:400;letter-spacing:3px;color:#5b8fc9;text-transform:uppercase;position:relative;z-index:1;margin-bottom:6px;}
  .hero-meta{font-size:13px;color:#3a6090;position:relative;z-index:1;margin-bottom:26px;}
  .badges{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;position:relative;z-index:1;}
  .badge{display:inline-flex;align-items:center;gap:6px;padding:7px 16px;border-radius:24px;font-size:12px;font-weight:500;background:rgba(0,100,255,0.1);border:1px solid rgba(0,140,255,0.25);color:#7dc4f5;text-decoration:none;transition:background 0.2s;}
  .badge:hover{background:rgba(0,140,255,0.2);}
  .badge-dot{width:6px;height:6px;border-radius:50%;background:#00bfff;}

  /* SECTIONS */
  .section{max-width:820px;margin:0 auto;padding:40px 24px 0;}
  .section-label{font-family:'Space Mono',monospace;font-size:11px;letter-spacing:3px;color:#0077cc;text-transform:uppercase;margin-bottom:6px;}
  .section-title{font-size:22px;font-weight:600;color:#e0eeff;margin-bottom:24px;padding-bottom:12px;border-bottom:1px solid rgba(0,100,255,0.15);}
  .divider{height:1px;background:rgba(0,80,200,0.1);margin:40px auto 0;max-width:820px;}

  /* ABOUT */
  .about-text{font-size:15px;line-height:1.85;color:#8aadd4;}
  .about-text strong{color:#c9d8f0;font-weight:600;}

  /* SKILLS */
  .sk-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:16px;}
  .sk-card{background:rgba(0,15,50,0.6);border:1px solid rgba(0,80,180,0.2);border-radius:10px;padding:16px;transition:border-color 0.2s;}
  .sk-card:hover{border-color:rgba(0,150,255,0.3);}
  .sk-cat{font-family:'Space Mono',monospace;font-size:10px;letter-spacing:2px;color:#0088dd;text-transform:uppercase;margin-bottom:10px;}
  .sk-tags{display:flex;flex-wrap:wrap;gap:6px;}
  .sk-tag{font-size:11px;font-weight:500;padding:4px 9px;border-radius:5px;background:rgba(0,50,120,0.5);border:1px solid rgba(0,100,200,0.25);color:#6aa8e0;}

  /* PROJECTS */
  .proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(340px,1fr));gap:16px;}
  .proj-card{background:rgba(0,15,45,0.7);border:1px solid rgba(0,80,180,0.2);border-radius:12px;padding:20px;transition:border-color 0.2s,transform 0.2s;}
  .proj-card:hover{border-color:rgba(0,150,255,0.35);transform:translateY(-2px);}
  .proj-icon{width:36px;height:36px;border-radius:8px;background:rgba(0,100,200,0.15);border:1px solid rgba(0,100,200,0.3);display:flex;align-items:center;justify-content:center;font-size:20px;margin-bottom:14px;}
  .proj-title{font-size:15px;font-weight:600;color:#d0e4ff;margin-bottom:6px;}
  .proj-desc{font-size:13px;color:#6a8fb8;line-height:1.6;margin-bottom:14px;}
  .proj-tags{display:flex;flex-wrap:wrap;gap:6px;}
  .proj-tag{font-family:'Space Mono',monospace;font-size:10px;padding:3px 8px;border-radius:4px;background:rgba(0,60,140,0.4);border:1px solid rgba(0,100,200,0.25);color:#4a8ec4;}

  /* EDUCATION */
  .edu-card{background:rgba(0,15,50,0.6);border:1px solid rgba(0,80,180,0.2);border-radius:12px;padding:20px 24px;display:flex;align-items:center;gap:20px;}
  .edu-icon{width:48px;height:48px;border-radius:10px;background:rgba(0,100,200,0.15);border:1px solid rgba(0,100,200,0.3);display:flex;align-items:center;justify-content:center;font-size:24px;flex-shrink:0;}
  .edu-degree{font-size:15px;font-weight:600;color:#d0e4ff;}
  .edu-uni{font-family:'Space Mono',monospace;font-size:12px;color:#00bfff;margin:2px 0;}
  .edu-date{font-size:12px;color:#3a6090;}

  /* FOOTER */
  .footer{margin-top:56px;text-align:center;padding:28px;border-top:1px solid rgba(0,80,180,0.15);font-family:'Space Mono',monospace;font-size:12px;color:#2a4870;letter-spacing:1px;}
  .footer span{color:#0077cc;}
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="grid-bg"></div>
  <div class="avatar">MA</div>
  <h1 class="hero-name">Maryam <span>Ali</span></h1>
  <p class="hero-title">Software Engineer &nbsp;·&nbsp; .NET &amp; Full Stack Developer</p>
  <p class="hero-meta">📍 Lahore, Pakistan &nbsp;·&nbsp; marium.ali1623@gmail.com &nbsp;·&nbsp; 03008816146</p>
  <div class="badges">
    <a href="mailto:marium.ali1623@gmail.com" class="badge"><span class="badge-dot"></span>Email</a>
    <a href="https://www.linkedin.com/in/maryamali-softwarengineer/" class="badge"><span class="badge-dot"></span>LinkedIn</a>
    <a href="https://github.com/merium6" class="badge"><span class="badge-dot"></span>GitHub</a>
  </div>
</div>

<!-- ABOUT -->
<div class="section">
  <p class="section-label">// about</p>
  <h2 class="section-title">Professional Summary</h2>
  <p class="about-text">
    Full Stack Developer with experience building <strong>scalable web applications</strong>, <strong>secure RESTful APIs</strong>, and <strong>AI-powered solutions</strong> using MERN Stack, ASP.NET Core, C#, React.js, Next.js, and Node.js. Skilled in <strong>Microservices, Entity Framework Core, JWT Authentication, RabbitMQ</strong>, and AI integrations including <strong>OpenAI APIs, chatbots, TTS, and automation workflows</strong>. Strong focus on clean architecture, performance, and scalable system design.
  </p>
</div>

<div class="divider"></div>

<!-- SKILLS -->
<div class="section">
  <p class="section-label">// stack</p>
  <h2 class="section-title">Technical Skills</h2>
  <div class="sk-grid">

    <div class="sk-card">
      <div class="sk-cat">⚙ Backend</div>
      <div class="sk-tags">
        <span class="sk-tag">ASP.NET Core</span>
        <span class="sk-tag">ASP.NET MVC</span>
        <span class="sk-tag">C#</span>
        <span class="sk-tag">Web API</span>
        <span class="sk-tag">REST APIs</span>
        <span class="sk-tag">EF Core</span>
        <span class="sk-tag">LINQ</span>
        <span class="sk-tag">Razor Pages</span>
        <span class="sk-tag">Node.js</span>
        <span class="sk-tag">Dapper</span>
      </div>
    </div>

    <div class="sk-card">
      <div class="sk-cat">🖥 Frontend</div>
      <div class="sk-tags">
        <span class="sk-tag">React.js</span>
        <span class="sk-tag">Next.js</span>
        <span class="sk-tag">JavaScript</span>
        <span class="sk-tag">TypeScript</span>
        <span class="sk-tag">jQuery</span>
        <span class="sk-tag">AJAX</span>
        <span class="sk-tag">HTML5</span>
        <span class="sk-tag">CSS3</span>
        <span class="sk-tag">Razor UI</span>
      </div>
    </div>

    <div class="sk-card">
      <div class="sk-cat">🗄 Databases</div>
      <div class="sk-tags">
        <span class="sk-tag">SQL Server</span>
        <span class="sk-tag">PostgreSQL</span>
        <span class="sk-tag">MySQL</span>
        <span class="sk-tag">MongoDB</span>
        <span class="sk-tag">Firebase</span>
      </div>
    </div>

    <div class="sk-card">
      <div class="sk-cat">🤖 AI &amp; Automation</div>
      <div class="sk-tags">
        <span class="sk-tag">OpenAI API</span>
        <span class="sk-tag">AI Chatbots</span>
        <span class="sk-tag">TTS</span>
        <span class="sk-tag">STT</span>
        <span class="sk-tag">AI Automation</span>
      </div>
    </div>

    <div class="sk-card">
      <div class="sk-cat">📨 Messaging</div>
      <div class="sk-tags">
        <span class="sk-tag">RabbitMQ</span>
        <span class="sk-tag">MassTransit</span>
        <span class="sk-tag">Hangfire</span>
        <span class="sk-tag">Worker Services</span>
        <span class="sk-tag">Event-Driven</span>
      </div>
    </div>

    <div class="sk-card">
      <div class="sk-cat">🔐 Auth &amp; Security</div>
      <div class="sk-tags">
        <span class="sk-tag">JWT</span>
        <span class="sk-tag">OAuth</span>
        <span class="sk-tag">ASP.NET Identity</span>
        <span class="sk-tag">RBAC</span>
        <span class="sk-tag">Keycloak</span>
      </div>
    </div>

    <div class="sk-card">
      <div class="sk-cat">🏗 Architecture</div>
      <div class="sk-tags">
        <span class="sk-tag">Clean Architecture</span>
        <span class="sk-tag">Microservices</span>
        <span class="sk-tag">Repository Pattern</span>
        <span class="sk-tag">MVC</span>
        <span class="sk-tag">Multi-Tenant</span>
        <span class="sk-tag">Layered Architecture</span>
      </div>
    </div>

    <div class="sk-card">
      <div class="sk-cat">🛠 Tools &amp; Platforms</div>
      <div class="sk-tags">
        <span class="sk-tag">Git</span>
        <span class="sk-tag">GitHub</span>
        <span class="sk-tag">GitLab</span>
        <span class="sk-tag">Azure DevOps</span>
        <span class="sk-tag">Docker</span>
        <span class="sk-tag">Postman</span>
        <span class="sk-tag">Swagger</span>
        <span class="sk-tag">VS Code</span>
        <span class="sk-tag">Visual Studio</span>
      </div>
    </div>

  </div>
</div>

<div class="divider"></div>

<!-- PROJECTS -->
<div class="section">
  <p class="section-label">// projects</p>
  <h2 class="section-title">Featured Projects</h2>
  <div class="proj-grid">

    <div class="proj-card">
      <div class="proj-icon">🔌</div>
      <div class="proj-title">Microsoft Dynamics 365 CRM Integration</div>
      <div class="proj-desc">Secure RESTful APIs for enterprise CRM integration with JWT authentication, RBAC, and full Swagger/OpenAPI documentation.</div>
      <div class="proj-tags">
        <span class="proj-tag">ASP.NET Core</span>
        <span class="proj-tag">C#</span>
        <span class="proj-tag">SQL Server</span>
        <span class="proj-tag">JWT</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-icon">🏥</div>
      <div class="proj-title">Healthcare Workflow System</div>
      <div class="proj-desc">Multi-tenant enterprise healthcare platform with async messaging via RabbitMQ/MassTransit and dynamic data import/export modules.</div>
      <div class="proj-tags">
        <span class="proj-tag">ASP.NET Core</span>
        <span class="proj-tag">RabbitMQ</span>
        <span class="proj-tag">PostgreSQL</span>
        <span class="proj-tag">EF Core</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-icon">🏢</div>
      <div class="proj-title">Property Management &amp; Booking System</div>
      <div class="proj-desc">Full-stack property management platform with booking APIs, Hangfire background jobs, and highly optimized database queries.</div>
      <div class="proj-tags">
        <span class="proj-tag">ASP.NET Core</span>
        <span class="proj-tag">Razor</span>
        <span class="proj-tag">Hangfire</span>
        <span class="proj-tag">SQL Server</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-icon">🤖</div>
      <div class="proj-title">AI-Powered Automation</div>
      <div class="proj-desc">OpenAI API integrations including chatbots, Text-to-Speech, Speech-to-Text, and intelligent automation workflows.</div>
      <div class="proj-tags">
        <span class="proj-tag">OpenAI API</span>
        <span class="proj-tag">C#</span>
        <span class="proj-tag">Node.js</span>
        <span class="proj-tag">React.js</span>
      </div>
    </div>

  </div>
</div>

<div class="divider"></div>

<!-- EDUCATION -->
<div class="section">
  <p class="section-label">// education</p>
  <h2 class="section-title">Education</h2>
  <div class="edu-card">
    <div class="edu-icon">🎓</div>
    <div>
      <div class="edu-degree">BS Software Engineering</div>
      <div class="edu-uni">University of the Punjab</div>
      <div class="edu-date">Oct 2020 – Jul 2024 &nbsp;·&nbsp; Lahore, Pakistan</div>
    </div>
  </div>
</div>

<!-- FOOTER -->
<div class="footer">
  <span>// let's build the future of code</span>&nbsp;&nbsp;·&nbsp;&nbsp;marium.ali1623@gmail.com
</div>

</body>
</html>
