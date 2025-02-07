<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Death Note</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        /* Estilo General */
        body {
            margin: 0;
            font-family: 'Raleway', sans-serif;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('C:/Users/PC/Desktop/diseño/fon9.jpg') no-repeat center center fixed;
            background-size: cover;
            color: #fff;
            scroll-behavior: smooth;
        }

        header {
            background-color: rgba(0, 0, 0, 0.8);
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
            padding: 10px 0;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            transition: background 0.3s ease;
        }

        header:hover {
            background-color: rgba(0, 0, 0, 0.9);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        h1 {
            margin: 0;
            font-size: 2.5rem;
            text-align: center;
            color: #f00;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
        }

        /* Navegación */
        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            margin: 0;
            padding: 0;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            text-decoration: none;
            color: #fff;
            font-weight: bold;
            transition: color 0.3s ease, transform 0.2s ease;
        }

        nav ul li a:hover {
            color: #f00;
            transform: scale(1.1);
        }

      /* Secciones */
.section {
    padding: 100px 20px;
    text-align: center;
    scroll-margin-top: 0; /* Ajusta el margen al desplazarse */
    background: rgba(0, 0, 0, 0.6);
    border-radius: 10px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.4);
    transition: transform 0.3s ease;
    margin-top: 0; /* Elimina el espacio superior */
    margin-bottom: 0; /* Elimina el espacio inferior */
}


        .section:hover {
            transform: translateY(-10px);
        }

        h2 {
            font-size: 2rem;
            color: #f00;
            text-shadow: 1px 1px 3px #000;
        }

        p {
            line-height: 1.8;
            font-size: 1.1rem;
        }

        /* Botón Volver al Inicio */
        .back-to-top {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            background: #f00;
            color: #fff;
            text-decoration: none;
            border-radius: 5px;
            transition: transform 0.3s, background 0.3s ease;
        }

        .back-to-top:hover {
            background: #900;
            transform: scale(1.1);
        }

        /* Galería */
        .carousel img {
            width: 200px;
            height: auto;
            border-radius: 10px;
            margin: 10px;
            transition: transform 0.5s ease, box-shadow 0.5s ease;
        }

        .carousel img:hover {
            transform: scale(1.1);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.7);
        }

        marquee {
            margin: 20px 0;
        }

        /* Videos */
        .video-container iframe {
            border: none;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.6);
            transition: transform 0.3s ease;
        }

        .video-container iframe:hover {
            transform: scale(1.05);
        }

        /* Footer */
        footer {
            background-color: rgba(0, 0, 0, 0.9);
            text-align: center;
            padding: 15px;
            margin-top: 30px;
        }

        footer p {
            margin: 0;
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Responsivo */
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
            }

            .carousel img {
                width: 100px;
            }
        }
        /*watsap*/
        {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        {
            
        }
        form {
            margin: 20px 0;
            width: 100%;
            max-width: 500px;
            padding: 20px;
            border: 1px solid #131313;
            border-radius: 5px;
            background-color: #0e0d0d;
        }
        label {
            display: block;
            margin-bottom: 10px;
            font-weight: bold;
        }
        input, select, button {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #aaa8a8;
            border-radius: 5px;
        }
        button {
            background-color: #25D366;
            color: white;
            font-size: 16px;
            cursor: pointer;
        }
        button:hover {
            background-color: #1da851;
        }
        iframe {
            width: 100%;
            height: 600px;
            border: none;
        }

      /* Estilo para tareas completadas */
li.completed {
    text-decoration: line-through;
    background-color: #111111; /* Fondo oscuro para tareas completadas */
    color: #fff; /* Texto blanco para mejor contraste */
    padding: 10px; /* Añadido para separación uniforme */
    border-radius: 5px; /* Suavizar bordes */
    margin-bottom: 5px; /* Espaciado entre tareas */
}

/* Botón para eliminar */
.remove-btn {
    background-color: #f44336; /* Color rojo vibrante */
    color: white; /* Texto blanco */
    border: none; /* Sin borde */
    padding: 5px 15px; /* Tamaño ajustado */
    cursor: pointer; /* Cursor pointer para interacción */
    border-radius: 5px; /* Bordes redondeados */
    transition: background-color 0.3s ease; /* Transición suave */
}

.remove-btn:hover {
    background-color: #d32f2f; /* Color más oscuro al pasar el cursor */
}

/* Botón para agregar tareas */
.add-btn {
    background-color: #4caf50; /* Verde vibrante */
    color: white; /* Texto blanco */
    border: none; /* Sin borde */
    padding: 15px; /* Tamaño más cómodo */
    cursor: pointer; /* Cursor pointer */
    width: 100%; /* Botón amplio */
    margin-top: 20px; /* Separación superior */
    border-radius: 5px; /* Bordes redondeados */
    font-size: 1.2rem; /* Fuente legible */
    transition: background-color 0.3s ease; /* Transición suave */
}

.add-btn:hover {
    background-color: #388e3c; /* Verde más oscuro al pasar el cursor */
}

/* Entrada de texto */
input[type="text"] {
    width: calc(100% - 20px); /* Ancho total menos márgenes */
    padding: 10px; /* Espaciado interno */
    margin-bottom: 10px; /* Separación inferior */
    border-radius: 5px; /* Bordes redondeados */
    border: 1px solid #ddd; /* Borde suave */
    font-size: 1rem; /* Tamaño de fuente legible */
    background-color: #fff; /* Fondo blanco */
    color: #333; /* Texto oscuro */
}

/* Mensaje de celebración */
.celebration {
    display: none; /* Oculto por defecto */
    text-align: center; /* Centrado */
    margin-top: 20px; /* Espaciado superior */
    font-size: 1.5rem; /* Tamaño de fuente grande */
    color: #4caf50; /* Verde vibrante */
    font-family: 'Chiller', serif; /* Fuente personalizada */
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2); /* Sombra ligera */
}

.celebration.show {
    display: block; /* Mostrar mensaje */
    animation: fadeIn 1s ease-in-out; /* Animación suave */
}

/* Animación para el mensaje de celebración */
@keyframes fadeIn {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}

/* Lista de tareas */
#task-list li {
    list-style: none; /* Sin viñetas */
    padding: 10px; /* Espaciado interno */
    margin-bottom: 5px; /* Separación entre elementos */
    border: 1px solid #ddd; /* Borde suave */
    border-radius: 5px; /* Bordes redondeados */
    background-color: #222; /* Fondo oscuro */
    color: white; /* Texto blanco */
    font-size: 1.2rem; /* Tamaño de fuente legible */
    display: flex; /* Alinear contenido */
    justify-content: space-between; /* Separación entre texto y botón */
    align-items: center; /* Centrado vertical */
}

/* Efecto al pasar el cursor por la lista */
#task-list li:hover {
    background-color: #333; /* Fondo más claro */
    transition: background-color 0.3s ease; /* Transición suave */
}

    </style>
</head>
<body>
    <!-- Inicio -->
    <div id="home"></div>

    <!-- Header -->
    <header>
        <!-- Contenedor principal del header -->
        <div class="container" style="display: flex; flex-direction: column; padding: 10px; gap: 10px;">
            <!-- Logo y título centrados -->
<div style="display: flex; align-items: center; justify-content: center; gap: 10px;">
    <img src="C:\Users\PC\Desktop\diseño\logo.jpg" alt="Logo Death Note" style="width: 50px; height: 50px; object-fit: cover; border-radius: 50%;">
    <h1 style="margin: 0; font-size: 1.8rem; font-family: 'Comic Sans MS', cursive;">Death Note</h1>
</div>

            <!-- Navegación y redes sociales -->
            <div style="display: flex; justify-content: space-between; align-items: center;">
                <!-- Navegación -->
                <nav>
                    <ul style="display: flex; gap: 15px; list-style: none; margin: 0; padding: 0;">
                        <li><a href="#about">Acerca de</a></li>
                        <li><a href="#links">Enlaces</a></li>
                        <li><a href="#gallery">Galería</a></li>
                        <li><a href="#videos">Videos</a></li>
                        <li><a href="#seccion-secundaria">Mas</a></li>
                        <li><a href="#google-sheet">Resumen temporadas</a></li>
                        <li><a href="#to-do">Death note</a></li>
                        <li><a href="#Whatsap">Whatsapp</a></li>
                    </ul>
                </nav>

                <!-- Íconos de redes sociales -->
                <div style="display: flex; gap: 10px;">
                    <a href="https://www.facebook.com" target="_blank" style="text-decoration: none;">
                        <img src="https://cdn-icons-png.flaticon.com/512/174/174848.png" alt="Facebook" style="width: 25px; height: 25px;">
                    </a>
                    <a href="https://wa.me" target="_blank" style="text-decoration: none;">
                        <img src="https://cdn-icons-png.flaticon.com/512/733/733585.png" alt="WhatsApp" style="width: 25px; height: 25px;">
                    </a>
                    <a href="https://www.instagram.com" target="_blank" style="text-decoration: none;">
                        <img src="https://cdn-icons-png.flaticon.com/512/174/174855.png" alt="Instagram" style="width: 25px; height: 25px;">
                    </a>
                </div>
            </div>
        </div>
    </header>
</body>


<!-- Script para mostrar la fecha y hora -->
<script>
    function updateDateTime() {
        const dateTimeElement = document.getElementById('date-time');
        const now = new Date();
        const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
        const formattedDate = now.toLocaleDateString('es-ES', options);
        const formattedTime = now.toLocaleTimeString('es-ES');
        dateTimeElement.textContent = `${formattedDate}, ${formattedTime}`;
    }

    // Actualizar la fecha y hora al cargar y cada segundo
    updateDateTime();
    setInterval(updateDateTime, 1000);
</script>

 <!-- About Section -->
<section id="about" class="section">
    <div class="container" style="display: flex; align-items: center; justify-content: center; gap: 20px; font-family: Arial, sans-serif;">

        <!-- Imagen izquierda -->
        <div class="image-container left" style="position: relative; order: 1;">
            <img src="C:\Users\PC\Desktop\diseño\i1.jpg" alt="Imagen izquierda" style="width: 300px; height: 300px; object-fit: cover; border-radius: 10px; border: 5px solid #fbb03b;">
            <div class="overlay" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; display: flex; align-items: center; justify-content: center; background-color: rgba(0, 0, 0, 0.6); color: white; opacity: 0; transition: opacity 0.3s ease;">
                <p>Light Yagami</p>
            </div>
        </div>

        <!-- Contenido central -->
        <div style="max-width: 600px; text-align: justify; text-align: center; font-family: 'Chiller', cursive; order: 2;">
            <h2 style="font-size: 2.5rem; animation: fadeInDown 1s ease;">Descubre el Mundo de Death Note</h2>
            <p style="font-size: 1.5rem; line-height: 1.8; color: #e23838; animation: fadeInUp 1s ease;">
                <strong>Death Note</strong> es una impactante serie de manga y anime que fusiona el suspenso psicológico con un toque sobrenatural. 
                La trama sigue a <strong>Light Yagami</strong>, un estudiante brillante que encuentra un cuaderno mágico, el <em>Death Note</em>, capaz de acabar con la vida de cualquier persona cuyo nombre sea escrito en él, siempre que visualice su rostro.
                <br><br>
                Su búsqueda por un mundo perfecto choca con el enigmático detective <strong>L</strong>, dando lugar a un juego de ingenio sin precedentes. 
            </p>
            
        </div>

        <!-- Imagen derecha -->
        <div class="image-container right" style="position: relative; order: 3;">
            <img src="C:\Users\PC\Desktop\diseño\i2.jpg" alt="Imagen derecha" style="width: 300px; height: 300px; object-fit: cover; border-radius: 10px; border: 5px solid #fbb03b;">
            <div class="overlay" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; display: flex; align-items: center; justify-content: center; background-color: rgba(0, 0, 0, 0.6); color: white; opacity: 0; transition: opacity 0.3s ease;">
                <p>Detective L</p>
            </div>
        </div>

    </div>
    <div style="text-align: center;">
        <a href="#home" class="back-to-top">Volver al inicio</a>
    </div>
</section>

<script>
    // Selecciona las imágenes
    const leftImage = document.querySelector('.image-container.left');
    const rightImage = document.querySelector('.image-container.right');

    // Función para intercambiar imágenes
    function swapImages() {
        // Intercambia el orden de las imágenes
        if (leftImage.style.order === "1") {
            leftImage.style.order = "3";
            rightImage.style.order = "1";
        } else {
            leftImage.style.order = "1";
            rightImage.style.order = "3";
        }
    }

    // Ejecuta la función cada 5 segundos
    setInterval(swapImages, 5000);
</script>




<!-- Links Section -->
<section id="links" class="section">
    <div class="container" style="max-width: 900px; margin: auto; font-family: Arial, sans-serif;">

        <h2 style="text-align: center; margin-bottom: 20px;">Enlaces para más contenidos en la web</h2>

        <div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px;">

            <!-- Enlace 1 -->
            <div style="text-align: left;">
                <a href="https://manga-y-anime.fandom.com/es/wiki/Death_Note" target="_blank" style="
                    display: inline-block;
                    padding: 12px 20px;
                    background: #1abc9c;
                    color: white;
                    font-size: 1.1rem;
                    font-weight: bold;
                    text-decoration: none;
                    border-radius: 25px;
                    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
                    transition: all 0.3s ease-in-out;
                ">Wiki de Death Note - Manga y Anime</a>
                <p style="margin-top: 10px;">Explora información detallada sobre la serie, sus personajes, y su impacto en el mundo del anime.</p>
            </div>
            <img src="C:\Users\PC\Desktop\diseño\ima1.jpg" alt="Wiki de Death Note" style="width: 100%; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);">

            <!-- Enlace 2 -->
            <img src="C:\Users\PC\Desktop\diseño\ima2.jpg" alt="Techopedia" style="width: 100%; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);">
            <div style="text-align: left;">
                <a href="https://www.techopedia.com/es/death-note-killer-within-fecha-lanzamiento" target="_blank" style="
                    display: inline-block;
                    padding: 12px 20px;
                    background: #3498db;
                    color: white;
                    font-size: 1.1rem;
                    font-weight: bold;
                    text-decoration: none;
                    border-radius: 25px;
                    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
                    transition: all 0.3s ease-in-out;
                ">Artículo en Techopedia</a>
                <p style="margin-top: 10px;">Lee un análisis sobre el impacto de Death Note y las teorías detrás de sus personajes y su narrativa.</p>
            </div>

            <!-- Enlace 3 -->
            <div style="text-align: left;">
                <a href="https://www.imdb.com/es/title/tt0877057/" target="_blank" style="
                    display: inline-block;
                    padding: 12px 20px;
                    background: #9b59b6;
                    color: white;
                    font-size: 1.1rem;
                    font-weight: bold;
                    text-decoration: none;
                    border-radius: 25px;
                    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
                    transition: all 0.3s ease-in-out;
                ">Death Note en IMDb</a>
                <p style="margin-top: 10px;">Consulta la calificación y las opiniones de los fanáticos sobre Death Note en una de las bases de datos más populares.</p>
            </div>
            <img src="C:\Users\PC\Desktop\diseño\ima3.jpg" alt="IMDb" style="width: 100%; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);">

        </div>

        <div style="text-align: center;">
            <a href="#home" class="back-to-top">Volver al inicio</a>
        </div>

    </div>
</section>

<!-- Agregar estilos de hover -->
<style>
    #links a:hover {
        transform: translateY(-5px);
        box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
        opacity: 0.9;
    }
</style>


<!-- Galería -->
<section id="gallery" class="section">
    <div class="container">
        <h2>Galería</h2>
        <div class="carousel" style="text-align: center;">
            <marquee behavior="scroll" direction="left" scrollamount="5">
                <img src="C:/Users/PC/Desktop/diseño/logo.jpg" alt="Inicio de la serie" class="gallery-img" data-target="reseña-akira">
                <img src="C:/Users/PC/Desktop/diseño/akira.jpg" alt="Akira sintiéndose Dios" class="gallery-img" data-target="reseña-akira">
                <img src="C:/Users/PC/Desktop/diseño/L.jpg" alt="L descubre la verdad" class="gallery-img" data-target="reseña-L">
                <img src="C:/Users/PC/Desktop/diseño/akiravsl.jpg" alt="Comienza la caza de Akira" class="gallery-img" data-target="reseña-akira-vs-L">
                <img src="C:/Users/PC/Desktop/diseño/shinigamis.jpg" alt="Los Shinigamis observando a Akira" class="gallery-img" data-target="reseña-shinigamis">
                <img src="C:/Users/PC/Desktop/diseño/riuk.jpg" alt="Ryuk llegando a la tierra" class="gallery-img" data-target="reseña-ryuk">
                <img src="C:/Users/PC/Desktop/diseño/misa.jpg" alt="Misa posee otra Death Note" class="gallery-img" data-target="reseña-misa">
            </marquee>
        </div>
    </div>
    <div style="text-align: center;">
        <a href="#home" class="back-to-top">Volver al inicio</a>
    </div>
</section>

<!-- Reseñas de los personajes -->
<section id="reseñas" class="section" style="display: none;">
    <div class="container">
        <div id="reseña-akira" class="reseña-content">
            <h2>Reseña - Light Yagami (Kira)</h2>
            <p>Light Yagami es un estudiante brillante que encuentra el Death Note. Su objetivo es eliminar a los criminales y convertirse en el dios de un nuevo mundo. Su inteligencia lo convierte en un oponente formidable.</p>
        </div>
        <div id="reseña-L" class="reseña-content">
            <h2>Reseña - L</h2>
            <p>L es un detective mundialmente famoso que asume el desafío de atrapar a Kira. Su astucia e intuición lo convierten en uno de los personajes más icónicos de la serie.</p>
        </div>
        <div id="reseña-akira-vs-L" class="reseña-content">
            <h2>Reseña - El enfrentamiento entre Kira y L</h2>
            <p>La rivalidad entre Light y L es uno de los puntos más intensos de la serie, con ambos personajes intentando superarse mutuamente con movimientos calculados.</p>
        </div>
        <div id="reseña-shinigamis" class="reseña-content">
            <h2>Reseña - Los Shinigamis</h2>
            <p>Los Shinigamis son dioses de la muerte. Ryuk, uno de ellos, lanza el Death Note a la tierra por aburrimiento, desencadenando toda la trama.</p>
        </div>
        <div id="reseña-ryuk" class="reseña-content">
            <h2>Reseña - Ryuk</h2>
            <p>Ryuk es el Shinigami que deja caer el Death Note en el mundo humano. Acompaña a Light por diversión y muestra interés en los eventos que ocurren.</p>
        </div>
        <div id="reseña-misa" class="reseña-content">
            <h2>Reseña - Misa Amane</h2>
            <p>Misa es una devota seguidora de Kira y poseedora de otro Death Note. Su amor por Light la lleva a realizar actos decisivos en la trama.</p>
        </div>
        <a href="#gallery" id="back-to-gallery" class="back-to-top" style="display: block; text-align: center; margin-top: 20px;">Volver a la Galería</a>
    </div>
    <div style="text-align: center;">
        <a href="#home" class="back-to-top">Volver al inicio</a>
    </div>
</section>

<!-- Script para la funcionalidad -->
<script>
    // Variables
    const gallerySection = document.querySelector("#gallery");
    const reseñasSection = document.querySelector("#reseñas");
    const galleryImages = document.querySelectorAll(".gallery-img");
    const backToGallery = document.querySelector("#back-to-gallery");
    const reseñaContents = document.querySelectorAll(".reseña-content");

    // Mostrar reseña al hacer clic en una imagen
    galleryImages.forEach(image => {
        image.addEventListener("click", () => {
            const targetId = image.getAttribute("data-target");
            
            // Ocultar galería y mostrar reseñas
            gallerySection.style.display = "none";
            reseñasSection.style.display = "block";

            // Mostrar solo la reseña seleccionada
            reseñaContents.forEach(content => {
                content.style.display = content.id === targetId ? "block" : "none";
            });
        });
    });

    // Volver a la galería
    backToGallery.addEventListener("click", () => {
        // Mostrar galería y ocultar reseñas
        gallerySection.style.display = "block";
        reseñasSection.style.display = "none";
    });
</script>


<!-- Videos Section -->
<section id="videos" class="section" style="padding: 50px 0; background-color: #000;">
    <div class="container" style="max-width: 1200px; margin: 0 auto; color: #fff;">
        <h2 style="text-align: center; font-size: 2.5rem; margin-bottom: 20px;">Videos</h2>
        <div class="video-container" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; align-items: center;">
            <!-- Video 1 -->
            <div class="video-item" style="text-align: center;">
                <iframe 
                    width="100%" 
                    height="315" 
                    src="https://www.youtube.com/embed/paqZw3ZP32k" 
                    title="Opening de Death Note" 
                    frameborder="0" 
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                    allowfullscreen 
                    style="border-radius: 8px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);">
                </iframe>
                <p style="font-size: 1.2rem; margin-top: 10px;">Opening Oficial de Death Note</p>
            </div>
            <!-- Video 2 -->
            <div class="video-item" style="text-align: center;">
                <iframe 
                    width="100%" 
                    height="315" 
                    src="https://www.youtube.com/embed/mCpoWf8hBN0" 
                    title="Resumen del Anime" 
                    frameborder="0" 
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                    allowfullscreen 
                    style="border-radius: 8px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);">
                </iframe>
                <p style="font-size: 1.2rem; margin-top: 10px;">Resumen del Anime de Death Note</p>
            </div>
        </div>
        <div style="text-align: center; margin-top: 30px;">
            <a href="#home" class="back-to-top" style="text-decoration: none; color: #1e90ff; font-size: 1.2rem;">Volver al inicio</a>
        </div>
    </div>
</section>


<!-- Mas Section -->
<section id="seccion-secundaria" class="section">
    <div class="container" style="font-family: Arial, sans-serif; text-align: center;">

        <h2>Conoce más sobre Light Yagami y los personajes</h2>
        <p>Haz clic en los botones de abajo para ir a las páginas correspondientes:</p>

        <div class="button-container" style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px; margin-top: 20px;">
            <a href="subpagina.html" class="section-link" style="
                display: flex; align-items: center; gap: 10px;
                padding: 10px 20px; 
                background: #3498db; 
                color: white; 
                font-size: 1rem; 
                font-weight: bold; 
                text-decoration: none; 
                border-radius: 25px; 
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); 
                transition: transform 0.3s ease, background 0.3s ease;">
                <img src="C:\Users\PC\Desktop\diseño\log1.jpg" alt="Light Yagami" class="icon" style="
                    width: 30px; 
                    height: 30px; 
                    object-fit: cover; 
                    border-radius: 50%; 
                    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);">
                Light Yagami 1
            </a>
            <a href="subpagina2.html" class="section-link" style="
                display: flex; align-items: center; gap: 10px;
                padding: 10px 20px; 
                background: #e74c3c; 
                color: white; 
                font-size: 1rem; 
                font-weight: bold; 
                text-decoration: none; 
                border-radius: 25px; 
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); 
                transition: transform 0.3s ease, background 0.3s ease;">
                <img src="C:\Users\PC\Desktop\diseño\log2.jpg" alt="Ryuk" class="icon" style="
                    width: 30px; 
                    height: 30px; 
                    object-fit: cover; 
                    border-radius: 50%; 
                    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);">
                Ryuk 2
            </a>
            <a href="subpagina3.html" class="section-link" style="
                display: flex; align-items: center; gap: 10px;
                padding: 10px 20px; 
                background: #2ecc71; 
                color: white; 
                font-size: 1rem; 
                font-weight: bold; 
                text-decoration: none; 
                border-radius: 25px; 
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); 
                transition: transform 0.3s ease, background 0.3s ease;">
                <img src="C:\Users\PC\Desktop\diseño\log3.jpg" alt="L" class="icon" style="
                    width: 30px; 
                    height: 30px; 
                    object-fit: cover; 
                    border-radius: 50%; 
                    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);">
                L 3
            </a>
            <a href="subpagina4.html" class="section-link" style="
                display: flex; align-items: center; gap: 10px;
                padding: 10px 20px; 
                background: #9b59b6; 
                color: white; 
                font-size: 1rem; 
                font-weight: bold; 
                text-decoration: none; 
                border-radius: 25px; 
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); 
                transition: transform 0.3s ease, background 0.3s ease;">
                <img src="C:\Users\PC\Desktop\diseño\log4.jpg" alt="Misa" class="icon" style="
                    width: 30px; 
                    height: 30px; 
                    object-fit: cover; 
                    border-radius: 50%; 
                    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);">
                Misa 4
            </a>
            <a href="subpagina5.html" class="section-link" style="
                display: flex; align-items: center; gap: 10px;
                padding: 10px 20px; 
                background: #f1c40f; 
                color: white; 
                font-size: 1rem; 
                font-weight: bold; 
                text-decoration: none; 
                border-radius: 25px; 
                box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); 
                transition: transform 0.3s ease, background 0.3s ease;">
                <img src="C:\Users\PC\Desktop\diseño\log5.jpg" alt="Rem" class="icon" style="
                    width: 30px; 
                    height: 30px; 
                    object-fit: cover; 
                    border-radius: 50%; 
                    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);">
                Rem 5
            </a>
        </div>
    </div>
    <div style="text-align: center;">
        <a href="#home" class="back-to-top">Volver al inicio</a>
    </div>
</section>



<!-- Google Sheet Section -->
<section id="google-sheet" class="section">
    
        <h2 class="section-title" style="color: rgb(177, 31, 31); text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5); text-align: center; margin-bottom: 20px;">Tabla de Resumen del anime</h2>

        <div style="display: flex; justify-content: center; align-items: center;">
            <iframe 
                src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTqBOt6scCydDOz0A_iHdfDGsz_9upYa7qVITs7Ggm8ZLVRshyb5Idt-t12kxWjf4cDNAkPxC-s-7B1/pubhtml?gid=0&single=true" 
                width="600" 
                height="300" 
                frameborder="0" 
                style="border: 2px solid rgba(0, 0, 0, 0.3); border-radius: 10px;">
            </iframe>
        </div>
        <div style="text-align: center;">
            <a href="#home" class="back-to-top">Volver al inicio</a>
        </div>
    </div>
</section>
<br>
<br><br><br><br><br>


<!-- To Do Section -->
<section id="to-do" class="section" style="background-image: url('libreta.png'); background-size: cover; background-position: center; padding: 20px; border-radius: 10px;">
    <div class="container">
        <!-- Título con el estilo de la libreta -->
        <h1 style="color: rgb(224, 220, 220); text-shadow: 2px 2px 4px rgba(255, 255, 255, 0.7); font-family: 'Chiller', serif; font-size: 2.5rem;"></h1><br><br><br><br><br><br>
        <h1 style="color: rgb(224, 220, 220); text-shadow: 2px 2px 4px rgba(255, 255, 255, 0.7); font-family: 'Chiller', serif; font-size: 2.5rem;">Death Note</h1>
        <ul id="task-list" style="list-style: none; padding: 0; color: rgb(228, 225, 225); font-family: 'Chiller', serif; font-size: 1.5rem;">
            <li>Escribir un nuevo nombre en el Death Note </li>
            <li>Como debe morir? </li>
            <li>Hora de la muerte </li>
        </ul>

        <input type="text" id="new-task" placeholder="Nueva tarea de Death Note..." style="margin-top: 20px; padding: 10px; width: 60%; border: 2px solid #a5a8aa; border-radius: 5px; font-size: 1rem;">
        <button class="add-btn" onclick="addTask()" style="padding: 10px 20px; background: #da0808; color: white; border: none; border-radius: 5px; font-size: 1rem; margin-left: 10px; cursor: pointer;">Agregar Tarea</button>

        <div class="celebration" id="victory-message" style="display: none; color: rgb(112, 2, 2); font-size: 1.8rem; font-family: 'Chiller', serif; text-shadow: 2px 2px 4px rgba(255, 255, 255, 0.7); margin-top: 20px;">¡Todas las tareas completadas! El nuevo mundo está listo.</div>
    </div>
    <script>
        const taskList = document.getElementById('task-list');
        const victoryMessage = document.getElementById('victory-message');

        // Función para agregar tareas
        function addTask() {
            const taskText = document.getElementById('new-task').value;
            if (taskText.trim() === '') {
                return;
            }

            const li = document.createElement('li');
            li.textContent = taskText;
            const removeBtn = document.createElement('button');
            removeBtn.textContent = 'Eliminar';
            removeBtn.className = 'remove-btn';
            removeBtn.style.marginLeft = '10px';
            removeBtn.style.padding = '5px 10px';
            removeBtn.style.background = '#e74c3c';
            removeBtn.style.color = 'white';
            removeBtn.style.border = 'none';
            removeBtn.style.borderRadius = '5px';
            removeBtn.style.cursor = 'pointer';
            removeBtn.onclick = removeTask;
            li.appendChild(removeBtn);
            li.onclick = toggleComplete;
            li.style.fontFamily = "'Chiller', serif";
            li.style.fontSize = '1.5rem';
            li.style.color = 'White';

            taskList.appendChild(li);
            document.getElementById('new-task').value = '';

            checkVictory();
        }

        // Función para eliminar tareas
        function removeTask(event) {
            event.target.parentElement.remove();
            checkVictory();
        }

        // Función para marcar como completada una tarea
        function toggleComplete(event) {
            if (event.target.tagName === 'LI') {
                event.target.classList.toggle('completed');
                event.target.style.textDecoration = event.target.classList.contains('completed') ? 'line-through' : 'none';
                checkVictory();
            }
        }

        // Verificar si todas las tareas están completadas
        function checkVictory() {
            const tasks = taskList.getElementsByTagName('li');
            const allCompleted = Array.from(tasks).every(task => task.classList.contains('completed'));

            if (allCompleted && tasks.length > 0) {
                victoryMessage.style.display = 'block';
            } else {
                victoryMessage.style.display = 'none';
            }
        }
    </script>
     <div style="text-align: center;">
        <a href="#home" class="back-to-top">Volver al inicio</a>
    </div>
   
</section>


<!-- WhatsApp -->
<section id="Whatsap" class="section">
    <div class="container">
        <h1>Integración con WhatsApp</h1>
        <form id="whatsappForm">
            <label for="name">Nombre:</label>
            <input type="text" id="name" name="name" required placeholder="Ingresa tu nombre">
            
            <label for="phone">Número de celular:</label>
            <input type="tel" id="phone" name="phone" required placeholder="Ej: +591XXXXXXXXX">
            
            <label for="option">Elige una opción:</label>
            <select id="option" name="option" required>
                <option value="">Selecciona una opción</option>
                <option value="Agendar cita">Agendar cita</option>
                <option value="Reclamos"> Realizar un reclamo</option>
                <option value="Sugerencias">Mas informcion</option>
            </select>
            
            <button type="submit">Enviar</button>
        </form>
    </div>
    <div style="text-align: center;">
        <a href="#home" class="back-to-top">Volver al inicio</a>
    </div>

    <script>
        document.getElementById('whatsappForm').addEventListener('submit', function(e) {
            e.preventDefault();

            // Obtener valores del formulario
            const name = document.getElementById('name').value;
            const userPhone = document.getElementById('phone').value;
            const option = document.getElementById('option').value;

            if (!name || !userPhone || !option) {
                alert('Por favor, completa todos los campos.');
                return;
            }

            // Mensaje dinámico para WhatsApp
            const message = `Hola, soy ${name}. Mi número es ${userPhone}. Quiero ${option}.`;

            // Número de destino (tu número de WhatsApp)
            const whatsappNumber = "59175883458"; // Cambia este número por el tuyo (código de país incluido)

            // Crear el enlace de WhatsApp
            const whatsappUrl = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;

            // Redirigir automáticamente al enlace de WhatsApp
            window.location.href = whatsappUrl;
        });
    </script>
</section>




<!-- Footer -->
<footer style="background-color: #222; color: white; padding: 20px; text-align: center;">
    <p>&copy; 2024 Página de Javier Mantilla de Death Note</p>
</footer>


<!-- Smooth Scroll Script -->
<script>
document.querySelectorAll('.back-to-top').forEach(button => {
    button.addEventListener('click', function (event) {
        event.preventDefault();
        document.querySelector('#home').scrollIntoView({
            behavior: 'smooth'
        });
    });
});
</script>
</body>
</html>
