1. Entramos a la consola y tecleamos vim

2. Para salir de vim teclamos :q

3. Para modificar un texto, escribo i(insertar)

4. Para movernos sin usar las teclas
 4.1. h = izquierda
 4.2. j = abajo
 4.3. k = arriba
 4.4. l = derecha

5. Para salir del modo Insertar(escribir) presiono Esc

6. Si quiero guardar lo que hice presiono :wq

----------------------------------------------------------
1. Abrir un archivo desde vim
	:edit ...ruta/archivo

2. Comandos Utiles:
	w: vamos saltando de palabra en palabra por la primera letra
	e: vamos saltando de palabra en palabra por la ultima letra
	b: al principio de la palabra actual

	10j: bajamos 10 lineas
	8k: subimos 10 lineas
	6w: siguiente 6ta palabra
	
	fy: buscar la siguiente 'y' en mi fila actual
	fm: buscar la siguiente 'm' en mi fila actual
	
	0: ir al inicio de la linea
	$: ir al final de la linea

	**estoy en una palabra y oprimo**
	*: buscar la siguiente misma palabra
	%: buscar el cierre del parentesis en el que estoy	

	gg: ir al inicio del documento
	G: ir al final del documento
	15G: a la linea 15
