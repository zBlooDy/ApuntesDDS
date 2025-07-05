# (💻) Despliegue

> 💭 Al estar trabajando en local, otra persona no se puede conectar ya que no se conoce la IP en donde esta el proyecto. Estas ip's cambian dinamicamente y son privadas.

-> Ante esta situacion, colocamos nuestro software en una computadora "dedicada".

Ejemplo ataque seguridad de un script - Linux: Nivel sistema operativo, osea entro a esa computadora fisicamente y ahi ejecuto - Javascript: Nivel software que desarrolle

-> Problemas asociados al despliegue

    - Seguridad fisica: Donde esta fisicamente la computadora dedicada
    - Computadora con recursos necesarios para nuestro software
    - Refrigeracion, energia y buena provision de servicio de red

**IaaS (Infrastructure as a Service):** En vez de ir fisicamente al centro de computos, es todo virtualmente. Uno pide donde necesita que el software funcione, y la empresa decidira donde ponerlo en esa zona.

Cosas minimas para desplegar: Memoria | Disco | Procesamiento | SO

## (🌐) Virtualizacion

-> Crear un contexto con ciertos detalles (memoria, disco, procesamiento, sist operativo) y pensar que nuestro software va a correr en esta "cajita virtualizada".

-> Nos permite independizarnos de software y hardware que el nodo real tiene.

### (🐳) Docker

Herramienta de virtualizacion de software.  
Virtualiza a nivel sistema operativo **(de tipo Linux)**. Ejecuta nativamente un proceso pero de una forma modificada, lo que lo hace mas eficiente.
Solo ejecuta en Linux.

### Como funciona Docker?

> Entorno de imagenes y contenedores...

❓ Que dice un Dockerfile:

Dockerfile nos dice como se va a construir el archivo docker

- Capa anterior a la imagen
- WORKDIR: Todos los path son relativos a ese directorio
- COPY archivos
- ENTRYPOINT: Que es lo que se ejecuta de primera instancia en el sistema, si no esta especificado.

---

**[🎨] Imagenes**: Descripciones de un sistema operativo virtualizado. Por cada imagen puedo crear n contenedores.
Son estaticas.
Se basan en "layers" imagenes mas pequenias que van construyendo a la imagen final (idea de commits en git). Esto permite hacer mas eficiente las descargas y construccion.
Tienen tags/etiquetas en vez de nombres. (docker build -t hola-mundo .)

**[📦] Contenedores (VM):** Estrategia de virtualizacion liviana, es una instancia que no representa una computadora sino un proceso.
Nace -> Ejecuta -> Finaliza

Analogia(Imagen: clase | Contenedor: objeto instancia de esa clase)

Dockerfile ---> Imagen ---> [Contenedor [proceso] ]

             ____________
            | Contenedor|
            |  |-------||
            |  |Proceso||
            |__________ |

[🔩] Operaciones sobre imagenes

    - Descargar (pull)
        - Entorno de ejecucion: Alpine/Debine/Node/Python
        - Servicios: Mongo/Keycloak

    - Construir (build)
        - Se pueden construir en base a alguna imagen especifica y realizar cambios (docker build . => Busca el dockerfile en el directorio y construye las capas de la imagen)

    - Compartir (push)

[🔩] Operaciones sobre contenedores

    - Ejecutar (run): A partir de una imagen
    - Conectarse al contenedor (exec): Entrar y ver como esta el proceso, mandarle mensajes, ver su salida standard
    - Operaciones como inicio/detencion/reinicio/fin
    - Eliminar: Detenerlo y destruir todo detalle del contenedor en el SO
    - (-net host: Levanta en la misma red que estoy yo
    -p puertoMiMaquina:puertoContenedor)

**Registros** : Para descargar/subir imagenes dockers

Procesos demons/larga vida, conviene levantar el servidor en -d (dettached/demon) lo que hace es iniciar el proceso y dejarlo en segundo plano

**Docker compose:** Permite ejecutar mediante el comando `docker compose` todos los detalles que ponia en la terminal, ports, environment, volumes, imagen, etc.

---

Arquitectura
Cliente-Servidor
HTTP
REST
Formatos de la Web (HTML,CSS,JS,JSON)
Como se distribuye la vista (Cliente Liviano - Cliente Pesado)
Como se distribuye la logica (Ej: Logica de base de datos esta en el servidor en cliente pesado)
Para que sirve CSS y HTML
Porque virtualizamos? Donde podemos desplegar aplicaciones?
React sobre los hooks que vimos (useEffect, useState, useContext)
Para que sirve cors? Porque existe?
Sistema de integracion continua?
Promises (async, await, then) Manejo asincronico de respuestas, herramienta q permite la programacion asincronica
Que usaria para desplegar?
