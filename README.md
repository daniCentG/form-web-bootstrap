**Formulario de Registro**

**AQUÍ una demo rápida del proyecto:** https://danicentg.github.io/form-web-bootstrap/

Este proyecto consiste en un formulario de registro moderno con íconos interactivos y animaciones, utilizando tecnologías web actuales. El objetivo es ofrecer una interfaz visualmente atractiva y responsiva-dinámica para la captura de datos de usuarios.
Tecnologías Utilizadas

    HTML5: Para la estructura del contenido.
    CSS3: Para el diseño y las animaciones.
        Uso de keyframes para animaciones.
        backdrop-filter para efectos de transparencia.
        Gradientes y box-shadow para estilos visuales.
    Bootstrap 5: Para los componentes de diseño como el grid layout y los botones.
    Font Awesome: Para los íconos de usuario, correo, teléfono y otros elementos visuales.
    Google Fonts y CDN: Para obtener fuentes e íconos de manera rápida y eficiente.

**Estructura del Proyecto**

El proyecto tiene dos archivos principales:

    index.html: El archivo HTML que contiene la estructura del formulario.
    style.css: El archivo CSS que se encarga de estilizar el formulario y controlar las animaciones.

**Explicación de las Partes Clave del Código**
1. Estructura HTML

**html**

<form class="form-container text-center" autocomplete="off">
    <div class="mb-3 position-relative">
        <input type="text" class="form-control rounded-pill px-4 py-3" placeholder="Nombres y Apellidos">
        <i class="fa-solid fa-user icon"></i>
    </div>
    <!-- Más campos de formulario aquí -->
    <button type="submit" class="btn btn-primary w-50 rounded-pill py-3">Enviar</button>
</form>

Este código define un formulario simple con varios campos de entrada, incluyendo nombres, contraseñas, correo electrónico y teléfono. Cada input tiene asociado un ícono mediante Font Awesome para mejorar la experiencia del usuario. Se utiliza la clase form-control de Bootstrap para aplicar estilos predeterminados.

2. Diseño y Animaciones en CSS

El archivo CSS define varios estilos personalizados que mejoran la apariencia del formulario, añadiendo efectos visuales y animaciones. Entre los aspectos más importantes destacan:
Gradiente de Fondo

**css**

body {
    background: linear-gradient(180deg, #00597c 0%, #333333 100%);
}

Se utiliza un gradiente de dos tonos para crear un fondo dinámico.
Estilo de Inputs

**css**

.form-control {
    background-color: transparent !important;
    border: 2px solid #56ccf2;
    color: #ffffff !important;
    transition: border-color 0.3s ease;
}
.form-control:focus {
    border-color: #42f5a1;
    outline: none;
}

Cada campo de entrada tiene un borde de color personalizable que cambia cuando se sitúa el foco (focus). Esto proporciona retroalimentación visual al usuario.
Animaciones de los Íconos

**css**

@keyframes iconRotate {
    from {
        transform: translateY(-50%) rotate(0deg);
    }
    to {
        transform: translateY(-50%) rotate(360deg); /* Giramos el icono completamente */
    }
}

Cada ícono asociado a los inputs tiene una animación que lo hace rotar cuando el usuario enfoca el campo. Esta animación utiliza @keyframes y la propiedad transform para rotar los íconos en 360 grados, dándole una sensación de interactividad al formulario.
Botones con Estilo Personalizado

**css**

.btn-primary { 
    background-color: #0e8e93 !important;
    border: none;
    transition: background-color 0.3s ease;
    color: #ffffff;
    box-shadow: 0 15px 32px rgba(0, 0, 0, 0.3);
}
.btn-primary:hover {
    background-color: #799f89 !important;
}

Se aplica un estilo personalizado al botón submit para modificar el color de fondo, las sombras y su apariencia al hacer hover.
3. Interacción de los Íconos

El ícono correspondiente a cada input se anima con diferentes efectos al recibir el foco. Estas animaciones mejoran la interacción visual y hacen que la interfaz sea más atractiva:

**css**

.form-control:focus + .icon {
    animation: iconRotate 0.5s forwards;
}

*Esta regla CSS aplica la animación iconRotate cuando un input es enfocado, rotando el ícono al enfocarse.*
*Instalación y Uso*

    Clona el repositorio o descarga el código.
    Abre el archivo index.html en cualquier navegador web moderno.
    Disfruta de la interacción :)

**Futuras Mejoras**

    Validación de formulario con JavaScript para garantizar que los datos ingresados sean correctos.
    Uso de localStorage o sessionStorage para mantener los datos del formulario entre sesiones.
    Implementación de mensajes de error para mejorar la usabilidad.
