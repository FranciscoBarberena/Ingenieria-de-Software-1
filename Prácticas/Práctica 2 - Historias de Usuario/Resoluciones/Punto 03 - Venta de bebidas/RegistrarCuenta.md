## Frente

* **ID**: `Registrar cuenta`
* **Título**: Como `Persona` quiero `crearme una cuenta` para `comprar bebidas alcohólicas en línea`.
* **Reglas de negocio**:
    * Solo se pueden crear cuentas de personas mayores a 18 años.
    * El mail debe ser único y será usado como nombre de usuario.

---
* Duda: mail de nombre de usuario es regla de negocio?
## Reverso
* Criterios de Aceptación (`Registrar cuenta`)

* **Escenario 1**: `Registro exitoso`
    * Dada `una edad de 19 años y un mail 1234@gmail.con no registrado previamente`,
    * Cuando `la Persona ingresa: nombre Pepe, apellido Gonzales, mail 1234@gmail.com y edad 19, y luego pulsa "Registrarse"`
    * Entonces `el sistema crea la cuenta y le asigna una contraseña, que se envía al mail 1234@gmail.com. Luego informa, "Registro exitoso, su contraseña ha sido enviada al mail 1234@gmail.com"`
* **Escenario 2**: `Registro fallido por edad menor a 18 años`
    * Dada `una edad de 17 años`,
    * Cuando `la Persona ingresa: nombre Pepe, apellido Gonzales, mail 1234@gmail.com y edad 17, y luego pulsa "Registrarse"`
    * Entonces `el sistema no crea la cuenta. Informa en pantalla: "Error: la edad mínima para crear una cuenta es 18 años. La ley 24.788 prohíbe la venta de bebidas alcohólicas a menores."`.
* **Escenario 3**: `Registro fallido por mail ya registrado`
    * Dado `un mail 4321@gmail.com ya registrado previamente`,
    * Cuando `la Persona ingresa: nombre Pepe, apellido Gonzales, mail 1234@gmail.com y edad 19, y luego pulsa "Registrarse"`
    * Entonces `el sistema no crea la cuenta. Informa en pantalla: "Error: el mail 1234@gmail.com ya se encuentra registrado.".`
---
