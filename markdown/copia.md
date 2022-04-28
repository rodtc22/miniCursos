Las buenas practicas dicen que

# Como hacer titulos? (Heading de nivel 1)

los headings tienen que estar entre espacios en blanco

###### Heading de nivel 6
Heading de nivel 1
==================
Heading de nivel 2
------------------

## Como hacer Parrafos?
Este es un parrafo, aqui pueden venir varias lineas.
Y un solo salto de linea como este, es solo como poner un `<br>` en html

## Break Lines (Saltos de linea para separar parrafos)

Este es un parrafo comun

Pero si pongo dos saltos de linea como este, entonces es como si este parrafo, estuviera en otro `<p>`, PARA BUENAS PRACTICAS EVITAR PONER TABULACIONES O ESPACIOS EXTRA, YA QUE ESO SE HACE DE OTRA FORMA

## Emphasis a textos (Negrita,Cursiva,Italic)

**NEGRITA**
Esta en **texto en Negrita**.
Esta**en**negrita.

*ITALIC*
Esta en *italic*
esto*se encuentra*en italic

***NEGRITA-ITALIC***
esto es un texto ***extremadamente importante***

~~TACHADO~~
esto es un ~~texto~~ equivocado


## Blockquotes (Bloques)

> Esto es una forma de hacer bloques

### Blockquotes (Bloques con multiples parrafos)

> Esto seria el primer 
> Esto seria el segundo parrafo, pero vamos a notar que podemos seguir mezaclando **bold** e *italic* aqui ***adentro***

### Blockquotes (Bloques con otros elementos).

> ## Titulo del bloque
> * ~~lista1~~
> * **lista2**
> *Me puede ayudar a hacer listas o algo asi*
> ***Las buenas practicas me dicen que estos bloques tienen que tener un salto de linea al inicio y al final***

## Listas

#### Listas enumeradas

*Para que no se mezclen, debemos poner un salto de linea, **antes y despues** de la lista*

1. First
2. Second
3. Tercero
4. Holi


1. siempre
1. salen
1. enumerados


1. obj1
2. obj2
    1. obj2.1
    2. obj2.2
        1. obj2.1.1
        2. obj2.1.1
    3. obj2.3
3. obj3


1. a
2. b
    2.1. ba
    2.2. bb
        2.2.1. Esto ya no funcion
    2.3. bc
3. d


1. hola
2. como
    - estas
    - hoy
3. bienvenido :D


#### Lista no Enumeradas

- a
- b
- c
 

- a
- b
    - ba
    - bb
        - bba
        - bbb
            Tambien podemos poner texto, si respetamos la indentacion
        - bbc
            - bbca
            
                > O poner otros mas, pero respetando la indenacion
                > holi :D

        - bbd
    - bc
    - bd
- c

## Imagenes

- Primera forma:
    ![Es el logo de la IPCP :D, aunque este texto no se vera](https://acm.iteso.mx/share/ICPC_masters_mexico_2022.jpg)
- Segunda forma:
    ![otro textito][loguitoicpc]

- Tercera forma
    ![fotoLocal](/../..direccion)

[loguitoicpc]:https://acm.iteso.mx/share/ICPC_masters_mexico_2022.jpg

## Como poner codigo?

Ponemos la etiqueta `body` o `<p>` de html
La instruccion `for i in range(10)` de python
El mensaje `cout<<"hola mundo"<<endl;` de c++

`` si nuestro codigo incluye `backsticks` se pone doble backsticks``


#### Como poner bloques de codigos?

```
    #Esta mas o menos
    for i in range(10):
        print('hola mundo')
```

```python
    #Esto es mejor
    for i in range(10):
        print('hola mundo')
```

```c++
    for(int i= 0 ;i < n; i++){
        cout<<primo[i]<<endl;
    }
```
```html
    <body>
        <h1> hola a todos </h1>
    </body>
```

---

## Lineas Separadoras

Se ponen cuando quieres separar una idea de otra

---

## Links

Los links se ponen asi [link para  Atcoder](https://atcoder.jp/home)

---

# URLs y Emails

Para mostrar directamente una urls o email
<https://atcoder.jp/home>
<rodritc99@gmail.com>

---

# Formato a los links

[Codeforces](https://codeforces.com/) es un buen juez
Tambien podemos ponerle estilo a la letra de ***[codeforces](https://codeforces.com/)***

## Mejor forma de poner links

Este es el link a [Codeforces][linkcodeforces]
[nombreAmostrar][linkPagina]

[linkcodeforces]:https://codeforces.com
[linkPagina]:url

---

## Checkbox

[x] opcion1
[ ] opcion2
- [x] mejor opcion1 
- [ ] mejor opcion2


---

## Notas de pie

Tengo un texto y hago aclaracion en aqui[^1].

Tengo otro parrfo y puedo hacer otra aclaracion aqui[^2].

Incluso puedo ponerles con otros nombre, pero igual sale enumerado[^otronombre].

Al final, ponemos esos pie de notas:
[^1]: aclaracion 1
[^2]: aclaracion 2
[^otronombre]: sadf















