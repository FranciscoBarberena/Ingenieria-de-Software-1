## Frente

* **ID**: `Mostrar precio`
* **Título**: Como `Usuario` quiero `ver el precio de mi compra` para `saber cuánto voy a gastar`.
* **Reglas de negocio**:
    * Si el usuario es premium se le hace un descuento del 20%.
    * Si el usuario seleccionó productos por un monto superior a los $4500 se le hace un 10% de descuento.
    * Ambos descuentos son acumulables.

---

* Duda: stock? en que casos se tiene en cuenta y en cuales no?


## Reverso
* Criterios de Aceptación (`Mostrar precio`)

* **Escenario 1**: `Usuario sin premium y un monto total menor a $4500`
    * Dado `que la cuenta del usuario no es premium, y el monto de sus bebidas seleccionadas es $1000`,
    * Cuando `el usuario presiona "Calcular precio"`
    * Entonces `el sistema informa: "Precio: $1000"`
* **Escenario 2**: `Usuario premium y un monto total mayor a $4500`
    * Dado `que la cuenta del usuario es premium, y el monto de sus bebidas seleccionadas es $5000`,
    * Cuando `el usuario presiona "Calcular precio"`
    * Entonces `el sistema aplica el descuento del 20% del premium, y del 10% por el monto mayor a $4500 e informa: "Precio: $3500`.
* **Escenario 3**: `Usuario premium y un monto total menor a $4500`
    * Dado `que la cuenta del usuario es premium, y el monto de sus bebidas seleccionadas es $3000`,
    * Cuando `el usuario presiona "Calcular precio"`
    * Entonces `el sistema aplica el descuento del 20% de premium, e informa: "Precio: $2400"`
* **Escenario 4**: `Usuario sin premium y con monto toal mayor a $4500`
    * Dado `que la cuenta del usuario no es premium, y el monto de sus bebidas seleccionadas es $5000`,
    * Cuando `el usuario presiona "Calcular precio"`
    * Entonces `el sistema aplica el descuento del 10% por el monto, e informa: "Precio: $4500"`


---
