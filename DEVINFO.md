## Informe de Desarrollo: Eticket

Este informe detalla el proceso de desarrollo de la página web "eticket", una aplicación ficticia con fines educativos que emula la funcionalidad y diseño de una plataforma de eventos existente.

### Tecnologías Utilizadas

* **HTML:** Se utilizó HTML para estructurar el contenido de la página de forma semántica y accesible. 
* **CSS:** Se implementó CSS para definir los estilos visuales de la página, incluyendo fuentes, colores, diseño de tarjetas de eventos y animaciones.
* **JavaScript:** Se utilizó JavaScript para agregar funcionalidades interactivas a la página, como la carga de eventos desde un archivo JSON y la animación del círculo de progreso en el carrusel.
* **Bootstrap:** Se empleó Bootstrap como un framework CSS para facilitar el diseño responsivo y aprovechar componentes predefinidos como botones y tarjetas.


### Proceso de Desarrollo

1. **Estructura y Diseño:**
    - Se inició creando los mockups en papel.
    - Se creó la estructura básica de la página utilizando HTML. 
    - Se implementó un diseño básico con CSS para las secciones principales, como el encabezado, el carrusel de imágenes destacadas y la sección de eventos.
    - Se utilizaron tarjetas Bootstrap para mostrar los eventos de manera uniforme y responsiva. 

2. **Carga de Eventos:**
    - Se creó el archivo `data/events.json` para almacenar la información de los eventos (nombre, imagen, ciudad).
    - Se implementó el script `setEvents.js` para realizar una petición a `events.json` utilizando la API Fetch.
    - El script procesa la respuesta JSON y genera el HTML dinámico para las tarjetas de eventos, insertándolas en el contenedor correspondiente.

3. **Carrusel con Animación:**
    - Se utilizó el carrusel Bootstrap para mostrar imágenes destacadas.
    - Se creó el script `progressCarousel.js` para animar un círculo de progreso en sincronía con el cambio de diapositivas en el carrusel.
    - El script calcula la circunferencia del círculo y lo configura inicialmente.
    - Se agrega un listener al evento "slide.bs.carousel" para reiniciar la animación del círculo cada vez que cambie la diapositiva.
    - La función `resetProgress` reinicia la animación del círculo utilizando propiedades CSS como `stroke-dashoffset` y `transition`.

### Decisiones de Diseño

* Se optó por un diseño limpio y minimalista utilizando colores neutros y tipografías claras para mejorar la legibilidad.
* Se utilizaron tarjetas Bootstrap para mostrar los eventos de manera organizada y visualmente atractiva.
* Se implementó un carrusel con animación de progreso para brindar dinamismo a la página y destacar las imágenes principales.

### Retos Enfrentados

* Uno de los retos fue lograr la animación fluida del círculo de progreso en sincronía con el cambio de diapositivas del carrusel. Esto se resolvió mediante cálculos de la circunferencia del círculo y la manipulación de propiedades CSS con JavaScript.
* Otro desafío fue asegurar la correcta estructura y semántica del HTML para lograr una página accesible y compatible con diferentes dispositivos.

### Próximos Pasos

* Se planea extender la funcionalidad de la página para permitir el filtrado y búsqueda de eventos por ciudad o categoría.
* Se implementará un sistema de autenticación para permitir a los usuarios guardar eventos favoritos o comprar entradas (en el caso de ser una aplicación de venta real).
* Se optimizará el código para mejorar el rendimiento y la experiencia del usuario.


Este informe detalla las decisiones de diseño, las tecnologías utilizadas y los retos superados durante el desarrollo de la página eticket. El proyecto continuará evolucionando con la implementación de nuevas funcionalidades y optimizaciones.
