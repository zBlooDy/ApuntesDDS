# (🌐) React

> 📠 Arquitectura cliente pesado: El cliente es el que transforma en HTML, por lo que el browser tiene mucha mas responsabilidad ahora. El servidor va a mandar html, css y codigo javascript de lo que se va a encargar todo el browser renderizando el HTML, ejecutando la funcionalidad de JS, validaciones y la logica de negocio parcialmente.

React surge con el objetivo de que no se actualice la pagina todo el tiempo cuando haces alguna funcionalidad o algo, solo la porcion que estas manipulando.

## [🔩] MVC (Model View Controller)

Usuario -> Vista -> Controlador -> Modelo -> Controlador -> Vista

- Model: El dominio de mi sistema, la logica de negocio, las entidades

- Vista: Lo que se va a mostrar para el usuario

- Controller: El orquestador del sistema, va a gestionar los endpoints con sus request, exponer mi API, redirecciona al usuario

> DOM (Document Object Model): Forma de manipular los objetos que estan en el HTML

### [🧧] MVVM (Model View ViewModel)

Cada componente ya es un MVC, el componente sabe todo lo que tiene que hacer ya que controla su logica y visualizacion.

Usuario -> Componente (Vista + Controlador) -> Modelo (estado o API) -> Componente

## [🔧] Fundamentos de React

Todo se separa en componentes

    - Genera el codigo de a componentes
    - Componentes => Bloques reutilizables
    - Separacion de responsabilidades y no por tecnologias, esta todo junto pero cada uno cumple su rol
    - Programacion declarativa
    - DOM virtual

## [✅] Buenas Practicas

    - Componente por archivo
    - Organizar el proyecto
    - Componentes pequeños y reutilizables

- useState(valorInicial)

Ejemplo:
const [contador, setContador] = useState(0)

Dato que lees - Funcion que va a hacer cambiar ese dato
