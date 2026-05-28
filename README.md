[index.html](https://github.com/user-attachments/files/28353319/index.html)[<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mickaël DESTAL – Portfolio BUT1 GMP</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0;}
:root{
  --accent:#1a56db;--accent2:#0f3460;
  --bg:#f4f3ef;--bg2:#eae9e3;
  --text:#1a1a18;--muted:#6b6b65;
  --border:rgba(0,0,0,0.12);--card-bg:#ffffff;
  --tag-bg:#e8edf8;--tag-text:#1a56db;
}
html{scroll-behavior:smooth;}
body{font-family:'DM Sans',sans-serif;background:var(--bg);color:var(--text);font-size:16px;line-height:1.65;min-height:100vh;}

nav{position:sticky;top:0;z-index:100;background:var(--bg);border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;padding:0 2.5rem;height:56px;}
.nav-logo{display:flex;align-items:center;}.nav-logo img{height:24px;width:auto;display:block;}
.nav-links{display:flex;gap:2rem;list-style:none;}
.nav-links a{font-size:13px;font-weight:500;color:var(--muted);text-decoration:none;letter-spacing:.03em;text-transform:uppercase;transition:color .2s;}
.nav-links a:hover{color:var(--accent);}

.hero{display:grid;grid-template-columns:1fr 1fr;min-height:calc(100vh - 56px);overflow:hidden;}
.hero-left{padding:5rem 3rem 5rem 4rem;display:flex;flex-direction:column;justify-content:center;}
.hero-tag{font-family:'DM Mono',monospace;font-size:11px;font-weight:500;color:var(--accent);text-transform:uppercase;letter-spacing:.1em;margin-bottom:1.2rem;display:flex;align-items:center;gap:8px;}
.hero-tag::before{content:'';display:inline-block;width:24px;height:1px;background:var(--accent);}
.hero-name{font-family:'Bebas Neue',sans-serif;font-size:clamp(4rem,8vw,7rem);line-height:.9;letter-spacing:.02em;color:var(--text);margin-bottom:1.5rem;}
.hero-name span{color:var(--accent);display:block;}
.hero-desc{font-size:16px;font-weight:300;color:var(--muted);max-width:400px;margin-bottom:2.5rem;line-height:1.8;}
.hero-ctas{display:flex;gap:1rem;flex-wrap:wrap;}
.btn-primary{background:var(--accent);color:#fff;border:none;padding:.75rem 1.75rem;font-family:'DM Sans',sans-serif;font-size:14px;font-weight:500;cursor:pointer;letter-spacing:.03em;text-transform:uppercase;transition:background .2s,transform .15s;text-decoration:none;display:inline-block;}
.btn-primary:hover{background:var(--accent2);transform:translateY(-1px);}
.btn-outline{background:transparent;color:var(--text);border:1px solid var(--border);padding:.75rem 1.75rem;font-family:'DM Sans',sans-serif;font-size:14px;font-weight:500;cursor:pointer;letter-spacing:.03em;text-transform:uppercase;transition:border-color .2s,color .2s;text-decoration:none;display:inline-block;}
.btn-outline:hover{border-color:var(--accent);color:var(--accent);}
.hero-right{background:var(--accent2);position:relative;display:flex;align-items:center;justify-content:center;overflow:hidden;}
.hero-blueprint{width:100%;height:100%;position:absolute;top:0;left:0;}
.hero-avatar-wrap{position:absolute;z-index:2;top:calc(50% + min(10vw,17vh) + 1.5rem);left:50%;transform:translateX(-50%);display:flex;flex-direction:column;align-items:center;gap:1.5rem;}.hero-info-card{background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.15);padding:1.25rem 2rem;text-align:center;min-width:240px;}
.hero-info-card p{color:rgba(255,255,255,.6);font-size:12px;text-transform:uppercase;letter-spacing:.08em;font-family:'DM Mono',monospace;margin-bottom:4px;}
.hero-info-card strong{color:#fff;font-size:15px;font-weight:400;display:block;}

section{padding:5rem 4rem;max-width:1100px;margin:0 auto;}
.section-header{display:flex;align-items:baseline;gap:1rem;margin-bottom:3rem;}
.section-num{font-family:'DM Mono',monospace;font-size:12px;color:var(--accent);letter-spacing:.1em;}
.section-title{font-family:'Bebas Neue',sans-serif;font-size:2.8rem;letter-spacing:.04em;line-height:1;color:var(--text);}
.section-line{flex:1;height:1px;background:var(--border);margin-left:1rem;align-self:center;}

.about-grid{display:grid;grid-template-columns:3fr 2fr;gap:3rem;align-items:start;}
.about-text p{font-size:16px;font-weight:300;color:var(--muted);margin-bottom:1rem;line-height:1.85;}
.about-stats{display:flex;flex-direction:column;gap:1rem;}
.stat-item{background:var(--card-bg);border:1px solid var(--border);padding:1.25rem 1.5rem;display:flex;flex-direction:column;}
.stat-value{font-family:'Bebas Neue',sans-serif;font-size:2.2rem;color:var(--accent);line-height:1;margin-bottom:4px;}
.stat-label{font-size:12px;color:var(--muted);text-transform:uppercase;letter-spacing:.08em;font-family:'DM Mono',monospace;}

.skills-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;}
.skill-card{background:var(--card-bg);border:1px solid var(--border);padding:1.75rem;transition:border-color .2s,transform .2s;}
.skill-card:hover{border-color:var(--accent);transform:translateY(-3px);}
.skill-icon{width:40px;height:40px;background:var(--tag-bg);display:flex;align-items:center;justify-content:center;margin-bottom:1rem;font-size:20px;}
.skill-name{font-family:'DM Mono',monospace;font-size:12px;font-weight:500;color:var(--accent);text-transform:uppercase;letter-spacing:.08em;margin-bottom:.5rem;}
.skill-desc{font-size:13px;color:var(--muted);line-height:1.6;}
.skill-tags{display:flex;flex-wrap:wrap;gap:6px;margin-top:1rem;}
.tag{font-family:'DM Mono',monospace;font-size:11px;background:var(--tag-bg);color:var(--tag-text);padding:3px 10px;letter-spacing:.03em;}

/* ── PROJETS ── */
.projects-list{display:flex;flex-direction:column;gap:0;}

.project-item{border:1px solid var(--border);margin-bottom:1rem;overflow:hidden;}

.project-card{background:var(--card-bg);display:grid;grid-template-columns:80px 1fr auto;align-items:center;gap:2rem;padding:2rem;cursor:pointer;transition:border-color .2s,background .2s;user-select:none;}
.project-card:hover{background:#fafaf8;}
.project-item.open .project-card{background:#fafaf8;border-bottom:1px solid var(--border);}

.project-num{font-family:'Bebas Neue',sans-serif;font-size:3.5rem;color:var(--bg2);line-height:1;text-align:center;transition:color .2s;}
.project-item.open .project-num{color:var(--accent);}

.project-body{flex:1;}
.project-title{font-family:'DM Sans',sans-serif;font-size:18px;font-weight:500;margin-bottom:.4rem;color:var(--text);}
.project-meta{font-family:'DM Mono',monospace;font-size:11px;color:var(--accent);text-transform:uppercase;letter-spacing:.08em;margin-bottom:.6rem;}
.project-desc{font-size:14px;color:var(--muted);line-height:1.65;}

.project-toggle{width:36px;height:36px;border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:20px;color:var(--muted);transition:transform .35s,background .2s,color .2s;flex-shrink:0;}
.project-item.open .project-toggle{transform:rotate(45deg);background:var(--accent);color:#fff;border-color:var(--accent);}

/* Panneau dépliable */
.project-detail{max-height:0;overflow:hidden;transition:max-height .5s cubic-bezier(.4,0,.2,1);}
.project-item.open .project-detail{max-height:800px;}

.project-detail-inner{padding:2.5rem 2rem 2rem 6.5rem;background:var(--card-bg);}

.detail-grid{display:grid;grid-template-columns:1fr 1fr;gap:2.5rem;align-items:start;}

.detail-section-title{font-family:'DM Mono',monospace;font-size:11px;font-weight:500;color:var(--accent);text-transform:uppercase;letter-spacing:.1em;margin-bottom:1rem;padding-bottom:.5rem;border-bottom:1px solid var(--border);}

.detail-text{font-size:14px;color:var(--muted);line-height:1.8;}

.detail-list{list-style:none;display:flex;flex-direction:column;gap:.6rem;}
.detail-list li{font-size:14px;color:var(--muted);display:flex;align-items:flex-start;gap:.6rem;line-height:1.5;}
.detail-list li::before{content:'→';color:var(--accent);font-family:'DM Mono',monospace;flex-shrink:0;margin-top:1px;}

.detail-placeholder{aspect-ratio:16/9;background:var(--bg2);border:1px dashed var(--border);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:.5rem;color:var(--muted);font-size:13px;font-family:'DM Mono',monospace;cursor:pointer;transition:border-color .2s;}
.detail-placeholder:hover{border-color:var(--accent);color:var(--accent);}
.detail-placeholder span{font-size:1.5rem;}

.detail-tags{display:flex;flex-wrap:wrap;gap:6px;margin-top:1.5rem;}

.contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:start;}
.contact-intro{font-size:16px;color:rgba(255,255,255,.6);font-weight:300;line-height:1.85;margin-bottom:2rem;}
.contact-items{display:flex;flex-direction:column;gap:1rem;}
.contact-item{display:flex;align-items:center;gap:1rem;font-size:14px;color:rgba(255,255,255,.8);}
.contact-item-icon{width:36px;height:36px;background:rgba(255,255,255,.1);display:flex;align-items:center;justify-content:center;font-size:16px;flex-shrink:0;color:rgba(255,255,255,.8);}
.contact-form{display:flex;flex-direction:column;gap:1rem;}
.contact-form input,.contact-form textarea{background:rgba(255,255,255,.08);border:1px solid rgba(255,255,255,.15);padding:.85rem 1.1rem;font-family:'DM Sans',sans-serif;font-size:14px;color:#fff;outline:none;transition:border-color .2s;resize:none;width:100%;}
.contact-form input::placeholder,.contact-form textarea::placeholder{color:rgba(255,255,255,.4);}
.contact-form input:focus,.contact-form textarea:focus{border-color:rgba(255,255,255,.5);}
.contact-form textarea{height:120px;}

footer{border-top:1px solid var(--border);padding:2rem 4rem;display:flex;justify-content:space-between;align-items:center;font-size:12px;color:var(--muted);font-family:'DM Mono',monospace;letter-spacing:.04em;}

.fade-in{opacity:0;transform:translateY(20px);transition:opacity .6s ease,transform .6s ease;}
.fade-in.visible{opacity:1;transform:translateY(0);}

@media(max-width:768px){
  .hero{grid-template-columns:1fr;}
  .hero-right{min-height:280px;}
  section{padding:3rem 1.5rem;}
  .skills-grid{grid-template-columns:1fr;}
  .project-card{grid-template-columns:1fr;}
  .project-detail-inner{padding:1.5rem;}
  .detail-grid{grid-template-columns:1fr;}
  .contact-grid{grid-template-columns:1fr;}
  .about-grid{grid-template-columns:1fr;}
  nav{padding:0 1.5rem;}
  .nav-links{gap:1rem;}
  footer{padding:1.5rem;flex-direction:column;gap:.5rem;}
}
</style>
</head>
<body>

<nav>
  <a href="#" class="nav-logo"><img src="assets/logo-gmp.png" alt="Logo Département GMP Toulouse"></a>
  <ul class="nav-links">
    <li><a href="#about">À propos</a></li>
    <li><a href="#skills">Compétences</a></li>
    <li><a href="#projects">Projets</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<div class="hero">
  <div class="hero-left">
    <div class="hero-tag">Portfolio BUT1 GMP — 2024/2025</div>
    <h1 class="hero-name">Mickaël<br><span>DESTAL</span></h1>
    <p class="hero-desc">Étudiant en 1ère année de BUT Génie Mécanique et Productique à l'IUT Paul Sabatier de Toulouse, passionné par la conception, la fabrication et l'industrie du futur.</p>
    <div class="hero-ctas">
      <a href="#projects" class="btn-primary">Voir mes projets</a>
      <a href="#contact" class="btn-outline">Me contacter</a>
    </div>
  </div>
  <div class="hero-right">
    <svg class="hero-blueprint" viewBox="0 0 600 700" fill="none" xmlns="http://www.w3.org/2000/svg">
      <g opacity="0.12">
        <line x1="0" y1="50" x2="600" y2="50" stroke="white" stroke-width="0.5"/>
        <line x1="0" y1="150" x2="600" y2="150" stroke="white" stroke-width="0.5"/>
        <line x1="0" y1="250" x2="600" y2="250" stroke="white" stroke-width="0.5"/>
        <line x1="0" y1="350" x2="600" y2="350" stroke="white" stroke-width="0.5"/>
        <line x1="0" y1="450" x2="600" y2="450" stroke="white" stroke-width="0.5"/>
        <line x1="0" y1="550" x2="600" y2="550" stroke="white" stroke-width="0.5"/>
        <line x1="50" y1="0" x2="50" y2="700" stroke="white" stroke-width="0.5"/>
        <line x1="150" y1="0" x2="150" y2="700" stroke="white" stroke-width="0.5"/>
        <line x1="250" y1="0" x2="250" y2="700" stroke="white" stroke-width="0.5"/>
        <line x1="350" y1="0" x2="350" y2="700" stroke="white" stroke-width="0.5"/>
        <line x1="450" y1="0" x2="450" y2="700" stroke="white" stroke-width="0.5"/>
        <line x1="550" y1="0" x2="550" y2="700" stroke="white" stroke-width="0.5"/>
        <circle cx="300" cy="350" r="120" stroke="white" stroke-width="1"/>
        <circle cx="300" cy="350" r="80" stroke="white" stroke-width="0.5" stroke-dasharray="6 4"/>
        <circle cx="300" cy="350" r="40" stroke="white" stroke-width="0.5"/>
        <line x1="180" y1="350" x2="420" y2="350" stroke="white" stroke-width="1"/>
        <line x1="300" y1="230" x2="300" y2="470" stroke="white" stroke-width="1"/>
        <rect x="150" y="150" width="300" height="400" stroke="white" stroke-width="1"/>
        <text x="155" y="145" fill="white" font-size="10" font-family="monospace">REV.01</text>
        <text x="380" y="565" fill="white" font-size="9" font-family="monospace">DESTAL M.</text>
        <text x="155" y="565" fill="white" font-size="9" font-family="monospace">BUT1 GMP</text>
      </g>
      <circle cx="300" cy="350" r="120" fill="rgba(255,255,255,0.12)" stroke="rgba(255,255,255,0.35)" stroke-width="2"/>
      <image href="assets/logo-gmp.png" x="210" y="260" width="180" height="180" preserveAspectRatio="xMidYMid meet" style="border-radius:50%;"/>
    </svg>
    <div class="hero-avatar-wrap">
      <div class="hero-info-card"><p>Formation</p><strong>BUT Génie Mécanique et Productique</strong></div>
      <div class="hero-info-card"><p>Établissement</p><strong>IUT Paul Sabatier — Toulouse</strong></div>
    </div>
  </div>
</div>

<!-- À PROPOS -->
<section id="about">
  <div class="section-header">
    <span class="section-num">01</span>
    <h2 class="section-title">À propos</h2>
    <div class="section-line"></div>
  </div>
  <div class="about-grid fade-in">
    <div class="about-text">
      <p>Je m'appelle Mickaël DESTAL et je suis actuellement en 1ère année de BUT Génie Mécanique et Productique (GMP) à l'IUT Paul Sabatier de Toulouse.</p>
      <p>La formation BUT GMP m'a permis de découvrir et maîtriser les grands domaines du génie mécanique : de la conception assistée par ordinateur à la fabrication, en passant par la mécanique des solides, la productique et la gestion de projets industriels.</p>
      <p>Passionné par les technologies de production et l'industrie 4.0, je souhaite mettre mes compétences au service de projets concrets et innovants.</p>
    </div>
    <div class="about-stats">
      <div class="stat-item"><span class="stat-value">BUT1</span><span class="stat-label">Génie Méca. & Productique</span></div>
      <div class="stat-item"><span class="stat-value">2024</span><span class="stat-label">Rentrée universitaire</span></div>
      <div class="stat-item"><span class="stat-value">5+</span><span class="stat-label">Projets réalisés</span></div>
      <div class="stat-item"><span class="stat-value">IUT</span><span class="stat-label">Paul Sabatier — Toulouse</span></div>
    </div>
  </div>
</section>

<!-- COMPÉTENCES -->
<section id="skills" style="background:var(--bg2);max-width:100%;width:100%;padding:5rem 4rem;">
<div style="max-width:1100px;margin:0 auto;">
  <div class="section-header">
    <span class="section-num">02</span>
    <h2 class="section-title">Compétences</h2>
    <div class="section-line"></div>
  </div>
  <div class="skills-grid fade-in">
    <div class="skill-card"><div class="skill-icon">⚙️</div><div class="skill-name">Conception CAO</div><div class="skill-desc">Modélisation 3D, assemblages, mise en plan et cotation fonctionnelle de pièces mécaniques.</div><div class="skill-tags"><span class="tag">SolidWorks</span><span class="tag">CATIA</span><span class="tag">Dessin tech.</span></div></div>
    <div class="skill-card"><div class="skill-icon">🔧</div><div class="skill-name">Fabrication</div><div class="skill-desc">Usinage conventionnel et à commande numérique, tournage, fraisage, programmation CN.</div><div class="skill-tags"><span class="tag">Tournage</span><span class="tag">Fraisage</span><span class="tag">FAO</span></div></div>
    <div class="skill-card"><div class="skill-icon">📐</div><div class="skill-name">Mécanique des solides</div><div class="skill-desc">Analyse des contraintes, cinématique, statique et résistance des matériaux.</div><div class="skill-tags"><span class="tag">Statique</span><span class="tag">RDM</span><span class="tag">Cinématique</span></div></div>
    <div class="skill-card"><div class="skill-icon">📊</div><div class="skill-name">Qualité & Métrologie</div><div class="skill-desc">Contrôle dimensionnel, tolérances, métrologie et outils qualité en environnement industriel.</div><div class="skill-tags"><span class="tag">Pied à coulisse</span><span class="tag">Tolérancement</span><span class="tag">ISO</span></div></div>
    <div class="skill-card"><div class="skill-icon">🏭</div><div class="skill-name">Productique</div><div class="skill-desc">Gestion de production, gammes d'usinage, optimisation des processus de fabrication.</div><div class="skill-tags"><span class="tag">Gammes</span><span class="tag">GPAO</span><span class="tag">Lean</span></div></div>
    <div class="skill-card"><div class="skill-icon">🤝</div><div class="skill-name">Gestion de projet</div><div class="skill-desc">Travail en équipe, planification, communication technique, rapports et présentations.</div><div class="skill-tags"><span class="tag">Gantt</span><span class="tag">Rapport</span><span class="tag">Oral</span></div></div>
  </div>
</div>
</section>

<!-- PROJETS -->
<section id="projects">
  <div class="section-header">
    <span class="section-num">03</span>
    <h2 class="section-title">Projets</h2>
    <div class="section-line"></div>
  </div>
  <div class="projects-list fade-in">

    <!-- Projet 01 -->
    <div class="project-item" id="proj1">
      <div class="project-card" onclick="toggleProject('proj1')">
        <div class="project-num">01</div>
        <div class="project-body">
          <div class="project-meta">Conception CAO — S1</div>
          <div class="project-title">Conception d'un étau de fraisage</div>
          <div class="project-desc">Modélisation complète d'un étau d'usinage sous SolidWorks : pièces, assemblage, mise en plan cotée et nomenclature.</div>
        </div>
        <div class="project-toggle">+</div>
      </div>
      <div class="project-detail">
        <div class="project-detail-inner">
          <div class="detail-grid">
            <div>
              <div class="detail-section-title">Description du projet</div>
              <p class="detail-text">Ce projet consistait à modéliser intégralement un étau de fraisage destiné à maintenir des pièces lors d'opérations d'usinage. Le travail couvrait la modélisation de chaque pièce constitutive, leur assemblage paramétrique, ainsi que la réalisation des plans de définition conformes aux normes ISO.<br><br>La contrainte principale était de respecter les jeux fonctionnels entre les pièces mobiles et fixes, en assurant un guidage linéaire sans jeu excessif.</p>
              <div class="detail-section-title" style="margin-top:1.5rem;">Compétences mobilisées</div>
              <ul class="detail-list">
                <li>Modélisation 3D paramétrique sous SolidWorks</li>
                <li>Création d'un assemblage avec contraintes</li>
                <li>Mise en plan cotée (cotation fonctionnelle)</li>
                <li>Rédaction de la nomenclature</li>
                <li>Respect des normes de dessin technique ISO</li>
              </ul>
              <div class="detail-tags">
                <span class="tag">SolidWorks</span><span class="tag">Assemblage</span><span class="tag">Mise en plan</span><span class="tag">ISO</span><span class="tag">Nomenclature</span>
              </div>
            </div>
            <div>
              <div class="detail-section-title">Visuel du projet</div>
              <div class="detail-placeholder"><span>🖼️</span>Ajoutez une capture SolidWorks<br>ou une photo de la pièce</div>
              <div style="margin-top:1.5rem;">
                <div class="detail-section-title">Résultats obtenus</div>
                <ul class="detail-list">
                  <li>Modèle 3D complet et fonctionnel</li>
                  <li>Plans conformes aux exigences pédagogiques</li>
                  <li>Assemblage animé démontrant le fonctionnement</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Projet 02 -->
    <div class="project-item" id="proj2">
      <div class="project-card" onclick="toggleProject('proj2')">
        <div class="project-num">02</div>
        <div class="project-body">
          <div class="project-meta">Fabrication — S1</div>
          <div class="project-title">Usinage d'une pièce au tour CN</div>
          <div class="project-desc">Rédaction de la gamme d'usinage, programmation ISO, mise en œuvre sur tour à commande numérique et contrôle dimensionnel final.</div>
        </div>
        <div class="project-toggle">+</div>
      </div>
      <div class="project-detail">
        <div class="project-detail-inner">
          <div class="detail-grid">
            <div>
              <div class="detail-section-title">Description du projet</div>
              <p class="detail-text">À partir d'un dessin de définition, il s'agissait de planifier et de réaliser l'usinage complet d'une pièce cylindrique complexe sur un tour à commande numérique. Le projet incluait l'analyse du dessin, le choix des outils et des conditions de coupe, la programmation en ISO, l'usinage et enfin la vérification métrologique.<br><br>Ce projet m'a permis de comprendre l'enchaînement complet d'un processus de fabrication, de la gamme à la pièce finie.</p>
              <div class="detail-section-title" style="margin-top:1.5rem;">Compétences mobilisées</div>
              <ul class="detail-list">
                <li>Lecture et analyse d'un dessin de définition</li>
                <li>Rédaction d'une gamme d'usinage</li>
                <li>Programmation ISO (G-code) pour tour CN</li>
                <li>Réglage et mise en œuvre de la machine</li>
                <li>Contrôle métrologique de la pièce finie</li>
              </ul>
              <div class="detail-tags">
                <span class="tag">Tournage CN</span><span class="tag">Prog. ISO</span><span class="tag">Gamme</span><span class="tag">Métrologie</span><span class="tag">G-code</span>
              </div>
            </div>
            <div>
              <div class="detail-section-title">Visuel du projet</div>
              <div class="detail-placeholder"><span>🖼️</span>Ajoutez une photo de la pièce<br>ou de la machine</div>
              <div style="margin-top:1.5rem;">
                <div class="detail-section-title">Résultats obtenus</div>
                <ul class="detail-list">
                  <li>Pièce usinée dans les tolérances imposées</li>
                  <li>Gamme d'usinage complète et documentée</li>
                  <li>Programme CN validé et testé</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Projet 03 -->
    <div class="project-item" id="proj3">
      <div class="project-card" onclick="toggleProject('proj3')">
        <div class="project-num">03</div>
        <div class="project-body">
          <div class="project-meta">Projet transversal — S2</div>
          <div class="project-title">Amélioration d'un système mécatronique</div>
          <div class="project-desc">Analyse d'un système existant, identification des axes d'amélioration, conception d'une solution et rédaction d'un dossier technique complet.</div>
        </div>
        <div class="project-toggle">+</div>
      </div>
      <div class="project-detail">
        <div class="project-detail-inner">
          <div class="detail-grid">
            <div>
              <div class="detail-section-title">Description du projet</div>
              <p class="detail-text">Ce projet transversal en équipe visait à analyser un système mécatronique existant, à identifier ses limites et à proposer une amélioration concrète. Le travail s'appuyait sur une démarche d'ingénierie complète : analyse fonctionnelle, cahier des charges, conception de la solution et validation.<br><br>Un dossier technique complet a été rédigé, et le projet a fait l'objet d'une présentation orale devant un jury composé d'enseignants.</p>
              <div class="detail-section-title" style="margin-top:1.5rem;">Compétences mobilisées</div>
              <ul class="detail-list">
                <li>Analyse fonctionnelle d'un système existant</li>
                <li>Rédaction d'un cahier des charges</li>
                <li>Travail en équipe et répartition des tâches</li>
                <li>Conception d'une solution améliorée</li>
                <li>Communication orale devant jury</li>
              </ul>
              <div class="detail-tags">
                <span class="tag">Analyse fonct.</span><span class="tag">Cahier des charges</span><span class="tag">Équipe</span><span class="tag">Présentation</span>
              </div>
            </div>
            <div>
              <div class="detail-section-title">Visuel du projet</div>
              <div class="detail-placeholder"><span>🖼️</span>Ajoutez un schéma ou une photo<br>du système étudié</div>
              <div style="margin-top:1.5rem;">
                <div class="detail-section-title">Résultats obtenus</div>
                <ul class="detail-list">
                  <li>Dossier technique complet rendu</li>
                  <li>Solution validée par l'équipe pédagogique</li>
                  <li>Présentation orale réussie devant jury</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Projet 04 -->
    <div class="project-item" id="proj4">
      <div class="project-card" onclick="toggleProject('proj4')">
        <div class="project-num">04</div>
        <div class="project-body">
          <div class="project-meta">SAÉ — S2</div>
          <div class="project-title">Situation d'apprentissage et d'évaluation</div>
          <div class="project-desc">Résolution d'une problématique industrielle réelle en équipe, intégrant conception, fabrication, démarche qualité et communication professionnelle.</div>
        </div>
        <div class="project-toggle">+</div>
      </div>
      <div class="project-detail">
        <div class="project-detail-inner">
          <div class="detail-grid">
            <div>
              <div class="detail-section-title">Description du projet</div>
              <p class="detail-text">La SAÉ (Situation d'Apprentissage et d'Évaluation) est un projet intégrateur qui mobilise simultanément plusieurs compétences du BUT GMP. Partant d'une problématique industrielle réelle, l'équipe devait proposer une solution complète alliant conception, fabrication et démarche qualité.<br><br>Ce type de projet est au cœur de la pédagogie BUT et vise à évaluer la capacité à travailler en conditions proches du monde professionnel.</p>
              <div class="detail-section-title" style="margin-top:1.5rem;">Compétences mobilisées</div>
              <ul class="detail-list">
                <li>Intégration de multiples compétences GMP</li>
                <li>Résolution de problème en équipe</li>
                <li>Démarche qualité et traçabilité</li>
                <li>Rédaction de livrables professionnels</li>
                <li>Communication technique orale et écrite</li>
              </ul>
              <div class="detail-tags">
                <span class="tag">SAÉ</span><span class="tag">Intégrateur</span><span class="tag">Qualité</span><span class="tag">Industrie</span><span class="tag">Équipe</span>
              </div>
            </div>
            <div>
              <div class="detail-section-title">Visuel du projet</div>
              <div class="detail-placeholder"><span>🖼️</span>Ajoutez une photo ou un rendu<br>de votre réalisation</div>
              <div style="margin-top:1.5rem;">
                <div class="detail-section-title">Résultats obtenus</div>
                <ul class="detail-list">
                  <li>Livrables complets rendus dans les délais</li>
                  <li>Compétences validées par l'équipe pédagogique</li>
                  <li>Expérience proche d'un contexte professionnel</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- CONTACT -->
<section id="contact" style="background:var(--accent2);max-width:100%;width:100%;padding:5rem 4rem;">
<div style="max-width:1100px;margin:0 auto;">
  <div class="section-header">
    <span class="section-num" style="color:rgba(255,255,255,.5);">04</span>
    <h2 class="section-title" style="color:#fff;">Contact</h2>
    <div class="section-line" style="background:rgba(255,255,255,.15);"></div>
  </div>
  <div class="contact-grid fade-in">
    <div>
      <p class="contact-intro">Vous souhaitez me contacter pour une opportunité de stage, un partenariat ou en savoir plus sur mon parcours ? N'hésitez pas à m'écrire.</p>
      <div class="contact-items">
        <div class="contact-item"><div class="contact-item-icon">✉</div><span>mickael.destal@example.com</span></div>
        <div class="contact-item"><div class="contact-item-icon">📍</div><span>Toulouse, Occitanie, France</span></div>
        <div class="contact-item"><div class="contact-item-icon">🎓</div><span>IUT Paul Sabatier — Promotion 2025</span></div>
      </div>
    </div>
    <div class="contact-form">
      <input type="text" placeholder="Votre nom">
      <input type="email" placeholder="Votre e-mail">
      <textarea placeholder="Votre message…"></textarea>
      <button class="btn-primary" style="align-self:flex-start;background:#fff;color:var(--accent2);">Envoyer le message</button>
    </div>
  </div>
</div>
</section>

<footer>
  <span>© 2025 Mickaël DESTAL — BUT1 GMP</span>
  <span>IUT Paul Sabatier · Toulouse</span>
</footer>

<script>
function toggleProject(id) {
  const item = document.getElementById(id);
  const isOpen = item.classList.contains('open');
  document.querySelectorAll('.project-item.open').forEach(el => el.classList.remove('open'));
  if (!isOpen) {
    item.classList.add('open');
    setTimeout(() => item.scrollIntoView({ behavior: 'smooth', block: 'nearest' }), 50);
  }
}

const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
</script>
</body>
</html>
Uploading index.html…]()

