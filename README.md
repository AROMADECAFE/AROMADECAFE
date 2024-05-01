<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jardín Aroma de Café</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Encabezado con el logotipo -->
    <header>
        <img src="logo.png" alt="Logo Jardín Aroma de Café">
    </header>

    <!-- Contenido principal -->
    <div class="main-content">
        <!-- Pestañas de navegación -->
        <nav>
            <ul>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#que-ofrecemos">¿Qué ofrecemos?</a></li>
                <li><a href="#programas">Programas</a></li>
            </ul>
        </nav>

        <!-- Sección ¿Qué ofrecemos? -->
        <section id="que-ofrecemos">
            <h2>Menú de Cafés</h2>
            <ul>
                <li>Expresso</li>
                <li>Macchiato</li>
                <li>Americano</li>
                <!-- Agrega más elementos del menú aquí -->
            </ul>

            <h2>Catálogo de Bouquets</h2>
            <ul>
                <li>Bouquet Lily's</li>
                <li>Bouquet Afí</li>
                <!-- Agrega más tipos de bouquets aquí -->
            </ul>
        </section>

        <!-- Sección Nosotros -->
        <section id="nosotros">
            <h2>Misión, Visión y Valores</h2>
            <h3>Misión</h3>
            <p>Superar las expectativas de nuestros clientes en experiencia y servicio...</p>
            <h3>Visión</h3>
            <p>Convertirnos en un referente reconocido por nuestra calidad y calidez...</p>
            <h3>Valores</h3>
            <ul>
                <li>Responsabilidad social</li>
                <li>Compromiso</li>
                <li>Hospitalidad</li>
                <li>Sostenibilidad</li>
                <li>Transparencia</li>
            </ul>
        </section>

        <!-- Sección Programas -->
        <section id="programas">
            <h2>Programas de Voluntariado</h2>
            <p>Participa en nuestras actividades de servicio local...</p>
        </section>
    </div>

    <!-- Pie de página con información de contacto -->
    <footer>
        <div class="contact-info">
            <p>Instagram: j.aromacafe</p>
            <p>Ubicación: Aruba 23819_B2, Villa Delsol I, 22205 Tijuana, B.C.</p>
            <p>Teléfono: 664-629-4423</p>
        </div>
    </footer>
</body>
</html>
body {
    background-color: #D3D3D3; /* Pantone 11-4201 Cloud Dancer */
    font-family: 'Lexend', sans-serif;
    color: #000;
    margin: 0;
    padding: 0;
}

header {
    padding: 20px;
}

nav {
    background-color: #7BAF9E; /* Pantone 14-6007 Sea Foam */
}

nav ul {
    list-style-type: none;
    display: flex;
    justify-content: space-around;
    padding: 10px 0;
}

nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
}

.main-content {
    padding: 20px;
}

section {
    margin-bottom: 30px;
}

footer {
    background-color: #7BAF9E; /* Pantone 14-6007 Sea Foam */
    color: #fff;
    padding: 20px;
    text-align: center;
}
// JavaScript para manejar pestañas de navegación

// Obtener referencias a las pestañas y contenido asociado
const tabButtons = document.querySelectorAll('.tab-button');
const tabContents = document.querySelectorAll('.tab-content');

// Asignar evento de clic a cada pestaña
tabButtons.forEach((button, index) => {
  button.addEventListener('click', () => {
    // Ocultar todo el contenido
    tabContents.forEach(content => {
      content.style.display = 'none';
    });

    // Mostrar solo el contenido correspondiente a la pestaña seleccionada
    tabContents[index].style.display = 'block';
  });
});
// JavaScript para validar formulario de reservación

const reservaForm = document.getElementById('reserva-form');

reservaForm.addEventListener('submit', (event) => {
  // Validar que se haya seleccionado al menos un taller
  const talleresSeleccionados = document.querySelectorAll('input[name="taller"]:checked');
  if (talleresSeleccionados.length === 0) {
    alert('Por favor selecciona al menos un taller.');
    event.preventDefault(); // Evitar enviar el formulario si no hay talleres seleccionados
  }
});
// JavaScript para inicializar FullCalendar y mostrar eventos

document.addEventListener('DOMContentLoaded', () => {
  const calendarEl = document.getElementById('calendar');

  const calendar = new FullCalendar.Calendar(calendarEl, {
    initialView: 'dayGridMonth', // Vista inicial del calendario
    events: [
      {
        title: 'Taller de Pintura',
        start: '2024-05-10',
        end: '2024-05-10',
      },
      {
        title: 'Taller de Catas de Café',
        start: '2024-05-15',
        end: '2024-05-15',
      },
      // Agregar más eventos aquí...
    ],
  });

  calendar.render(); // Renderizar el calendario
});
