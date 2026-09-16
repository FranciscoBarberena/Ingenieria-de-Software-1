# Parte I: Redes de Petri

## Inciso A

* Describa qué tipos de problemas se pueden modelar utilizando Redes de Petri.
    * Las Redes de Petri sirven para modelar problemas con un alto grado de concurrencia y paralelismo. Es por esto que se usan para representar sistemas en tiempo real.

## Inciso B

* Enumere y explique elementos, vistos en teoría, que se utilizan para modelar las Redes de Petri.
    * Para modelar las Redes de Petri, se pueden usar representaciones gráficas o la representación matemática
    * **Representación gráfica**: cada estado se modela como un circulo y cada transición como una barra. Cualquier flecha direccionada debe ir de una transición a un estado o viceversa (nunca directamente estado-estado o transición-transición).
    * **Representación matemática**: una Red de Petri se representa como una tupla de 4 elementos (4-upla). De la siguiente manera:
        * C = (P, T, I, O)
            * P representa los estados (*places*)
            * T representa las transiciones
            * I representa la función de entrada
            * O representa la función de salida

## Inciso C

* Explique que son las marcas o *tokens*.
    * Las marcas o *tokens* representan el flujo de actividades de la red. Cada vez que pasa un instante, si se dan las condiciones necesarias, dichos *tokens* realizarán una transición y viajará a otro estado.
    * Las condiciones necesarias y la manera en la que un *token* viaja tienen que ver con la cantidad de flechas de entrada y de salida de una transición:
        * Si una transición tiene 5 flechas de entrada, necesita que 5 *tokens* apunten hacia ella para poder ejecutarse
        * Si un transición tiene 2 flechas de salida, una vez que suceda, de ella se desprenderán 2 *tokens*.

## Inciso D

* Explique qué significa una transición que tiene salidas pero no entradas.
    * Una transición como la descrita se representa de la siguiente manera:
        * |--->
        * Lo que significa es que esa transición está siempre habilitada, y de ella se desprenden *tokens* aleatoriamente. Por ejemplo, se puede usar para modelar que ”llegan clientes de manera aleatoria”.

## Inciso E

* Explique qué significa una transición que tiene entradas pero no salidas.
    * Una transición como la descrita se representa de la siguiente manera:
        * --->|
        * Lo que significa es que a esa transición siempre pueden llegar *tokens*. Una vez que lo hacen, dejan de ser parte del problema. Por ejemplo: “Salen los clientes que ya terminaron de comprar”.

# Parte II: Repaso de conceptos generales

1. **Opción correcta: B.** Tres *tokens* que representan 3 jugadores.
2. **Opción correcta: C.** Las transiciones se representan con una barra vertical.
3. **Opción correcta: B.** Las flechas en las Redes de Petri representan arcos dirigidos.
4. **Opción correcta: C.** Estado ---> Transición
5. **Opción correcta: A.** Sí, está habilitada porque hay un *token* en el sitio de entrada.
6. **Opción correcta: C.** Que haya un token en cada uno de los sitios de entrada.
7. **Opción correcta: C.** No, porque falta el *token* del cobrador.
8. **Opción correcta: A.** Una transición con un único arco de entrada, consume solo 1 *token* al dispararse.