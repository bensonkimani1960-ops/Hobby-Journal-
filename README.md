<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Ben Logic Hobby and Research Hub - Arduino, RC engineering, yo-yos, coding and inventions.">
<title>Ben Logic | Hobby & Research Hub</title>
<style>
:root{--bg:#101827;--card:#1c293c;--text:#fff;--accent:#00d5ff;--nav:#172235;--muted:#b7c5d8;--border:#30435b;--input:#172235;--shadow:#0003;}
body.light{--bg:#edf3f8;--card:#fff;--text:#142033;--accent:#007eae;--nav:#dce7f0;--muted:#52647a;--border:#cbd7e3;--input:#f5f8fb;--shadow:#0001;}
*{box-sizing:border-box;scroll-behavior:smooth;}
html{scroll-behavior:smooth;scroll-padding-top:90px;}
body{margin:0;width:100%;min-width:320px;overflow-x:hidden;font-family:Arial,sans-serif;background:var(--bg);color:var(--text);line-height:1.7;transition:background .25s,color .25s;}
img{max-width:100%;height:auto;}
header{padding:55px 20px;text-align:center;background:linear-gradient(135deg,#102c50,#006c91);}
header h1{font-size:clamp(32px,7vw,48px);margin:0 0 10px;letter-spacing:3px;}
header p{color:#d4f5ff;}
.tagline{font-size:13px;letter-spacing:2px;}
button{background:var(--accent);color:#071522;border:0;padding:11px 16px;border-radius:7px;cursor:pointer;font-weight:bold;margin:5px 3px;transition:opacity .2s,transform .2s;max-width:100%;}
button:hover{opacity:.85;transform:translateY(-1px);}
button:focus-visible,a:focus-visible,input:focus-visible,textarea:focus-visible{outline:2px solid var(--accent);outline-offset:3px;}
nav{background:var(--nav);padding:15px;display:flex;justify-content:center;align-items:center;flex-wrap:wrap;gap:15px;position:sticky;top:0;z-index:20;border-bottom:1px solid var(--border);width:100%;min-height:60px;}
nav a{color:var(--text);text-decoration:none;font-size:14px;font-weight:bold;white-space:nowrap;}
nav a:hover{color:var(--accent);}
.menu-toggle{display:none;}
.container{width:min(100% - 40px,1200px);max-width:1100px;margin-inline:auto;margin:auto;padding:25px;}
section{padding:35px 0;scroll-margin-top:75px;}
h2{color:var(--accent);border-bottom:1px solid var(--border);padding-bottom:10px;}
h3{color:var(--accent);}
p,li{color:var(--muted);}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,230px),1fr));gap:18px;}
.card{background:var(--card);padding:22px;border-radius:12px;border:1px solid var(--border);box-shadow:0 4px 12px var(--shadow);transition:transform .2s;overflow-wrap:anywhere;min-width:0;}
.card:hover{transform:translateY(-3px);}
.card a{color:var(--accent);}
.hero-image{width:100%;max-width:500px;display:block;margin:20px auto;border-radius:10px;background:#fff;padding:10px;object-fit:contain;}
.image-error{display:none;text-align:center;padding:20px;background:var(--card);border:1px dashed var(--border);border-radius:10px;}
input,textarea{width:100%;padding:12px;margin:8px 0;border-radius:6px;border:1px solid var(--border);background:var(--input);color:var(--text);font:inherit;max-width:100%;min-width:0;}
textarea{resize:vertical;}
pre{max-width:100%;overflow-x:auto;padding:16px;background:#080f1b;color:#00e5ff;border-radius:8px;font-size:14px;}
.note{background:var(--card);border-left:4px solid var(--accent);padding:12px 16px;margin:18px 0;}
.journal-entry{margin-top:15px;}
.journal-entry p{white-space:normal;overflow-wrap:anywhere;}
.small{font-size:12px;color:var(--muted);}
.empty{text-align:center;padding:20px;background:var(--card);border-radius:10px;color:var(--muted);}
footer{text-align:center;padding:30px;background:var(--nav);color:var(--muted);border-top:1px solid var(--border);}
@media(min-width:1200px){.container{max-width:1200px;}header{padding:75px 20px;}section{padding:45px 0;}.grid{gap:24px;}}
@media(min-width:900px) and (max-width:1199px){.container{max-width:1000px;}}
@media(min-width:651px) and (max-width:899px){.container{width:94%;padding:20px 10px;}header{padding:45px 15px;}nav{gap:12px;}nav a{font-size:13px;}.grid{grid-template-columns:repeat(2,minmax(0,1fr));}}
@media(max-width:650px){header{padding:35px 15px;}header h1{font-size:clamp(28px,9vw,40px);letter-spacing:2px;}.container{width:100%;padding:12px 16px;}section{padding:25px 0;scroll-margin-top:65px;}nav{flex-direction:column;align-items:stretch;gap:0;padding:8px;}.menu-toggle{display:block;width:100%;padding:14px;margin:0;}nav a{display:none;width:100%;padding:12px;text-align:center;border-top:1px solid var(--border);}nav.open a{display:block;}.grid{grid-template-columns:1fr;gap:14px;}.card{padding:17px;}.hero-image{max-width:100%;}button{padding:12px 15px;}input,textarea{font-size:16px;}footer{padding:25px 15px;}}
@media(max-width:380px){.container{padding:10px;}header h1{font-size:27px;}.card{padding:14px;}h2{font-size:21px;}pre{font-size:12px;}}
@media(hover:none){.card:hover{transform:none;}button:hover{transform:none;opacity:1;}}
@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto;}*,*::before,*::after{transition:none!important;animation:none!important;}}
</style>
</head>
<body>
<header id="home">
<h1>BEN LOGIC</h1>
<p class="tagline">HOBBY • ENGINEERING • CODING • RESEARCH</p>
<p>Welcome to my world of creativity and invention.</p>
<button id="themeButton" onclick="toggleTheme()">Switch Theme</button>
</header>
<nav id="navigation">
<button class="menu-toggle" onclick="toggleMenu()" aria-expanded="false" aria-controls="navigation">☰ MENU</button>
<a href="#home">Home</a><a href="#arduino">Arduino</a><a href="#rc">RC Engineering</a><a href="#yoyo">Yo-Yo</a><a href="#coding">Coding</a><a href="#research">Research</a><a href="#journal">Journal</a>
</nav>
<main class="container">
<section id="intro">
<h2>My Hobby Journey</h2>
<div class="card"><p>I am passionate about technology, electronics, engineering, coding and creative inventions. This is where I document my projects, experiments and learning journey.</p></div>
<div class="grid">
<div class="card"><h3>Arduino</h3><p>Electronics, sensors and microcontrollers.</p></div>
<div class="card"><h3>RC Engineering</h3><p>Remote-controlled vehicles and machines.</p></div>
<div class="card"><h3>Yo-Yo</h3><p>Tricks, equipment and skill development.</p></div>
<div class="card"><h3>Coding</h3><p>Python, HTML, CSS and Arduino programming.</p></div>
</div>
</section>
<section id="rc">
<h2>RC Engineering</h2>
<div class="grid">
<div class="card"><h3>RC Vehicles</h3><p>Cars, trucks and custom RC machines.</p></div>
<div class="card"><h3>Mechanical Design</h3><p>Gears, motors, Lego mechanisms and inventions.</p></div>
<div class="card"><h3>RC Experiments</h3><p>Transmitters, receivers and motor control.</p></div>
</div>
<div class="note"><strong>My goal:</strong> Combine Arduino, Lego, motors and RC technology to build original machines.</div>
</section>
<section id="arduino">
<h2>Arduino Laboratory</h2>
<div class="card"><h3>What is Arduino?</h3><p>Arduino is an open-source electronics platform used to create interactive projects, robots, automation systems and inventions.</p></div>
<div class="card">
<h3>Arduino UNO R3</h3>
<img class="hero-image" src="https://docs.arduino.cc/static/bcc9ff87c195de70ed7e0731050bd9ca/image.svg" alt="Arduino UNO R3 board" loading="lazy" onerror="this.style.display='none';document.getElementById('arduinoImageError').style.display='block';">
<div id="arduinoImageError" class="image-error">Arduino board image could not load. Check your internet connection.</div>
<p>The UNO R3 is a microcontroller board powered by the ATmega328P.</p>
<ul><li>14 digital input/output pins</li><li>6 analog input pins</li><li>6 PWM pins</li><li>USB connection</li><li>Reset button</li><li>5V and 3.3V power pins</li><li>16 MHz clock</li></ul>
</div>
<h3>Arduino UNO Main Parts</h3>
<div class="grid">
<div class="card"><h3>Microcontroller</h3><p>The main chip that processes instructions.</p></div>
<div class="card"><h3>Digital Pins</h3><p>Used to read or send HIGH and LOW signals.</p></div>
<div class="card"><h3>Analog Pins</h3><p>Read analog voltage signals from sensors.</p></div>
<div class="card"><h3>USB Port</h3><p>Connects Arduino to a computer or compatible phone.</p></div>
<div class="card"><h3>Power Jack</h3><p>Accepts suitable external power.</p></div>
<div class="card"><h3>Reset Button</h3><p>Restarts the Arduino program.</p></div>
</div>
<h3>Arduino Sensors Library</h3>
<div class="grid">
<div class="card"><h3>Ultrasonic Sensor</h3><p>Measures distance using sound waves.</p></div>
<div class="card"><h3>LDR Sensor</h3><p>Detects the intensity of light.</p></div>
<div class="card"><h3>DHT11 Sensor</h3><p>Measures temperature and humidity.</p></div>
<div class="card"><h3>PIR Sensor</h3><p>Detects movement using infrared changes.</p></div>
<div class="card"><h3>IR Sensor</h3><p>Detects objects using infrared light.</p></div>
<div class="card"><h3>Soil Moisture Sensor</h3><p>Measures moisture in soil.</p></div>
<div class="card"><h3>Joystick Module</h3><p>Detects movement in two directions.</p></div>
<div class="card"><h3>Sound Sensor</h3><p>Detects sound intensity.</p></div>
<div class="card"><h3>Flame Sensor</h3><p>Detects infrared radiation associated with flames.</p></div>
<div class="card"><h3>Gas Sensor</h3><p>Detects certain gases in the environment.</p></div>
</div>
<div class="note">Sensor voltage and connections differ by model. Check the datasheet before connecting a sensor.</div>
<div class="card"><h3>ArduinoDroid Application</h3><p>ArduinoDroid is an Android application for writing, compiling and uploading Arduino programs.</p><ul><li>Write Arduino code.</li><li>Compile programs.</li><li>Upload code to compatible boards.</li><li>Practice programming using your phone.</li></ul><p>Direct uploading requires compatible USB OTG hardware, board support and permissions.</p></div>
<div class="card"><h3>First Arduino Program: Blink LED</h3><pre><code>void setup() {
pinMode(13, OUTPUT);
}
void loop() {
digitalWrite(13, HIGH);
delay(1000);
digitalWrite(13, LOW);
delay(1000);
}</code></pre><p>This program switches the built-in LED on and off every second.</p></div>
</section>
<!-- END OF PART 1 - PASTE PART 2 BELOW THIS LINE -->
<section id="yoyo">
<h2>Yo-Yo Zone</h2>
<div class="card"><h3>Introduction to Yo-Yos</h3><p>A yo-yo is a toy consisting of two connected discs with an axle around which a string is wound. It is used for tricks, freestyle and competition.</p></div>
<h3>Types of Yo-Yos</h3>
<div class="grid">
<div class="card"><h3>Responsive</h3><p>Returns to your hand with a tug.</p></div>
<div class="card"><h3>Unresponsive</h3><p>Requires a bind trick to return.</p></div>
<div class="card"><h3>Fixed Axle</h3><p>Uses a fixed axle instead of a bearing.</p></div>
<div class="card"><h3>Looping</h3><p>Designed for repeated looping tricks.</p></div>
<div class="card"><h3>Offstring (4A)</h3><p>Yo-yo is not attached to the string.</p></div>
<div class="card"><h3>Freehand (5A)</h3><p>Uses a counterweight for tricks.</p></div>
</div>
<h3>Popular Yo-Yo Brands</h3>
<div class="grid">
<div class="card"><h3>YoYoFactory</h3><p>Performance and competition yo-yos.</p></div>
<div class="card"><h3>MagicYoyo</h3><p>Beginner and advanced yo-yos.</p></div>
<div class="card"><h3>Duncan</h3><p>Classic and modern yo-yos.</p></div>
<div class="card"><h3>Offset YoYo</h3><p>Modern performance yo-yos.</p></div>
<div class="card"><h3>C3yoyodesign</h3><p>Competition-focused yo-yos.</p></div>
<div class="card"><h3>One Drop</h3><p>Precision-machined yo-yos.</p></div>
</div>
<h3>Parts of a Yo-Yo</h3>
<div class="card"><ul><li>Body or halves – main structure.</li><li>Bearing – allows spinning.</li><li>Axle – connects the halves.</li><li>Response pads – control return response.</li><li>String – connects the yo-yo to your finger.</li><li>Hub – central axle area.</li><li>Weight rings – adjust weight distribution.</li></ul></div>
<h3>Yo-Yo Learning Levels</h3>
<div class="grid">
<div class="card"><h3>Level 1: Beginner</h3><p>Sleeper, Forward Pass and Walk the Dog.</p></div>
<div class="card"><h3>Level 2: Intermediate</h3><p>Trapeze, Brain Twister and string tricks.</p></div>
<div class="card"><h3>Level 3: Advanced</h3><p>Eli Hops, Brent Stole and complex combinations.</p></div>
<div class="card"><h3>Level 4: Competition</h3><p>Freestyle, speed, precision and combinations.</p></div>
</div>
<p class="small">These are suggested learning stages, not official universal rankings.</p>
</section>
<section id="coding">
<h2>Coding Academy</h2>
<div class="grid">
<div class="card"><h3>Python</h3><p>Learn programming, logic and automation.</p></div>
<div class="card"><h3>Web Development</h3><p>HTML, CSS and JavaScript projects.</p></div>
<div class="card"><h3>Arduino Coding</h3><p>Write programs for electronic inventions.</p></div>
</div>
</section>
<section id="research">
<h2>Research &amp; Inventions</h2>
<div class="grid">
<div class="card"><h3>New Ideas</h3><p>Document creative ideas and future inventions.</p></div>
<div class="card"><h3>Project Development</h3><p>Turn ideas into working prototypes.</p></div>
<div class="card"><h3>Experiments</h3><p>Record results and discoveries.</p></div>
<div class="card"><h3>Innovation</h3><p>Explore new solutions to practical problems.</p></div>
</div>
</section>
<section id="journal">
<h2>My Research Journal</h2>
<p>Write down your latest ideas and discoveries.</p>
<div class="card">
<h3 id="formHeading">Create a Journal Entry</h3>
<input id="title" type="text" placeholder="Project or journal title" maxlength="100">
<textarea id="note" rows="5" placeholder="Write your notes here..." maxlength="5000"></textarea>
<button onclick="saveNote()">Save Entry</button>
<button id="cancelEdit" onclick="cancelEditing()" hidden>Cancel Edit</button>
</div>
<div class="card">
<h3>Search Journal</h3>
<input id="searchNotes" type="search" placeholder="Search your saved entries..." oninput="showNotes()">
<p id="noteCount" class="small"></p>
</div>
<div id="entries" aria-live="polite"></div>
<button onclick="exportNotes()">Export Journal</button>
</section>
</main>
<footer>
<h3>BEN LOGIC</h3>
<p>Hobby &amp; Research Hub</p>
<p>Learning • Creating • Experimenting • Inventing</p>
<p class="small">Designed for curiosity and innovation.</p>
</footer>
<script>
function storageGet(k,f){try{const v=localStorage.getItem(k);return v===null?f:v;}catch(e){return f;}}
function storageSet(k,v){try{localStorage.setItem(k,v);return true;}catch(e){alert("Browser storage is unavailable or full.");return false;}}
function toggleTheme(){document.body.classList.toggle("light");const t=document.body.classList.contains("light")?"light":"dark";storageSet("benTheme",t);updateThemeButton();}
function updateThemeButton(){const b=document.getElementById("themeButton");b.textContent=document.body.classList.contains("light")?"Switch to Dark Mode":"Switch to Light Mode";}
if(storageGet("benTheme","dark")==="light"){document.body.classList.add("light");}
updateThemeButton();
function toggleMenu(){const nav=document.getElementById("navigation");const b=nav.querySelector(".menu-toggle");const o=nav.classList.toggle("open");b.setAttribute("aria-expanded",String(o));b.textContent=o?"✕ CLOSE MENU":"☰ MENU";}
document.querySelectorAll("nav a").forEach(function(l){l.addEventListener("click",function(){const nav=document.getElementById("navigation");const b=nav.querySelector(".menu-toggle");nav.classList.remove("open");b.setAttribute("aria-expanded","false");b.textContent="☰ MENU";});});
function escapeHTML(v){return String(v).replace(/[&<>"']/g,function(c){return {"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c];});}
function getNotes(){try{const n=JSON.parse(storageGet("benNotes","[]"));return Array.isArray(n)?n:[];}catch(e){return [];}}
let editingId=null;
function saveNote(){const t=document.getElementById("title").value.trim();const n=document.getElementById("note").value.trim();if(!t||!n){alert("Please enter a title and your notes.");return;}const e=getNotes();if(editingId!==null){const i=e.findIndex(function(x){return x.id===editingId;});if(i!==-1){e[i].title=t;e[i].note=n;e[i].updated=new Date().toLocaleString();}}else{e.unshift({id:Date.now().toString()+Math.random().toString(36).slice(2),title:t,note:n,date:new Date().toLocaleString()});}if(!storageSet("benNotes",JSON.stringify(e))){return;}const w=editingId!==null;clearForm();showNotes();alert(w?"Journal entry updated!":"Journal entry saved!");editingId=null;}
function clearForm(){document.getElementById("title").value="";document.getElementById("note").value="";document.getElementById("formHeading").textContent="Create a Journal Entry";document.getElementById("cancelEdit").hidden=true;}
function editNote(id){const e=getNotes().find(function(x){return x.id===id;});if(!e)return;document.getElementById("title").value=e.title;document.getElementById("note").value=e.note;document.getElementById("formHeading").textContent="Edit Journal Entry";document.getElementById("cancelEdit").hidden=false;editingId=id;document.getElementById("journal").scrollIntoView({behavior:"smooth"});}
function cancelEditing(){editingId=null;clearForm();}
function deleteNote(id){if(!confirm("Delete this entry?"))return;const e=getNotes().filter(function(x){return x.id!==id;});storageSet("benNotes",JSON.stringify(e));if(editingId===id){cancelEditing();}showNotes();}
function showNotes(){const box=document.getElementById("entries");const c=document.getElementById("noteCount");const q=(document.getElementById("searchNotes").value||"").toLowerCase().trim();let e=getNotes();if(q){e=e.filter(function(x){return (x.title+" "+x.note).toLowerCase().includes(q);});}c.textContent=e.length+" entr"+(e.length===1?"y":"ies")+" found";if(e.length===0){box.innerHTML='<div class="empty">'+(q?"No entries match your search.":"No journal entries yet. Write your first one above!")+'</div>';return;}box.innerHTML=e.map(function(x){return '<div class="card journal-entry"><h3>'+escapeHTML(x.title)+'</h3><p>'+escapeHTML(x.note).replace(/\n/g,"<br>")+'</p><p class="small">'+escapeHTML(x.updated?("Updated: "+x.updated):("Created: "+x.date))+'</p><button onclick="editNote(\''+x.id+'\')">Edit</button> <button onclick="deleteNote(\''+x.id+'\')">Delete</button></div>';}).join("");}
function exportNotes(){const e=getNotes();if(e.length===0){alert("No entries to export.");return;}const t=e.map(function(x){return "TITLE: "+x.title+"\nDATE: "+(x.date||"")+"\n"+x.note+"\n\n---\n";}).join("\n");const b=new Blob([t],{type:"text/plain"});const a=document.createElement("a");a.href=URL.createObjectURL(b);a.download="ben-logic-journal.txt";a.click();URL.revokeObjectURL(a.href);}
showNotes();
</script>
</body>
</html>

