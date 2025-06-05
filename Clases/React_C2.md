Call to action: Tipicamente botones, links, imagenes, al clickearlo es un llamado para hacer algo.

Listner de eventos: Van a dentro de un div y suelen inicar con on...

```jsx

export function ContadorClicks({ganador, clicks, setClicks}) {
    //const {clicks, setClicks} = useState(0)  //Nos permite definir esa variable que va a ser nuestro contador. Dupla para leer y actualizar esa varible

    return
        <div classname={'ContadorClicks ${ ganador ? 'ganador' : ''}'}>
            <div classname="ContadorClicks-contador">Cantidad de clicks: {clicks}</div>

            <div classname="ContadorClicks-lienzo" 'onClick=(() => setClicks(clicks + 1))'></div> //No van las ''
}
```

---

> 🚨 Cuando un componente no depende de su propio estado sino que necesita saber de otro componente se empieza a complejizar:

En React un componente puede recibir parametros, que se conocen como props (↑ en la funcion de ContadorClicks implementamos que llegue en caso de ser ganador).

El tema es que no se puede romper el encapsulamiento, es decir, entre componentes no se puede compartir atributos, variables. Lo que se tiene que hacer es "subir el estado". Subir el estado se refiere a del componente hijo al componente padre, que es justamente quien necesita ese ESTADO.

Al pasar el contador y el setter, pierdo la logica, pero se los puedo mandar x parametro

```jsx
function calcularGanador(clicksIzquierda, clicksDerecha) {
  if (clicksIzquierda > clicksDerecha) {
    ganador = "izquierda";
  } else if (clicksDerecha > clicksIzquierda) {
    ganador = "derecha";
  } else {
    ganador = "empate";
  }
}

function notificarCambioGanador(ganador) {
  //fetch("https://analiticasutn.com/reporte", {ganador})
  if (ganador !== "empate")
    console.log("Cambio el lienzo ganador, ahora es: ", ganador);
}

export function ComparadorClicks() {
  const { clicksIzquierda, setClicksIzquierda } = useState(0);
  const { clicksDerecha, setClicksDerecha } = useState(0);

  // Ganador va a ser un string que sea "izquierda", "derecha", "empate"
  const ganador = calcularGanador(clicksIzquierda, clicksDerecha);

  useEffect(() => {
    notificarCambioGanador();
  }, [ganador]);

  return;
  <div classname="ComparadorClicks">
    <ContadorClicks
      clicks={clicksIzquierda}
      setClicks={setClicksIzquierda}
      ganador={ganador === "izquierda"}
    />

    <ContadorClicks
      clicks={clicksDerecha}
      setClicks={setClicksDerecha}
      ganador={ganador === "derecha"}
    />
  </div>;
}
```
