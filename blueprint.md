# Blueprint: Portfolio de Diseñador de Videojuegos

## Visión General

Este documento detalla el diseño, la funcionalidad y la evolución de un portafolio web personal para Dylan Piserchia, un diseñador de videojuegos. El objetivo es crear un sitio moderno, visualmente atractivo y fácil de navegar que muestre de manera efectiva sus proyectos y su experiencia profesional.

---

## Esquema del Proyecto y Características Implementadas

Esta sección documenta el estado actual del proyecto, incluyendo todas las decisiones de diseño y las características implementadas hasta la fecha.

### **1. Estructura General y Estilo**
*   **Tecnologías:** HTML, Tailwind CSS para el diseño, y JavaScript para la interactividad.
*   **Paleta de Colores:** Un tema oscuro y moderno (`bg-gray-900`) con texto claro (`text-gray-200`) para un alto contraste y una apariencia profesional.
*   **Tipografía:** Se utiliza la fuente "Inter" de Google Fonts para una legibilidad clara y moderna.
*   **Iconografía:** Se emplea "Material Icons" para los iconos, como las flechas de navegación.
*   **Archivos Principales:**
    *   `index.html`: Página de inicio.
    *   `about.html`: Página "Acerca de mí".
    *   `style.css`: Hoja de estilos personalizada.
    *   Páginas de detalle para cada proyecto (ej. `star-trek-infinite.html`).

### **2. Componentes de la Interfaz**

*   **Encabezado (`<header>`):**
    *   **Diseño:** Fijo en la parte superior (`fixed`), con un fondo semitransparente y un efecto de desenfoque (`bg-opacity-80 backdrop-blur-md`) para que el contenido se desplace por debajo.
    *   **Navegación:** Incluye enlaces a "Home", "Projects" y "About".

*   **Sección Principal - Hero (`<section id="hero">`):**
    *   **Diseño:** Un diseño de dos columnas en pantallas de escritorio (`md:flex-row`).
    *   **Contenido Izquierdo:** Título principal con el nombre, una descripción profesional y un botón para descargar el currículum.
    *   **Contenido Derecho (Logo):**
        *   Se ha reemplazado la imagen de marcador de posición por el logo personal `DP_Logo.png`.
        *   El tamaño del logo se ha reducido en un 20% (`w-4/5`) y se ha centrado horizontalmente (`mx-auto`) para un mejor equilibrio visual.
        *   Se ha eliminado cualquier sombra (`shadow-2xl`) para un aspecto más limpio y plano.

*   **Sección de Proyectos (`<section id="projects">`):**
    *   **Diseño:** Un carrusel horizontal que permite a los usuarios desplazarse por los proyectos destacados.
    *   **Tarjetas de Proyecto:** Cada tarjeta tiene un diseño consistente con una imagen, título, descripción y un botón de "Ver" que enlaza a la página de detalle del proyecto.
    *   **Controles de Navegación del Carrusel:**
        *   **Posición:** Los botones de flecha (izquierda y derecha) están agrupados.
        *   **Ubicación:** Se encuentran "al norte" del carrusel, es decir, en un área separada justo debajo del título de la sección ("Featured Projects") y alineados a la izquierda. Esto evita que se superpongan con el contenido del carrusel.
        *   **Estilo:** Botones redondeados con un color de fondo sutil que cambia al pasar el ratón por encima (`hover:bg-gray-600`).

*   **Pie de Página (`<footer>`):**
    *   **Diseño:** Simple y limpio, con un borde superior para separarlo del contenido principal.
    *   **Contenido:** Incluye el aviso de copyright.

### **3. Interactividad (JavaScript)**
*   **Funcionalidad del Carrusel:** Se ha implementado un script simple que maneja el desplazamiento suave (`scroll-smooth`) del carrusel cuando se hace clic en los botones de flecha "anterior" y "siguiente".

---

## Plan de Implementación Actual

Esta sección describe el plan para la última solicitud de cambio realizada.

**Solicitud:** Mover las flechas de navegación del carrusel para que estén juntas y ubicadas arriba (al norte) del primer elemento, sin superponerse.

**Pasos de Implementación:**

1.  **Eliminar Posicionamiento Absoluto:** Se quitaron las clases de posicionamiento (`absolute`, `top-1/2`, `left-0`, `right-0`, etc.) de los botones de flecha para que dejen de superponerse al carrusel.
2.  **Crear un Contenedor para los Botones:** Se creó un nuevo `div` para agrupar los dos botones (`<button id="prevBtn">` y `<button id="nextBtn">`).
3.  **Ubicar el Contenedor:** Este nuevo `div` se colocó en el flujo normal del documento, específicamente entre el título `<h3>Featured Projects</h3>` y el `div` del carrusel.
4.  **Alinear a la Izquierda:** Se aplicaron clases de Flexbox (`flex justify-start`) al contenedor de los botones para alinearlos a la izquierda de la página.
5.  **Ajustar Márgenes:** Se añadió un margen inferior (`mb-4`) al contenedor de los botones para crear una separación visual adecuada con el carrusel que se encuentra debajo.
