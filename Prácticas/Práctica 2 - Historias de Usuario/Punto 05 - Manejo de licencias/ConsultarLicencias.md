## Frente

* **ID**: `Consultar licencias`
* **Título**: Como `Administrativo` quiero `consultar las licencias de mis empleados` para `estar al tanto de su productividad`.
* **Reglas de negocio**:
    * Solo se podrá imprimir un informe por mes para cada empleado.

---

## Reverso
* Criterios de Aceptación (`Consultar licencias`)

* **Escenario 1**: `Consulta exitosa`
    * Dado `un cuil 27-23326545-8 correspondiente a un empleado, y la última impresión del informe de dicho empleado siendo hace 4 meses`,
    * Cuando `el administrativo ingresa: cuil "27-23326545-8", rango de fechas 20/5/26 - 20/9/26 y presiona "Imprimir informe"`
    * Entonces `el sistema imprime un informe de las licencias solicitadas en ese rango de fechas`
* **Escenario 2**: `Consulta fallida por cuil inexistente`
    * Dado `un cuil 27-23326544-8 no correspondiente a un empleado`,
    * Cuando `el administrativo ingresa: cuil "27-23326544-8", rango de fechas 20/5/26 - 20/9/26 y presiona "Imprimir informe"`
    * Entonces `el sistema no imprime nada. Informa en pantalla: "Error: el cuil 27-23326544-8 no corresponde a un empleado"`.
* **Escenario 3**: `Consulta fallida por segunda impresión en el mes`
    * Dado `un cuil 27-23326546-8 correspondiente a un empleado, y la última impresión del informe de dicho empleado siendo hace 20 días`,
    * Cuando ``el administrativo ingresa: cuil "27-23326546-8", rango de fechas 20/5/26 - 20/9/26 y presiona "Imprimir informe"``
    * Entonces `el sistema no imprime nada. Informa en pantalla: "Error: solo se puede imprimir un informe de cada empleado por mes. Impresión del último informe de 27-23326546-8: hace 20 días"`.
* **Escenario 4**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 5**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 6**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 7**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 8**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 9**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`
* **Escenario 10**: `títuloEscenario`
    * Dado `contexto`,
    * Cuando `evento`
    * Entonces `resultado`

---
