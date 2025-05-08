# Persistencia y Modelo Documental 


## (📦) Persistencia y nuestros temas de interes
   
    [🔧] Tecnicas para resolver problemas como:
        - Mantener los datos sin perderlos => Durabilidad
        - Manejar grandes volumenes de datos de forma eficiente
    
    [💾] Un medio puede ser una base de datos:
        - Donde se guarda la informacion (disco, memoria, etc)
        - Como se representa (archivos, tablas, documentos, diccionarios clave/valor, etc)
    
    [🧮] Como razonamos sobre la logica de la informacion?
        
        ► Modelo Relacional (SQL)
            - Basado en tablas y relaciones entre tablas (entidades)
            - Se puede representar mediante un DER
            - Operaciones CRUD / ABM / ABMC:* (Alta | Baja | Modificacion | Consulta) Son las operaciones que usamos con los datos 
            - Busca mantener redudancia minima (que la informacion se duplique lo menos posible) y operaciones CRUD ricas en contenido/informacion
        
        ► Modelos No Relacionales (noSQL)
            
            Documental: 
                - Estructura clave - valor que se organiza en colecciones
            
            Clave Valor: 
                - Se representa la informacion en forma de diccionario clave - valor
                - Operaciones CRUD simples y rapidas
            
            Tabular
    
## (📮) Bases de Datos

    📂 Implementacion concreta de un motor de persistencia
        - Bajo un paradigma / modelo de persistencia
        - Persistiendo en un medio particular (disco, memoria, hibridas)
        - Con requeremientos no funcionales
        - Utiliza un lenguaje de consulta especifico


## (💡) Lenguaje de Consulta

> **SQL**: Asociado al modelo relacional, el cual es un lenguaje de consulta con operaciones como:
    
    - Crear: insert
    - Eliminar: delete
    - Modificar: update
    - Consultar: select

> **Javascript de MongoDB**: Solo funciona en MongoDB