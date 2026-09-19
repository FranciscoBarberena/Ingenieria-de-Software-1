## Frente

* **ID**: `Iniciar sesión`
* **Título**: Como `Empleado` quiero `iniciar sesión` para `solicitar una licencia`.
* **Reglas de negocio**:


---


## Reverso
* Criterios de Aceptación (`Iniciar sesión`)

* **Escenario 1**: `Logueo exitoso`
    * Dado `un mail 1234@gmail.com ya registrado, cuya contraseña es "12345"`,
    * Cuando `el Empleado ingresa: mail 1234@gmail.com y contraseña 12345, y luego pulsa "Iniciar sesión"`
    * Entonces `el sistema comprueba que la contraseña y el mail se corresponden, y lo redirige a la página principal.`
* **Escenario 2**: `Logueo fallido por mail no registrado`
    * Dado `un mail 4321@gmail.com no registrado en el sistema`,
    * Cuando `el Empleado ingresa: mail 4321@gmail.com y contraseña 12345, y luego pulsa "Iniciar sesión"`
    * Entonces `el sistema comprueba que el mail se encuentre registrado. Informa: "Error: el mail 4321@gmail.com no se encuentra registrado."`.
* **Escenario 3**: `Logueo fallido por contraseña inválida`
    * Dado `un mail 1234@gmail.com ya registrado, cuya contraseña no es "c0ntrasenia"`,
    * Cuando `el Empleado ingresa: mail 1234@gmail.com y contraseña "c0ntrasenia", y luego pulsa "Iniciar sesión"`
    * Entonces `el sistema comprueba que la contraseña y el mail no se corresponden. Informa: "Error: No se pudo iniciar sesión, mail y/o contraseña incorrecta/s"`
---
