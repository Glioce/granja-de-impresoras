# granja-de-impresoras

## Objetivos
+ Hacer que la granja esté trabajando todo el tiempo
+ Registrar varios datos: tiempo de impresión, colores utilizados, tamaño de piezas
+ Con los datos registrados, calcular ganancias y tomar decisiones como compra de filamento
+ Automatizar la cola de impresión
+ Mostrar a los clientes en tiempo real el estado de la impresión y avisar cuando la impresión está lista

En la primera instalación (iniciada en diciembre de 2019) se busca que la granja esté formada por:
+ 4 impresoras Creality Ender 3
+ 1 impresora MakerBot Replicator 2
+ 1 impresora MakerBot Replicator 2X
+ 3 Raspberry Pi 3 B+ (cada Raspberry controla 2 impresoras y 2 webcam)
+ 4 webcam

Actualización en enero de 2020:
+ 6 impresoras Creality Ender 3
+ 1 impresora MakerBot Replicator 2
+ 1 impresora MakerBot Replicator 2X
+ 5 Raspberry Pi 3 B+ (cada Raspberry controla 2 impresoras y 2 webcam)
+ 6 webcam
+ 1 Router CNC Stepcraft 840
+ 1 Cortadora láser

## Tutoriales
Cómo configurar varias instancias de OctoPrint en una sola RPi  
Tuto principal  
http://thomas-messmer.com/index.php/14-free-knowledge/howtos/79-setting-up-octoprint-for-multiple-printers  
Otros tutoriales  
http://headrevision.com/2019/02/15/how-to-multiple-3d-printers-using-octoprint-2019-raspberry-pi-and-ender-3/  
https://floatingcam.com/blog/multiple-printers-and-octoprint/

Cómo poner un botón de apagado  
https://www.quartoknows.com/page/raspberry-pi-shutdown-button

## Instancias de Impresoras
+ 192.168.1.7/ender1/
+ 192.168.1.7/ender2/
+ 192.168.1.65/ender3/
+ 192.168.1.65/ender4/

## Usuario y Contraseña
User: inventoteca
Password: Inventoprint

## Datos de OctoPrint
OctoPrint version 1.3.12  
OctoPi version 0.17.0  

## Datos de las impresoras
### Creality Ender 3
Volumen de impresión: 250 x 250 x 250 mm ??  
Temperatura de extrusor PLA: 220 ℃  
Temperatura de plataforma PLA: 30 ℃ piezas pequeñas  
Velocidad  
Altura mínima de capas  
Altura máxima de capas  

### MakerBot Replicator 2
Volumen de impresión: 270 x 250 x 250 mm ??  
Temperatura de extrusor PLA: 220 ℃  
Temperatura de plataforma PLA: 30 ℃ piezas pequeñas  
Velocidad  
Altura mínima de capas  
Altura máxima de capas  

### MakerBot Replicator 2X
Volumen de impresión: 250 x 250 x 250 mm ??  
Temperatura de extrusor PLA: 220 ℃  
Temperatura de plataforma PLA: 30 ℃ piezas pequeñas  
Velocidad  
Altura mínima de capas  
Altura máxima de capas  
