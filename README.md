<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Nikky ❤️ Will You Be My Valentine?</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      overflow: hidden;
      color: #fff;
    }

    .container {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
      text-align: center;
    }

    .card {
      background: rgba(255, 255, 255, 0.15);
      backdrop-filter: blur(10px);
      border-radius: 25px;
      padding: 35px;
      max-width: 420px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.25);
      animation: fadeIn 2s ease;
    }

    img {
      width: 100%;
      border-radius: 20px;
      margin-bottom: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    }

    h1 {
      font-size: 2.2em;
      margin-bottom: 10px;
    }

    h2 {
      font-size: 1.4em;
      margin-bottom: 20px;
      font-weight: 400;
    }

    p {
      font-size: 1.05em;
      line-height: 1.6;
      margin-bottom: 25px;
    }

    .buttons button {
      font-size: 1.1em;
      padding: 12px 28px;
      margin: 10px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .yes {
      background: #ff4d6d;
      color: white;
    }

    .yes:hover {
      transform: scale(1.15);
      background: #ff1e4d;
    }

    .no {
      background: white;
      color: #ff4d6d;
    }

    .no:hover {
      transform: scale(1.05);
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Floating Hearts */
    .heart {
      position: fixed;
      bottom: -20px;
      color: rgba(255,255,255,0.8);
      font-size: 20px;
      animation: floatUp 8s linear infinite;
    }

    @keyframes floatUp {
      from {
        transform: translateY(0) scale(1);
        opacity: 1;
      }
      to {
        transform: translateY(-120vh) scale(1.5);
        opacity: 0;
      }
    }
  </style>
</head>

<body>

<div class="container">
  <div class="card">
    <img src="nikky.jpg" alt="Us ❤️">

    <h1>Nikky 💖</h1>
    <h2>This is from my heart…</h2>

    <p>
      Every moment with you feels special.<br>
      Your smile, your kindness, the way you are —
      it all means more to me than you know.
    </p>

    <p>
      This Valentine’s Day, I just wanted to ask you
      something simple, honest, and full of feeling.
    </p>

    <h2>Will you be my Valentine? 🌹</h2>

    <div class="buttons">
      <button class="yes" onclick="yesClicked()">Yes 💕</button>
      <button class="no" onclick="noClicked()">No 🙈</button>
    </div>
  </div>
</div>

<script>
  function yesClicked() {
    alert(
      "You just made me smile so much ❤️\n\n" +
      "Thank you for being you.\n" +
      "This Valentine’s Day just became very special 💖"
    );
  }

  function noClicked() {
    alert("That button is just teasing 😌💖");
  }

  // Floating hearts animation
  function createHeart() {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = Math.random() * 20 + 15 + "px";
    heart.style.animationDuration = Math.random() * 4 + 6 + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
      heart.remove();
    }, 8000);
  }

  setInterval(createHeart, 300);
</script>

</body>
</html>

