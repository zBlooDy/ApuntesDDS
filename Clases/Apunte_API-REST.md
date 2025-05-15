## HTTP

- HTTP es un protocolo de comunicacion basado en el modelo Cliente-Servidor, esta la version segura que es HTTPS.

- Un cliente se conecta con un servidor para realizar peticiones y el servidor atiende las mismas

- HTTP transmite datos en texto plano
- HTTPS utiliza TLS/SSL para cifrar los datos

> HTTP se maneja con codigos de respuesta, lo cual nos indica el resultado de la peticion realizada.

### Verbos HTTP

    - GET: Solicita un recurso sin modificarlo
    - POST: Envia datos al servidor para que se procesen
    - PUT: Actualiza/crea un recurso del sistema
    - DELETE: Elimina un recurso del sistema
    - PATCH:

## API

- Es una interfaz de programacion de aplicaciones

1. Servidor expone API's
2. Cliente consume API's y expone UIs

### API REST

- No es un protocolo, el formato de intercambio de datos es libre

- Todos los objetos se manejan

## URL's

- Las URL's tienen 3 partes: dominio / base / query_string

  - Dominio: No forma parte del HTTP
  - Base : Es la parte obligatoria para referenciar un recurso/listado
  - Query string: Key/valor opcional para hacer un "filtrado"
