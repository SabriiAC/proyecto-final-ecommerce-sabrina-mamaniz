# Sello Propio | Remeras Personalizadas

Proyecto desarrollado por Sabrina Belén Mamaniz para el trayecto formativo Front-End JS en Talento Tech.

---

## Propósito del Sitio Web

Sello Propio es una tienda y taller de indumentaria personalizada con identidad ligada al rock nacional, la cultura pop y los pedidos especiales por encargo. El lema central sintetiza la propuesta de valor del negocio:

> "¿Querés una sola? También la hacemos. Remeras personalizadas desde 1 unidad."

El sitio web fue pensado para resolver tres necesidades concretas:
1. Exhibir los modelos y variantes de estampado disponibles: remeras de bandas de rock, prendas con códigos interactivos de Spotify y buzos hoodie con frisa abrigada.
2. Construir confianza con el visitante al compartir reseñas y opiniones de clientes que ya recibieron sus prendas.
3. Facilitar la solicitud de presupuestos y encargos personalizados a través de un formulario directo conectado con Formspree y un acceso rápido a la cuenta de Instagram oficial (@sellopropio.ok).

---

## Identidad Visual y Criterios de Diseño

La estética de la interfaz respeta de forma deliberada la identidad gráfica del emprendimiento:
- Paleta neutra de base: Blanco puro (#ffffff) y fondo tiza (#fafafa), logrando una superficie limpia, despejada y con alta legibilidad.
- Color de acento: Rojo sello (#c5221f), extraído del imagotipo original, reservado para llamados a la acción, etiquetas de estado y detalles de interacción.
- Tipografía y contraste: Fuente Inter (importada desde Google Fonts) combinada con textos en gris grafito (#111111), asegurando una jerarquía visual clara y un contraste adecuado para lectura prolongada.
- Elementos de marca: Isotopo circular del sello distintivo presente en el encabezado, en la sección de bienvenida y en el cierre del pie de página.

---

## Especificaciones Técnicas y Requisitos Cumplidos

El proyecto abarca los conceptos de desarrollo frontend estructurados a lo largo de las clases:

1. HTML5 Semántico:
   - Uso de etiquetas semánticas para estructurar el contenido: header, nav, main, section, article y footer.
   - Navegación interna accesible mediante una lista desordenada (ul) con anclas hacia las secciones del documento (#inicio, #productos, #resenas, #contacto).
   - Tabla informativa (table, thead, tbody, tr, th, td, colspan) con plazos y condiciones de entrega según el volumen de prendas.
   - Contenido multimedia con atributos descriptivos alt en imágenes y un reproductor de video incrustado mediante iframe.

2. CSS Externo y Maquetado Responsivo:
   - Hoja de estilos externa (styles.css) vinculada en la cabecera.
   - Barra de navegación con eliminación de viñetas, supresión de subrayados y transiciones suaves en estado hover.
   - Flexbox en la sección de catálogo (.contenedor-flex-productos) con propiedades display: flex, flex-wrap: wrap, justify-content: center y gap: 25px para una distribución dinámica de las tarjetas.
   - CSS Grid en la sección de testimonios (.contenedor-grid-resenas) aplicando repeat(auto-fit, minmax(280px, 1fr)) con separación uniforme de 20px.
   - Reglas de medios (@media con punto de corte en 768px) para adaptar la grilla de productos, el menú principal y el formulario de contacto a pantallas de celulares.

3. Formulario y Gestión de Consultas:
   - Campos rotulados con etiquetas label accesibles, campos de entrada input con atributos requeridos, selector desplegable select y área de texto textarea.
   - Envío de datos configurado mediante método POST dirigido al servicio de Formspree.

---

## Integración con Formspree

### Justificación Técnica
Al ser un proyecto estático compuesto únicamente por HTML y CSS, el navegador no dispone de un motor de backend (como Node.js, Python o PHP) para enviar correos electrónicos por sí mismo.

Formspree actúa como intermediario para resolver este flujo:
1. El visitante completa sus datos y presiona el botón de envío.
2. El formulario despacha una petición HTTP POST hacia el identificador del servicio en Formspree (https://formspree.io/f/mgaopaoo).
3. Formspree procesa la solicitud y notifica de manera automática la consulta a la casilla de correo del administrador.

### Pasos de Configuración:
1. Crear una cuenta en formspree.io y generar un formulario nuevo.
2. Copiar el código del endpoint asignado.
3. Vincularlo en el atributo action del formulario dentro de index.html:

```html
<form class="formulario" action="https://formspree.io/f/mgaopaoo" method="POST">
```
