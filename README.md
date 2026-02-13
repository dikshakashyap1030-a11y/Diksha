# Diksha
Valentine 
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>For Yash ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      color: #fff;
      text-align: center;
    }.card {
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(10px);
  border-radius: 25px;
  padding: 40px 30px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.2);
  max-width: 350px;
  animation: fadeIn 1.5s ease;
}

h1 {
  margin-bottom: 10px;
  font-size: 28px;
}

p {
  font-size: 16px;
  line-height: 1.6;
  margin: 15px 0 25px;
}

button {
  background: #ff4b6e;
  border: none;
  padding: 12px 22px;
  border-radius: 20px;
  font-size: 16px;
  color: white;
  cursor: pointer;
  transition: 0.3s ease;
}

button:hover {
  background: #ff1e4d;
  transform: scale(1.05);
}

.hidden-message {
  margin-top: 20px;
  font-size: 15px;
  display: none;
  animation: fadeIn 1s ease forwards;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(15px); }
  to { opacity: 1; transform: translateY(0); }
}

.hearts {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  pointer-events: none;
}

.heart {
  position: absolute;
  bottom: -20px;
  font-size: 20px;
  animation: floatUp linear infinite;
  opacity: 0.8;
}

@keyframes floatUp {
  from { transform: translateY(0) scale(1); }
  to { transform: translateY(-110vh) scale(1.5); }
}

  </style>
</head>
<body>
  <div class="card">
    <h1>Happy Valentine's Day, Yash ❤️</h1>
    <p>
      You are the most special part of my life. 
      Every moment with you feels magical and full of love.
    </p><button onclick="showMessage()">Click for a surprise 💌</button>

<div class="hidden-message" id="loveMsg">
  I love you forever, and I always will. 💖<br />
  Thank you for being mine. 🌙✨
</div>

  </div>  <div class="hearts" id="hearts"></div>  <script>
    function showMessage() {
      document.getElementById('loveMsg').style.display = 'block';
    }

    const heartsContainer = document.getElementById('hearts');

    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.innerText = '❤';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = 3 + Math.random() * 4 + 's';
      heart.style.fontSize = 15 + Math.random() * 20 + 'px';
      heartsContainer.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 7000);
    }

    setInterval(createHeart, 300);
  </script></body>
</html>
