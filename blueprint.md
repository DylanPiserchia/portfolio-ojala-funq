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

*   **Sección de Proyectos (`<section id="projects">`):**
    *   **Diseño:** Un carrusel horizontal que permite a los usuarios desplazarse por los proyectos destacados.
    *   **Tarjetas de Proyecto:** Cada tarjeta tiene un diseño consistente con una imagen, título, descripción y un botón de "Ver" que enlaza a la página de detalle del proyecto.
    *   **Controles de Navegación del Carrusel:**
        *   **Posición:** Los botones de flecha están agrupados y ubicados "al norte" del carrusel, alineados a la izquierda.
        *   **Estilo de Botones:** Son círculos perfectos (`w-8 h-8 rounded-full`) con un fondo `bg-gray-700` que cambia a `hover:bg-gray-600`.
        *   **Estilo de Iconos:** Los iconos de flecha (`material-icons`) están centrados dentro de los botones (`flex items-center justify-center`) y tienen un tamaño de fuente `text-xl` para una apariencia proporcionada.

*   **Pie de Página (`<footer>`):**
    *   **Diseño:** Simple y limpio, con un borde superior para separarlo del contenido principal.
    *   **Contenido:** Incluye el aviso de copyright.

### **3. Interactividad (JavaScript)**
*   **Funcionalidad del Carrusel:** Se ha implementado un script simple que maneja el desplazamiento suave (`scroll-smooth`) del carrusel cuando se hace clic en los botones de flecha "anterior" y "siguiente".

---

## Plan de Implementación Actual

Esta sección describe el plan para la última solicitud de cambio realizada.

**Solicitud:** Reducir el tamaño de los botones de navegación del carrusel y sus iconos para una apariencia más proporcionada.

**Pasos de Implementación:**

1.  **Reducir Tamaño de Botones:** Se cambiaron las clases de tamaño de `w-12 h-12` a `w-8 h-8` para hacer los botones más pequeños.
2.  **Asegurar Forma Circular:** Se mantuvo la clase `rounded-full` para que sigan siendo círculos perfectos.
3.  **Centrar Iconos:** Se conservaron las clases `flex items-center justify-center` para mantener los iconos centrados.
4.  **Reducir Tamaño de Iconos:** Se añadió la clase `text-xl` a los `<span>` de los iconos para reducir su tamaño y hacer que encajen mejor en los botones más pequeños.
