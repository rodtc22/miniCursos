Las buenas practicas dicen que

# Como hacer titulos? (Heading de nivel 1)

los headings tienen que estar entre espacios en blanco

###### Heading de nivel 6

Otro Heading de nivel 1
=======================

Otro Heading de nivel 2
-----------------------


## Como hacer Parrafos?

Aqui pueden venir varias lineas, Y un solo salto de linea como este
es como poner un `<br>` de html.

## Break Lines (Separar Parrafos)

Parrafo1

Este es otro parrafo, las buenas practicas de programacion, me dicen que no tengo que poner tabulaciones o cosas asi.

## Estilos de Texto

**NEGRITA**
*ITALIC*
***NEGRITA ITALIC***
~~TACHADO~~

## Citas

> Esto es una forma de hacer una cita

### Citas multiples parrafos

> esto seria el contenido del parrafo1...
> esto seria el contenido del parrafo2...

### Citas con mas elementos

> **ESTO ES EL TITULO**
> * ~~me equivoque en esto, por eso lo tacho~~
> * *el segundo item de la lista en la cita*
> pueden venir mas parrafos 
> `<br>` y codigo creo, espero que si :D

## Listas

####Listas enumeradas

*para que no se mezclen, tenemos que poner un **salto de linea, antes y despues** de cada lista*

1. hola
2. como
3. estas
4. tu


1. siempre
1. se
1. enumera solito


1. obj1
2. obj2
	1. obj2.1
	2. obj2.2
		1. obj2.2.1
		2. obj2.2.2
	3. obj2.3
3. obj3


1. hola
2. como
	- estas
	- hoy
3. bienvenido :D


##### Lista no Enumerada

- a
- b
- c


- a
- b
	- ba
		- bba
		- bbb
			Tambien podemos poner texto, si respetamos la indentacion
		- bbc
			- bbca
				> incluso poner citas
				> pero si respetamos la indentacion 
		- bbd
	- bb
	- bc
	- bd
- c

- Primera forma:
    ![Es el logo de la IPCP :D, aunque este texto no se vera](https://acm.
iteso.mx/share/ICPC_masters_mexico_2022.jpg)
- Segunda forma:
    ![otro textito][loguitoicpc]

- Tercera forma
    ![fotoLocal](/../..direccion)

[loguitoicpc]:https://acm.iteso.mx/share/ICPC_masters_mexico_2022.jpg


## Como poner codigo?

Ponemos la etiqueta `body` o `<p>` de html
La instrucciono `for i in range(10)` de python
El mensaje `cout<<"hola mundo"<<endl;` de c++

`` si muestro codigo que incluye `backsticks` se pone con doble backsticks``

#### Como poner bloques de codigos?

```
	#Esta mas o menos
	for i in range(10):
		print('Hola mundo')
```

```python
	#Esta mas o menos
	for i in range(10):
		print('Hola mundo')
```

```c++
	//esto es un comentario
	for(int i= 0 ;i < n;i++){
		cout<<primo[i]<<endl;
	}
```


```html
	<body>
		<h1> Hola a todos </h1>
	</body>
```

## Lineas separadoras

Se ponen cuando quieres separar una idea de otra

---

## Links

Los links se ponen asi [link para Atcoder](https://atcoder.jp/home)

---

# URLs y Emails

Para mostrar directamente una ruls o email
<https://atcoder.jp/home>
<rodritc99@gmail.com>

---

# Formato a los links

[Codeforces](https://codeforces.com/) esun buen juez

Tambien podemos ponerle estilo a la letra de ***[codeforces]***(https://codeforces.com/)

## Mejor forma de poner links

[nombreAmostrar][linkPage]
Este es el link a [Codeforces][linkcodeforces]

[linkPage]:url
[linkcodeforces]:https://codeforces.com

---

## Checkbox

[x] opcion1
[ ] opcion2

- [x] mejor opcion1
- [ ] mejor opcion2

---

## Pie de notas

Tengo un texto y hago aclaracion en aqui[^1]

Tengo otro parrafo y puedo hacer otra aclaracion aqui[^2]

Incluso puedo ponerles otro nombre, pero igual sale enumerado[^otro_nombre].

Al final , ponemos los pie de notas:
[^1]: aclaracion 1
[^2]: aclaracion 2
[^otronombre]: cualquier otra cosa


