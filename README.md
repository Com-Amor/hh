<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Página Especial</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #fff0f5;
      overflow-x: hidden;
    }

    header {
      background-color: #f08080;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 24px;
      font-weight: bold;
    }

    .main-image {
      text-align: center;
      margin-top: 20px;
    }

    .main-image img {
      max-width: 90%;
      height: auto;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }

    .message {
      text-align: center;
      margin: 20px;
      font-size: 20px;
      color: #444;
    }

    .hearts {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: -1;
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: red;
      clip-path: polygon(50% 0%, 61% 18%, 98% 35%, 75% 68%, 50% 100%, 25% 68%, 2% 35%, 39% 18%);
      opacity: 0.7;
      animation: float 6s linear infinite;
    }

    @keyframes float {
      0% { transform: translateY(100vh) scale(1); }
      100% { transform: translateY(-10vh) scale(0.5); }
    }

    .slideshow {
      display: flex;
      justify-content: center;
      margin: 30px auto;
      max-width: 90%;
    }

    .slideshow img {
      max-width: 100%;
      max-height: 400px;
      margin: 0 10px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }

    .download-btn {
      display: flex;
      justify-content: center;
      margin-bottom: 40px;
    }

    .download-btn a {
      background-color: #f08080;
      color: white;
      padding: 10px 20px;
      text-decoration: none;
      border-radius: 8px;
      font-size: 16px;
    }

    .download-btn a:hover {
      background-color: #e06666;
    }
  </style>
</head>
<body>
  <header>
    sempre que se sentir sozinha, lembre:
  </header>

  <div class="main-image">
    <img src="imagem-principal.jpeg" alt="Imagem especial">
  </div>

  <div class="message">
    "você nunca estará sozinha, porque meu pensamento vive grudado em você, escondido em um sorriso bobo, ou até naquele suspiro que nem sabemos o por quê!"
  </div>

  <div class="slideshow">
    <img src="foto1.jpeg" alt="Foto 1">
    <img src="foto2.jpeg" alt="Foto 2">
    <img src="foto3.jpeg" alt="Foto 3">
  </div>

  <div class="download-btn">
    <a href="imagem-principal.jpeg" download>Baixar imagem</a>
  </div>

  <div class="hearts">
    <!-- corações serão adicionados dinamicamente -->
  </div>

  <script>
    // gerar corações aleatórios
    for (let i = 0; i < 50; i++) {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = `${Math.random() * 100}vw`;
      heart.style.animationDuration = `${4 + Math.random() * 3}s`;
      document.querySelector('.hearts').appendChild(heart);
    }
  </script>
</body>
</html>
