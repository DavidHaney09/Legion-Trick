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
      background-color: #0e0e0e;
      color: #ffd700;
    }

    header {
      background: linear-gradient(to right, #1c1c1c, #2e2e2e);
      padding: 30px;
      text-align: center;
      font-size: 3em;
      color: #ffd700;
      text-shadow: 0 0 10px #fff30055;
    }

    section {
      background-color: #1a1a1a;
      margin: 20px auto;
      padding: 20px;
      border-radius: 10px;
      width: 90%;
      max-width: 800px;
      box-shadow: 0 0 10px #ffd70044;
    }

    a {
      color: #ffcc00;
      text-decoration: none;
      font-weight: bold;
    }

    a:hover {
      text-decoration: underline;
    }

    iframe {
      width: 100%;
      height: 400px;
      border: none;
      border-radius: 10px;
      box-shadow: 0 0 10px #ffd70033;
    }

    .comentarios input,
    .comentarios textarea {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      border: 1px solid #ffd70055;
      border-radius: 5px;
      background-color: #111;
      color: #fff;
    }

    .comentarios button {
      margin-top: 10px;
      background-color: #ffd700;
      color: #000;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .comentarios button:hover {
      background-color: #e6c200;
    }

    .mensaje {
      background-color: #222;
      padding: 10px;
      margin-top: 10px;
      border-left: 4px solid #ffd700;
      border-radius: 5px;
    }

    footer {
      background-color: #111;
      text-align: center;
      padding: 15px;
      font-size: 0.9em;
      border-top: 1px solid #444;
      color: #999;
    }
  </style>
</head>
<body>

  <header>Legion-Trick</header>

  <section>
    <h2>¿Qué es esto?</h2>
    <p>
      Esta página será mi espacio personal, donde nosotros, los usuarios, podremos comunicarnos, hablar, compartir y descubrir más. Aquí verás mis redes sociales, videos y mucho más.
    </p>
  </section>

  <section>
    <h2>Mi canal de YouTube</h2>
    <p>Haz clic y visita mi canal para ver contenido único:</p>
    <a href="https://youtube.com/@davidhaney-w1b?si=ZM5V8hiHU0tSw-1e" target="_blank">Visitar canal @davidhaney</a>
  </section>

  <section>
    <h2>Último video subido</h2>
    <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" allowfullscreen></iframe>
  </section>

  <section class="comentarios">
    <h2>Comentarios</h2>
    <form id="formulario">
      <input type="text" id="nombre" placeholder="Tu nombre" required>
      <textarea id="mensaje" rows="3" placeholder="Escribe tu comentario..." required></textarea>
      <button type="submit">Enviar</button>
    </form>
    <div id="mensajes"></div>
  </section>

  <footer>
    &copy; 2025 Legion-Trick. Todos los derechos reservados.
  </footer>

  <script>
    const formulario = document.getElementById('formulario');
    const mensajesDiv = document.getElementById('mensajes');

    formulario.addEventListener('submit', function (e) {
      e.preventDefault();
      const nombre = document.getElementById('nombre').value;
      const mensaje = document.getElementById('mensaje').value;

      const nuevoMensaje = document.createElement('div');
      nuevoMensaje.className = 'mensaje';
      nuevoMensaje.innerHTML = `<strong>${nombre}:</strong> ${mensaje}`;
      mensajesDiv.appendChild(nuevoMensaje);

      formulario.reset();
    });
  </script>

</body>
</html>
