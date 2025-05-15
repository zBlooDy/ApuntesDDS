# (💻) Frontend

Todo aquello que nos permite interactuar con el sistema, hoy en dia esta muy vinculado con el browser.

GUI y UI (Nos perm)

Grupos de aplicaciones

    - Browser
    - Desktop
    - Mobile

# (💾) Backend

Es la capa de aplicacion que maneja la logica de negocio, acceso a datos y seguridad.

(🔩) Se va a encargar de:

    - Procesar peticiones de front-end (APIs REST, GraphQL, RPC)
    - Leer/escribir en bases de datos, sistemas o servicios externos
    - Autenticacion, autorizacion y validacion de datos
    - Tareas de larga duracion

Se ejecuta en servidores y suele implementarse con lenguajes/frameworks como Node.js, Python, Java/Spring, etc.

### (📕) Cliente Liviano

> 🎲 El servidor produce HTML casi definitivo entonces el cliente hace pocas transformaciones o en algunos casos nignuna

    - Responsabilidad minima: Solo maneja la UI y la captura de la interaccion del usuario
    - Procesamiento en servidor: Toda la logica de negocio se realiza en el servidor

=> Facil despliegue y mantenimiento

### (📚) Cliente Pesado

> 🎲 Genera estructuras aptas para el consumo programatico y el cliente lo transforma en HTML

    - Responsabilidad elevada: Aparte de la UI, ejecuta parte o toda la logica de negocio, ademas de almacenar o procesar datos localmente.
    - Descentralizacion: Reduce la carga del server, pero implica tareas de despliegue y actualizacion
    -

=> Tenemos menor latencia para operaciones locales o offline
=> Puede seguir trabajando sin conexion

### Caracteristicas de una aplicacion

**[🎫] Usabilidad (UX):** Capacidad de la pagina ser comprendido, aprendido, usado y ser atractivo para el usuario

**[🎫] Accesibilidad:** Capacidad que tiene de ser utilizable para todo tipo de usuario que interactue con nuestra pagina

**[🎫] Responsive:** Capacidad que tiene la pagina de adaptarse a los diferentes tamaños desde donde se acceda a la misma
