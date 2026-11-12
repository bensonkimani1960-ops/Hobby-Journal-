
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BEN LOGIC | Hobby & Research Hub</title>

<style>
:root {
  --bg: #081426;
  --card: #12243d;
  --text: #f4f7fb;
  --accent: #00aaff;
  --muted: #b5c5d8;
}

body.light {
  --bg: #edf3f9;
  --card: #ffffff;
  --text: #142338;
  --accent: #0077cc;
  --muted: #52657a;
}

* {
  box-sizing: border-box;
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.6;
}

header {
  text-align: center;
  padding: 45px 15px;
  background: linear-gradient(135deg, #06101f, #064b82);
}

header h1 {
  font-size: 42px;
  margin: 0;
  letter-spacing: 3px;
}

header p {
  color: #d5eaff;
}

nav {
  background: #06101f;
  padding: 14px;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 16px;
  position: sticky;
  top: 0;
  z-index: 10;
}

nav a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

nav a:hover {
  color: var(--accent);
}

button {
  background: var(--accent);
  color: white;
  border: none;
  padding: 10px 16px;
  border-radius: 7px;
  cursor: pointer;
  font-weight: bold;
}

button:hover {
  opacity: 0.85;
}

.container {
  max-width: 1100px;
  margin: auto;
  padding: 25px 16px;
}

section {
  margin-bottom: 45px;
  scroll-margin-top: 80px;
}

h2 {
  color: var(--accent);
  border-bottom: 2px solid var(--accent);
  padding-bottom: 8px;
}

h3 {
  color: var(--accent);
}

.card {
  background: var(--card);
  padding: 20px;
  margin: 15px 0;
  border-radius: 12px;
  box-shadow: 0 4px 12px #0003;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 15px;
}

img {
  max-width: 100%;
  border-radius: 10px;
}

pre {
  background: #030b16;
  color: #9be7ff;
  padding: 15px;
  border-radius: 8px;
  overflow-x: auto;
}

code {
  font-family: monospace;
}

table {
  width: 100%;
  border-collapse: collapse;
}

td, th {
  border: 1px solid var(--muted);
  padding: 10px;
  text-align: left;
}

input, textarea {
  width: 100%;
  padding: 12px;
  margin: 8px 0;
  border-radius: 6px;
  border: 1px solid #8b9bb0;
  font: inherit;
}

footer {
  text-align: center;
  padding: 25px;
  background: #06101f;
  color: white;
}
</style>
</head>

<body>

<header>
  <h1>BEN LOGIC</h1>
  <p>Hobby • Technology • Engineering • Research • Innovation</p>
  <button onclick="toggleTheme()">Change Theme</button>
</header>

<nav>
  <a href="#home">Home</a>
  <a href="#arduino">Arduino</a>
  <a href="#sensors">Sensors</a>
  <a href="#arduinodroid">ArduinoDroid</a>
  <a href="#rc">RC Models</a>
  <a href="#yoyo">Yo-Yo</a>
  <a href="#coding">Coding</a>
  <a href="#research">Research</a>
  <a href="#journal">Journal</a>
</nav>

<main class="container">

<section id="home">
  <h2>Welcome to My Hobby Hub</h2>
  <div class="card">
    <p>
      Welcome to BEN LOGIC, a personal website for learning,
      experimenting, building and researching technology.
    </p>
    <p>
      Explore electronics, Arduino projects, RC engineering,
      yo-yo tricks, programming and creative inventions.
    </p>
  </div>

  <div class="grid">
    <div class="card"><h3>Arduino</h3><p>Electronics and microcontrollers.</p></div>
    <div class="card"><h3>RC Engineering</h3><p>Remote-controlled vehicles and machines.</p></div>
    <div class="card"><h3>Yo-Yo</h3><p>Tricks, equipment and skills.</p></div>
    <div class="card"><h3>Coding</h3><p>Python, HTML, CSS and Arduino programming.</p></div>
  </div>
</section>

<section id="arduino">
  <h2>Arduino Laboratory</h2>

  <div class="card">
    <h3>What is Arduino?</h3>
    <p>
      Arduino is an open-source electronics platform used to build
      interactive projects. It can read information from sensors
      and control devices such as LEDs, motors and displays.
    </p>
  </div>

  <div class="card">
    <h3>Arduino UNO R3</h3>
    <img
      src="https://docs.arduino.cc/static/bcc9ff87c195de70ed7e0731050bd9ca/image.svg"
      alt="Arduino UNO board"
      loading="lazy"
    >
    <p>
      The Arduino UNO R3 is a popular beginner-friendly
      microcontroller board.
    </p>

    <table>
      <tr><th>Feature</th><th>Description</th></tr>
      <tr><td>Microcontroller</td><td>ATmega328P</td></tr>
      <tr><td>Operating voltage</td><td>5V</td></tr>
      <tr><td>Digital pins</td><td>14</td></tr>
      <tr><td>PWM pins</td><td>6</td></tr>
      <tr><td>Analog inputs</td><td>6</td></tr>
      <tr><td>USB connection</td><td>Programming and power</td></tr>
    </table>
  </div>

  <div class="card">
    <h3>Main Parts of Arduino UNO</h3>
    <ul>
      <li><b>Microcontroller:</b> The brain of the board.</li>
      <li><b>Digital pins:</b> Read or control digital signals.</li>
      <li><b>Analog pins:</b> Read changing voltage levels.</li>
      <li><b>USB port:</b> Connects the board to a computer.</li>
      <li><b>Power jack:</b> Supplies external power.</li>
      <li><b>Reset button:</b> Restarts the program.</li>
      <li><b>5V and 3.3V pins:</b> Provide regulated voltage.</li>
      <li><b>GND:</b> Ground connection.</li>
    </ul>
  </div>

  <div class="card">
    <h3>First Arduino Program: Blink LED</h3>
    <pre><code>void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);
  delay(1000);

  digitalWrite(13, LOW);
  delay(1000);
}</code></pre>
    <p>This program switches the built-in LED on and off every second.</p>
  </div>
</section>

<section id="sensors">
  <h2>Arduino Sensors Library</h2>

  <div class="card">
    <p>
      Sensors detect changes in the environment and send information
      to the Arduino.
    </p>
  </div>

  <div class="grid">
    <div class="card"><h3>HC-SR04</h3><p>Measures distance using ultrasonic sound waves.</p></div>
    <div class="card"><h3>LDR</h3><p>Detects light intensity.</p></div>
    <div class="card"><h3>DHT11</h3><p>Measures temperature and humidity.</p></div>
    <div class="card"><h3>PIR</h3><p>Detects movement from people or animals.</p></div>
    <div class="card"><h3>IR Sensor</h3><p>Detects infrared light and nearby objects.</p></div>
    <div class="card"><h3>Soil Moisture</h3><p>Measures moisture in soil.</p></div>
    <div class="card"><h3>Joystick</h3><p>Provides directional control.</p></div>
    <div class="card"><h3>Sound Sensor</h3><p>Detects sound levels.</p></div>
    <div class="card"><h3>Flame Sensor</h3><p>Detects certain infrared signals from flames.</p></div>
    <div class="card"><h3>Gas Sensor</h3><p>Detects certain gases in the air.</p></div>
    <div class="card"><h3>Touch Sensor</h3><p>Detects physical touch.</p></div>
    <div class="card"><h3>Accelerometer</h3><p>Measures acceleration and tilt.</p></div>
    <div class="card"><h3>Water Level</h3><p>Detects water level.</p></div>
    <div class="card"><h3>Magnetic Sensor</h3><p>Detects magnetic fields.</p></div>
  </div>
</section>

<section id="arduinodroid">
  <h2>ArduinoDroid App</h2>

  <div class="card">
    <h3>What is ArduinoDroid?</h3>
    <p>
      ArduinoDroid is an Android application that allows you to
      write, compile and upload Arduino programs using a phone
      or tablet.
    </p>

    <h3>What can you do with it?</h3>
    <ul>
      <li>Write Arduino C/C++ code.</li>
      <li>Compile programs.</li>
      <li>Upload code to compatible Arduino boards.</li>
      <li>Work on electronics projects using an Android device.</li>
    </ul>

    <h3>Basic connection steps</h3>
    <ol>
      <li>Install ArduinoDroid from a trusted app source.</li>
      <li>Connect your Arduino UNO using a suitable USB OTG adapter.</li>
      <li>Open ArduinoDroid.</li>
      <li>Write or open your program.</li>
      <li>Compile and upload the code.</li>
    </ol>
    <p>
      Some phones and boards require compatible USB drivers,
      cables and permissions.
    </p>
  </div>
</section>

<section id="rc">
  <h2>RC Engineering</h2>

  <div class="card">
    <h3>What is RC?</h3>
    <p>
      RC means Radio Control. It allows you to control a vehicle
      or machine wirelessly using a transmitter and receiver.
    </p>
  </div>

  <div class="grid">
    <div class="card"><h3>RC Cars</h3><p>Remote-controlled cars.</p></div>
    <div class="card"><h3>RC Tipper Trucks</h3><p>Vehicles with lifting cargo beds.</p></div>
    <div class="card"><h3>DC Motors</h3><p>Convert electrical energy into rotation.</p></div>
    <div class="card"><h3>Servo Motors</h3><p>Provide controlled angular movement.</p></div>
    <div class="card"><h3>Gears</h3><p>Transfer motion and change speed or torque.</p></div>
    <div class="card"><h3>RC Transmitters</h3><p>Send control signals to the receiver.</p></div>
  </div>

  <div class="card">
    <h3>My Engineering Goals</h3>
    <ul>
      <li>Build an RC tipper truck.</li>
      <li>Combine Arduino with RC control.</li>
      <li>Experiment with motors and gears.</li>
      <li>Build mechanical inventions using LEGO parts.</li>
    </ul>
  </div>
</section>

<section id="yoyo">
  <h2>Yo-Yo Zone</h2>

  <div class="card">
    <h3>What is a Yo-Yo?</h3>
    <p>
      A yo-yo is a toy made of two connected halves with an axle
      between them. A string allows it to spin, return or perform tricks.
    </p>
  </div>

  <div class="card">
    <h3>Types of Yo-Yos</h3>
    <ul>
      <li><b>Responsive:</b> Returns to your hand with a tug.</li>
      <li><b>Unresponsive:</b> Needs a bind to return to your hand.</li>
      <li><b>Fixed Axle:</b> Uses a fixed axle instead of a ball bearing.</li>
      <li><b>Looping:</b> Designed for repeated looping tricks.</li>
      <li><b>Offstring (4A):</b> The string is not attached to the yo-yo.</li>
      <li><b>Freehand (5A):</b> Uses a counterweight attached to the string.</li>
    </ul>
  </div>

  <div class="card">
    <h3>Popular Yo-Yo Brands</h3>
    <ul>
      <li>YoYoFactory</li>
      <li>MagicYoyo</li>
      <li>Duncan</li>
      <li>Offset YoYo</li>
      <li>C3yoyodesign</li>
      <li>One Drop</li>
      <li>Yoyofriends</li>
    </ul>
  </div>

  <div class="card">
    <h3>Parts of a Yo-Yo</h3>
    <ul>
      <li><b>Body halves:</b> The two main sides.</li>
      <li><b>Bearing:</b> Allows the yo-yo to spin freely.</li>
      <li><b>Axle:</b> Connects the two halves.</li>
      <li><b>Response pads:</b> Help the yo-yo return when needed.</li>
      <li><b>String:</b> Used to perform tricks.</li>
      <li><b>Hub:</b> The central area around the axle.</li>
      <li><b>Weight rings:</b> Add weight to selected models.</li>
    </ul>
  </div>

  <div class="card">
    <h3>Yo-Yo Skill Levels</h3>

    <h4>Beginner</h4>
    <ul>
      <li>Gravity Pull</li>
      <li>Forward Pass</li>
      <li>Walk the Dog</li>
      <li>Sleeper</li>
    </ul>

    <h4>Intermediate</h4>
    <ul>
      <li>Trapeze</li>
      <li>Brain Twister</li>
      <li>Split Bottom Mount</li>
      <li>Man on the Flying Trapeze</li>
    </ul>

    <h4>Advanced</h4>
    <ul>
      <li>Eli Hops</li>
      <li>Brent Stole</li>
      <li>Complex combinations</li>
    </ul>

    <h4>Competition</h4>
    <ul>
      <li>Freestyle routines</li>
      <li>Precision tricks</li>
      <li>Speed and execution</li>
    </ul>

    <p><i>These are suggested learning stages, not official universal rankings.</i></p>
  </div>
</section>

<section id="coding">
  <h2>Coding Academy</h2>

  <div class="grid">
    <div class="card">
      <h3>Python</h3>
      <p>A beginner-friendly programming language used for automation, applications and data.</p>
    </div>

    <div class="card">
      <h3>HTML</h3>
      <p>Creates the structure and content of websites.</p>
    </div>

    <div class="card">
      <h3>CSS</h3>
      <p>Controls website colors, layouts and appearance.</p>
    </div>

    <div class="card">
      <h3>JavaScript</h3>
      <p>Adds interactive features to websites.</p>
    </div>

    <div class="card">
      <h3>Arduino C/C++</h3>
      <p>Used to program Arduino boards and electronic projects.</p>
    </div>
  </div>
</section>

<section id="research">
  <h2>Research & Inventions</h2>

  <div class="card">
    <h3>My Research Areas</h3>
    <ul>
      <li>Robotics and automation.</li>
      <li>Arduino electronics.</li>
      <li>RC engineering.</li>
      <li>Mechanical design.</li>
      <li>3D modelling and printing.</li>
      <li>New inventions and experiments.</li>
    </ul>
  </div>

  <div class="card">
    <h3>Innovation Mindset</h3>
    <p>
      Learn something, experiment with it, identify a problem,
      design a solution and build a working prototype.
    </p>
  </div>
</section>

<section id="journal">
  <h2>Research Journal</h2>

  <div class="card">
    <h3>Write a New Note</h3>

    <input id="noteTitle" type="text" placeholder="Enter note title">

    <textarea id="noteText" rows="5"
      placeholder="Write your research, project idea or discovery..."></textarea>

    <button onclick="saveNote()">Save Note</button>

    <h3>My Saved Notes</h3>
    <div id="notes"></div>
  </div>
</section>

</main>

<footer>
  <p>BEN LOGIC | Hobby & Research Hub</p>
  <p>Learn • Build • Experiment • Innovate</p>
</footer>

<script>
function toggleTheme() {
  document.body.classList.toggle("light");

  const theme = document.body.classList.contains("light")
    ? "light"
    : "dark";

  localStorage.setItem("benTheme", theme);
}

if (localStorage.getItem("benTheme") === "light") {
  document.body.classList.add("light");
}

function escapeHTML(text) {
  return String(text).replace(/[&<>"']/g, function(char) {
    return {
      "&": "&amp;",
      "<": "&lt;",
      ">": "&gt;",
      '"': "&quot;",
      "'": "&#039;"
    }[char];
  });
}

function getNotes() {
  try {
    return JSON.parse(localStorage.getItem("benNotes")) || [];
  } catch (error) {
    return [];
  }
}

function saveNote() {
  const title = document.getElementById("noteTitle").value.trim();
  const content = document.getElementById("noteText").value.trim();

  if (!title || !content) {
    alert("Please enter both a title and note.");
    return;
  }

  const notes = getNotes();

  notes.unshift({
    id: Date.now(),
    title: title,
    content: content,
    date: new Date().toLocaleString()
  });

  localStorage.setItem("benNotes", JSON.stringify(notes));

  document.getElementById("noteTitle").value = "";
  document.getElementById("noteText").value = "";

  showNotes();
}

function showNotes() {
  const notes = getNotes();
  const container = document.getElementById("notes");

  if (notes.length === 0) {
    container.innerHTML = "<p>No notes saved yet.</p>";
    return;
  }

  container.innerHTML = notes.map(function(note) {
    return `
      <div class="card">
        <h3>${escapeHTML(note.title)}</h3>
        <p>${escapeHTML(note.content).replace(/\n/g, "<br>")}</p>
        <small>${escapeHTML(note.date)}</small>
        <br><br>
        <button onclick="deleteNote(${note.id})">Delete</button>
      </div>
    `;
  }).join("");
}

function deleteNote(id) {
  if (!confirm("Are you sure you want to delete this note?")) {
    return;
  }

  const notes = getNotes().filter(function(note) {
    return note.id !== id;
  });

  localStorage.setItem("benNotes", JSON.stringify(notes));
  showNotes();
}

showNotes();
</script>

</body>
</html>
