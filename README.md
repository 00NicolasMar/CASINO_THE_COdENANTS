# CASINO_THE_COdENANTS
## 1. Introducción y Contexto
### ¿Cuál es el problema que aborda este proyecto?
El proyecto es un casino virtual el cual cuenta con dos juegos disponibles, uno llamado Royale Roulette y Magic Dice. El primero es una ruleta la cual consatara de 37 numeros del 0 al 36, de los cuales 18 son numeros identificados por color negro, los 18 restantes siendo rojos y el 0 siendo elo unico numero color verde de toda la ruleta. Este juego cuenta con la opción de ingresar un monto de apuesta, y seleccionar las siguientes opciones de apuesta, la cual generará una ganancia correspondiente a lo seleccionado.
#### Escoger color
##### -Los colores rojo y negro generan una ganancia del *2 del dinero apostado
##### -El color Verde genera una ganancia del *50 siendo este el premio mayor de la ruleta 
#### Número 
##### -La opción de escoger un número está, y siempre y cuando se acierte el número, la ganancia se dará en un *5 del valor apostado
#### Par o Impar
##### -Si se acierta que es par o impar, la ganancia será de *1.5 del valor apostado
El hecho de que existan estas opciones de apuesta no implica que sea necesario seleccionarlas todas, por lo que si no desea ingresar en su apuesta algunas de las anteriores opciones, puede expresar “ninguno”, lo que indicará que no se apostara en tal apartado. (debe seleccionar al menos 1 de las opciones de apuesta, o si no no se hará efectiva la apuesta).
### ¿Qué nos motivó a elegir este tema?
Realmente nunca hubo un interés en particular por los juegos de azar, simplemente nos generaba curiosidad el entender el funcionamiento de un casino virtual, más específicamente los juegos de ruleta o dados mágicos. Ya que se creería que uno tiene más posibilidades de ganar que de perder, pero realmente esto es así?
Veámoslo de la siguiente manera, en una ruleta de casino convencional se cuentan con 37 números, por lo tanto según el casino oddschecker la posibilidad de acertar dicho número es básicamente de un  2,70% contra un 97,30 de perder, pero en cuanto apuestas relacionadas con un conjunto específico de números (color o paridad) la posibilidad en cada caso es de ganar es de 48.6%.
Visto de esta manera no está tan mal… ya que al apostar por un color tienes una posibilidad de ganar del 50% lo que significa duplicar tu dinero, o no?

### ¿Cuál es el objetivo principal del proyecto?
Presentar el funcionamiento de los juegos de azar virtuales como lo son el casino o los dados mágicos.

## 2. Marco Teórico
### ¿Qué autores o fuentes sirvieron de referencia principal?
Para la realización del juego de la ruleta de casino, utilizamos como referencia y guia de desarrollo, los siguientes videos y paginas web.

#### 1. https://www.youtube.com/watch?v=SfcR7GXEd6Y

este video explica de manera rápida, pero clara como se programa una ruleta con condiciones simples, por lo que fue un muy buen pie de inicio a la hora de empezar a escribir el código.

#### 2. https://www.scj.cl/funcionamiento-de-los-juegos/juegos-de-ruleta#:~:text=La%20ruleta%20es%20un%20juego,rueda%20horizontal%20giratoria%2C%20denominada%20ruleta.
	
esta página web nos ayudó a comprender el funcionamiento de diversos tipos de ruletas, y así basarnos en una en específico para la realización de mi código (la ruleta europea).

#### 3. https://www.youtube.com/watch?v=jJyKET9ZVdE

este video nos sirvio para aprender a usar las palabras reservadas try, except y finally, las cuales nos funcionaron para que a la hora de ingresar en el input un dato diferente a un entero o al el dato que se solicite en el input, no nos de un error, si no que en cambio nos de un print indicando que el valor ingresado es invalido o algo por el estilo.

## 3. Metodología
### ¿Qué métodos utilizamos para desarrollar el proyecto?
para el desarrollo del proyecto se inicio primero entendiendo como funcionaria el juego principal de la ruleta y cual seria, determinando de forma unanime que lo mejor era hacer una ruleta de casino. Seguido a esto se procedio con el planteamiento de su funcionamiento por medio de diagramas que presentarian de manera comprensible y mas visual como funcionaria dicho programa. 


