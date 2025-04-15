<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Legion-Trick</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #121212;
      color: #fff;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    
    header {
      background-color: #333;
      padding: 20px;
      font-size: 2em;
    }
    
    section {
      padding: 20px;
      margin: 10px;
      background-color: #1c1c1c;
      border-radius: 8px;
    }
    
    a {
      color: #1e90ff;
      text-decoration: none;
    }

    .video {
      margin-top: 20px;
    }

    iframe {
      width: 80%;
      height: 450px;
      border: none;
    }

    .comments {
      margin-top: 20px;
      padding: 20px;
      background-color: #333;
      border-radius: 10px;
      width: 80%;
      margin: 20px auto;
    }

    .comments input, .comments textarea {
      width: 100%;
      padding: 10px;
      margin: 5px 0;
      border: 1px solid #555;
      border-radius: 5px;
      background-color: #2c2c2c;
      color: white;
    }

    .comments button {
      background-color: #1e90ff;
      padding: 10px 20px;
      border: none;
      cursor: pointer;
      border-radius: 5px;
    }

    .comments button:hover {
      background-color: #0066cc;
    }

    footer {
      padding: 20px;
      background-color: #333;
      margin-top: 30px;
      font-size: 0.8em;
    }
  </style>
</head>
<body>

  <header>Legion-Trick</header>

  <section>
    <h2>Bienvenidos a Legion-Trick</h2>
    <p>Esta página será el espacio donde podrás comunicarte, compartir ideas y conocer más sobre mis proyectos. Aquí también encontrarás mi contenido y redes sociales.</p>
  </section>

  <section>
    <h2>Canal de YouTube</h2>
    <p>Visita mi canal en YouTube y suscríbete para ver más contenido:</p>
    <a href="https://youtube.com/@davidhaney-w1b?si=ZM5V8hiHU0tSw-1e" target="_blank">Canal de YouTube</a>
  </section>

  <section class="video">
    <h2>Último Video</h2>
    <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </section>

  <section class="comments">
    <h2>Deja tu Comentario</h2>
    <form id="comment-form">
      <input type="text" id="name" placeholder="Tu nombre" required><br>
      <textarea id="comment" placeholder="Escribe tu comentario aquí..." rows="4" required></textarea><br>
      <button type="submit">Enviar Comentario</button>
    </form>
    <div id="comment-list"></div>
  </section>

  <footer>
    <p>&copy; 2025 Legion-Trick. Todos los derechos reservados.</p>
  </footer>

  <script>
    document.getElementById('comment-form').addEventListener('submit', function(event) {
      event.preventDefault();
      
      let name = document.getElementById('name').value;
      let comment = document.getElementById('comment').value;
      
      let commentDiv = document.createElement('div');
      commentDiv.classList.add('comment-item');
      commentDiv.innerHTML = `<strong>${name}</strong>: <p>${comment}</p>`;
      
      document.getElementById('comment-list').appendChild(commentDiv);
      
      // Limpiar los campos después de enviar el comentario
      document.getElementById('name').value = '';
      document.getElementById('comment').value = '';
    });
  </script>
</body>
</html>
