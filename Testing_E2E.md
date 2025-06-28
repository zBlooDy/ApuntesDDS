## Testing E2E

Ambiente de Homologacion o QA: Es el mundo de los testers en el cual se encargan de probar los flujos de la aplicacion para que funcionen correctamente.

=> Herramienta para test de integracion: Testcontainers

### Test End to End

    - Se testean en conjunto todos los componente sde un sistema ante determinados flujo
    - Cubren a todo el sistema, involucrando dependencias
    - Son ejecutados por los QA/Testers a la hora de hacer control de calidad
    - Son diseñadas en conjunto con los desarrolladores

### Buenas practicas en E2E

=> Menos es mas: Evitar testear todo con E2E
=> Datos de prueba consistentes
=> Tests confiables (no flakys: test que fallan de forma intermitente)
=> Asertar comportamiento, no solo clicks
=> Separar flujos principales de casos borde

### Errores comunes --> Soluciones

- Tests que fallan aleatoriamente => Esperas explicitas, datos consistentes
- Datos que cambian entre corridas => Usar fixtures/mocks
- Test lentos y dificiles de mantener => Automatizar solo flujos criticos
- Pocas aserciones o poco significativas => Verificar resultados esperados
