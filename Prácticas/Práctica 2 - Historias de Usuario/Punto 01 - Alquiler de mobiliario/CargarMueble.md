## Frente

* **ID**: `Cargar mueble`
* **Título**: Como `Encargado` quiero `Cargar un mueble` para `que un Cliente lo alquile`.
* **Reglas de negocio**:
    * El código de inventario no puede repetirse.
    * El Encargado debe estar autenticado en el sistema.

---

* DUDA : el estado solo puede ser libre, de baja o alquilado. Eso deberia tenerlo en cuenta para los casos de error? EJ: el usuario puede ingresar "estado: por alquilar", y eso sería inválido. Lo mismo con las fechas. Mi pregunta es básicamente si se tiene en cuenta que a veces al usuario no se le da la opción de ingresar texto libre, sino que se le daría una serie de opciones limitadas. 
* DUDA: que pasa con la autenticación del encargado?? es posible que el encargado aprete "cargar mueble" sin autenticarse? Eso daría error o directamente no se le daría la opción de cargar?. Esto afecta qué pongo en el Dado del escenario 2 y 3. Qué informa el sistema si el usuario no esta autenticado y ademas el codigo ya esta cargado??


## Reverso
* Criterios de Aceptación (`Cargar mueble`)

* **Escenario 1**: `Carga exitosa`  

    * Dado `el código de inventario 12345 no cargado y el Encargado autenticado en el sistema`,
    * Cuando `el Encargado ingresa el código de inventario 12345, la fecha de creación 20/5/2018, la fecha de último mantenimiento 12/10/2021, el estado libre y el precio de alquiler $5000 y presiona "Cargar mueble".`
    * Entonces `el mueble se sube al sistema, y se muestra un mensaje en pantalla que dice "El mueble se ha cargado correctamente.".`
    
* **Escenario 2**: `Carga fallida por código de inventario existente`
    * Dado `el código de inventario 12345 ya cargado`,
    * Cuando `el Encargado ingresa el código de inventario 12345, la fecha de creación 20/5/2018, la fecha de último mantenimiento 12/10/2021, el estado libre y el precio de alquiler $5000 y presiona "Cargar mueble".`
    * Entonces `el mueble no se sube al sistema, e informa en pantalla "Error: el mueble con código 12345 ya se encuentra en el sistema.".`
    
* **Escenario 3**: `Carga fallida por falta de autenticación`
    * Dado `el Encargado no autenticado en el sistema`,
    * Cuando `el Encargado ingresa el código de inventario 12345, la fecha de creación 20/5/2018, la fecha de último mantenimiento 12/10/2021, el estado libre y el precio de alquiler $5000 y presiona "Cargar mueble".`
    * Entonces `el mueble no se sube al sistema, e informa en pantalla: "Error de autenticación, por favor ingrese al sistema antes de realizar una carga."`.

---
