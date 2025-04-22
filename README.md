<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Site Interativo Acessível</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 20px;
      transition: background-color 0.3s ease;
    }

    h1 {
      color: #2c3e50;
    }

    .menu {
      display: none;
      background-color: #ecf0f1;
      padding: 10px;
      margin-top: 20px;
      border: 1px solid #bdc3c7;
    }

    button {
      padding: 10px 20px;
      background-color: #3498db;
      color: white;
      border: none;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.2s ease;
    }

    button:hover {
      background-color: #2980b9;
      transform: scale(1.1);
    }

    .image-container {
      margin-top: 20px;
    }

    .image-container img {
      max-width: 100%;
    }

    .menu img {
      max-width: 100px;
      display: block;
      margin: 10px 0;
    }
  </style>
</head>
<body>
  <header>
    <h1>Bem-vindo ao nosso site interativo!</h1>
    <p id="intro">Explore conteúdos acessíveis e interativos!</p>
  </header>

  <section>
    <h2 id="menu-toggle" aria-labelledby="menu-title">Menu Interativo</h2>
    <button id="menu-button" aria-expanded="false" aria-controls="menu" onclick="toggleMenu()">Abrir Menu</button>

    <div id="menu" class="menu" role="navigation" aria-labelledby="menu-toggle">
      <ul>
        <li>
          <a href="#">
            <img src="https://i.pinimg.com/736x/04/2c/c4/042cc4aa67d7ab4ce59117a268cddd6c.jpg" alt="Gato com expressão surpresa olhando para cima">
            Link 1
          </a>
        </li>
        <li>
          <a href="#">
            <img src="https://i.pinimg.com/736x/46/79/bd/4679bd6b54275be56f4b7c35e78563b8.jpg" alt="Gato com um capacete preto, parecendo estar em um filme de ação">
            Link 2
          </a>
        </li>
        <li>
          <a href="#">
            <img src="https://i.pinimg.com/736x/ef/09/cd/ef09cdfc63740214cdb8cd5bc4e69f68.jpg" alt="Gato com expressão divertida usando óculos vermelhos">
            Link 3
          </a>
        </li>
      </ul>
    </div>
  </section>

  <section class="image-container">
    <h2>Imagem do Gato Engraçadinho</h2>
    <img src="https://i.pinimg.com/736x/d2/f2/ca/d2f2ca7d8ccb6c9b3b5144dcb766948b.jpg" alt="Ilustração de um gato de desenho que possui um chapéu vermelho, amarelo e azul, com a parte da frente verde. O gato é visto lambendo um pirulito. Imagem aparenta ser uma paródia do meme 'cachorro com chapeu de criança lambendo pirulito'.">
  </section>

  <section>
    <h2>Mudar Cor de Fundo</h2>
    <button onclick="changeBackgroundColor()">Mudar Cor de Fundo</button>
  </section>

  <script>
    function toggleMenu() {
      const menu = document.getElementById('menu');
      const button = document.getElementById('menu-button');
      const isExpanded = button.getAttribute('aria-expanded') === 'true';
      button.setAttribute('aria-expanded', !isExpanded);
      menu.style.display = isExpanded ? 'none' : 'block';
    }

    function changeBackgroundColor() {
      const body = document.body;
      const currentColor = body.style.backgroundColor;
      body.style.backgroundColor =
        currentColor === 'rgb(52, 152, 219)'
          ? 'rgb(39, 174, 96)'
          : 'rgb(52, 152, 219)';
    }
  </script>
</body>
</html>
