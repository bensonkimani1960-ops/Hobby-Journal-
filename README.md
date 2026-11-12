
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ben Logic | Hobby & Research Hub</title>

<style>
:root {
  --bg:#101827;
  --card:#1c293c;
  --text:#ffffff;
  --accent:#00d5ff;
}
* {box-sizing:border-box;scroll-behavior:smooth}
body {
  margin:0;
  font-family:Arial,sans-serif;
  background:var(--bg);
  color:var(--text);
}
header {
  padding:55px 20px;
  text-align:center;
  background:linear-gradient(135deg,#102c50,#006c91);
}
header h1 {font-size:36px;margin-bottom:10px}
header p {color:#d4f5ff}
nav {
  background:#172235;
  padding:15px;
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:15px;
  position:sticky;
  top:0;
  z-index:10;
}
nav a {
  color:white;
  text-decoration:none;
  font-size:14px;
}
nav a:hover {color:var(--accent)}
button {
  background:var(--accent);
  color:#071522;
  border:0;
  padding:10px 16px;
  border-radius:7px;
  cursor:pointer;
}
.container {max-width:1100px;margin:auto;padding:25px}
section {padding:35px 0}
h2 {color:var(--accent)}
.grid {
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:18px;
}
.card {
  background:var(--card);
  padding:22px;
  border-radius:12px;
  border:1px solid #30435b;
  transition:transform .2s;
}
.card:hover {transform:translateY(-5px)}
.card h3 {color:var(--accent)}
.card a {color:var(--accent)}
input,textarea {
  width:100%;
  padding:12px;
  margin:8px 0;
  border-radius:6px;
  border:1px solid #53647b;
  background:#172235;
  color:white;
}
footer {
  text-align:center;
  padding:25px;
  background:#172235;
  color:#aaa;
}
.light {
  --bg:#edf3f8;
  --card:#ffffff;
  --text:#142033;
}
.light nav,.light footer {background:#dce7f0}
.light nav a {color:#142033}
</style>
</head>

<body>

<header>
<h1>BEN LOGIC</h1>
<p>Hobby • Engineering • Coding • Research</p>
<p>Welcome to my world of creativity and invention.</p>
<button onclick="toggleTheme()">Switch Theme</button>
</header>

<nav>
<a href="#home">Home</a>
<a href="#arduino">Arduino</a>
<a href="#rc">RC Engineering</a>
<a href="#yoyo">Yo-Yo</a>
<a href="#coding">Coding</a>
<a href="#research">Research</a>
<a href="#journal">Journal</a>
</nav>

<div class="container">

<section id="home">
<h2>My Hobby Journey</h2>
<p>
I am passionate about technology, electronics,
engineering, coding and creative inventions.
This is where I document my projects,
experiments and learning journey.
</p>
</section>

<section id="arduino">
<h2>Arduino Laboratory</h2>
<div class="grid">
<div class="card">
<h3>Electronics</h3>
<p>Circuits, sensors, LEDs, buzzers and components.</p>
</div>
<div class="card">
<h3>Arduino Projects</h3>
<p>Microcontrollers, motors, displays and automation.</p>
</div>
<div class="card">
<h3>Experiments</h3>
<p>Record circuit experiments and discoveries.</p>
</div>
</div>
</section>

<section id="rc">
<h2>RC Engineering</h2>
<div class="grid">
<div class="card">
<h3>RC Vehicles</h3>
<p>Cars, trucks and custom RC machines.</p>
</div>
<div class="card">
<h3>Mechanical Design</h3>
<p>Gears, motors, Lego mechanisms and inventions.</p>
</div>
<div class="card">
<h3>RC Experiments</h3>
<p>Transmitters, receivers and motor control.</p>
</div>
</div>
</section>

<section id="yoyo">
<h2>Yo-Yo Zone</h2>
<div class="grid">
<div class="card">
<h3>Yo-Yo Tricks</h3>
<p>Practice tricks and record your progress.</p>
</div>
<div class="card">
<h3>Collections</h3>
<p>Explore yo-yos, bearings, strings and accessories.</p>
</div>
</div>
</section>

<section id="coding">
<h2>Coding Academy</h2>
<div class="grid">
<div class="card">
<h3>Python</h3>
<p>Learn programming, logic and automation.</p>
</div>
<div class="card">
<h3>Web Development</h3>
<p>HTML, CSS and JavaScript projects.</p>
</div>
<div class="card">
<h3>Arduino Coding</h3>
<p>Write programs for electronic inventions.</p>
</div>
</div>
</section>

<section id="research">
<h2>Research & Inventions</h2>
<div class="grid">
<div class="card">
<h3>New Ideas</h3>
<p>Document creative ideas and future inventions.</p>
</div>
<div class="card">
<h3>Project Development</h3>
<p>Turn ideas into working prototypes.</p>
</div>
</div>
</section>

<section id="journal">
<h2>My Research Journal</h2>
<p>Write down your latest ideas and discoveries.</p>

<input id="title" placeholder="Project or journal title">
<textarea id="note" rows="5"
placeholder="Write your notes here..."></textarea>
<button onclick="saveNote()">Save Entry</button>

<div id="entries"></div>
</section>

</div>

<footer>
<p>BEN LOGIC | Hobby & Research Hub</p>
<p>Learning • Creating • Experimenting • Inventing</p>
</footer>

<script>
function toggleTheme() {
 document.body.classList.toggle("light");
}

function saveNote() {
 const title = document.getElementById("title").value.trim();
 const note = document.getElementById("note").value.trim();

 if (!title || !note) {
   alert("Please enter a title and your notes.");
   return;
 }

 const entries = JSON.parse(
   localStorage.getItem("benNotes") || "[]"
 );

 entries.unshift({
   title:title,
   note:note,
   date:new Date().toLocaleString()
 });

 localStorage.setItem("benNotes",JSON.stringify(entries));

 document.getElementById("title").value="";
 document.getElementById("note").value="";
 showNotes();
}

function showNotes() {
 const entries = JSON.parse(
   localStorage.getItem("benNotes") || "[]"
 );

 document.getElementById("entries").innerHTML =
 entries.map((entry,index) => `
 <div class="card" style="margin-top:15px">
 <h3>${escapeHTML(entry.title)}</h3>
 <p>${escapeHTML(entry.note).replace(/\n/g,"<br>")}</p>
 <small>${escapeHTML(entry.date)}</small><br><br>
 <button onclick="deleteNote(${index})">Delete</button>
 </div>
 `).join("");
}

function escapeHTML(value) {
 return value.replace(/[&<>"']/g, char => ({
 "&":"&amp;","<":"&lt;",">":"&gt;",
 '"':"&quot;","'":"&#39;"
 })[char]);
}

function deleteNote(index) {
 const entries = JSON.parse(
   localStorage.getItem("benNotes") || "[]"
 );
 entries.splice(index,1);
 localStorage.setItem("benNotes",JSON.stringify(entries));
 showNotes();
}

showNotes();
</script>

</body>
</html>
