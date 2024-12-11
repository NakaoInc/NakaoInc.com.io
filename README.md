<!DOCTYPE html>
<html lang="es">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nakao Inc. | Servicios Tecnológicos</title>
  <style>
    /* Estilos básicos para el sitio */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
    }

    /* Estilo del encabezado */
    header {
      background-color: #004080;
      color: white;
      padding: 10px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 2rem;
    }

    header p {
      margin: 5px 0 0;
      font-size: 1rem;
    }

    /* Barra de búsqueda */
    .search-bar {
      display: flex;
      justify-content: center;
      margin: 10px 0;
    }

    .search-bar input[type="text"] {
      padding: 10px;
      width: 80%;
      max-width: 600px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    /* Contenedor principal */
    .container {
      padding: 20px;
    }

    /* Estilización de tarjetas */
    .card {
      background-color: white;
      border: 1px solid #ddd;
      border-radius: 5px;
      margin: 10px;
      padding: 15px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      transition: transform 0.2s ease;
    }

    .card:hover {
      transform: scale(1.05);
    }

    .card h3 {
      margin-top: 0;
    }

    /* Pie de página */
    footer {
      background-color: #004080;
      color: white;
      text-align: center;
      padding: 10px 0;
      position: relative;
      bottom: 0;
      width: 100%;
    }

    /* Sección de testimonios */
    .testimonials-container {
      padding: 20px;
      text-align: center;
      background-color: #e8f0fe;
      border: 1px solid #004080;
      margin: 10px;
      border-radius: 8px;
    }

    /* Sección de contacto */
    .contact-form {
      padding: 20px;
      background-color: #fff;
      border: 1px solid #004080;
      border-radius: 5px;
      margin: 20px 0;
    }

    /* Botón de envío */
    .button {
      display: inline-block;
      padding: 10px 15px;
      color: white;
      background-color: #004080;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.2s ease;
    }

    .button:hover {
      background-color: #00264d;
    }
  </style>
</head>

<body>
  <!-- Encabezado -->
  <header>
    <h1>Nakao Inc.</h1>
    <p>Especialistas en instalación, ensamblaje y soporte técnico para PC</p>
  </header>

  <!-- Barra de búsqueda -->
  <div class="search-bar">
    <input type="text" id="searchInput" placeholder="Buscar servicios..." oninput="filterCards()" />
  </div>

  <!-- Contenedor Principal de Servicios -->
  <div class="container" id="cardContainer">
    <div class="card">
      <h3>💻 Instalación de Windows</h3>
      <ul>
        <li>Windows 10: <strong>Bs 250</strong></li>
        <li>Windows 11: <strong>Bs 250</strong></li>
        <li>Configuración inicial: <strong>Bs 20</strong></li>
      </ul>
    </div>
    <div class="card">
      <h3>🖥 Ensamblaje de PC</h3>
      <ul>
        <li>Asesoría de componentes: <strong>Bs 100</strong></li>
        <li>Montaje completo: <strong>Bs 300</strong></li>
      </ul>
    </div>
    <div class="card">
      <h3>🔧 Soporte Técnico</h3>
      <ul>
        <li>Diagnóstico de hardware: <strong>Bs 150</strong></li>
        <li>Reparación de software: <strong>Bs 200</strong></li>
      </ul>
    </div>
  </div>

  <!-- Sección de Testimonios -->
  <div class="testimonials-container">
    <h2>🌟 Testimonios de Clientes</h2>
    <p>"¡Excelente servicio! Recomiendo Nakao Inc. para cualquier necesidad de soporte técnico." - Cliente Satisfecho</p>
    <p>"El ensamblaje fue rápido y profesional. ¡Muy contento con mi nueva PC!" - Otro Cliente</p>
  </div>

  <!-- Sección de Contacto -->
  <div class="contact-form">
    <h3>📧 Contáctanos</h3>
    <form action="#" method="post">
      <label for="name">Nombre:</label><br />
      <input type="text" id="name" name="name" required /><br />
      <label for="email">Correo Electrónico:</label><br />
      <input type="email" id="email" name="email" required /><br />
      <label for="message">Mensaje:</label><br />
      <textarea id="message" name="message" rows="4" style="width: 100%;" required></textarea><br />
      <button type="submit" class="button">Enviar Mensaje</button>
    </form>
  </div>

  <!-- Pie de página -->
  <footer>
    <p>&copy; 2024 Nakao Inc. | Todos los derechos reservados.</p>
  </footer>

  <script>
    function filterCards() {
      const input = document.getElementById("searchInput").value.toLowerCase();
      const cards = document.querySelectorAll(".card");

      cards.forEach(card => {
        const title = card.querySelector("h3").textContent.toLowerCase();
        if (title.includes(input)) {
          card.style.display = "block";
        } else {
          card.style.display = "none";
        }
      });
    }
  </script>
</body>

</html>
