## Frente

* **ID**: `Agregar elemento`
* **Título**: Como `Administrador` quiero `agregar un elemento al sistema` para `que luego forme parte de un kit`.
* **Reglas de negocio**:
    * El precio de compra no puede superar $1.000.000
    * Si el elemento no es nacional, entonces se guarda un impuesto adicional del 10% calculado sobre el precio de compra

---
* Duda :numero de serie unico se asume, no va en reglas de negocio.
* Duda en el escenario 1 hace falta poner el origen de fabricacion y el precio de compra en el dado?? no es parte del contexto, solo es lo que ingresa el usuario

## Reverso
* Criterios de Aceptación (`Agregar elemento`)

* **Escenario 1**: `Agregado de elemento nacional exitoso`
    * Dado `un número de serie 0156 no registrado, un precio de compra $100.000 y origen de fabricación "nacional"`,
    * Cuando `el administrador ingresa: número de serie 0156, tipo de elemento "micrófono", precio de compra $100.0000, origen de fabricación "nacional" y fecha de alta "20/8/26"`
    * Entonces `el sistema agrega el elemento. Informa: "Elemento agregado exitosamente!`
* **Escenario 2**: `Agregado de elemento internacional exitoso`
    * Dado `un número de serie 0156 no registrado, un precio de compra $100.000 y origen de fabricación "internacional"`,
    * Cuando `el administrador ingresa: número de serie 0156, tipo de elemento "micrófono", precio de compra $100.0000, origen de fabricación "internacional" y fecha de alta "20/8/26"`
    * Entonces `el sistema agrega el elemento, y guarda un impuesto de $10.000. Informa: "Elemento agregado exitosamente!`
* **Escenario 3**: `Agregado de elemento fallido por precio de compra muy alto`
    * Dado `un precio de compra $2.000.000`,
    * Cuando `el administrador ingresa: número de serie 0156, tipo de elemento "micrófono", precio de compra $100.0000, origen de fabricación "internacional" y fecha de alta "20/8/26"`
    * Entonces `el sistema no agrega el elemento. Informa: "Error: el precio de compra debe ser menor a $1.000.000"`
* **Escenario 4**: `Agregado de elemento fallido por número de serie ya registrado`
    * Dado `un número de serie 0156 ya registrado`,
    * Cuando `el administrador ingresa: número de serie 0156, tipo de elemento "micrófono", precio de compra $100.0000, origen de fabricación "internacional" y fecha de alta "20/8/26"`
    * Entonces `el sistema no agrega el elemento. Informa: "Error: el elemento con código de serie 0156 ya se encuentra en el sistema"`

---
