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
+ 192.168.1.47/replicator-2/
+ 192.168.1.47/replicator-2x/

## Usuario y Contraseña
User: inventoteca
Password: Inventoprint

## Datos de OctoPrint
OctoPrint version 1.3.12  
OctoPi version 0.17.0  

## Datos de las impresoras
### Creality Ender 3
Volumen de impresión: 220 x 220 x 250 mm  
Temperatura de extrusor PLA: 220 ℃  
Temperatura de plataforma PLA: 50 ℃ piezas pequeñas  
Velocidad  
Altura mínima de capas  
Altura máxima de capas  

### MakerBot Replicator 2
Volumen de impresión: 260 x 150 x 150 mm ??  
Temperatura de extrusor PLA: 220 ℃  
Temperatura de plataforma PLA: 30 ℃ piezas pequeñas  
Velocidad  
Altura mínima de capas  
Altura máxima de capas  

### MakerBot Replicator 2X
Volumen de impresión: 225 x 145 x 150 mm ??  
Temperatura de extrusor PLA: 220 ℃  
Temperatura de plataforma PLA: 30 ℃ piezas pequeñas  
Velocidad  
Altura mínima de capas  
Altura máxima de capas  

### Cambios en código G para Makerbots en Ultimaker Cura
; — start of START GCODE – 
M73 P0 (enable build progress) 
;this next line won’t work, but has the steps command 
M92 X88.8 Y88.8 Z400 E101 ; sets steps per mm for Rep2 
G90 (set positioning to absolute) 
(**** begin homing ****) 
G162 X Y F4000 (home XY axes maximum) 
G161 Z F3500 (home Z axis minimum) 
G92 Z-5 (set Z to -5) 
G1 Z0.0 (move Z to “0”) 
G161 Z F100 (home Z axis minimum) 
M132 X Y Z A B (Recall stored home offsets for XYZAB axis) 
(**** end homing ****) 
G92 X147 Y66 Z5 
G1 X105 Y-60 Z10 F4000.0 (move to waiting position) 
G130 X0 Y0 A0 B0 (Set Stepper motor Vref to lower value while heating) 
G130 X127 Y127 A127 B127 (Set Stepper motor Vref to defaults) 
G0 X105 Y-60 (Position Nozzle) 
G0 Z0.6 (Position Height) 
; — end of START GCODE – 



; — start of END GCODE – 
G92 Z0 
G1 Z140 F900 
M18 
M104 S0 T0 
M73 P100 (end build progress) 
G162 X Y F3000 
M18 
; — end of END GCODE –
