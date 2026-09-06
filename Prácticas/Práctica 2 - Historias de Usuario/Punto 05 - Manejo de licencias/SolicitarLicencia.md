## Frente

* **ID**: `Solicitar licencia`
* **Título**: Como `Empleado autenticado` quiero `soliciar una licencia` para `tener tiempo libre`.
* **Reglas de negocio**:
    * Para poder solicitar una licencia, el empleado debe tener más de 1 mes de antigüedad.
    * Podrá solicitar una licencia un empleado que no tenga una licencia vigente

---

* Duda lo de que envia el mail con la confirmacion es una regla de negocio?
* Está bien en el titulo pner: como empleado autenticado....?
* Hace falta verificar la matricula del medico??
* Deberia informar algo en pantalla cuando la confirmacion es en el mail???

## Reverso
* Criterios de Aceptación (`Solicitar licencia`)

* **Escenario 1**: `Solicitud exitosa`
    * Dado `un Empleado con más de 1 mes de antigüedad, sin ninguna licencia vigente`,
    * Cuando `el Empleado ingresa: tipo de licencia "presencial", fecha de inicio de reposo "15/10/26", matrícula de médico personal "12345", diagnóstico: "pierna rota", destinatario: "titular"`
    * Entonces `el sistema registra la licencia y envía un mail al Empleado con el código de licencia 35, confirmando la licencia y los días otorgados.`
* **Escenario 2**: `Solicitud fallida por falta de antigüedad`
    * Dado `un Empleado con 0 meses de antigüedad`,
    * Cuando `el Empleado ingresa: tipo de licencia "presencial", fecha de inicio de reposo "15/10/26", matrícula de médico personal "12345", diagnóstico: "pierna rota", destinatario: "titular"`
    * Entonces `el sistema no registra la licencia. Informa: "Error: para soliciar una licencia, se necesita al menos 1 mes de antigüedad`.
* **Escenario 3**: `Solicitud fallida por licencia vigente`
    * Dado `un empleado con una licencia vigente`,
    * Cuando `el Empleado ingresa: tipo de licencia "presencial", fecha de inicio de reposo "15/10/26", matrícula de médico personal "12345", diagnóstico: "pierna rota", destinatario: "titular"`
    * Entonces `el sistema no registra la licencia. Informa: "Error: no se puede solicitar una licencia, ya tienes una licencia vigente `

---
