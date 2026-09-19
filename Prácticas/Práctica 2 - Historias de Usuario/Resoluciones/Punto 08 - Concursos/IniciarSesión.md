## Frente

* **ID**: `Iniciar sesión`
* **Título**: Como `Docente` quiero `iniciar sesión` para `inscribirme a un concurso`.
* **Reglas de negocio**:


---


## Reverso
* Criterios de Aceptación (`Iniciar sesión`)

* **Escenario 1**: `Logueo exitoso`
    * Dado `un mail 1234@gmail.com ya registrado, cuya contraseña es "12345"`,
    * Cuando `el Docente ingresa: mail 1234@gmail.com y contraseña 12345, y luego pulsa "Iniciar sesión"`
    * Entonces `el sistema comprueba que la contraseña y el mail se corresponden, y lo redirige a una lista de materias.`
* **Escenario 2**: `Logueo fallido por Docente no registrado`
    * Dado `un mail 4321@gmail.com no registrado en el sistema`,
    * Cuando `el Docente ingresa: mail 4321@gmail.com y contraseña 12345, y luego pulsa "Iniciar sesión"`
    * Entonces `el sistema comprueba que el mail se encuentre registrado. Informa: "Error: No se pudo iniciar sesión, mail y/o contraseña incorrecta/s"`.
* **Escenario 3**: `Logueo fallido por contraseña inválida`
    * Dado `un mail 1234@gmail.com ya registrado, cuya contraseña no es "c0ntrasenia"`,
    * Cuando `el Docente ingresa: mail 1234@gmail.com y contraseña "c0ntrasenia", y luego pulsa "Iniciar sesión"`
    * Entonces `el sistema comprueba que la contraseña y el mail no se corresponden. Informa: "Error: No se pudo iniciar sesión, mail y/o contraseña incorrecta/s"`
---
