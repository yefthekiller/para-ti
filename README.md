<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Para ti 💌</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to top right, #ff9a9e, #fad0c4);
      height: 100vh;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: 'Segoe UI', sans-serif;
      color: #fff;
      text-align: center;
    }

    h1 {
      font-size: 3em;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
    }

    p {
      font-size: 1.2em;
      max-width: 600px;
      margin-top: 1em;
      text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 10s infinite;
    }

    .heart::before,
    .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      left: -10px;
      top: 0;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh) rotate(45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-10vh) rotate(45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div>
    <h1>Te amo 💕</h1>
    <p>
      Gracias por estar en mi vida. Cada día contigo es un regalo que valoro más de lo que las palabras pueden expresar.
      Esta no es solo una página, es una parte de mi corazón dedicada a ti. ❤️
    </p>
  </div>

  <script>
    // Crear corazones flotantes
    const totalHearts = 30;
    for (let i = 0; i < totalHearts; i++) {
      let heart = document.createElement("div");
      heart.className = "heart";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (5 + Math.random() * 5) + "s";
      heart.style.opacity = Math.random();
      heart.style.transform = `scale(${0.5 + Math.random() * 1}) rotate(45deg)`;
      document.body.appendChild(heart);
    }
  </script>
</body>
</html>
