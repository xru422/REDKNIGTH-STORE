# Red Knight Store - Plataforma E-commerce de Videojuegos Premium (Rojo y Negro)

Red Knight Store es una plataforma web moderna, rápida y responsiva para explorar, buscar, comparar, guardar y comprar videojuegos. Presenta una estética agresiva y elegante basada en un esquema de color **Rojo y Negro** con efectos de glassmorphism neón, inspirada en las marcas líderes del gaming.

El proyecto está diseñado bajo una arquitectura de **Single Page Application (SPA) con enrutamiento basado en hash (`#/`)**, utilizando tecnologías web estándar y limpias, garantizando modularidad, alto rendimiento (Lighthouse > 90) y accesibilidad (WCAG).

---

## 🚀 Tecnologías Utilizadas

*   **Estructura:** HTML5 Semántico y optimizado para SEO (Tags Open Graph, Twitter Cards, Schema.org JSON-LD).
*   **Estilos:** CSS3 Moderno (CSS Variables, Flexbox, CSS Grid, Transitions & Keyframe Animations).
*   **Lógica:** JavaScript Vanilla Moderno (ES6+, Clases, Módulos, Eventos, Fetch API, Async/Await y LocalStorage).
*   **Imágenes Reales de Videojuegos:** Integración directa de imágenes reales en alta resolución (portadas, banners y capturas) a través de CDNs de contenido oficial de Steam y Nintendo Switch.
*   **Offline Fallback:** Generador dinámico en JavaScript que renderiza portadas vectoriales en formato SVG Base64 si un recurso de red no estuviera disponible.

---

## 📁 Estructura del Proyecto

```text
/proyecto
│   index.html              # Archivo HTML principal con layout SPA semántico
│   robots.txt              # Configuración básica para rastreo de buscadores
│   sitemap.xml             # Mapeo de rutas dinámicas del sitio
│
├───css/
│       animations.css      # Transiciones neón, zoom de modales, preloader y scroll effects
│       responsive.css      # Puntos de quiebre para móviles, tablets y portátiles
│       styles.css          # Variables de diseño rojo/negro, reset, mega-menú y layout base
│
└───js/
        app.js              # Enrutador SPA de hash, IntersectionObserver y control de sesión
        cart.js             # Gestión del carrito, wishlist, totales y pasarela de pago (checkout)
        catalog.js          # Base de datos de 17 juegos, renderizador de grids y comparador técnico
        filters.js          # Motor de filtros cruzados de precio, género, marcas y ordenación
        modal.js            # Control unificado de modales, formularios y Lightbox de galería
        search.js           # Buscador predictivo en tiempo real con sugerencias rápidas
        slider.js           # Carrusel del Hero Banner con auto-reproducción y pausa por hover
```

---

## 🎨 Sistema de Diseño y Experiencia Premium

1.  **Esquema de Color Rojo y Negro:** Colores de fondo oscuros profundos (`#050508`) combinados con acentos en rojo neón/carmesí (`#ff003c`) y bordes de cristal rojo translúcidos.
2.  **Temas Dinámicos de Plataforma:** Las consolas (PlayStation, Xbox, Nintendo, PC) adaptan sus acentos visuales a variantes y tonos de rojo carmesí, rubí y coral, logrando una interfaz cohesiva y alineada con la marca.
3.  **Glassmorphism Premium:** Las tarjetas y menús flotantes emplean fondos translúcidos (`rgba(18, 12, 13, 0.7)`) con desenfoque de fondo (`backdrop-filter: blur(16px)`) para emular acabados de cristal físico.
4.  **Caché de Imágenes y Optimización:** El catálogo almacena en memoria (`svgCache`) las respuestas visuales de las portadas y capturas para evitar parpadeos visuales al filtrar o realizar búsquedas en tiempo real.

---

## 🛠️ Cómo Ejecutar el Proyecto Localmente

Se recomienda abrir el proyecto mediante un servidor web local (aunque también es compatible abriendo directamente `index.html` en Windows).

### Opción A: Servidor Node.js (Recomendado)
Abre la consola CMD en el directorio `/proyecto` y ejecuta:
```bash
cmd /c npx -y serve -l 8000
```
Accede en tu navegador a: `http://localhost:8000/`

### Opción B: Python
Abre la consola en el directorio `/proyecto` y ejecuta:
```bash
python -m http.server 8000
```
Accede en tu navegador a: `http://localhost:8000/`

---

## 💡 Códigos y Funcionalidades para Pruebas

*   **Cupones en el Carrito (`#/cart`):** Usa `GAMER10` (10% extra) o `ANTIGRAVITY25` (25% extra) para recalcular los totales en tiempo real con descuentos y tasas (IVA 15%).
*   **Checkout y Biblioteca (`#/account`):** Simula el formulario de compra con cualquier dato ficticio. Los juegos se trasladarán a tu **Biblioteca de Juegos** en la sección "Mi Cuenta", donde podrás pulsar "JUGAR AHORA" para probar el lanzamiento del juego.
*   **Comparador:** Añade juegos desde sus detalles y pulsa el botón flotante "Comparar" para ver la comparativa técnica a tres bandas.
