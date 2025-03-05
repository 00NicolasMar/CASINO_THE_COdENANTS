# CASINO THE COdENANTS
## 1. Introducción y Contexto
### ¿Cuál es el proyecto?
El proyecto es un casino virtual tematizado en la serie de videojuegos Halo, el cual cuenta con 2 juegos de azar, llamados "SpartanRoulette" y "RiquezaDelCovenant" .
### ¿Qué nos motivó a elegir este tema?
Nos generaba curiosidad el entender el funcionamiento de un casino virtual, más específicamente los juegos de ruleta. Ya que se creería que uno tiene más posibilidades de ganar que de perder, pero realmente esto es así?
Veámoslo de la siguiente manera, en una ruleta de casino convencional se cuentan con 37 números, por lo tanto según el casino oddschecker la posibilidad de acertar dicho número es básicamente de un  2,70% contra un 97,30 de perder, pero en cuanto apuestas relacionadas con un conjunto específico de números (color o paridad) la posibilidad en cada caso es de ganar es de 48.6%.
Visto de esta manera no está tan mal… ya que al apostar por un color tienes una posibilidad de ganar del 50% lo que significa duplicar tu dinero, o no?. 

### ¿Cuál es el objetivo principal del proyecto?
#### Implementar las herramientas vistas en el curso de programación para desarrollar un programa que simule 2 juegos de casino tipo Slot.
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
### Herrmientas vistas en el curso que se ultilizaron en el código: Bucles, listas, condicionales y funciones.
# RiquezaDelCovenant
Este juego es una maquina tragamonedas que muestra en un recuadro de 3 filas y 3 columnas donde salen simbolos aleatorios en cada casilla.
### Reglas de ganancia
 - Si coincide el mismo simbolo en 3 casillas seguidas, gana **X10** en base al valor apostado.
 - Si coincide el mismo simbolo en 2 casillas seguidas, gana **X2** en base al dinero apostado.
#### Si no se cumplen las 2 opciones anteriores, el jugador pierde el dinero apostado. 
### Herrmientas vistas en el curso que se ultilizaron en el código: Bucles, listas, condicionales, funciones y matricez.



## 2. Marco Teórico
### ¿Que fuentes utilizamos para la realizacion?
Para la realización del proyecto, utilizamos como referencia y guia de desarrollo, los siguientes videos y paginas web.

#### 1. https://www.youtube.com/watch?v=SfcR7GXEd6Y

Este video explica de manera rápida, pero clara como se programa una ruleta con condiciones simples, por lo que fue un muy buen pie de inicio a la hora de empezar a escribir el código.

#### 2. https://www.scj.cl/funcionamiento-de-los-juegos/juegos-de-ruleta#:~:text=La%20ruleta%20es%20un%20juego,rueda%20horizontal%20giratoria%2C%20denominada%20ruleta.
	
Esta página web nos ayudó a comprender el funcionamiento de diversos tipos de ruletas, y así basarnos en una en específico para la realización de mi código (la ruleta europea).

#### 3. https://www.youtube.com/watch?v=jJyKET9ZVdE

Este video nos sirvio para aprender a usar las palabras reservadas try, except y finally, las cuales nos funcionaron para que a la hora de ingresar en el input un dato diferente a un entero o al el dato que se solicite en el input, no nos de un error, si no que en cambio nos de un print indicando que el valor ingresado es invalido o algo por el estilo.

#### 4. https://www.youtube.com/watch?v=tU50HfCd4XQ&t=721s  y  https://www.youtube.com/shorts/aFgA4s6bhQM

Estos videos presentan una guía básica del como podriamos desarrollar el programa para simular la máquina tragamonedas.

## 3. Metodología
### ¿Qué métodos utilizamos para desarrollar el proyecto?
Para el desarrollo del proyecto se inicio primero entendiendo como funcionaria el juego principal del casino y cual seria. Determinando de forma unanime que estaria bien hacer hacer una ruleta de casino. 

Seguido a esto, se procedio con el planteamiento de su funcionamiento por medio de un diagrama que presentarian de manera comprensible y mas visual como funcionaria dicho programa. Pero adicional a eso nos toco ver videos de guia para poder desarrollar el codigo de la ruleta asi como un repaso a los temas vistos en clase. Cabe aclarar que siempre es util plantear que es lo que queremos hacer y un paso a paso de la realizacion del codigo, ya que a la hora de "traducirlo" a python siempre sera mas sencillo, ya que nos ahorrariamos bastante tiempo probando a ver que es lo que funciona, y no improvisariamos a la hora de ralizar el codigo.
A continuacion presentamos el diagrama:

```mermaid
  flowchart TD
    Inicio(Inicio) -->FM[Función Main] -->
    IMPR[import random]-->
    IMPT[import time]-->
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
    F -->|no|G{juegos == t}
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
    F -->|sí|Rul[ruleta]
    Rul --> RA[imprimir numeros]
    -->R0["0['#', 3, 6, 9, ..., 36]"]
    -->R1["1[ 0 , 2, 5, 8, ..., 35]"]
    -->R2["2['#', 1, 4, 7, ..., 34]"]
    -->RB["numeros_ruleta = [0, 1, 2]"]
    -->RC["for i in range(len(números_ruleta)):"]
    -->RD["for i in range(len(numeros_ruleta[i])):"]-->RC
    RD-->RE{"numeros_ruleta[i][j] == cambiar_num:"}
    -->|no|RD
    -->|sí|RF["numeros_ruleta[i][j] = ❌"]-->RD
    -->RG[for fila in numeros_ruleta:]
    -->RH["print(' '.join(map(str,fila)))"]-->RG
    -->RI["color_apuesta = input(Un color entre rojo (r), negro (n), verde (v) o ninguno (x):)"]
    RI -->J["while color_apuesta not in [r, n, v, x]"]
    J -->K["print(Ese color no está en la ruleta. Intenta de nuevo.)"]
    -->RL["color_apuesta = input(Un color entre rojo (r), negro (n), verde (v) o ninguno (x):)"]-->J
    -->RJ["numero_par = input(Selecciona si tu número será par (p), impar (i) o ninguno (x): )"]
    -->RM["while numero_par not in [p, i, x]"]
    -->RN["print(Opción inválida. Intenta de nuevo.)"]
    -->RO["numero_par = input(Selecciona si tu número será par (p), impar (i) o ninguno (x): )"]-->RM
    -->RP["numero_elegido = input(Escoge un número entre 0 y 36 o ninguno (x))"]
    -->RQ{numero_elegido != 'x'}-->|no|RAA
    RQ-->|sí|RS[while True:]
    -->RT{"try: numero_elegido = int(numero_elegido)"}
    -->|sirve|RU{0 <= numero_elegido <= 36}-->RV
    RU-->|sí|RX[break]-->RAA
    RV["print(Número fuera de rango. Intenta de nuevo.)"]-->RW
    RT-->|error|RY
    RW["numero_elegido = input(Escoge un número entre 0 y 36 o ninguno (x))"]-->RS
    RY["print(Entrada inválida. Intenta de nuevo.)"]
    -->RZ["numero_elegido = input(Escoge un número entre 0 y 36 o ninguno (x))"]-->RS
    RAA["print(Girando la ruleta...)"]-->
    RAB["for _ in range(10)"]-->
    RAC["print(Números girando:  + str(random.randint(0, 36)), end='\r')"]-->
    RAD["time.sleep(0.3)"]-->RAB
    RAB-->RAE["numero_ruleta = random.randint(0, 36)"]
    -->RAF["imprimir_ruleta(numero_ruleta)"]
    -->RAG{numero_ruleta == 0:}
    -->|sí|RAH[color_ruleta = 'verde']
    RAG-->|no|RAI{"numero_ruleta in [2, 4, 6, 8, 10, 11, 13, 15, 17, 20, 22, 24, 26, 28, 29, 31, 33, 35]:"}
    -->|sí|RAJ[color_ruleta = 'negro']
    RAI-->|no|RAK['rojo']-->
    RAL["print('La ruleta cayó en el número ' + str(numero_ruleta) + ' ' + str(color_ruleta)"]-->
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
    AX{jugar_nuevamente != 'si'}-->WH
    AX -->Fin(Break : Fin)
 ```
### ¿Qué herramientas o recursos se emplearon en el desarrollo?

Para su desarrollo utilizamos la herramienta web Google Colab: https://colab.google/ ya que esta nos brinda una facilidades a la hora de escribir y probar el codigo de manera sencilla, facilidades como lo son:

- Acceso a GPU / TPU.
- Compartir código gracias a la programación colaborativa.
- Visualizaciones gráficas sencillas.
  
##### (cabe recalcar que se desactivo la sistencia de IA). 

![image](https://github.com/user-attachments/assets/32a16a0d-fc05-4a57-ba8c-46bfcdb4d32b)

![image](https://github.com/user-attachments/assets/45f1bbf3-d57d-4209-a967-3bc6be5f8449)

 - Adicionalmente utilizamos la página de Unicode para los emojis de la maquina tragamonedas :) .

 - Tambien utilizamos el programa Visual Studio Code. Ya que gracias a este logramos probar el programa y comprobar nuevamente el funcionamiento del codigo.
## 5. ¿Cómo funciona el programa?
##### A continuacion haremos una explicacion paso a paso del codigo, para que el entendimiento de su funcionamiento sea claro.
#### - Import y Definir función principal

```pseudocode
import random
import time

def casino():
    print("Bienvenido al Casino The CoDenants, un lugar en el cual podras entrar de manera limpia al mundo de la ludopatia(fake)")

    dinero = float(input("Ingresa la cantidad de dinero con la cual quieres jugar: "))
    if dinero <= 0:
        print("La cantidad apostada debe ser mayor a 0.")
        return

    juegos = input("Selecciona el juego que deseas jugar: 'ruleta' (r) o 'tragamonedas' (t): ")

    while True:
        if juegos == "r":
          # aqui se realiza una impresion de la ruleta condicionado de que el numero que caiga sera reemplazado por el simbolo de x (unicode)
            def imprimir_ruleta(cambiar_numero=None):
                numeros_ruleta = [
                    ["#", 3, 6, 9, 12, 15, 18, 21, 24, 27, 30, 33, 36],
                    [0, 2, 5, 8, 11, 14, 17, 20, 23, 26, 29, 32, 35],
                    ["#", 1, 4, 7, 10, 13, 16, 19, 22, 25, 28, 31, 34]
                ]
                for i in range(len(numeros_ruleta)):
                    for j in range(len(numeros_ruleta[i])):
                        if numeros_ruleta[i][j] == cambiar_numero:
                            numeros_ruleta[i][j] = "❌"

                for fila in numeros_ruleta:
                    print(" ".join(map(str, fila)))
            # Apuestas de color
            color_apuesta = input("Escoge un color entre rojo, negro, verde o ninguno (n): ")
            while color_apuesta not in ["rojo", "negro", "verde", "n"]:
                print("Ese color no está en la ruleta. Intenta de nuevo.")
                color_apuesta = input("Escoge un color entre rojo, negro, verde o ninguno (n): ")

            # Apuestas de par o impar
            numero_par = input("Selecciona si tu número será 'par', 'impar' o 'ninguno'(n): ")
            while numero_par not in ["par", "impar", "n"]:
                print("Opción inválida. Intenta de nuevo.")
                numero_par = input("Selecciona 'par', 'impar' o 'ninguno': ")

            # Apuestas de numeros especificos
            numero_elegido = input("Escoge un número entre 0 y 36 o escribe 'ninguno': ")
            if numero_elegido != "n":
                while True:
                    try:
                        numero_elegido = int(numero_elegido)
                        if 0 <= numero_elegido <= 36:
                            break
                        else:
                            print("Número fuera de rango. Intenta de nuevo.")
                            numero_elegido = input("Escoge un número entre 0 y 36 o escribe 'ninguno': ")
                    except ValueError:
                        print("Entrada inválida. Intenta de nuevo.")
                        numero_elegido = input("Escoge un número entre 0 y 36 o escribe 'ninguno': ")

            # Giro de la ruleta
            print("Girando la ruleta...")
            for _ in range(10):
                print("Números girando: " + str(random.randint(0, 36)), end="\r")
                time.sleep(0.3)

            numero_ruleta = random.randint(0, 36)
            imprimir_ruleta(numero_ruleta)
            if numero_ruleta == 0:
              color_ruleta = "verde"
            elif numero_ruleta in [2, 4, 6, 8, 10, 11, 13, 15, 17, 20, 22, 24, 26, 28, 29, 31, 33, 35]:
              color_ruleta = "negro"
            else: "rojo"

            print("La ruleta cayó en el número " + str(numero_ruleta) + " " + str(color_ruleta))

            # Cálculo de ganancias
            ganancia = 0
            condiciones_totales = 0
            condiciones_acertadas = 0

            #calculos de condiciones
            if color_apuesta != "n":
                condiciones_totales += 1
                if color_apuesta == color_ruleta:
                    ganancia += dinero * 2
                    condiciones_acertadas += 1
                    print("¡Acertaste el color " + str(color_apuesta) + "!")

            if numero_par != "n":
                condiciones_totales += 1
                if numero_par == "par" and numero_ruleta % 2 == 0 and numero_ruleta != 0:
                    ganancia += dinero * 1.5
                    condiciones_acertadas += 1
                    print("¡Acertaste que el número es par! ")
                elif numero_par == "impar" and numero_ruleta % 2 != 0:
                    ganancia += dinero * 1.5
                    condiciones_acertadas += 1
                    print("¡Acertaste que el número es impar! ")

            if numero_elegido != "n":
                condiciones_totales += 1
                if numero_ruleta == numero_elegido:
                    ganancia += dinero * 5
                    condiciones_acertadas += 1
                    print("¡Adivinaste el número exacto " + str(numero_elegido) + "!")
                elif numero_elegido == 0 and numero_ruleta == numero_elegido:
                    ganancia += dinero * 50
                    condiciones_acertadas += 1
                    print("¡Soldado acertó que el numero era exactamente 0, ganaste el premio mayor.... un duro usted!")
            #calculos de ganancias de dineros
            print("Dinero ingresado: $" + str(dinero))
            print("Ganancia total: $" + str(ganancia))

        elif juegos == "t":
            def tragamonedas(dinero):
                print("🎰 Juego Tragamonedas 🎰")
                print("Jugando...")
                time.sleep(2)
                # simbolos a imprimir (son del sistema unicode)
                simbolos = ["🍒", "🍋", "🔔", "⭐", "7️⃣", "❌", "👨‍✈️", "👽", "☘️", "🌌", "☣️", "🧬", "☠️", "🛸"]

                matriz = []
                for _ in range(3):
                    fila = []
                    for _ in range(3):
                        fila.append(random.choice(simbolos))
                    matriz.append(fila)

                for fila in matriz:
                    print(" | ".join(fila))

                time.sleep(1)
                resultado = matriz[1]  # Tomamos la fila del medio como la que define si gano o no
                print("Resultado: " + ' | '.join(resultado))

                # Lineas de ganancia de tragamonedas
                if len(set(resultado)) == 1:
                    print("¡Felicidades! Obtuvo tres iguales. Gano 10 veces tu apuesta.")
                    return dinero * 10
                elif len(set(resultado)) == 2:
                    print("¡Casi! Dos iguales. Gano el doble de tu apuesta.")
                    return dinero * 2
                else:
                    print("Lo siento, no gano en vertical.")
                    return 0

                # comprobacion de que la columna del medio tiene iguales
                columna_medio = []
                for i in range(3):
                    columna_medio.append(matriz[i][1])
                if len(set(columna_medio)) == 1:
                    print("¡Felicidades! Obtuviste tres iguales en la columna del medio. Ganaste 1.5 veces tu apuesta.")
                    ganancia += dinero * 1.5 # ganancia dada en caso de que si sean iguales
            #lineas de impresion de ganancia correspondiente
            ganancia = tragamonedas(dinero)
            print("Ganancia total: $" +str(ganancia)) # ganancia total
        #lineas que permiten al jugador continuar jugando o salirse del programa
        jugar_nuevamente = input("¿Quieres jugar otra vez? (sí/no): ")
        if jugar_nuevamente != "si":
            print("Gracias por jugar en el Casino The CoDenants. ¡Hasta la próxima!")
            break

if __name__ == "__main__":
    casino()
```
Una vez dadas las condiciones, se ejecuta el programa.

### ¿Qué problemas hubieron y cómo los solucionamos?
En el desarrollo del codigo hubieron bastantes inconvenientes a la hora de su realizacion, uno de ellos, para nosotros el mas importante era hacer que si el jugador fallaba alguna de las condiciones que escogio apostar, perdiera todo su dinero, ya que siempre que fallaba una de sus condiciones ganaba igualmente dinero, cosa que si bien es justa, en terminos de caino implica perdidas, y quien dijo que un casino era justo. Por lo que decidimos establecer que cada condicion que seleccionara seria 1 condicion agregada a sus condiciones totales, y si acertaba una, estas significarian 1 unidad a sus condiciones ganadas estableciendo asi que si o si el numero de condiciones totales debia ser igual a el numero de condiciones acertadas.

Otro problema que tuvimos, fue el hecho de que si el jugador ingresaba un numero que no perteneciera al rango (0, 36) nos daba error, cosa que si bien no es critica, corta la experiencia, por lo que teniamos que buscar una solucion al problema (fue un poco dificil porque no sabiamos que funcionaba), para llegar a la solucion con ayuda de un compañero, nos dijo que investigaramos un poco sobre las excepciones, por lo que despues de un ratito viendo un video logramos dar la solucion a dicho "problema".

## 6. Conclusion.
Este proyecto nos permitió aplicar y reforzar los conociomientos adquiridos durante el curso. Logramos demostrar de forma práctica la relación que pueden tener las herramientas que hay en el ambito de la programación en situaciones cotidianas como lo pueden ser los juegos, ya sean o no de azar, seguramente se puedan desarrollar diversos casos sobre el contexto del mundo real con las herramientas que utilizamos, el trabajo en equipo fue determinante para ello, como grupo, quedamos satisfechos con el desarrollo de este proyecto.

# Como dijo el doctor, Parto con dolor, o apliquemos la de la pelicula de interestelar, la unica manera de que los humanos descubran como llegar a alguna parte, es dejando algo atras...........
