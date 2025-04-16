<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Legion-Trick</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #121212;
      color: #ffd700;
    }

    header {
      background-color: #1c1c1c;
      padding: 40px 20px;
      text-align: center;
      font-size: 2.5em;
      font-weight: bold;
      border-bottom: 2px solid #ffd700;
    }

    section {
      padding: 20px;
      margin: 20px;
      background-color: #1e1e1e;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.1);
    }

    h2 {
      color: #ffda44;
    }

    a {
      color: #ffd700;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    textarea, input {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      border-radius: 5px;
      border: none;
      background-color: #2b2b2b;
      color: #fff;
    }

    button {
      background-color: #444;
      color: #ffd700;
      padding: 10px;
      border: none;
      border-radius: 5px;
      margin-top: 10px;
      cursor: pointer;
    }

    footer {
      background-color: #0f0f0f;
      text-align: center;
      padding: 15px;
      font-size: 0.9em;
      border-top: 1px solid #ffd700;
    }

    .mensaje {
      margin-top: 10px;
      background-color: #2c2c2c;
      padding: 10px;
      border-left: 4px solid #ffd700;
      border-radius: 5px;
    }
  </style>
</head>
<body>

<header># Legion-Trick</header>

<section>
  <h2>Bienvenido a Legion-Trick</h2>
  <p>Esta página por ahora será la mía, para que nosotros los usuarios podamos comunicarnos, hablar y compartir. También encontrarás mis redes sociales y más contenido personal.</p>
</section>

<section>
  <h2>Mi canal de YouTube</h2>
  <p>Sígueme en mi canal para ver contenido exclusivo:</p>
  <a href="https://youtube.com/@davidhaney-w1b?si=ZM5V8hiHU0tSw-1e" target="_blank">David Haney en YouTube</a>
</section>

<section>
  <h2>Comentarios y sugerencias</h2>
  <form id="formulario">
    <input type="text" id="nombre" placeholder="Tu nombre" required>
    <textarea id="comentario" rows="4" placeholder="Escribe tu comentario aquí..." required></textarea>
    <button type="submit">Enviar</button>
  </form>
  <div id="comentarios"></div>
</section>

<footer>
  © 2025 Legion-Trick. Todos los derechos reservados.
</footer>

<script>
  const form = document.getElementById('formulario');
  const comentariosDiv = document.getElementById('comentarios');

  form.addEventListener('submit', function (e) {
    e.preventDefault();
    const nombre = document.getElementById('nombre').value;
    const comentario = document.getElementById('comentario').value;

    const nuevoComentario = document.createElement('div');
    nuevoComentario.className = 'mensaje';
    nuevoComentario.innerHTML = `<strong>${nombre}</strong>: ${comentario}`;
    
    comentariosDiv.appendChild(nuevoComentario);
    form.reset();
  });
</script>

</body>
</html>
