<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Migas Crunch - Disfruta de los mejores combos de Migas Tolimenses en Colombia. ¡Deléitate con la tradición colombiana!">
  <meta name="keywords" content="Migas Tolimenses, cocina colombiana, comida típica, combos, restaurante, Tena Cundinamarca">
  <meta name="author" content="Migas Crunch">
  <title>Migas Crunch</title>
  <style>
    /* General */
    body {
      font-family: 'Arial', sans-serif;
      font-size: 16px;
      line-height: 1.5;
      margin: 0;
      padding: 0;
      background-color: #f0f0f0;
      color: #333;
    }
  
    header, footer {
      background-color: #333;
      color: #fff;
      text-align: center;
      padding: 20px;
    }
  
    footer p {
      margin: 0;
    }
  
    main {
      margin: 30px;
    }
  
    h1, h2 {
      color: #0066cc;
      font-family: 'Helvetica', sans-serif;
      font-weight: bold;
      margin-bottom: 15px;
    }
  
    /* Estilos para el área de contacto */
    .contacto-superior {
      display: flex;
      justify-content: space-between;
      background-color: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      font-size: 14px;
      margin-bottom: 30px;
    }
  
    .contacto-superior div {
      flex: 1;
    }
  
    .contacto-superior img {
      max-width: 230px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
  
    /* Estilos del formulario */
    form {
      background-color: #fff;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      max-width: 600px;
      margin: 0 auto;
    }
  
    label {
      font-weight: bold;
      margin-bottom: 5px;
      display: inline-block;
    }
  
    input[type="text"], input[type="email"], textarea {
      width: 100%;
      padding: 15px;
      margin-bottom: 20px;
      border: 1px solid #ddd;
      border-radius: 8px;
      font-size: 16px;
      transition: border-color 0.3s ease;
    }
  
    input[type="text"]:focus, input[type="email"]:focus, textarea:focus {
      border-color: #0066cc;
      outline: none;
    }
  
    input[type="submit"] {
      background-color: #28a745;
      color: white;
      padding: 12px 25px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 18px;
      transition: background-color 0.3s ease;
      width: 100%;
    }
  
    input[type="submit"]:hover {
      background-color: #218838;
    }
  
    /* Estilo para los productos */
    #productos ul {
      list-style-type: none;
      padding: 0;
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: space-around;
    }
  
    #productos li {
      background-color: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      width: 45%;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
  
    #productos li:hover {
      transform: translateY(-10px);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    }
  
    /* Mejoras de responsividad */
    @media (max-width: 768px) {
      .contacto-superior {
        flex-direction: column;
        align-items: center;
        padding: 10px;
      }
  
      .contacto-superior img {
        max-width: 100%;
        margin-left: 0;
        margin-top: 20px;
      }
  
      form {
        padding: 20px;
      }
  
      #productos ul {
        display: flex;
        flex-direction: column;
        align-items: center;
      }
  
      #productos li {
        width: 90%;
        margin-bottom: 20px;
      }
  
      h1, h2 {
        font-size: 1.5em;
      }
    }
  
    /* Estilos para el chatbot */
    #chatbot {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 1000;
    }
  
    #chatbot button {
      background-color: #0066cc;
      color: white;
      border: none;
      border-radius: 50%;
      padding: 20px;
      font-size: 20px;
      cursor: pointer;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      transition: background-color 0.3s ease;
    }
  
    #chatbot button:hover {
      background-color: #004d99;
    }
  
    /* Ventana del chat */
    .chat-window {
      position: fixed;
      bottom: 80px;
      right: 20px;
      width: 320px;
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      display: none;
      flex-direction: column;
      overflow: hidden;
    }
  
    .chat-header {
      background-color: #333;
      color: white;
      padding: 12px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  
    .chat-messages {
      padding: 15px;
      max-height: 200px;
      overflow-y: auto;
    }
  
    .message {
      padding: 10px;
      border-radius: 6px;
      margin-bottom: 15px;
      font-size: 14px;
    }
  
    .message.bot {
      background-color: #f1f1f1;
    }
  
    .message.user {
      background-color: #28a745;
      color: white;
    }
  
    input[type="text"] {
      padding: 12px;
      width: calc(100% - 24px);
      margin-bottom: 10px;
      border: 1px solid #ddd;
      border-radius: 6px;
    }
  
    button {
      background-color: #28a745;
      color: white;
      padding: 12px 20px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 16px;
      transition: background-color 0.3s ease;
    }
  
    button:hover {
      background-color: #218838;
    }

    /* Ajuste al tamaño del logo */
    #logo {
      max-width: 150px;  /* Ajusta el tamaño máximo del logo */
      height: auto;      /* Mantiene las proporciones originales */
    }
  </style>
</head>
<body>
  <header>
    <img src="logo123.png" alt="Logo de Migas Crunch" id="logo">
    <h1>Migas Crunch</h1>
  </header>

  <div class="contacto-superior" aria-label="Información de contacto">
    <div>
      <p>Teléfono: +57 3134867182</p>
      <p>Correo electrónico: <a href="mailto:info@migascrunch.com" aria-label="Enviar un correo a Migas Crunch">info@migascrunch.com</a></p>
      <p>Dirección: La Gran Vía Km 3 Gallineral, Tena Cundinamarca, Colombia</p>
    </div>
    <div>
      <img src="https://www.lacocinadepili.com/img/como-hacer-migas-tradicionales-345.jpg" alt="Migas Tolimenses">
    </div>
  </div>

  <main>
    <section id="inicio">
      <h1>Bienvenidos a Migas Crunch</h1>
      <p>Las Migas son un producto gastronómico delicioso y tradicional que te transportará a la esencia de la cocina colombiana.</p>
    </section>

    <section id="productos">
      <h1>Nuestros combos todo a $20.000</h1>
      <ul>
        <li>Combo Clásico: Migas Tolimenses, Café o Chocolate caliente, Frutas frescas.</li>
        <li>Combo Colombiano: Migas Tolimenses, Arepa o Pandebono, Queso fresco o cuajada, Café o Jugo de frutas.</li>
        <li>Combo Dulce: Migas Tolimenses, Helado de vainilla o chocolate, Salsa de caramelo o chocolate, Frutas frescas.</li>
        <li>Combo Salado: Migas Tolimenses, Queso rallado o queso crema, Chorizo o salchicha, Salsa de ají o salsa de tomate.</li>
        <li>Combo Vegetariano: Migas Tolimenses, Ensalada de lechuga, tomate y pepino, Queso fresco o cuajada, Jugo de frutas o té herbal.</li>
        <li>Combo Especial: Migas Tolimenses, Huevo revuelto o huevo frito, Tocineta o chorizo, Pan tostado o arepa.</li>
      </ul>
    </section>

    <section id="blog">
      <h1>El rincón de Migas</h1>
      <article>
        <p>Las Migas Tolimenses son un delicioso y tradicional producto gastronómico de la región del Tolima, Colombia. Estas migas son una mezcla perfecta de sabores y texturas que te transportarán a la esencia de la cocina colombiana.</p>
        <p><strong>Ingredientes de alta calidad:</strong> Harina de trigo, Plátano maduro, Chicharrón, Queso rallado, Cebolla, Ajo, Aceite vegetal, Sal y pimienta.</p>
        <p><strong>Beneficios:</strong> Las Migas Tolimenses son una excelente fuente de carbohidratos y energía, ideales para vegetarianos y veganos, sin gluten ni lactosa.</p>
      </article>
    </section>

    <section id="mision-vision">
      <h1>Misión y Visión</h1>
      <h2>Misión:</h2>
      <p>Nuestra misión es ofrecer una experiencia gastronómica auténtica a través de nuestros productos, destacando la calidad y frescura en cada porción. Nos comprometemos a preservar la tradición de la cocina colombiana, en particular las Migas Tolimenses, brindando un servicio amable y accesible que fomente el bienestar de nuestros clientes. Además, buscamos apoyar a la economía local, utilizando ingredientes frescos de la región y promoviendo el desarrollo de pequeños productores.</p>
      <h2>Visión:</h2>
      <p>Ser la marca líder en la creación y comercialización de productos gastronómicos tradicionales de Colombia, reconocida por su calidad, innovación y contribución al fortalecimiento de las costumbres culinarias del país. Nuestra visión es expandir nuestras operaciones a nivel nacional e internacional, llevando nuestras migas tolimesas a más personas, mientras continuamos ofreciendo un servicio excepcional y manteniendo nuestros valores de responsabilidad social y ambiental.</p>
    </section>

    <section id="contacto">
      <h1>¡Contáctanos!</h1>
      <form action="#">
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required>

        <label for="email">Correo electrónico:</label>
        <input type="email" id="email" name="email" required>

        <label for="mensaje">Mensaje:</label>
        <textarea id="mensaje" name="mensaje" rows="4" required></textarea>

        <input type="submit" value="Enviar mensaje">
      </form>
    </section>
  </main>

  <!-- Chatbot -->
  <div id="chatbot" class="chatbot-button">
    <button id="openChat">🗨️</button>
  </div>

  <div id="chatWindow" class="chat-window">
    <div class="chat-header">
      <h3>Chat con nosotros</h3>
      <button id="closeChat">X</button>
    </div>
    <div id="chatMessages" class="chat-messages">
      <div class="message bot">¡Hola! ¿En qué puedo ayudarte hoy?</div>
    </div>
    <input type="text" id="userMessage" placeholder="Escribe tu mensaje..." />
    <button id="sendMessage">Enviar</button>
  </div>

  <footer>
    <p>&copy; 2025 Migas Crunch. Todos los derechos reservados.</p>
    <!-- Reproductor de audio -->
    <audio controls autoplay>
      <source src="audio123.wav" type="audio/mp3">
      Tu navegador no soporta el elemento de audio.
    </audio>
  </footer>

  <script>
    // Abrir el chat al hacer clic en el botón
    document.getElementById("openChat").addEventListener("click", function() {
      document.getElementById("chatWindow").style.display = "flex";
    });

    // Cerrar el chat al hacer clic en el botón de cerrar
    document.getElementById("closeChat").addEventListener("click", function() {
      document.getElementById("chatWindow").style.display = "none";
    });

    // Enviar mensaje
    document.getElementById("sendMessage").addEventListener("click", function() {
      var userMessage = document.getElementById("userMessage").value;
      if (userMessage.trim() !== "") {
        var chatMessages = document.getElementById("chatMessages");
        
        // Mensaje del usuario
        var userDiv = document.createElement("div");
        userDiv.classList.add("message", "user");
        userDiv.textContent = userMessage;
        chatMessages.appendChild(userDiv);
        
        // Respuesta automática del bot
        var botDiv = document.createElement("div");
        botDiv.classList.add("message", "bot");
        botDiv.textContent = "¡Gracias por tu mensaje! Nuestro equipo se pondrá en contacto contigo pronto.";
        chatMessages.appendChild(botDiv);
        
        // Limpiar el campo de texto
        document.getElementById("userMessage").value = "";

        // Desplazar el chat hacia abajo
        chatMessages.scrollTop = chatMessages.scrollHeight;
      } else {
        alert("Por favor ingresa un mensaje antes de enviarlo.");
      }
    });
  </script>
</body>
</html>
