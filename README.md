# mylove
<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>প্রপোজ ফর সুমি</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom, #1b0036, #000);
      font-family: 'Arial', sans-serif;
      overflow: hidden;
      text-align: center;
      color: white;
    }

    h1 {
      margin-top: 60px;
      font-size: 2.5em;
      animation: fadeIn 2s ease-in-out;
    }

    p {
      font-size: 1.3em;
      margin: 20px;
    }

    .btn {
      background-color: #fff;
      color: #ff0066;
      padding: 12px 24px;
      margin: 10px;
      font-size: 1.1em;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      transition: 0.3s;
    }

    .btn:hover {
      background-color: #ff0066;
      color: #fff;
    }

    .response {
      font-size: 2em;
      margin-top: 30px;
      animation: fadeIn 1s ease-in-out;
    }

    .emoji {
      font-size: 3em;
      animation: pop 0.5s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes pop {
      0% { transform: scale(0); }
      100% { transform: scale(1); }
    }

    .heart, .flower {
      position: absolute;
      font-size: 2em;
      animation: float 5s linear infinite;
      opacity: 0.8;
    }

    @keyframes float {
      0% { transform: translateY(0); }
      100% { transform: translateY(100vh); }
    }

    audio {
      display: none;
    }
  </style>
</head>
<body>

  <!-- মিউজিক প্লে -->
  <audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
  </audio>

  <h1>হেই সুমি 💌</h1>
  <p>আমি তোমাকে খুব ভালোবাসি... তুমি কি আমায় ভালোবাসবে? ❤️</p>

  <button class="btn" onclick="sayYes()">হ্যাঁ, ভালোবাসি</button>
  <button class="btn" onclick="sayNo()">না, দুঃখিত</button>

  <div class="response" id="response"></div>

  <script>
    function sayYes() {
      document.body.style.background = "linear-gradient(to bottom, #ff007f, #ffcce6)";
      document.getElementById('response').innerHTML =
        "<div class='emoji'>💖 আমি তো তোমাকেই ভালোবাসি! 💖</div>";
      createHearts();
      createFlowers();
    }

    function sayNo() {
      document.body.style.background = "#111";
      document.getElementById('response').innerHTML =
        "<div class='emoji'>😢 তুমি আমাকে ফিরিয়ে দিলে...</div>";
    }

    function createHearts() {
      for (let i = 0; i < 30; i++) {
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.top = Math.random() * -100 + "px";
        heart.style.fontSize = (Math.random() * 20 + 20) + "px";
        heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 6000);
      }
    }

    function createFlowers() {
      for (let i = 0; i < 20; i++) {
        let flower = document.createElement("div");
        flower.className = "flower";
        flower.innerHTML = "🌹";
        flower.style.left = Math.random() * 100 + "vw";
        flower.style.top = Math.random() * -100 + "px";
        flower.style.fontSize = (Math.random() * 20 + 20) + "px";
        flower.style.animationDuration = (Math.random() * 3 + 3) + "s";
        document.body.appendChild(flower);
        setTimeout(() => flower.remove(), 6000);
      }
    }
  </script>

</body>
</html
