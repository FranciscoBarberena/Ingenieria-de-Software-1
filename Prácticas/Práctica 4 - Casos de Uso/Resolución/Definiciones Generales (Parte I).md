# Inciso A

* El desarrollo centrado en el usuario es una metodología de creación de productos que coloca al usuario final y sus necesidades en el centro de todas las fases, desde la investigación inicial hasta la evaluación.

# Inciso B

* La técnica de casos de uso es el proceso de modelado de las “funcionalidades” del sistema en término de los eventos que interactúan entre los usuarios y el sistema. Es decir, cada caso de uso sirve para representar un requerimiento funcional del sistema, y ver cómo este se relaciona con los distintos actores y otros CU.

# Inciso C

* Un actor es un rol (persona, sistema externo o tiempo) que inicia un caso de uso del sistema.
* Un escenario es el detalle de un caso de uso, en el que se describe su nombre, descripción, actores, precondiciones, curso normal, curso alterno y postcondición.

# Inciso D

* Las distintas relaciones que pueden aparecer en el diagrama de casos de uso son:
    * **Asociaciones:** Relación entre un actor y un CU en el que interactúan entre sí. Si la flecha es dirigida, (A → B), indica que A ejecuta B. Si no lo es, indica simplemente que están relacionados.
    * **Extensiones** (*extends*): Un caso de uso puede extender la funcionalidad de otro. Los CU extensiones solo pueden ser iniciados por el CU que extienden
    * **Uso o inclusión** (*uses*): Combina los pasos comunes de 2 o más CU. Si los casos de uso A y B, ambos utilizan C, se crea una flecha dirigida de A y B hacia C, indicando que lo usan.
    * **Herencia:** Relación entre actores donde un actor hereda las funcionalidades de uno o varios actores.

# Inciso E

* Beneficios de usar CU:
    * Herramienta para capturar requerimientos funcionales.
    * Descompone el alcance del sistema en piezas más manejables.
    * Medio de comunicación con los usuarios.
    * Utiliza lenguaje común y fácil de entender por las partes.
    * Permite estimar el alcance del proyecto y el esfuerzo a realizar.
    * Define una línea base para la definición de los planes de prueba.
    * Define una línea base para toda la documentación del sistema.
    * Proporciona una herramienta para el seguimiento de los requisitos.
