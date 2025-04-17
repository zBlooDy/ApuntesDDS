# Desarrollo Backend

## Redes

> 💭 Recordando: HTTP (o su variante encriptada HTTPS) : Es un protocolo basado en texto plano, sin estado, y que se basa principalmente en pedidos HTTP los cuales tienen metodos, rutas, parametros, cuerpos y cabeceras. 

=> A partir de HTTP se monta REST, una especie de protocolo de mas alto nivel que busca respetar ciertas convenciones y buenas practicas para el uso de HTTP. Por ejemplo:

    - DELETE: Solo se usa para eliminar informacion
    - GET:    Solo se usa para acceder informacion

🔰 Otro punto importante de REST es la *orientacion a recursos*. Esta plantea que las rutas HTTP representan contenidos organizados en una estructura arborea que podemos consultar y operar. 

    -/usuarios  
    -/usuarios/123 
    -/usuarios/123/pedidos


## Arquitectura Logica

> 🧮 Concepto: La arquitectura logica nos va a mostrar el diseño de mas alto nivel de los componentes software. Vamos a ver como los modulos, paquetes, clases e interfaces se organizan, comparten tecnologicas, estilos de comunicacion, etc. Es decir, como interactuan estos componentes.

### Algunas arquitecturas logicas

    💠 MVC Web (Servidor) : Inspirado en el patron Model-View-Controller, la logica del servidor va a estar dividida en:
        - Controladores: Manejan la interaccion del usuario
        - Modelos      : Representan los datos y logica del negocio
        - Vistas       : Generan las respuestas en HTML o datos.
    
    💠 MVC Web (Cliente) : Al utilizar un cliente pesado, el patron MVC puede migrar al navegador. Existen frameworks que permiten organizar el codigo del cliente separado en: Logica | Datos | Presentacion

### Modelos

    📜 Basado en concerns (incumbencias) : El Backend se organiza en capas como Presentacion, Dominio y Persistencia. Al separar, ofrece un mayor grado de desacoplamiento y escabalidad.

    📜 Capas: Incluye capas como Controladores, Servicios, Repositorios y Modelos. Ademas utiliza DTOs (Data Transfer Objects) los cuales son objettos que llevan informacion entre procesos

    📜 Orientado a Objetos (OO) : Tiene el objetivo de modelar todo el dominio a partir de objetos que colaboran entre si, sin una estructura a-priori sino que se basan en los requerimientos. 

---

> 📊 Cada estructura tiene sus ventajas/desvantajas, la eleccion dependera el tipo de aplicacion, los requerimientos, las tecnologias disponibles y del plan de negocio.

## Tipos de Cliente


**Pesado:** Genera estructuras aptas para el consumo programatico y el cliente lo transforma en HTML

**Liviano:** El servidor produce HTML casi definitivo entonces el cliente hace pocas transformaciones o en algunos casos nignuna

En el mundo `node`, `express` nos sirve como framework para implementar servidores para ambos estilos arquitectónicos.