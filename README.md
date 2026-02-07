<html>
<head>
  <title>For Ashmita ❤️</title>
  <style>
    body {
      background: linear-gradient(180deg, #fdeff9, #fbc2eb);
      font-family: 'Arial', sans-serif;
      text-align: center;
      padding: 60px 20px;
      color: #2c2c2c;
      overflow: hidden;
    }
    h1 {
      font-weight: normal;
      font-size: 26px;
    }
    p {
      font-size: 18px;
      line-height: 1.7;
    }
    button {
      margin-top: 20px;
      font-size: 18px;
      padding: 12px 28px;
      border: none;
      border-radius: 30px;
      background: #ff4d6d;
      color: white;
      cursor: pointer;
    }
    .no {
      background: #aaa;
      position: absolute;
    }
    .heart {
      position: fixed;
      bottom: -10px;
      font-size: 18px;
      animation: floatUp 6s linear infinite;
      opacity: 0.6;
    }
    @keyframes floatUp {
      from { transform: translateY(0); }
      to { transform: translateY(-120vh); }
    }
  </style>
</head>

<body>

<h1 id="text">Hey Ashmita ❤️</h1>
<p id="sub">Even though we’re miles apart…</p>
<button id="btn" onclick="next()">Continue 💌</button>

<script>
let step = 0;

function next() {
  step++;
  if (step === 1) {
    text.innerText = "Long distance isn’t easy 🌍";
    sub.innerText = "But loving you has always been.";
  }
  else if (step === 2) {
    text.innerText = "I miss you every single day";
    sub.innerText = "Your smile, your voice, your presence.";
  }
  else if (step === 3) {
    text.innerText = "So I made this for you ❤️";
    sub.innerText = "Because some feelings deserve effort.";
  }
  else if (step === 4) {
    text.innerText = "Ashmita, will you be my Valentine? 💖";
    sub.innerText = "";
    btn.style.display = "none";
    document.body.innerHTML +=
      '<br><button onclick="yes()">Yes 💕</button>' +
      '<button class="no" id="no" onmouseover="moveNo()">No 😢</button>';
  }
}

function moveNo() {
  const no = document.getElementById("no");
  no.style.top = Math.random() * 80 + "%";
  no.style.left = Math.random() * 80 + "%";
}

function yes() {
  document.body.innerHTML =
    "<h1>Happy Valentine’s Day, Ashmita ❤️</h1>" +
    "<p>This distance is temporary.</p>" +
    "<p>What I feel for you is not.</p>" +
    "<p>I choose you — today, and every day.</p>" +
    "<p style='margin-top:30px;'>— Yours, always 💖</p>";
}

function createHeart() {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerText = "💗";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = (Math.random() * 3 + 4) + "s";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 7000);
}

setInterval(createHeart, 600);
</script>

</body>
</html>
