# cespedverde.github.io
Servicio de Jardinería
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Servicios de Jardinería</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Servicios de Jardinería</h1>
        <nav>
            <ul>
                <li><a href="#about">Nosotros</a></li>
                <li><a href="#services">Servicios</a></li>
                <li><a href="#contact">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <section id="about">
        <h2>Sobre Nosotros</h2>
        <p>Somos una empresa dedicada a proporcionar servicios de jardinería de alta calidad. Nuestro equipo está compuesto por profesionales con años de experiencia en el cuidado y mantenimiento de jardines.</p>
    </section>

    <section id="services">
        <h2>Servicios</h2>
        <ul>
            <li>Mantenimiento de jardines</li>
            <li>Poda de árboles y arbustos</li>
            <li>Diseño de jardines</li>
            <li>Instalación de sistemas de riego</li>
        </ul>
    </section>

    <section id="contact">
        <h2>Contacto</h2>
        <form id="contact-form">
            <label for="name">Nombre:</label>
            <input type="text" id="name" name="name" required>
            <label for="email">Correo electrónico:</label>
            <input type="email" id="email" name="email" required>
            <label for="message">Mensaje:</label>
            <textarea id="message" name="message" required></textarea>
            <button type="submit">Enviar</button>
        </form>
        <div id="form-response"></div>
    </section>

    <footer>
        <p>&copy; 2024 Servicios de Jardinería. Todos los derechos reservados.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f9;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 1em 0;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 1em;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

section {
    padding: 2em;
    margin: 1em auto;
    max-width: 800px;
    background: white;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h2 {
    color: #4CAF50;
}

form {
    display: flex;
    flex-direction: column;
}

form label {
    margin: 0.5em 0 0.2em;
}

form input, form textarea {
    padding: 0.5em;
    margin-bottom: 1em;
    border: 1px solid #ccc;
    border-radius: 4px;
}

form button {
    background-color: #4CAF50;
    color: white;
    padding: 0.7em;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

form button:hover {
    background-color: #45a049;
}

footer {
    text-align: center;
    padding: 1em 0;
    background-color: #333;
    color: white;
}
document.getElementById('contact-form').addEventListener('submit', function(event) {
    event.preventDefault();

    var name = document.getElementById('name').value;
    var email = document.getElementById('email').value;
    var message = document.getElementById('message').value;

    var response = document.getElementById('form-response');
    response.innerHTML = `<p>Gracias, ${name}. Hemos recibido tu mensaje y nos pondremos en contacto contigo pronto.</p>`;
});
