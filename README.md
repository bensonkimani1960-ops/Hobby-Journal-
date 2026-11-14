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
<a href="#home">Home</a><a href="#arduino">Arduino</a><a href="#rc">RC Engineering</a><a href="#web">Web Development</a><a href="#yoyo">Yo-Yo</a><a href="#coding">Coding</a><a href="#research">Research</a><a href="#journal">Journal</a>
</nav>
<main class="container">
<section id="intro">
<h2>My Hobby Journey</h2>
<div class="card"><p>I am passionate about technology, electronics, engineering, coding and creative inventions. This is where I document my projects, experiments and learning journey.</p></div>
<div class="grid">
<div class="card"><h3>Arduino</h3><p>Electronics, sensors and microcontrollers.</p></div>
<div class="card"><h3>RC Engineering</h3><p>Remote-controlled vehicles and machines.</p></div>
<div class="card"><h3>Web Development</h3><p>HTML, CSS and JavaScript websites.</p></div>
<div class="card"><h3>Yo-Yo</h3><p>Tricks, equipment and skill development.</p></div>
<div class="card"><h3>Coding</h3><p>Python, HTML, CSS and Arduino programming.</p></div>
</div>
</section>

<section id="rc">
<h2>RC Engineering - RC Cars</h2>
<div class="card"><h3>What is an RC Car?</h3><p>An RC car is a remote-controlled car that you drive with a transmitter or your phone. The car has a receiver that listens to your commands and tells the motors and steering what to do. It is the best project to learn motors, batteries, steering, and Arduino coding.</p></div>

<div class="card">
<h3>My Bluetooth RC Car</h3>
<img class="hero-image" src="rc-car.jpg" alt="Finished Arduino Bluetooth RC Car">
<p>This is the finished car — Arduino UNO, L298N motor driver, HC-05 Bluetooth module, battery pack and 4 wheels on a blue chassis.</p>
</div>

<h3>Types of RC Cars</h3>
<div class="grid">
<div class="card"><h3>On-Road / Drift Car</h3><p>Fast on smooth ground. Good for drifting and racing on tarmac.</p></div>
<div class="card"><h3>Off-Road Buggy</h3><p>For grass, dirt and rough ground. Strong suspension.</p></div>
<div class="card"><h3>Monster Truck</h3><p>Big wheels. Jumps over obstacles. Very powerful.</p></div>
<div class="card"><h3>Crawler</h3><p>Slow but climbs over rocks. Very strong torque.</p></div>
</div>

<h3>Main Parts of an RC Car</h3>
<div class="card"><ul>
<li><strong>Chassis:</strong> The frame. Holds everything together. Can be plastic, metal or Lego.</li>
<li><strong>Motor:</strong> Makes wheels spin. Brushed = cheap for beginners. Brushless = fast and powerful.</li>
<li><strong>ESC / Motor Driver:</strong> Controls speed of motor. Like accelerator in a real car. In Arduino projects we use L298N.</li>
<li><strong>Servo Motor:</strong> Controls steering. Turns front wheels left and right.</li>
<li><strong>Battery:</strong> NiMH = safe and cheap. LiPo = powerful and light, needs careful charging.</li>
<li><strong>Transmitter + Receiver:</strong> Transmitter is remote in your hand. Receiver is inside car. In this project your phone is the transmitter via Bluetooth.</li>
<li><strong>Wheels + Suspension:</strong> Bigger wheels = better for off-road. Suspension helps over bumps.</li>
</ul></div>

<h3>How an RC Car Works</h3>
<div class="card"><ol>
<li>You push throttle on remote / phone</li>
<li>Transmitter sends radio / Bluetooth signal</li>
<li>Receiver in car gets the signal</li>
<li>Motor driver tells motor how fast to spin</li>
<li>Servo turns the steering</li>
</ol></div>

<div class="card">
<h3>Blueprint - RC Car Design</h3>
<img class="hero-image" src="rc-car-blueprint.jpg" alt="Arduino Bluetooth RC Car Blueprint">
<p>Top view and side view. This shows where every part goes on the chassis. Chassis size: 150mm x 100mm. Wheel diameter: 50mm.</p>
<ul>
<li>Arduino UNO in the middle</li>
<li>L298N motor driver next to Arduino</li>
<li>HC-05 Bluetooth module at the front</li>
<li>Battery pack at the rear</li>
<li>DC motors on left and right</li>
</ul>
</div>

<div class="card"><h3>PROJECT: Build Your Own Bluetooth Arduino RC Car</h3>
<p><strong>Electronics needed:</strong></p>
<ul><li>Arduino UNO</li><li>L298N motor driver module</li><li>2x DC motors + wheels + chassis (or 4x motors)</li><li>HC-05 Bluetooth module</li><li>9V battery / 2x Li-ion batteries + battery holder</li><li>Breadboard and jumper wires</li><li>Phone with Bluetooth RC Controller app</li></ul>

<h3>Circuit Diagram</h3>
<img class="hero-image" src="rc-car-circuit.jpg" alt="RC Car Circuit Diagram">
<p><strong>Wire Colours:</strong> Red = Power, Black = Ground, Yellow = Signal (TX/RX/ENA), Blue = Signal (IN1-IN4), Green = Signal (ENB)</p>
<p><strong>Circuit Connections:</strong></p>
<ul><li>L298N IN1 to Arduino Pin 2</li><li>L298N IN2 to Arduino Pin 3</li><li>L298N IN3 to Arduino Pin 4</li><li>L298N IN4 to Arduino Pin 5</li><li>L298N ENA to Arduino Pin 9 (speed left)</li><li>L298N ENB to Arduino Pin 10 (speed right)</li><li>L298N 12V to Battery +</li><li>L298N GND to Battery - AND Arduino GND</li><li>L298N OUT1, OUT2 to Left Motor</li><li>L298N OUT3, OUT4 to Right Motor</li><li>HC-05 VCC to 5V</li><li>HC-05 GND to GND</li><li>HC-05 TX to Arduino Pin 0 (RX)</li><li>HC-05 RX to Arduino Pin 1 (TX)</li></ul>
<p class="small">Tip: Disconnect HC-05 TX/RX wires when uploading code, then reconnect them.</p>

<p><strong>Code:</strong></p>
<pre><code>// BEN LOGIC Bluetooth RC Car
// Use App: Bluetooth RC Controller
// F = Forward, B = Backward, L = Left, R = Right, S = Stop

char command;
int IN1 = 2;
int IN2 = 3;
int IN3 = 4;
int IN4 = 5;
int ENA = 9;
int ENB = 10;

void setup() {
  Serial.begin(9600);
  pinMode(IN1, OUTPUT);
  pinMode(IN2, OUTPUT);
  pinMode(IN3, OUTPUT);
  pinMode(IN4, OUTPUT);
  pinMode(ENA, OUTPUT);
  pinMode(ENB, OUTPUT);
  stopCar();
}

void loop() {
  if (Serial.available() > 0) {
    command = Serial.read();
  }

  if (command == 'F') {
    forward();
  } else if (command == 'B') {
    backward();
  } else if (command == 'L') {
    turnLeft();
  } else if (command == 'R') {
    turnRight();
  } else if (command == 'S') {
    stopCar();
  }
}

void forward() {
  digitalWrite(IN1, HIGH);
  digitalWrite(IN2, LOW);
  digitalWrite(IN3, HIGH);
  digitalWrite(IN4, LOW);
  analogWrite(ENA, 200);
  analogWrite(ENB, 200);
}

void backward() {
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, HIGH);
  digitalWrite(IN3, LOW);
  digitalWrite(IN4, HIGH);
  analogWrite(ENA, 200);
  analogWrite(ENB, 200);
}

void turnLeft() {
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, HIGH);
  digitalWrite(IN3, HIGH);
  digitalWrite(IN4, LOW);
  analogWrite(ENA, 180);
  analogWrite(ENB, 180);
}

void turnRight() {
  digitalWrite(IN1, HIGH);
  digitalWrite(IN2, LOW);
  digitalWrite(IN3, LOW);
  digitalWrite(IN4, HIGH);
  analogWrite(ENA, 180);
  analogWrite(ENB, 180);
}

void stopCar() {
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, LOW);
  digitalWrite(IN3, LOW);
  digitalWrite(IN4, LOW);
  analogWrite(ENA, 0);
  analogWrite(ENB, 0);
}</code></pre>
<p><strong>How to drive it:</strong> Pair phone to HC-05 (password 1234 or 0000), open Bluetooth RC Controller app, connect, then use arrow buttons to drive.</p></div>

<div class="card"><h3>RC Car Upgrades</h3><ul>
<li><strong>Faster:</strong> Use stronger battery and brushless motor</li>
<li><strong>Stronger:</strong> Use metal gears and bigger wheels</li>
<li><strong>Smarter:</strong> Add ultrasonic sensor for obstacle avoidance</li>
<li><strong>Longer range:</strong> Use NRF24L01 radio module instead of Bluetooth</li>
</ul></div>

<div class="note"><strong>My goal:</strong> Combine Arduino, Lego, motors and RC technology to build original machines.</div>
</section>
<!-- END OF PART 1A - PASTE PART 1B BELOW -->

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

<h3>Arduino Projects</h3>

<div class="card"><h3>Project 1: Fade - LED Brightness Control</h3>
<p><strong>Electronics needed:</strong></p>
<ul><li>Arduino UNO</li><li>1x LED</li><li>1x 220 ohm resistor</li><li>Breadboard and jumper wires</li></ul>
<p><strong>Circuit Diagram:</strong></p>
<ul><li>LED long leg (positive) to Pin 9 through 220 ohm resistor</li><li>LED short leg (negative) to GND</li></ul>
<p><strong>Code:</strong></p>
<pre><code>int ledPin = 9;
void setup() {
  pinMode(ledPin, OUTPUT);
}
void loop() {
  for (int b = 0; b <= 255; b++) {
    analogWrite(ledPin, b);
    delay(10);
  }
  for (int b = 255; b >= 0; b--) {
    analogWrite(ledPin, b);
    delay(10);
  }
}</code></pre>
<p>The LED slowly gets brighter, then slowly fades out using PWM.</p></div>

<div class="card"><h3>Project 2: Servo Motor Control</h3>
<p><strong>Electronics needed:</strong></p>
<ul><li>Arduino UNO</li><li>1x SG90 servo motor</li><li>Jumper wires</li></ul>
<p><strong>Circuit Diagram:</strong></p>
<ul><li>Servo Brown / Black wire to GND</li><li>Servo Red wire to 5V</li><li>Servo Orange / Yellow wire to Pin 9</li></ul>
<p><strong>Code:</strong></p>
<pre><code>#include &lt;Servo.h&gt;
Servo myServo;
void setup() {
  myServo.attach(9);
}
void loop() {
  myServo.write(0);
  delay(1000);
  myServo.write(90);
  delay(1000);
  myServo.write(180);
  delay(1000);
  myServo.write(90);
  delay(1000);
}</code></pre>
<p>The servo moves from 0 to 90 to 180 degrees and back.</p></div>

<div class="card"><h3>Project 3: Liquid Crystal Display - LCD 16x2</h3>
<p><strong>Electronics needed:</strong></p>
<ul><li>Arduino UNO</li><li>1x LCD 16x2 with I2C module</li><li>Jumper wires</li></ul>
<p><strong>Circuit Diagram:</strong></p>
<ul><li>LCD VCC to 5V</li><li>LCD GND to GND</li><li>LCD SDA to A4</li><li>LCD SCL to A5</li></ul>
<p><strong>Code:</strong></p>
<pre><code>#include &lt;Wire.h&gt;
#include &lt;LiquidCrystal_I2C.h&gt;
LiquidCrystal_I2C lcd(0x27, 16, 2);
void setup() {
  lcd.init();
  lcd.backlight();
  lcd.setCursor(0, 0);
  lcd.print("BEN LOGIC");
  lcd.setCursor(0, 1);
  lcd.print("Arduino Lab");
}
void loop() {
}</code></pre>
<p>If the LCD is blank, change 0x27 to 0x3F in the code.</p></div>

<div class="card"><h3>Project 4: Light Activated Alarm</h3>
<p><strong>Electronics needed:</strong></p>
<ul><li>Arduino UNO</li><li>1x LDR</li><li>1x 10k ohm resistor</li><li>1x Buzzer</li><li>1x LED</li><li>1x 220 ohm resistor</li></ul>
<p><strong>Circuit Diagram:</strong></p>
<ul><li>LDR one leg to 5V, other leg to A0 and to GND through 10k resistor</li><li>Buzzer positive to Pin 8, negative to GND</li><li>LED positive to Pin 13 through 220 ohm resistor, negative to GND</li></ul>
<p><strong>Code:</strong></p>
<pre><code>int ldrPin = A0;
int buzzerPin = 8;
int ledPin = 13;
void setup() {
  pinMode(buzzerPin, OUTPUT);
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}
void loop() {
  int lightValue = analogRead(ldrPin);
  Serial.println(lightValue);
  if (lightValue &lt; 300) {
    digitalWrite(ledPin, HIGH);
    tone(buzzerPin, 1000);
  } else {
    digitalWrite(ledPin, LOW);
    noTone(buzzerPin);
  }
  delay(200);
}</code></pre>
<p>Dark = alarm ON. Bright = alarm OFF.</p></div>

<div class="card"><h3>Project 5: 4 LEDs in Sequence - Chaser</h3>
<p><strong>Electronics needed:</strong></p>
<ul><li>Arduino UNO</li><li>4x LEDs</li><li>4x 220 ohm resistors</li><li>Breadboard and jumper wires</li></ul>
<p><strong>Circuit Diagram:</strong></p>
<ul><li>LED 1 to Pin 2</li><li>LED 2 to Pin 3</li><li>LED 3 to Pin 4</li><li>LED 4 to Pin 5</li><li>Each LED through a 220 ohm resistor to GND</li></ul>
<p><strong>Code:</strong></p>
<pre><code>int leds[] = {2, 3, 4, 5};
void setup() {
  for (int i = 0; i &lt; 4; i++) {
    pinMode(leds[i], OUTPUT);
  }
}
void loop() {
  for (int i = 0; i &lt; 4; i++) {
    digitalWrite(leds[i], HIGH);
    delay(200);
    digitalWrite(leds[i], LOW);
  }
  for (int i = 3; i &gt;= 0; i--) {
    digitalWrite(leds[i], HIGH);
    delay(200);
    digitalWrite(leds[i], LOW);
  }
}</code></pre>
<p>The LEDs chase forward and then backward like a running light.</p></div>

<div class="card"><h3>Project 6: Traffic Lights</h3>
<p><strong>Electronics needed:</strong></p>
<ul><li>Arduino UNO</li><li>1x Red LED, 1x Yellow LED, 1x Green LED</li><li>3x 220 ohm resistors</li><li>Breadboard and jumper wires</li></ul>
<p><strong>Circuit Diagram:</strong></p>
<ul><li>Red LED to Pin 8</li><li>Yellow LED to Pin 9</li><li>Green LED to Pin 10</li><li>Each LED through 220 ohm resistor to GND</li></ul>
<p><strong>Code:</strong></p>
<pre><code>int redPin = 8;
int yellowPin = 9;
int greenPin = 10;
void setup() {
  pinMode(redPin, OUTPUT);
  pinMode(yellowPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
}
void loop() {
  digitalWrite(greenPin, HIGH);
  delay(5000);
  digitalWrite(greenPin, LOW);
  digitalWrite(yellowPin, HIGH);
  delay(2000);
  digitalWrite(yellowPin, LOW);
  digitalWrite(redPin, HIGH);
  delay(5000);
  digitalWrite(redPin, LOW);
}</code></pre>
<p>Green = GO for 5 seconds, Yellow = GET READY for 2 seconds, Red = STOP for 5 seconds.</p></div>

</section>
<!-- END OF PART 1 - PASTE PART 2 BELOW THIS LINE -->


<section id="web">
<h2>Web Development - How Websites Are Made</h2>

<div class="card">
<h3>What is Web Development?</h3>
<p>Web Development is building websites like this one — BEN LOGIC. Every website you see on your phone is made from 3 main languages working together: HTML, CSS, and JavaScript.</p>
<p>Think of it like building a house:</p>
<ul>
<li><strong>HTML = The Structure / Bricks</strong> — Walls, doors, rooms</li>
<li><strong>CSS = The Paint / Design</strong> — Colours, size, beauty</li>
<li><strong>JavaScript = The Electricity / Brain</strong> — Lights, buttons, actions</li>
</ul>
</div>

<div class="card">
<h3>1. HTML - HyperText Markup Language</h3>
<p><strong>What it does:</strong> HTML creates the content and structure. Text, headings, images, buttons, links, videos.</p>
<p>Without HTML, a website would be blank.</p>
<p><strong>Example:</strong></p>
<pre><code>&lt;h1&gt;Hello World&lt;/h1&gt;
&lt;p&gt;This is my first website&lt;/p&gt;
&lt;button&gt;Click Me&lt;/button&gt;
&lt;img src="my-photo.jpg"&gt;</code></pre>
<p><strong>Important HTML tags:</strong></p>
<ul>
<li><code>&lt;h1&gt; to &lt;h6&gt;</code> = Headings, big to small</li>
<li><code>&lt;p&gt;</code> = Paragraph, normal text</li>
<li><code>&lt;img&gt;</code> = Image</li>
<li><code>&lt;a&gt;</code> = Link to another page</li>
<li><code>&lt;button&gt;</code> = Clickable button</li>
<li><code>&lt;div&gt;</code> = Box to hold things together</li>
<li><code>&lt;section&gt;</code> = A part of the page, like Arduino section</li>
</ul>
<p>This BEN LOGIC website is mostly HTML. Every section you see — RC, Arduino, Yo-Yo — is an HTML section.</p>
</div>

<div class="card">
<h3>2. CSS - Cascading Style Sheets</h3>
<p><strong>What it does:</strong> CSS makes the website beautiful. Colours, fonts, sizes, spacing, dark mode / light mode, cards, shadows.</p>
<p>Without CSS, a website would look like plain black text on white paper. No colours, no boxes.</p>
<p><strong>Example:</strong></p>
<pre><code>body {
  background: #101827;
  color: white;
}

h2 {
  color: #00d5ff;
}

.card {
  background: #1c293c;
  padding: 22px;
  border-radius: 12px;
}</code></pre>
<p><strong>What this CSS means:</strong></p>
<ul>
<li><code>background</code> = Background colour</li>
<li><code>color</code> = Text colour</li>
<li><code>padding</code> = Space inside the box</li>
<li><code>border-radius</code> = Rounded corners</li>
</ul>
<p>In this website, the blue cards, the dark background, and the blue headings are all CSS.</p>
</div>

<div class="card">
<h3>3. JavaScript - The Brain</h3>
<p><strong>What it does:</strong> JavaScript makes the website do things. When you click a button and something happens, that is JavaScript.</p>
<p>Without JavaScript, a website is just a poster. It looks nice but does nothing.</p>
<p><strong>Example:</strong></p>
<pre><code>function sayHello() {
  alert("Hello! Welcome to BEN LOGIC");
}</code></pre>
<p><strong>JavaScript in this website:</strong></p>
<ul>
<li><strong>Switch Theme button</strong> = JavaScript changes dark mode to light mode</li>
<li><strong>MENU button on phone</strong> = JavaScript opens and closes the menu</li>
<li><strong>Journal</strong> = JavaScript saves what you type</li>
<li><strong>Search / Filter</strong> = JavaScript shows and hides things</li>
</ul>
</div>

<div class="card">
<h3>How They Work Together</h3>
<pre><code>&lt;!-- HTML: The Button --&gt;
&lt;button onclick="sayHello()"&gt;Click Me&lt;/button&gt;

&lt;!-- CSS: The Style --&gt;
button {
  background: #00d5ff;
  padding: 11px 16px;
  border-radius: 7px;
}

&lt;!-- JavaScript: The Action --&gt;
function sayHello() {
  alert("You clicked the button!");
}</code></pre>
<p><strong>HTML</strong> makes the button → <strong>CSS</strong> makes it blue and round → <strong>JavaScript</strong> makes it talk when you click it.</p>
</div>

<h3>My Web Development Journey</h3>
<div class="grid">
<div class="card"><h3>Level 1: HTML</h3><p>I learned to create headings, paragraphs, images and sections.</p></div>
<div class="card"><h3>Level 2: CSS</h3><p>I learned to add colours, cards, and make it look good on phone and computer.</p></div>
<div class="card"><h3>Level 3: JavaScript</h3><p>I learned to add theme switch, menu, and interactive journal.</p></div>
<div class="card"><h3>Level 4: Projects</h3><p>Now I build full websites like BEN LOGIC and add my Arduino + RC projects to them.</p></div>
</div>

<div class="note"><strong>My goal:</strong> Use web development to show my inventions to the world — not just build them, but share them.</div>
</section>

<section id="yoyo">
<h2>Yo-Yo</h2>
<div class="card"><h3>What is Yo-Yo?</h3><p>Yo-Yo is a skill toy. You throw it down, it spins, and you bring it back with tricks. It improves focus, hand control and patience.</p></div>
<div class="grid">
<div class="card"><h3>Beginner Tricks</h3><ul><li>Sleeper</li><li>Walk the Dog</li><li>Forward Pass</li></ul></div>
<div class="card"><h3>Intermediate Tricks</h3><ul><li>Rock the Baby</li><li>Eiffel Tower</li><li>Brain Twister</li></ul></div>
<div class="card"><h3>Advanced Tricks</h3><ul><li>Trapeze</li><li>Double or Nothing</li><li>Bind Return</li></ul></div>
</div>
<div class="card"><h3>Types of Yo-Yos</h3><ul><li><strong>Responsive:</strong> Comes back with a tug. Best for beginners.</li><li><strong>Unresponsive:</strong> Spins longer. Needs a Bind to return. Best for advanced tricks.</li></ul></div>
</section>

<section id="coding">
<h2>Coding</h2>
<div class="card"><h3>What is Coding?</h3><p>Coding is giving instructions to a computer. You write the instructions in a language the computer understands.</p></div>
<div class="grid">
<div class="card"><h3>Python</h3><p>Easy to learn. Good for games, apps, and AI.</p><pre><code>print("Hello BEN LOGIC")</code></pre></div>
<div class="card"><h3>HTML + CSS</h3><p>For building websites.</p><pre><code>&lt;h1&gt;My Website&lt;/h1&gt;</code></pre></div>
<div class="card"><h3>JavaScript</h3><p>For making websites interactive.</p><pre><code>alert("Hello!")</code></pre></div>
<div class="card"><h3>Arduino C++</h3><p>For controlling electronics, motors and sensors.</p><pre><code>digitalWrite(13, HIGH);</code></pre></div>
</div>
</section>

<section id="research">
<h2>Research</h2>
<div class="card"><h3>My Research Topics</h3><ul><li>How Bluetooth controls robots</li><li>How sensors help robots see the world</li><li>How to make RC cars faster and smarter</li><li>How websites and apps are built</li></ul></div>
<div class="card"><h3>What I Want To Invent</h3><p>A smart RC car that can avoid obstacles by itself, follow a line, and be controlled from a phone.</p></div>
</section>

<section id="journal">
<h2>My Journal</h2>
<div class="card"><p>Write your ideas, experiments and progress here. It is saved on this device.</p>
<input type="text" id="journalTitle" placeholder="Title...">
<textarea id="journalText" rows="4" placeholder="Write your journal entry..."></textarea>
<button onclick="saveJournal()">Save Entry</button>
<button onclick="clearJournal()">Clear All</button>
<div id="journalList"></div>
</div>
</section>

</main>
<footer>
<p>© 2026 BEN LOGIC | Hobby & Research Hub</p>
<p class="small">Built with HTML, CSS and JavaScript. Arduino, RC Engineering, Yo-Yo, Coding & Research.</p>
</footer>

<script>
function toggleTheme(){
  document.body.classList.toggle('light');
  const isLight = document.body.classList.contains('light');
  localStorage.setItem('benlogic-theme', isLight ? 'light' : 'dark');
  document.getElementById('themeButton').textContent = isLight ? 'Switch to Dark' : 'Switch Theme';
}
function toggleMenu(){
  const nav = document.getElementById('navigation');
  nav.classList.toggle('open');
}
document.addEventListener('click', function(e){
  const nav = document.getElementById('navigation');
  if(window.innerWidth <= 650 && nav.classList.contains('open') && !e.target.closest('#navigation')){
    nav.classList.remove('open');
  }
});
function saveJournal(){
  const title = document.getElementById('journalTitle').value.trim();
  const text = document.getElementById('journalText').value.trim();
  if(!title && !text){ alert('Write something first!'); return; }
  let entries = JSON.parse(localStorage.getItem('benlogic-journal') || '[]');
  entries.unshift({title: title || 'Untitled', text: text, date: new Date().toLocaleString()});
  localStorage.setItem('benlogic-journal', JSON.stringify(entries));
  document.getElementById('journalTitle').value = '';
  document.getElementById('journalText').value = '';
  displayJournal();
}
function displayJournal(){
  const list = document.getElementById('journalList');
  let entries = JSON.parse(localStorage.getItem('benlogic-journal') || '[]');
  if(entries.length === 0){ list.innerHTML = '<p class="empty">No entries yet. Write your first one!</p>'; return; }
  list.innerHTML = entries.map(function(e){
    return '<div class="journal-entry card"><h3>'+e.title+'</h3><p class="small">'+e.date+'</p><p>'+e.text+'</p></div>';
  }).join('');
}
function clearJournal(){
  if(confirm('Delete all journal entries?')){ localStorage.removeItem('benlogic-journal'); displayJournal(); }
}
window.onload = function(){
  const savedTheme = localStorage.getItem('benlogic-theme');
  if(savedTheme === 'light'){ document.body.classList.add('light'); document.getElementById('themeButton').textContent = 'Switch to Dark'; }
  displayJournal();
};
</script>
</body>
</html>
