## Frente

* **ID**: `Cargar mueble`
* **Título**: Como `Encargado` quiero `Cargar un mueble` para `que un Cliente lo alquile`.
* **Reglas de negocio**:
    * El código de inventario no puede repetirse.

---



## Reverso
* Criterios de Aceptación (`Cargar mueble`)

* **Escenario 1**: `Carga exitosa`  

    * Dado `el código de inventario 12345 no cargado`,
    * Cuando `el Encargado ingresa el código de inventario 12345, la fecha de creación 20/5/2018, la fecha de último mantenimiento 12/10/2021, el estado libre y el precio de alquiler $5000 y presiona "Cargar mueble".`
    * Entonces `el mueble se sube al sistema, y se muestra un mensaje en pantalla que dice "El mueble se ha cargado correctamente.".`
    
* **Escenario 2**: `Carga fallida por código de inventario existente`
    * Dado `el código de inventario 12345 ya cargado`,
    * Cuando `el Encargado ingresa el código de inventario 12345, la fecha de creación 20/5/2018, la fecha de último mantenimiento 12/10/2021, el estado libre y el precio de alquiler $5000 y presiona "Cargar mueble".`
    * Entonces `el mueble no se sube al sistema, e informa en pantalla "Error: el mueble con código 12345 ya se encuentra en el sistema.".`
---
