# Sello Propio | Remeras Personalizadas 👕

Proyecto desarrollado para el curso **Talento Tech - Front-End JS** .

---

## 🎯 Propósito del Sitio Web

**Sello Propio** es una marca y tienda de indumentaria personalizada con identidad de rock nacional, cultura pop y pedidos especiales a medida:
> *"¿Querés una sola? También la hacemos. Remeras personalizadas desde 1 unidad."*

El objetivo de esta página web es:
1. Exhibir los modelos y tipos de estampados que realiza el emprendimiento (remeras de rock, códigos de Spotify escaneables y buzos con capucha).
2. Transmitir cercanía y confianza mostrando reseñas reales de clientes.
3. Permitir que los visitantes soliciten presupuestos y encargos de manera directa a través de un **formulario conectado a Formspree** y enlace directo a su cuenta de Instagram oficial ([@sellopropio.ok](https://www.instagram.com/sellopropio.ok/)).

---

## 🎨 Identidad Visual y Estilo

La estética se basó fielmente en la identidad gráfica de la marca en Instagram:
- **Colores principales**: Blanco puro (`#ffffff`) y fondo tiza (`#fafafa`) para un diseño limpio y sobrio.
- **Color de acento**: Rojo sello (`#c5221f`), extraído directamente del logo y de las piezas gráficas de la marca.
- **Texto y contraste**: Negro / grafito (`#111111`) para máxima legibilidad.
- **Tipografía**: Fuente **Inter** (importada desde Google Fonts), seleccionada por su sobriedad, modernidad y claridad de lectura.
- **Logo oficial**: Archivo circular del sello distintivo integrado tanto en el encabezado como en la sección de presentación y pie de página.

---

## 🛠️ Requisitos Técnicos Cumplidos (Clases 01 a 08)

1. **HTML Semántico**:
   - Etiquetas semánticas: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`.
   - Menú de navegación en lista desordenada `<ul>` con enlaces internos hacia las secciones (`#inicio`, `#productos`, `#resenas`, `#contacto`).
   - Tabla informativa (`<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`, `colspan`) con los tiempos de producción según el pedido.
   - Contenido multimedia con imágenes descriptivas (`alt`) y contenedor con `<iframe>` de video.
2. **CSS Externo y Diseño Responsivo**:
   - Hoja de estilos externa `styles.css` vinculada en el `<head>`.
   - Estilos para la barra de navegación: eliminación de viñetas (`list-style: none`), remoción de subrayados (`text-decoration: none`) y efectos de interacción al pasar el cursor (`:hover`).
   - **Flexbox**: Aplicado en el catálogo de productos (`.contenedor-flex-productos`) con `display: flex; flex-wrap: wrap; justify-content: center; gap: 25px;`.
   - **CSS Grid**: Aplicado en la sección de reseñas (`.contenedor-grid-resenas`) con `grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px;`.
   - **Media Queries**: Reglas `@media (max-width: 768px)` para adaptar el menú, hero, productos y formulario a pantallas de celulares.
3. **Formulario y Conexión con Formspree**:
   - Campos estructurados con sus respectivas etiquetas `<label>`, `<input>`, `<select>` y `<textarea>`.
   - Conexión configurada por método `POST` hacia Formspree.

---

## 📬 Documentación de Formspree

### ¿Por qué se utiliza Formspree en este proyecto?
Al tratarse de un sitio web estático desarrollado con HTML y CSS (sin un lenguaje de backend como Node.js o PHP), el navegador no cuenta por sí solo con la capacidad de enviar un email directamente. 

**Formspree** soluciona esta necesidad actuando como un puente o receptor intermedio:
1. El usuario completa el formulario y hace clic en *"Enviar Consulta"*.
2. El formulario envía una petición HTTP `POST` a la URL proporcionada por Formspree (`https://formspree.io/f/mgaopaoo`).
3. Formspree procesa la solicitud y redirige automáticamente todos los datos del cliente al correo electrónico del administrador del negocio.

### Instrucciones para configurar el formulario:
1. Iniciar sesión en [formspree.io](https://formspree.io).
2. Crear un formulario nuevo y copiar el código generado.
3. Colocar dicho código en el atributo `action` del formulario en `index.html`:
   ```html
   <form class="formulario" action="https://formspree.io/f/mgaopaoo" method="POST">
   ```

---

## 📁 Estructura de Archivos

```text
├── index.html        # Estructura semántica HTML5
├── styles.css        # Estilos CSS (Flexbox, Grid, Media Queries)
├── README.md         # Documentación de la pre-entrega
└── img/
    └── logo.jpg      # Logo oficial de Sello Propio
```

---

## 🚀 Despliegue en GitHub Pages

- **Repositorio**: `https://github.com/SabriiAC/proyecto-final-ecommerce-sabrina-mamaniz`
- **Sitio en vivo**: `https://SabriiAC.github.io/proyecto-final-ecommerce-sabrina-mamaniz/`
