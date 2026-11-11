# Hobby-Journal-
a website about hobbies 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Hobby Journal | Arduino • Yo-Yo • RC Models</title>
    <style>
        * { box-sizing: border-box; }
        body { font-family: system-ui, sans-serif; margin: 0; background: #f4f4f5; color: #222; line-height: 1.6; }
        body.dark { background: #111; color: #eee; }
        body.dark section, body.dark .card { background: #1e1e1e; color: #eee; border-color: #333; }
        header { background: #111; color: white; padding: 2.5rem 1rem; text-align: center; }
        header h1 { margin: 0; font-size: 2rem; }
        header p { color: #bbb; }
        nav { display: flex; justify-content: center; flex-wrap: wrap; gap: 0.4rem; background: #222; padding: 0.6rem; position: sticky; top: 0; z-index: 10; }
        nav a { color: white; padding: 0.6rem 1.1rem; text-decoration: none; border-radius: 999px; }
        nav a:hover { background: #444; }
        nav button { margin-left: 0.5rem; border: 0; border-radius: 999px; padding: 0.6rem 1rem; cursor: pointer; }
        main { max-width: 960px; margin: 0 auto; padding: 1.5rem 1rem; }
        section { background: white; padding: 1.5rem; border-radius: 14px; margin-bottom: 1.5rem; box-shadow: 0 2px 12px rgba(0,0,0,0.06); }
        .tag { background: #eee; padding: 0.2rem 0.8rem; border-radius: 999px; font-size: 0.85rem; }
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 1rem; margin-top: 1rem; }
        .card { border: 1px solid #eee; border-radius: 12px; padding: 1rem; }
        .card img { width: 100%; height: 140px; object-fit: cover; border-radius: 8px; background: #ddd; }
        .progress { height: 8px; background: #eee; border-radius: 999px; overflow: hidden; margin-top: 0.5rem; }
        .progress div { height: 100%; background: #22c55e; }
        input, textarea, select { width: 100%; padding: 0.7rem; border: 1px solid #ddd; border-radius: 8px; margin-top: 0.5rem; font: inherit; }
        button.primary { background: #111; color: white; border: 0; padding: 0.7rem 1.2rem; border-radius: 8px; cursor: pointer; margin-top: 0.6rem; }
        footer { text-align: center; color: #888; padding: 2rem 1rem; }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to My Hobby Journey 🚀</h1>
        <p>Arduino • Yo-Yo • RC Models — Build. Practice. Repeat.</p>
        <p id="greeting">Hello, Maker!</p>
    </header>

    <nav>
        <a href="#home">Home</a>
        <a href="#arduino">⚡ Arduino</a>
        <a href="#yoyo">🪀 Yo-Yo</a>
        <a href="#rc">🚗 RC Models</a>
        <a href="#gallery">📸 Gallery</a>
        <a href="#log">📝 My Log</a>
        <button onclick="toggleDark()">🌙 Dark Mode</button>
    </nav>

    <main>
        <section id="home">
            <span class="tag">About Me</span>
            <h2>Hi, I'm learning by doing</h2>
            <p>This is my journal. I don't just watch tutorials — I build, I fail, I fix, I try again.</p>
            <div class="grid">
                <div class="card"><h3>⚡ Arduino</h3><p>Circuits, sensors & code</p><p><b>Projects:</b> 3</p></div>
                <div class="card"><h3>🪀 Yo-Yo</h3><p>Skill, patience & flow</p><p><b>Tricks learned:</b> 4</p></div>
                <div class="card"><h3>🚗 RC Models</h3><p>Speed, tuning & crashes</p><p><b>Cars:</b> 2</p></div>
            </div>
        </section>

        <section id="arduino">
            <span class="tag">Electronics</span>
            <h2>Arduino Projects</h2>
            <p>My brain for electronics. I learn one sensor at a time.</p>
            <div class="grid">
                <div class="card"><h3>💡 Blink LED</h3><p>First project ever.</p><p>✅ Done</p><div class="progress"><div style="width:100%"></div></div></div>
                <div class="card"><h3>🌡️ Temp + LCD</h3><p>DHT11 shows temp on screen.</p><p>🔧 In Progress</p><div class="progress"><div style="width:60%"></div></div></div>
                <div class="card"><h3>🤖 Line Follower</h3><p>Car that follows black line.</p><p>💡 Idea</p><div class="progress"><div style="width:10%"></div></div></div>
            </div>
        </section>

        <section id="yoyo">
            <span class="tag">Skill Toy</span>
            <h2>Yo-Yo Tricks</h2>
            <p>Looks easy on YouTube. It's not. 😅</p>
            <div class="grid">
                <div class="card"><h3>Sleeper</h3><p>Hold 25 seconds</p><p>✅ Done</p></div>
                <div class="card"><h3>Trapeze</h3><p>Landing 7/10 times</p><p>🔧 Practicing</p></div>
                <div class="card"><h3>Bind Return</h3><p>For unresponsive yoyo</p><p>🔧 Practicing</p></div>
                <div class="card"><h3>Rock the Baby</h3><p>Classic trick</p><p>💡 Next</p></div>
            </div>
        </section>

        <section id="rc">
            <span class="tag">RC Models</span>
            <h2>RC Models</h2>
            <p>Fast cars, broken parts, happy wallet — no, sad wallet.</p>
            <div class="grid">
                <div class="card"><h3>1:10 Drift Car</h3><p>New tyres, better steering. Drifts clean now.</p><p>✅ Running</p></div>
                <div class="card"><h3>RC Crawler</h3><p>For rocks and off-road.</p><p>💡 Wishlist</p></div>
                <div class="card"><h3>🛠️ Repair Log</h3><p>Broken arm: 2x<br>Broken wheel: 1x<br>Lesson: Don't drift into wall</p></div>
            </div>
        </section>

        <section id="gallery">
            <span class="tag">Photos</span>
            <h2>Gallery</h2>
            <p>Replace these with your own photos later.</p>
            <div class="grid">
                <div class="card"><img alt="Arduino photo"><p>Arduino setup</p></div>
                <div class="card"><img alt="Yo-Yo photo"><p>Yo-Yo practice</p></div>
                <div class="card"><img alt="RC car photo"><p>RC car</p></div>
            </div>
        </section>

        <section id="log">
            <h2>📝 My Daily Log</h2>
            <p>What did you do today? It saves in your browser, even if you close the page.</p>
            <select id="logHobby">
                <option>Arduino</option><option>Yo-Yo</option><option>RC Models</option>
            </select>
            <input id="logTitle" placeholder="Title: e.g. Fixed temp sensor">
            <textarea id="logText" rows="3" placeholder="What happened? What did you learn?"></textarea>
            <button class="primary" onclick="saveLog()">Save Entry</button>
            <button class="primary" onclick="clearLogs()" style="background:#dc2626">Clear All</button>
            <div id="entries"></div>
        </section>
    </main>

    <footer>
        <p>Made with ❤️ by me • My Hobby Journal • 2026</p>
        <p><a href="#home">Back to top ↑</a></p>
    </footer>

    <script>
        // 1. Greeting based on time
        const hour = new Date().getHours();
        let greet = "Hello, Maker!";
        if (hour < 12) greet = "Good morning, Maker! ☀️";
        else if (hour < 18) greet = "Good afternoon, Maker! ⚡";
        else greet = "Good evening, Maker! 🌙";
        document.getElementById('greeting').textContent = greet;

        // 2. Dark mode
        function toggleDark() {
            document.body.classList.toggle('dark');
        }

        // 3. Save log in browser
        function loadLogs() {
            const logs = JSON.parse(localStorage.getItem('hobbyLogs') || '[]');
            document.getElementById('entries').innerHTML = logs.map(l =>
                `<div class="card" style="margin-top:1rem"><b>[${l.hobby}] ${l.title}</b><br><small>${l.date}</small><p>${l.text}</p></div>`
            ).join('');
        }
        function saveLog() {
            const hobby = document.getElementById('logHobby').value;
            const title = document.getElementById('logTitle').value.trim();
            const text = document.getElementById('logText').value.trim();
            if (!title || !text) return alert('Add title + notes first');
            const logs = JSON.parse(localStorage.getItem('hobbyLogs') || '[]');
            logs.unshift({ hobby, title, text, date: new Date().toLocaleString() });
            localStorage.setItem('hobbyLogs', JSON.stringify(logs));
            document.getElementById('logTitle').value = '';
            document.getElementById('logText').value = '';
            loadLogs();
        }
        function clearLogs() {
            if (confirm('Delete all log entries?')) {
                localStorage.removeItem('hobbyLogs');
                loadLogs();
            }
        }
        loadLogs();
    </script>
</body>
</html>
