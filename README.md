# XP-Points
Creador de formas basado en puntos guardado en archivos INI // Point-Based Shape Creator saved in INI Files


### Que es?

XP-Points son 2 programas juntos, el primero, Editor, es el encargado de dejarte crear formas utilizando puntos, como se ve en el video de abajo los puntos se ponen en
la cuadricula, uniendose mostrando como quedaria la figura que estas creando.

El segundo programa, Preview, te deja abrir y mostrar las formas que estan dentro de los archivos .ini.

Video que muestra como funcionan los 2 programas

https://user-images.githubusercontent.com/90771298/226188685-991b8522-a136-4158-83d5-edb8dbd8de8c.mp4

### Como funciona?

# Editor
Cuando das clic en alguna parte dentro de la cuadricula se crea un punto, este es el Punto-1, luego si das otro clic en otra parte, se crea otro punto, el Punto-2, cada punto es un objeto diferente, el Punto-2 crea una linea desde sus propias X e Y a las X e Y del Punto-1, el Punto-3 se conecta al Punto 2 y sigue asi, el maximo numero de puntos es 20.

El cuadro de texto es el nombre de como el archivo si iba a guardar, cuando se presiona el boton "Guardar", cada punto que este en la cuadricula abre o crea el archivo ini con el nombre que este en el cuadro de texto, agarra las coordenadas del primer punto y las guarda algo asi:
`[Line-1]
X1=9
y1=8`

luego hace lo mismo para el segundo punto, pero lo guarda en `[Line-1]` pero en lugar de guardarlo en X1 e Y1, se guardaria en X2 e Y2
`[Line-1]
X1=9
y1=8
X2=12
y2=5`

para el tercer punto, se hace lo mismo, pero se cambia `[Line-1]` a `[Line-2]`, y sigue asi hasta que todos los puntos se hayan guardado.

Para guardar la escala, el color rojo, verde y azul se hace lo mismo, pero se guarda de esta forma:
`
[Propiedades]
Red= Color Rojo
Green= Color Verde
Blue= Color azul
Escala= Aqui la escala
`

# Preview
En el campo de texto se pone el nombre del archivo para ver
# El archivo tiene que estar en la misma carpeta!
El boton "Dibujar" abre el archivo ini, cargando los datos ("Coordenadas,color, escala, etc") a un objeto llamado "obj_test" que es el encargado de dibujar la imagen.

Para dibujar la forma, crea un trianglefan usando los puntos del archivo INI, y se usa la variable que contiene los datos de los colores R,G,B para colorear la imagen.

El objeto "obj_test" tiene una variable, "imagefill", si es verdadera, la imagen se muestra con los bordes y el color, pero si no solo se muestran los bordes.
