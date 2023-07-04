# ACE1-23VJ0778201901973PROY2
- - - -
# Proyecto 2
- - - -
# Manual Tecnico

- - - - 

## Variables Utilizadas

Las siguientes varibles son los sprite para cada personaje visible a la hora de imprimir en el modo de video

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/fb6696e0-12f7-41a9-9c47-c08608902ffa)

Se inicializo desde el principio las siguientes cadenas que seran llamadas luego por los diferentes metodos para imprimir en pantalla:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/89bbca3a-d7ce-4eea-b3e4-ada2559ec6dc)

Los mesnajes que salen en el menu de configuracion:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/739fe253-ecc9-45d4-b59b-799556e36670)

Se coloco un buffer para colocar la direccion para cargar nivel:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/90bb2820-a458-4d55-baf6-cd5f39b76af3)

Por defecto, al inicar el programa tiene como configuracion que por scan code esta registrado los controles de las flachas, estas podran ser cambiadas desde el menu de configuracion:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/874e506f-cf84-417f-9302-68a8f45e091c)

Estas son las rutas cargadas para mostrar los niveles por defecto, estas seran utilizadas para ser cargadas una tras otra para seguir la linea del juego:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/285df93a-c012-4575-b090-97b57e1606b4)

- - - - 
## Funciones

Al iniciar el programa, el inicio se configuro para que sea puesta la pantalla como en modo de video, con las siguientes interrupciones:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/d3047a0e-c3f0-44ea-85d3-1e8c91ecc2a2)

Esta es la estructura que se utlizara para desplegar cada uno de los menu que se tienen en el programa, poniendo donde queremos que empice la flecha que se utlizada para controlar el flujo del programa, se imprimira en un x y y, se configura para que cada etiqueta que le sigue a la primera, solo vaya aumentando, asi no poniendo direcciones como tales, solo siguiendo una misma linea con la misma x para todas las opciones, donde el offset imprime cada una de las cadenas que se inicializaron al principio:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/6c930d52-579d-496b-82df-685e855c2b3c)

Se llama a Desplegar Menu Principal, donde este llama al anterior menu, para que este leyendo las opciones por flecha que se estan teniendo, haciendo tambien la compraracion de que es lo que esta seleccionando para entrara a esa funcion por medio de un AL sera comprado, eso mismo se utlizara para desplegar los distintos menus que se tienen:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/ed10e823-7092-4b57-af92-9cf6d744cd46)

Al iniciar a jugar, se llama a la instruccion de Iniciar_nivel, donde se hace un movimiento donde vamos a darle valor al nivel actual para llevar una secuencia a favor, se resetea cod_name que es la variable que nos ayuda a saber que archivo debe de ir cargando a la pantalla, donde se va reescribiendo lo que queremos para que lo vaya mostrando, de igual forma de hace asi para cada nivel:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/8039edb1-1ce4-40a9-a6f2-ee97180e88c9)

El siguiente como tal es quien hace correr el juego, donde primero llama a pintar_mapa que es el que pinta los sprite de jugador, pared, objetivo, y las cajas. para luego ir a entrada_juego que luego de cargar se manda por AH el scan code de las varibles que se inicialiaron para movernos con las flechas:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/40c52c0f-4de9-4f5f-a309-934ad3e0b241)

Siguiendo con el flujo se llamo a pintar mapa, que tiene varios ciclos, con los que va ir pintando las diferentes figuras que se le van mostrando cuando lee el archivo:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/2a55c922-c661-4612-966f-ff5ae0db9195)

Entrada_juego es el manejo de las entradas del juego, donde se configura que se puede mover para cualqueir lado el jugador, haciendo tambien la iterrupcion de leer el f2 donde es la pausa del juego:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/4e8e077b-fa27-4f79-a5de-57dce892e770)

Mover jugador es un procedimiento con el cual diremos donde esta el jugador, compararemos si hay pared, caja y objetivo, donde validaremos donde se puede mover y donde no, se utlizada color en mapa para conocer donde es que se encuentras las diferentes figuras, y las instrucciones respectivas si hay que sumar o restar para hacer el movimiento del personaje, haciendo memoria que al subir se resta y al bajar se suma, de igual forma para ir a izquierda se resta y a la derecha se suma:

![image](https://github.com/rauudy/ACE1-23VJ0778201901973PROY2/assets/66295181/c11ffc3b-3ef6-4ee7-8895-62248ea860b2)













