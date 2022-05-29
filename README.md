
# Mecatronica I Fuente 18V 3A en base regulador de tensión LM723
Placa para realizar la fuente de Mecatrónica I regulable en tensión (1,2V a 18V) con limitador de corriente (0.1A a 3A).
Tambien está diseñada para poder conectarla con un voltimetro/amperimetro disponible en el mercado para ser colocada en el propio gabinete.

# Vistas
<img src="https://github.com/SNolasco86/KICad_PowerSource_LM723/blob/main/shapes3D/Kicad_Projects.png" width="425" height="295">
<img src="https://github.com/SNolasco86/KICad_PowerSource_LM723/blob/main/shapes3D/Kicad_Projects_Top.png" width="425" height="295">
<img src="https://github.com/SNolasco86/KICad_PowerSource_LM723/blob/main/shapes3D/Kicad_Projects_Top_without.png" width="425" height="295">
<img src="https://github.com/SNolasco86/KICad_PowerSource_LM723/blob/main/shapes3D/Kicad_Projects_Top_bottom.png" width="425" height="295">
# Recursos
La placa permite generar señales eléctricas como así también recibir señales desde circuitos externos. El esqumático puede verse en este [PDF](https://github.com/SNolasco86/KICad_PowerSource_LM723/tree/main/sch/Board.pdf).


# Consideraciones de la Placa
## Gerbers
Los archivos Gerbers que están en este directorio [[link](https://github.com/SNolasco86/KICad_PowerSource_LM723/release/)] contienen todo lo necesario para realizar la fabricación de la placa en forma industrial. Es decir, pueden ser proporcionados a cualquier fabricante de placas. En las mismas extenciones de dichos archivos se encuentran información de las capas con las que fue diseñada esta placa. Para conocer e interpretar el formato de cada extensión puede revisarse la siguiente publicación [link](https://www.proto-electronics.com/es/blog/archivos-gerber-para-qe-sirven).

## PDFs
Se exportan las diferentes capas de la placa en formato PDF de forma tal que pueda ser diseñado en forma manual. Existen diferentes métodos "caseros" con los que se puede llevar adelante la fabricación de una placa siempre y cuando el diseño lo permita. Esto quiere decir que no cualquier diseño PCB puede ser fabricado en forma manual. Esto se deben a las siguientes condiciones:
 - **Paso mínimo:** Es la mínima resolución que se considera en todo el diseño. Esto se tiene en cuenta tanto en la resolución de una pista como el margen de los pads. En el caso de intentar realizar la placa con los métodos de planchado o luz ultravioleta, aquellas placas con pasos mínimos muy pequeños son dificil de lograr.
 - **Pistas de cobre:** Los proceso de fabricación logran obtener las pistas de cobre con diferentes resoluciones según el requerimiento del cliente. En caso de querer realizar las pistas sobre una placa simple faz se debe utilizar diferentes métodos. A continuación se listan los dos métodos más comunes:
    - **Método con plancha:** Este método consiste en imprimir la capa, donde se tienen las pistas de cobre, en una hoja satinada (revistas o papel fotográfico) con una impresora laser y luego se transfiere esta impresión al pedazo de placa. En el siguiente enlace se muestra el proceso [link](https://www.neoteo.com/circuitos-impresos-el-metodo-de-la-plancha/). 
    - **Método con luz UV:** En este método se requieren más elementos complejos que el primero. Se utiliza una una hoja plástica transparente  para realizar la impresión, una pintura especial que será depositada en la placa como así también es importante tener una cámara con luz UV. Una muestra de este proceso puede verse en el siguiente enlace [link](http://uedesign.com.ar/PDFs/M%C3%A9todo_UV.pdf).

    Como se dijo anteriormente, son procesos compejos de lograr y se requiere de varios intentos. Una vez obtenida la placa con las pistas pintadas, el proceso de reacción química para remover las áreas de cobre es **peligroso** y debe tomarse todas las medidas se seguridad pertinentes. Aquí algunas referencias sobre seguridad [link](https://aulavirtual.fio.unam.edu.ar/pluginfile.php/61611/mod_resource/content/1/Seguridad%20en%20los%20laboratorios%20qu%C3%ADmicos.pdf).

 - **Máscaras anti-soldantes:** Todas las placas fabricadas industrialmente tienen, en sus capas con pistas de cobre, una máscara con una pintura anti-soldante. Esto evita que el estaño en el proceso de soldadura no se propague por todas las pistas y únicamente queden depositados en los pads. Esta casa es casi imposible de realizar en forma manual, existen técnicas pero son muy costosas y poco recomendables.
 - **Perforaciones:** Los fabricantes de placas tienen herramientas que permiten una exactitud en las perforaciones, además de complir con las secciones requeridas. En caso de realizarla manualmente este proceso podría contener errores propios de la manipulación manual y falto de precisión.

## Capas
La placa está diseñada para ser fabricada a simple faz. En los archivos [PDF](https://github.com/SNolasco86/KICad_PowerSource_LM723/tree/main/pcb/) de fabricación se pueden identificar dos capas:
 - **Capa Superior [[minilab-F.Cu.pdf](https://github.com/SNolasco86/KICad_PowerSource_LM723/blob/main/pcb/Top.pdf)]:** En esta capa se colocarán los componentes electrónicos y en caso de fabricar manualmente la placa, se deberá insertar los cables-puentes de la placa. Estos "puentes" emulan las coneciones de la capa inferior. 
 - **Capa inferior[[minilab-B.Cu.pdf](https://github.com/SNolasco86/KICad_PowerSource_LM723/blob/main/pcb/Bottom.pdf)]:** Es la capa dónde se trandrán las pistas de cobre y se realizarán las soldaduras.
 
 
