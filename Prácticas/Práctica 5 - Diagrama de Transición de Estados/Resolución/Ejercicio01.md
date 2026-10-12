## Ejercicio 01

* Errores en el diagrama:
    * “Apagando” debería ser un estado final, representado por un punto negro rodeado de un círculo.
    * La condición de la primera transición `[la licuadora está apagada]` es innecesaria. Si la licuadora se encuentra en el estado inicial, necesariamente debe estar apagada
    * Falta un evento que permita pasar del estado “Funcionando en velocidad 2” a “Funcionando a velocidad 1”. Debería ser disparado por el botón “disminuir”.