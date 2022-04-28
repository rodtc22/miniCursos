# GIT

>WINDOWS: USAR INSTALADOR Y AGREGAR GIT A LAS VARIABLES DE ENTORNO

>LINUX: sudo apt install git

Sirve para sacar versiones de un proyecto,es decir,
acabo de escribir X lineas de codigo con el nombre version1, sigo programando...
y luego puedo guardandolo como version2, y asi...

1. \
	1.1. \
		1.1.1. \
		1.1.2. \
		1.1.3. \
	1.2. \
	1.3. 

Estas se llaman "ramas/branch" donde puedo "retroceder en el tiempo" en caso de que lo haya arruinado en 1.1.3 y puedo volver a 1.1.2
lo bueno es que no guarda un solo archivo, si no que TODO el proyecto(pudiendo contener cientos de archivos)

> Forma de trabajo: Primero estan en el staging area y luego se los pasa al repositorio como commit

# COMANDOS
**Creamos el _Staging Area_** (estando adentro de la carpeta)
``` sh
git init
```

**Ver estado del _Staging Area_**
``` sh
git status -s
```

**Agregar archivos al _Staging area_**
	
``` sh
git add index.html
git add .		//o para agregar todo
```

**Tratando de agregar archivos al Repositorio por primera vez**
``` sh
git commit -m "Comienzo del proyecto"
git config --global user.email "rodrigoticonacoronel.22@gmail.com"
git config --global user.name "rodtc22"
```

**Reiniciamos la consola y ahora si recien podemos agregar archivos al Repositorio Local como nuevo commit**
``` sh
git commit -m "Comienzo"
```

**El comando commit mas usado**
``` sh
git commit -am "parrafo y tamanio de fuente"
```

**Agregar un nuevo commit(con nuevos cambios), poniendole un nombre que lo identifique**
``` sh
git add (ARCHIVO O .)
git status -s					//podemos verificar que ya no estn en el staging area
git commit -m "Agregado de Parrafo Lorem."
```

**Lista los commits**
``` sh
git log --oneline
```
	
**Lista de commits detallados**
``` sh
git log --source
```

**Volver a un commit**
``` sh
git log --source						//para ver el commit exacto
git reset --hard -q f1695e95481eefa0e244d780fbb68f47a98416be
git log --source						//para ver que si volvio
```


_PARA PONER MI PROYECTO EN GITHUB_
> 0. ir al perfil, clickear repositorios y clickear nuevo 
> 1. poner un nombre al repositorio y mejor si clickeamos Add a README file y clickear Crear repositorio
> 2. clickear el boton verde CODE y copiar el url
> 3. Para subir la primera vez a un repositorio, ponemos estos 2 pasos extra

``` sh
git remote add origin url
git branch -m main
```
> 4. Para subir al repositorio
``` sh
git push -u origin main
```
> 4.es posible que pida mi usuario y contrasenia del github para sincronizar git + github, pero solo eso
