# CASINO THE COdENANTS
## 1. Introducción y Contexto
### ¿Cuál es el proyecto?
El proyecto es un casino virtual tematizado en la serie de videojuegos Halo, el cual cuenta con 2 juegos de azar, llamados "SpartanRoulette" y "RiquezaDelCovenant" .
### ¿Qué nos motivó a elegir este tema?
Nos generaba curiosidad el entender el funcionamiento de un casino virtual, más específicamente los juegos de ruleta. Ya que se creería que uno tiene más posibilidades de ganar que de perder, pero realmente esto es así?
Veámoslo de la siguiente manera, en una ruleta de casino convencional se cuentan con 37 números, por lo tanto según el casino oddschecker la posibilidad de acertar dicho número es básicamente de un  2,70% contra un 97,30 de perder, pero en cuanto apuestas relacionadas con un conjunto específico de números (color o paridad) la posibilidad en cada caso es de ganar es de 48.6%.
Visto de esta manera no está tan mal… ya que al apostar por un color tienes una posibilidad de ganar del 50% lo que significa duplicar tu dinero, o no?. 

### ¿Cuál es el objetivo principal del proyecto?
Presentar el funcionamiento de los juegos de azar virtuales como lo son la ruleta, y demas juegos que se pueden encontrar en este entorno. asi como desarrollar un programa que permita jugarlos y replicar algunos juegos de casino con el fin de generar un interes en los jugadores (no fomentamos la ludopatia, simplemente es una simulacion). 

# Ahora si, a volvernos millonarios.
# SpartanRoulette
Este juego es una ruleta que consta de 37 casillas, señaladas con números del 0 al 36, de los cuales 18 son números identificados por color negro, los 18 restantes son de color rojo y el 0 siendo el único número color verde de toda la ruleta. Este juego cuenta con la opción de ingresar un monto de dinero, y seleccionar las siguientes opciones de apuesta, la cual generará una ganancia correspondiente a lo seleccionado.
### Opciones de apuesta:
#### Escoger color
 - Los colores rojo y negro generan una ganancia de **X2 sobre el dinero apostado**.
 - El color Verde genera una ganancia del **X50** sobre el dinero apostado, siendo este el premio mayor de la ruleta. 
#### Número 
 - La opción de escoger un número está, y siempre y cuando se acierte el número, la ganancia obtenida sera de **X5** sobre el valor apostado.
#### Par o Impar
 - Si se acierta que es par o impar, la ganancia será de **X1.5 veces el valor apostado**.
El hecho de que existan estas opciones de apuesta no implica que sea necesario seleccionarlas todas, por lo que si no desea ingresar en su apuesta algunas de las anteriores opciones, puede expresar “ninguno”, lo que indicará que no se apostara en tal apartado. (debe seleccionar al menos 1 de las opciones de apuesta, o si no no se hará efectiva la apuesta).
#### Si no acerta alguna de las opciones seleccionadas, el jugador pierde el dinero apostado. 
### Herrmientas vistas en el curso que se ultilizaron en el codigo: Bucles, listas, condicionales y funciones.
# RiquezaDelCovenant
Este juego es una maquina tragamonedas que muestra en un recuadro de 3x3, donde pueden salir simbolos aleatorios en cada casilla.
### Reglas de ganancia
 - Si coincide el mismo simbolo en 3 casillas seguidas, gana **X10** en base al valor apostado.
 - Si coincide el mismo simbolo en 2 casillas seguidas, gana **X2** en base al dinero apostado.
#### Si no se cumplen las 2 opciones anteriores, el jugador pierde el dinero apostado. 
### Herrmientas vistas en el curso que se ultilizaron en el codigo: Bucles, listas, condicionales, funciones y matricez.****



## 2. Marco Teórico
### ¿Que fuentes utilizamos para la realizacion?
Para la realización del juego de la ruleta de casino, utilizamos como referencia y guia de desarrollo, los siguientes videos y paginas web.

#### 1. https://www.youtube.com/watch?v=SfcR7GXEd6Y

este video explica de manera rápida, pero clara como se programa una ruleta con condiciones simples, por lo que fue un muy buen pie de inicio a la hora de empezar a escribir el código.

#### 2. https://www.scj.cl/funcionamiento-de-los-juegos/juegos-de-ruleta#:~:text=La%20ruleta%20es%20un%20juego,rueda%20horizontal%20giratoria%2C%20denominada%20ruleta.
	
esta página web nos ayudó a comprender el funcionamiento de diversos tipos de ruletas, y así basarnos en una en específico para la realización de mi código (la ruleta europea).

#### 3. https://www.youtube.com/watch?v=jJyKET9ZVdE

este video nos sirvio para aprender a usar las palabras reservadas try, except y finally, las cuales nos funcionaron para que a la hora de ingresar en el input un dato diferente a un entero o al el dato que se solicite en el input, no nos de un error, si no que en cambio nos de un print indicando que el valor ingresado es invalido o algo por el estilo.

## 3. Metodología
### ¿Qué métodos utilizamos para desarrollar el proyecto?
para el desarrollo del proyecto se inicio primero entendiendo como funcionaria el juego principal del casino y cual seria. Determinando de forma unanime que estaria bien hacer hacer una ruleta de casino. 

Seguido a esto, se procedio con el planteamiento de su funcionamiento por medio de un diagrama que presentarian de manera comprensible y mas visual como funcionaria dicho programa. Pero adicional a eso nos toco ver videos de guia para poder desarrollar el codigo de la ruleta asi como un repaso a los temas vistos en clase. Cabe aclarar que siempre es util plantear que es lo que queremos hacer y un paso a paso de la realizacion del codigo, ya que a la hora de "traducirlo" a python siempre sera mas sencillo, ya que nos ahorrariamos bastante tiempo probando a ver que es lo que funciona, y no improvisariamos a la hora de ralizar el codigo.
A continuacion presentamos el diagrama:

```mermaid
 flowchart TD
    Inicio(Inicio) -->FM[Función Main] -->
    Q[ganancias = 0] -->
    R[condiciones_totales = 0] -->
    S[Condiciones_acertadas = 0]-->
    FC[Función Casino] -->
    A["print (Bienvenido al Casino)"] 
    A --> B[input: Ingrese el dinero]
    B -->C{dinero <= 0}
    C -->|Sí|D["print (La cantidad apostada debe ser mayor a 0.)"]
    D -->B
    C -->|No|WH[input: Selecciona el juego que deseas jugar: ruleta 'r' o tragamonedas 't':]
    WH -->E[While True:]
    E -->F{juegos == r}
    F -->G{juegos == t}
    G -->H[función tragamonedas]
    H -->TA["print(🎰 Juego Tragamonedas 🎰)"]
    TA-->TB["print(juganado)"]
    TB-->TC["time.sleep(2)"]
    -->TD["simbolos = [🍒, 🍋, 🔔, ⭐, 7️⃣, ❌, 👨‍✈️, 👽, ☘️, 🌌, ☣️, 🧬, ☠️, 🛸]"]
    -->TE["matriz = []"]
    -->TF["for _ in range(3)"]
    -->TG["fila = []"]
    -->TH["for _ in range (3)"]
    -->TI["fila.append(random.choise(simbolos))"]-->|x3|TH
    -->TJ["matriz.append(fila)"]-->TF
    -->TK[for fila in matriz]
    -->TL["print(' | '.join(fila))"]-->TK
    -->TM["resultado = matriz[1]"]
    -->TN["print('Resultado: ' + ' | '.join(resultado))"]
    -->TO[ganancia_h = 0]
    -->TP{"len(set(resultado)) == 1:"}
    TP-->|sí|TV["print(¡Felicidades! Gano 10 veces tu apuesta.)"]
    -->TW[ganancia_h = dinero * 10]-->TX
    TP-->|no|TQ{"len(set(resultado)) == 2:"}
    TQ-->|sí|TR["print(Casi todas, solo se dobla tu apuesta)"]
    -->TS[ganancia_h = dinero * 2]-->TX
    TQ-->|no|TT["print(mala suerte, perdiste)"]-->TX
    TX[ganancia = 0]
    -->TY["columna_medio = []"]
    -->TAA["for i in range(3)"]
    -->TZ["columna_medo.append(matriz[i][1])"]-->|x3|TAA
    TZ-->TAB{"len(set(columna_medio)) == 1:"}
    -->|sí|TAC["print("¡Felicidades! Obtuviste tres iguales en la columna del medio. Ganaste 1.5 veces tu apuesta.]
    -->TAD[ganancia_v = dinero * 1.5]-->TAE
    TAB --> |no|TAE
    TAE[return ganancia_h + ganancia_v]
    -->TAF["ganancia = tragamonedas(dinero)"]
    -->TAG["print('Ganancia total: $' +str(ganancia))"]
    -->AW
    G -->|Else|GA["print(Opción de juego no válida. Por favor, elige 'Casino' o 'nose'.)"]
    F -->Efe["color_apuesta = input(Un color entre rojo, negro, verde o ninguno:)"]
    Efe -->J{"color_apuesta  not in [rojo, negro, verde, ninguno]"}
    J -->K[Ingrese una opción válida]
    K -->J
    J -->Co(Continue)
    Co -->Ele["numero_par = input(Selecciona si tu número será 'par', 'impar' o 'ninguno':"]
    Ele -->Ola{"numero_par not in ['par', 'impar', 'ninguno']:"}
    Ola -->Wao["print( Opción no válida. Por favor, elige entre 'par', 'impar' o 'ninguno'.)"]
    Wao -->con(Continue)
    con -->L{número_ruleta == 0}
    L -->|Sí|M[verde]
    L -->Ene{2, 4, 6, 8, 10, 11, 13, 15, 17, 20, 22, 24, 26, 28, 29, 31, 33, 35}
    Ene -->|Sí|N[negro]
    Ene -->|Else|O[rojo]
    M --> P
    N --> P
    O --> P[print: resultado del número y color]-->
    T[color_apuesta = input: color] -->
    U{color_apuesta != ninguno} -->
    V[condiciones_totales += 1] -->
    W{color_apuesta == color_ruleta} -->
    X[ganancias += dinero * 2]-->
    Y[Condiciones_acertadas += 1]-->
    Z[print: acertaste resultado]-->
    AA{numero_par != ninguno}-->
    AB[condiciones_totales += 1] -->
    AC{numero_par == par & numero_ruleta % 2 == 0 & numero_ruleta != 0}-->
    AD[ganancia += dinero * 1.5]-->
    AE[condiciones_acertadas += 1]-->
    AF[print : Acertaste par]
    AC -->AG{numero_par == impar & numero_ruleta % 2 != 0} -->
    AH[ganacia += dinero * 1.5]-->
    AI[condiciones_acertadas += 1]-->
    AJ[print : Acertaste impar]-->AK
    AF -->AK{numero_elegido != ninguno} -->
    AL[condiciones_totales += 1] -->
    AM{numero_ruleta == numero_elegido} -->
    AN[ganancias += dinero * 5] -->
    AO[condiciones_acertadas += 1]-->
    AP[print : Adivinaste el número]-->
    AQ{condiciones_acertadas < condiciones_totales}
    AQ -->|Sí|AS[Print: Perdiste]-->AU
    AQ -->|No|AT[Print: Ganaste]-->AU
    AU[Print : Dinero Ingresado]-->
    AV[Print : Ganancia Total]-->
    AW[jugar_nuevamente = input ¿quieres volver a jugar?]-->
    AX{jugar_nuevamente != sí}-->|Dijo que sí|F
    AX -->|Dió otra respuesta|Fin(Break : Fin)
 ```
### ¿Qué herramientas o recursos se emplearon en el desarrollo?

Para su desarrollo utilizamos la herramienta web Google Colab: https://colab.google/ ya que esta nos brinda una facilidades a la hora de escribir y probar el codigo de manera sencilla, facilidades como lo son:

- Acceso a GPU / TPU.
- Compartir código gracias a la programación colaborativa.
- Visualizaciones gráficas sencillas.
  
##### (cabe recalcar que se desactivo la sistencia de IA). 

![image](https://github.com/user-attachments/assets/32a16a0d-fc05-4a57-ba8c-46bfcdb4d32b)


 Tambien utilizamos el programa Visual Studio Code. Ya que gracias a este logramos probar el programa y comprobar nuevamente el funcionamiento del codigo.

## 5. ¿Cómo funciona el programa?
##### A continuacion haremos una explicacion paso a paso del codigo, para que el entendimiento de su funcionamiento sea claro.
#### - Import y Definir funcion principal

```pseudocode
import random
import time

def casino():

        print("Bienvenido al Casino The CoDenants")
```
En esta primera parte del codigo, se hizo un import de random que va a ser util para la seleccion del numero ganador de la ruleta, y el import time que va a ser el encargado de simular un giro de ruleta.
Tambien se definio la funcion principal del programa que fue llamada Casino, haciendo asi la primera impresion del codigo, la cual sera la bienvenida al casino.
#### - Ingreso de monto de apuesta

```pseudocode
 dinero = float(input("Ingresa la cantidad de dinero con la cual quieres jugar: "))
        if dinero <= 0:
            print("La cantidad apostada debe ser mayor a 0.")
```
En este apoartado se realiza el ingreso del monto el cual va a apostar el jugador, utilizando el condicional `if` se establece que si se ingresa un valor menor a 0 no puede jugar, ya que no es valido el monto.
#### - Seleccion de juego.

```pseudocode
 juegos = input("Selecciona el juego que deseas jugar: 'Ruleta' o 'nose': ")
        while True:
          if juegos == "ruleta":
```
En este apartado se realiza la seleccion de el juego que desea jugar (actualmente solo esta disponible la ruleta). luego un bucle while el cual dera util a la hora de finalizar el juego de la ruleta permitiendo que el jugador pueda volver a apotar en el mismo juego, y se establece el inicio del juego (ruleta) si se selecciona dicha opcion. 
#### - Apuestas a color y pareidad

```pseudocode
            color_apuesta = input("Escoge un color entre rojo, negro, verde o ninguno: ")
            if color_apuesta  not in ["rojo", "negro", "verde", "ninguno"]:
                print("Ese color no está en la ruleta. Por favor, elige entre 'rojo', 'negro', 'verde' o 'ninguno'.")

            numero_par = input("Selecciona si tu número será 'par', 'impar' o 'ninguno': ")
            if numero_par not in ["par", "impar", "ninguno"]:
                print("Opción no válida. Por favor, elige entre 'par', 'impar' o 'ninguno'.")
```
En estas lineas se establecen dos apuestas que se pueden realizar en el casino, como lo son la seleccion de color y de propiedad par de el numer, utilizando condicional if, indicando que si seleccionas algo diferente a las opciones dadas, no puedes continuar tu apuesta.
#### - Apuesta a Numero especifico

```pseudocode
numero_elegido = input("Escoge un número entre 0 y 36 o escribe ninguno: ")
            if numero_elegido != "ninguno":
                try:
                    numero_elegido = int(numero_elegido)
                    if numero_elegido < 0 or numero_elegido > 36:
                        print("El número que escogiste no hace parte de la ruleta. Por favor, elige un número entre 0 y 36.")
                   
                except ValueError:
                    print("Debes ingresar otro numero o escribir ninguno.")
```
En este apartado se establece la opcion de escoger un numero que este dentro del rango (0, 36), en el cual si eliges un numero que no se encuentre en el rango, no podras continuar tu apuesta y deberas seleccionar un numero que si este dentro del rango anteriormente mencionado. (aqui se utilizo el try, except para que el codigo no diera error, si no que en vez de eso hiciera una impresion indicando que se debe ingresar otro numero)
#### - Giro de ruleta

```pseudocode
	    print("Girando la ruleta...")
            for _ in range(10):
              print("Numeros girando: " + str(random.randint(0, 36)), end="\r")
              time.sleep(0.5)
              numero_ruleta = random.randint(0, 36)
```
Aqui se hace la simulacion del giro de la ruleta, utilizando el `import random` y `import time`, haciendo primero un print que simule el girando la ruleta...., luego estableciendo que haga un conteo de 10 numeros (cado uno durando 0.5seg), y que al final de como resultado el numero seleccionado de manera aleatoria, numero el cual sera el que cayo en la ruleta. (dicho numero estara en el rango 0, 36).
#### - Establecer color a cada numero

```pseudocode
	    if numero_ruleta == 0:
              color_ruleta = "verde"
            elif numero_ruleta in [2, 4, 6, 8, 10, 11, 13, 15, 17, 20, 22, 24, 26, 28, 29, 31, 33, 35]:
              color_ruleta = "negro"
            else:
              color_ruleta = "rojo"
```
En este apartado se establecen condiciones que determinaran el color a cada numero, el 0 siendo el unico verde, y por medio de una lista establecer que los numeros  [2, 4, 6, 8, 10, 11, 13, 15, 17, 20, 22, 24, 26, 28, 29, 31, 33, 35] son de color negro, dejando asi a los numero que no sean pertenecientes a la lista anterior ni 0 como numeros rojos.
#### - Numero Ganador

```pseudocode
print("La ruleta cayó en el número " + str(numero_ruleta)+ " " + str(color_ruleta))
```
Esta linea hace una impresion del numero que cayo en la ruleta y tambien a que color pertenece.
#### - Apuestas combinadas

```pseudocode
ganancia = 0
            condiciones_totales = 0
            condiciones_acertadas = 0
```
Estas lineas son utiles para determinar que si el jugador hizo mas de una apuesta, asegurando que la ganacia corresponda a las apuestas que hizo.
#### - 

```pseudocode
            if color_apuesta != "ninguno":
                condiciones_totales += 1
                if color_apuesta == color_ruleta:
                    ganancia += dinero * 2
                    condiciones_acertadas += 1
                    print("¡Acertaste el color " + str(color_apuesta) + "! Ganaste el doble de tu apuesta.")

            if numero_par != "ninguno":
                condiciones_totales += 1
                if numero_par == "par" and numero_ruleta % 2 == 0 and numero_ruleta != 0:
                    ganancia += dinero * 1.5
                    condiciones_acertadas += 1
                    print("¡Acertaste que el número es par! ")
                elif numero_par == "impar" and numero_ruleta % 2 != 0:
                    ganancia += dinero * 1.5
                    condiciones_acertadas += 1
                    print("¡Acertaste que el número es impar! ")

            if numero_elegido != "ninguno":
                condiciones_totales += 1
                if numero_ruleta == numero_elegido:
                    ganancia += dinero * 5
                    condiciones_acertadas += 1
                    print("¡Adivinaste el número exacto" + str(numero_elegido) + "! Ganaste 5 veces tu apuesta.")
```
Estas lineas son las encargadas de determinar las ganancias por medio de las condiciones totales y las condiciones ganadas, dando como resultado que si el jugador hizo mas de 1 apuesta cada condicion correspondera a las condiciones que debera acertar para ganar el dinero.
#### - Determinacion de ganacias

```pseudocode
            if condiciones_acertadas < condiciones_totales:
                ganancia = 0
                print("No acertaste todas las condiciones seleccionadas... Perdiste tu dinero.")
            else:
                print("¡Increíble! Acertaste todas las "+ str(condiciones_acertadas) + " condiciones seleccionadas.")
	    print("Dinero ingresado: $" + str(dinero))
            print("Ganancia total: $" + str(ganancia))
```
En estas lineas se establece que cada apuesta hecha tiene que corresponder a las apuestas acertadas, con el fin de que la ganancia sea acorde a lo que se apostó, y tambien determinando que si de las apuestas que hizo fallo al menos 1, pierde todo su dinero, haciendo una impresion de lo que tenia vs lo que gano o perdio segun sea el caso.
#### - Seleccion de otro juego 

```pseudocode
          elif juegos == "nose":
            print("Aun no, espera que dejemos la ruleta super jajajs")
          else:
            print("Opción de juego no válida. Por favor, elige 'ruleta' o 'nose'."
```
En estas lineas se establece el caso en el cual el jugador en vez de jugar ruleta selecciona otro juego, o algo diferente a las opciones.
#### - ¿Deseas continuar jugando? 

```pseudocode
          jugar_nuevamente = input("¿Quieres jugar nuevamente? sí o no bro..: ")
          if jugar_nuevamente != "si":
              print("Gracias por jugar en el Casino The CoDenants. ¡Hasta la próxima!")
              break
```
En estas lineas se cierra por asi decirlo el bucle while, dando una opcion al jugador de si desea continuar jugando o si ya perdio lo suficiente. 
#### - Cierre

```pseudocode
if __name__ == "__main__": 
    casino()
```
Una vez dadas las condiciones, se ejecuta el programa.

### ¿Qué problemas hubieron y cómo los solucionamos?
En el desarrollo del codigo hubieron bastantes inconvenientes a la hora de su realizacion, uno de ellos, para nosotros el mas importante era hacer que si el jugador fallaba alguna de las condiciones que escogio apostar, perdiera todo su dinero, ya que siempre que fallaba una de sus condiciones ganaba igualmente dinero, cosa que si bien es justa, en terminos de caino implica perdidas, y quien dijo que un casino era justo. Por lo que decidimos establecer que cada condicion que seleccionara seria 1 condicion agregada a sus condiciones totales, y si acertaba una, estas significarian 1 unidad a sus condiciones ganadas estableciendo asi que si o si el numero de condiciones totales debia ser igual a el numero de condiciones acertadas.

Otro problema que tuvimos, fue el hecho de que si el jugador ingresaba un numero que no perteneciera al rango (0, 36) nos daba error, cosa que si bien no es critica, corta la experiencia, por lo que teniamos que buscar una solucion al problema (fue un poco dificil porque no sabiamos que funcionaba), para llegar a la solucion con ayuda de un compañero, nos dijo que investigaramos un poco sobre las excepciones, por lo que despues de un ratito viendo un video logramos dar la solucion a dicho "problema".

## 6. Conclusion.









