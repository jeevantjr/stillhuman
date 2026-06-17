<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Dr. Thangarasa Jeevaraaj | AI Reviewer | Health Informatician</title>

<meta name="description" content="AI Reviewer, Health Informatics Specialist, Digital Health Developer, Physician, Researcher">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<link rel="stylesheet"
href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

<style>

:root{
--primary:#0F4C81;
--secondary:#00A8E8;
--accent:#1E9E63;
--dark:#111827;
--light:#F5F7FA;
--white:#ffffff;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
font-family:'Inter',sans-serif;
background:#f7f9fc;
color:#1f2937;
line-height:1.7;
}

html{
scroll-behavior:smooth;
}

.container{
width:90%;
max-width:1200px;
margin:auto;
}

section{
padding:80px 0;
}

h1,h2,h3{
font-weight:700;
}

a{
text-decoration:none;
}

/* HERO */

.hero{
background:linear-gradient(135deg,#0F4C81,#00A8E8);
color:white;
padding:100px 0;
}

.hero-grid{
display:grid;
grid-template-columns:300px 1fr;
gap:50px;
align-items:center;
}

.profile-img{
width:280px;
height:280px;
border-radius:50%;
object-fit:cover;
border:8px solid rgba(255,255,255,.2);
}

.hero h1{
font-size:3rem;
margin-bottom:10px;
}

.hero h3{
font-weight:400;
margin-bottom:20px;
}

.badges{
display:flex;
flex-wrap:wrap;
gap:10px;
margin:20px 0;
}

.badge{
background:rgba(255,255,255,.15);
padding:8px 14px;
border-radius:50px;
font-size:.9rem;
}

.btn-group{
margin-top:30px;
display:flex;
flex-wrap:wrap;
gap:15px;
}

.btn{
padding:14px 22px;
border-radius:50px;
font-weight:600;
transition:.3s;
}

.btn-primary{
background:white;
color:#0F4C81;
}

.btn-outline{
border:2px solid white;
color:white;
}

.btn:hover{
transform:translateY(-3px);
}

/* COUNTERS */

.stats{
margin-top:-60px;
}

.stats-grid{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:20px;
}

.stat-card{
background:white;
padding:30px;
border-radius:20px;
box-shadow:0 10px 30px rgba(0,0,0,.08);
text-align:center;
}

.stat-number{
font-size:2.5rem;
font-weight:800;
color:var(--primary);
}

/* SECTION TITLE */

.section-title{
text-align:center;
margin-bottom:50px;
}

.section-title h2{
font-size:2.2rem;
color:var(--primary);
}

/* ABOUT */

.about{
background:white;
}

.about p{
font-size:1.1rem;
max-width:900px;
margin:auto;
text-align:center;
}

/* SKILLS */

.skills-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:25px;
}

.skill-card{
background:white;
padding:30px;
border-radius:20px;
box-shadow:0 10px 25px rgba(0,0,0,.06);
transition:.3s;
}

.skill-card:hover{
transform:translateY(-6px);
}

.skill-card i{
font-size:40px;
color:var(--secondary);
margin-bottom:15px;
}

/* PROJECTS */

.projects{
background:#f4f7fb;
}

.project-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(350px,1fr));
gap:25px;
}

.project-card{
background:white;
padding:30px;
border-radius:20px;
box-shadow:0 10px 25px rgba(0,0,0,.07);
}

.project-card h3{
margin-bottom:10px;
color:var(--primary);
}

.tech{
margin:15px 0;
display:flex;
flex-wrap:wrap;
gap:8px;
}

.tech span{
background:#eef5ff;
padding:6px 10px;
border-radius:30px;
font-size:.85rem;
}

.project-links{
margin-top:20px;
}

.project-links a{
margin-right:15px;
font-weight:600;
color:var(--secondary);
}

/* TIMELINE */

.timeline{
position:relative;
max-width:900px;
margin:auto;
}

.timeline::before{
content:'';
position:absolute;
left:50%;
width:4px;
height:100%;
background:#00A8E8;
}

.timeline-item{
width:50%;
padding:20px 40px;
position:relative;
}

.timeline-item:nth-child(odd){
left:0;
text-align:right;
}

.timeline-item:nth-child(even){
left:50%;
}

.timeline-item::before{
content:'';
position:absolute;
top:30px;
width:18px;
height:18px;
background:#00A8E8;
border-radius:50%;
}

.timeline-item:nth-child(odd)::before{
right:-11px;
}

.timeline-item:nth-child(even)::before{
left:-11px;
}

/* CONTACT */

.contact{
background:linear-gradient(135deg,#0F4C81,#00A8E8);
color:white;
text-align:center;
}

.contact a{
color:white;
}

footer{
padding:30px;
text-align:center;
background:#0b2d4d;
color:white;
}

/* RESPONSIVE */

@media(max-width:900px){

.hero-grid{
grid-template-columns:1fr;
text-align:center;
}

.profile-img{
margin:auto;
}

.stats-grid{
grid-template-columns:repeat(2,1fr);
}

.timeline::before{
left:20px;
}

.timeline-item,
.timeline-item:nth-child(even),
.timeline-item:nth-child(odd){
left:0;
width:100%;
text-align:left;
padding-left:60px;
}

.timeline-item::before{
left:10px !important;
}
}

</style>
</head>

<body>

<section class="hero">
<div class="container">
<div class="hero-grid">

<img src="profile.jpg" class="profile-img" alt="Dr Jeevaraj">

<div>

<h1>Dr. Thangarasa Jeevaraaj</h1>

<h3>
Physician • Health Informatician • AI Reviewer • Digital Health Developer
</h3>

<p>
Bridging medicine, artificial intelligence, data science,
public health, and human-centered technology.
</p>

<div class="badges">
<div class="badge">MBBS</div>
<div class="badge">MCGP</div>
<div class="badge">MSc Biomedical Informatics</div>
<div class="badge">MD Health Informatics Trainee</div>
</div>

<div class="btn-group">

<a class="btn btn-primary"
href="https://drjeevaraj.com"
target="_blank">
Portfolio Website
</a>

<a class="btn btn-outline"
href="mailto:tjeevaraj78@gmail.com">
Email Me
</a>

</div>

</div>
</div>
</div>
</section>

<section class="stats">
<div class="container">

<div class="stats-grid">

<div class="stat-card">
<div class="stat-number">20+</div>
Years in Medicine
</div>

<div class="stat-card">
<div class="stat-number">8</div>
Health Systems Built
</div>

<div class="stat-card">
<div class="stat-number">2</div>
Research Papers
</div>

<div class="stat-card">
<div class="stat-number">3</div>
Languages
</div>

</div>
</div>
</section>

<section class="about">
<div class="container">
<div class="section-title">
<h2>Professional Profile</h2>
</div>

<p>
Medical Doctor and Health Informatics specialist with over
20 years of healthcare experience. Experienced in evaluating
complex information, validating data, reviewing AI-generated
outputs, and developing digital health systems for real-world
public health environments across Sri Lanka.
</p>

</div>
</section>

<section>
<div class="container">

<div class="section-title">
<h2>AI Review & Evaluation Expertise</h2>
</div>

<div class="skills-grid">

<div class="skill-card">
<i class="fas fa-brain"></i>
<h3>AI Output Review</h3>
<p>Evaluate accuracy, reasoning, consistency and usefulness.</p>
</div>

<div class="skill-card">
<i class="fas fa-check-circle"></i>
<h3>Quality Assurance</h3>
<p>Validation, fact checking and error detection.</p>
</div>

<div class="skill-card">
<i class="fas fa-file-medical"></i>
<h3>Clinical Expertise</h3>
<p>Healthcare domain knowledge for medical AI review.</p>
</div>

<div class="skill-card">
<i class="fas fa-chart-line"></i>
<h3>Data Analytics</h3>
<p>Public health data analysis and interpretation.</p>
</div>

</div>
</div>
</section>

<section class="projects">

<div class="container">

<div class="section-title">
<h2>Featured Projects</h2>
</div>

<div class="project-grid">

<div class="project-card">
<h3>OutbreakWatch</h3>
<p>Disease surveillance and outbreak early warning system.</p>

<div class="tech">
<span>Python</span>
<span>Django</span>
<span>PostgreSQL</span>
</div>

<div class="project-links">
<a href="https://jeevantjr.github.io/OutbreakWatch-main/" target="_blank">Live Demo</a>
</div>
</div>

<div class="project-card">
<h3>FloodTrackerApp</h3>
<p>Disaster response and emergency management platform.</p>

<div class="tech">
<span>React</span>
<span>Node.js</span>
<span>PWA</span>
</div>

<div class="project-links">
<a href="https://jeevantjr.github.io/FloodTrackerApp-main/" target="_blank">Live Demo</a>
</div>
</div>

<div class="project-card">
<h3>District Health Stats PWA</h3>

<p>Interactive district health analytics dashboard.</p>

<div class="project-links">
<a href="https://jeevantjr.github.io/rdhs-stats-pwa-main/" target="_blank">Live Demo</a>
</div>

</div>

<div class="project-card">
<h3>Health Fleet Manager</h3>

<p>Fleet scheduling and logistics management system.</p>

<div class="project-links">
<a href="https://jeevantjr.github.io/vmsrdhstrinco-main/" target="_blank">Live Demo</a>
</div>

</div>

</div>
</div>
</section>

<section>

<div class="container">

<div class="section-title">
<h2>Career Timeline</h2>
</div>

<div class="timeline">

<div class="timeline-item">
<h3>2006</h3>
<p>MBBS – University of Jaffna</p>
</div>

<div class="timeline-item">
<h3>2016</h3>
<p>MCGP Qualification</p>
</div>

<div class="timeline-item">
<h3>2022</h3>
<p>MSc Biomedical Informatics</p>
</div>

<div class="timeline-item">
<h3>2026</h3>
<p>National Cancer Control Programme</p>
</div>

<div class="timeline-item">
<h3>2026</h3>
<p>MD Health Informatics Trainee</p>
</div>

</div>
</div>

</section>

<section class="contact">

<div class="container">

<h2>Connect</h2>

<br>

<p>
<i class="fas fa-envelope"></i>
<a href="mailto:tjeevaraj78@gmail.com">
tjeevaraj78@gmail.com
</a>
</p>

<br>

<p>
<i class="fab fa-linkedin"></i>
<a href="https://linkedin.com/in/geevanathy" target="_blank">
LinkedIn Profile
</a>
</p>

<br>

<p>
<i class="fas fa-globe"></i>
<a href="https://drjeevaraj.com" target="_blank">
www.drjeevaraj.com
</a>
</p>

</div>

</section>

<footer>

© 2026 Dr. Thangarasa Jeevaraaj
<br>
AI Reviewer • Health Informatician • Digital Health Developer

</footer>

</body>
</html>