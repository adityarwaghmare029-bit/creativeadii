<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Friendship Day, Samiksha!</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: url('background.jpg') no-repeat center center fixed;
      background-size: cover;
      overflow: hidden;
      color: #fff;
      text-align: center;
      padding-top: 60px;
      position: relative;
      z-index: 1;
    }

    h1 {
      font-size: 3em;
      color: #ffb6c1;
      animation: floatText 3s infinite;
      text-shadow: 2px 2px 4px #000;
    }

    p {
      font-size: 1.3em;
      margin: 15px auto;
      max-width: 90%;
      text-shadow: 1px 1px 2px #000;
    }

    .heart {
      font-size: 4em;
      animation: beat 1s infinite;
    }

    .btn {
      padding: 12px 25px;
      font-size: 1em;
      background-color: #ff69b4;
      color: white;
      border: none;
      border-radius: 25px;
      text-decoration: none;
      margin-top: 30px;
      display: inline-block;
      box-shadow: 2px 2px 5px #000;
      transition: background 0.3s ease;
    }

    .btn:hover {
      background-color: #e91e63;
    }

    /* Heart animation */
    .falling-heart {
      position: fixed;
      top: -50px;
      font-size: 24px;
      color: #ff4d6d;
      animation: fall linear infinite;
      z-index: 0;
    }

    @keyframes beat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.2); }
    }

    @keyframes floatText {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    @keyframes fall {
      to {
        transform: translateY(110vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <div class="heart">❤️</div>
  <h1>Happy Friendship Day, Samiksha!</h1>

  <p>
    From the bottom of my heart,<br>
    I'm really thankful to have you in my life.<br>
    You're not just a best friend… you're my forever person 💞
  </p>

  <a href="friendship.mp4" download class="btn">🎥 Download My Surprise Video</a>

  <p style="margin-top: 60px;">
    I am with you forever… whenever you need me.<br><br>
    — Your bestfriend, <strong>Aditya 💫</strong>
  </p>

  <!-- JavaScript for falling hearts -->
  <script>
    const hearts = ["❤️", "💖", "💕", "💘", "💞"];
    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("falling-heart");
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = 4 + Math.random() * 3 + "s";
      heart.innerText = hearts[Math.floor(Math.random() * hearts.length)];
      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 7000);
    }

    setInterval(createHeart, 300);
  </script>

</body>
</html>
