<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kids Cartoon World</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#f0f8ff;color:#243047}
header{background:linear-gradient(120deg,#6c5ce7,#00b894);color:white;text-align:center;padding:25px 12px}
header h1{margin:0;font-size:clamp(26px,5vw,42px)}
nav{display:flex;justify-content:center;gap:8px;flex-wrap:wrap;background:#fff;padding:12px;position:sticky;top:0;z-index:5;box-shadow:0 2px 8px #ddd}
button,select,input{font:inherit}
button{border:0;border-radius:10px;padding:11px 16px;background:#6c5ce7;color:white;cursor:pointer;font-weight:bold}
button:hover{filter:brightness(.92)}
nav button{background:#e8e5ff;color:#4937bd}
main{max-width:1000px;margin:auto;padding:18px}
.card{background:white;border-radius:16px;padding:20px;margin:16px 0;box-shadow:0 4px 15px #0000000c}
.hidden{display:none!important}
input,select{padding:12px;border:1px solid #ccd3df;border-radius:9px;max-width:100%}
.welcome{text-align:center;padding:45px 20px}
.welcome input{width:min(100%,320px);display:block;margin:15px auto}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(210px,1fr));gap:14px}
.subject{border:2px solid #eee;border-radius:13px;padding:15px}
.subject h3{margin-top:0}
#drawingCanvas{width:100%;height:350px;border:2px dashed #999;border-radius:12px;touch-action:none;background:white;display:block}
.option{display:block;width:100%;text-align:left;background:#eef0ff;color:#222;margin:9px 0}
.option.correct{background:#c8f7d5}
.option.wrong{background:#ffd4d4}
footer{text-align:center;padding:25px;color:#596579}
.small{color:#657087;font-size:14px}
</style>
</head>
<body>
<header>
  <h1>🎨 Kids Cartoon World 🌈</h1>
  <p>Learn • Play • Draw • Discover!</p>
</header>

<nav>
  <button onclick="showSection('home')">🏠 Home</button>
  <button onclick="showSection('quiz')">🧠 Quiz</button>
  <button onclick="showSection('learning')">📚 Learning</button>
  <button onclick="showSection('drawing')">🎨 Drawing</button>
</nav>

<main>
<section id="home" class="card welcome">
  <div id="nameArea">
    <h2>Welcome, Little Explorer! 🌟</h2>
    <p>Enter your name to begin your adventure.</p>
    <input id="playerName" type="text" maxlength="30" placeholder="Enter your name">
    <button id="startButton" type="button">🚀 Start Learning</button>
    <p id="nameError" style="color:#d63031" aria-live="polite"></p>
  </div>
  <div id="welcomeArea" class="hidden">
    <h2 id="welcomeMessage"></h2>
    <p>Your learning adventure starts now!</p>
    <button onclick="showSection('quiz')">Start a Quiz 🧠</button>
    <button onclick="showSection('learning')">Explore Learning 📚</button>
  </div>
</section>

<section id="quiz" class="hidden">
  <div class="card">
    <h2>🧠 Quiz Zone</h2>
    <label>Subject:
      <select id="subjectSelect">
        <option>Science</option>
        <option>Mathematics</option>
        <option>Social Studies</option>
        <option>English Grammar</option>
        <option>Hindi</option>
        <option>Computer</option>
        <option>General Knowledge</option>
        <option>Environmental Studies</
