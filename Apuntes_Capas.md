## Estructura de capas

=> Idea de separar nuestro proyecto en 3 capas:
    - Controladores (lo mas cercano al FrontEnd)
    - Services
    - Repositorios (lo mas cercano a la base de datos)

**Controladores**: Se exponen las APIs, se reciben las solicitudes externas (GET, POST, PUT, etc) y se pasan a la capa de "Services"

**Services**: Separa el como se hace algo (dominio) del cuando y en que orden se hace (services)

**Repositorios** : Se encarga de persistir la informacion, ya sea una base de datos o una lista por ejemplo. Traduce las entidades del dominio a un formato persistible y viceversa.


- Con cualquier dominio se recomienda hacer una entidad sobre ellos. Las capas terminan siendo carpetas:
    
    - Controllers = Van a ir los endpoint que tiene la entidad, se exponen las API, se reciben las solicitudes externas (GET, POST, etc)
    
    - Services    = Como se genera determinada entidad, como se orquesta? Luego de que pasa por el endpoint del controller, viene a services, es un intermedario entre la request y la base de datos. En services, va a tener el **repositorio**.

    - Models   
        - Entidades = Las clases y sus funciones basicas
        - Repositorios = Se maneja la base de datos / lista de las entidades de nuestro dominio. Por ejemplo agregar, eliminar, etc.
    
    - Routes = Tiene las rutas de los endpoint
    

## Paginacion

Es una tecnica que permite dividir grandes cantidades de datos en peque;as porciones, las cuales son las paginas.
    - Mejora el rendimiento (se trabaja con menos datos)
    - Menor consumo de red
    - Navegacion mas comoda y por paginas


> Ejemplo en una request: 
    - GET /productos?page=2&limit=10 (Lo que hace es cortar la lista de todos los productos y tomar esos productos)