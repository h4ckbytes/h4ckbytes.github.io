---
date: 2022-09-07 12:26:40
layout: post
title: Comandos básicos de linux hacking
subtitle: El diablo está en los detalles.
description: Aprenderás los comandos básicos de linux y detalles de estos que nos pueden ayudar en el hacking.
image: https://www.curvearro.com/wp-content/uploads/2019/10/Ethical-Hacking-Curvearro.jpg

optimized_image: https://www.curvearro.com/wp-content/uploads/2019/10/Ethical-Hacking-Curvearro.jpg
 

         
category: linux
tags:
  - linux
  - Introducción

author: mranderson
---

## Comando Id

Es muy sabido que hay varios usuarios a nivel de sistema y con el comando <a href="#">id</a> puedes ver a que grupo perteneces,
 . Cuando comprometemos una maquina *linux* ver en todo momento en que grupo estamos puede ser interesante. 
Toma encuenta que hay algun que otro grupo que puede presentar un riesgo de ESCALA DE PRIVILEGIOS o algo del estilo como grupos: docker ,kxd, root, etc.
Uno que representa un riesgo es el comando de grupo sudo por obvias razones, el cual te permite ser admin total de todo.

```bash
$ whoami
user
$ id
uid=1000(username) gid=1000(username) groups=1000(username),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),116(lpadmin),126(sambashare)
```





Cada grupo se pueden ver en una ruta del sistema que está aquí, con **cat** se puede visualizar.
```bash
$ cat /etc/group
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:
tty:x:5:
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:
man:x:12:
proxy:x:13:
kmem:x:15:
dialout:x:20:
floppy:x:25:user
```
## Filtrar con grep

Cuando hay tanta data lo mejor es aplicar un filtro.
Si quieres operar sobre un output, tú puedes tipearlo, significa que el output 
del comando anterior que has ejecutado, ahora digamos que quieres tratarlo
 para efecturar una segunda operatoria.
Pues hay un comando en linux que es *grep* que sirve apra aplicar filtros, seguramente lo usaras bastante.

```bash
$ cat /etc/group | grep "floppy"
floppy:x:11:
```
Lo chulo del comando "grep" es que si quisiéramos ver en que linea esta floppy lo haríamos añadiendo el parametro <a>-n</a> al final.

```bash
$ cat /etc/group | grep "floppy" -n
11:floppy:x:11:
``` 

  
## Comandos básicos

Ahora, podrán ver los comandos más básicos y más usados en linux

<ul>
  <li><code>ls</code>: Listar archivos y directorios.</li>
  <li><code>pwd</code>: Mostrar el directorio actual.</li>
  <li><code>cd</code>: Cambiar de directorio.</li>
  <li><code>mkdir</code>: Crear un directorio.</li>
  <li><code>touch</code>: Crear un archivo vacío.</li>
  <li><code>cp</code>: Copiar archivos y directorios.</li>
  <li><code>mv</code>: Mover o renombrar archivos y directorios.</li>
  <li><code>rm</code>: Eliminar archivos y directorios.</li>
  <li><code>cat</code>: Mostrar el contenido de un archivo.</li>
  <li><code>grep</code>: Buscar texto en archivos.</li>
  <li><code>chmod</code>: Cambiar los permisos de un archivo o directorio.</li>
  <li><code>chown</code>: Cambiar el propietario de un archivo o directorio.</li>
  <li><code>ps</code>: Mostrar procesos en ejecución.</li>
  <li><code>kill</code>: Terminar procesos.</li>
  <li><code>top</code>: Ver información sobre el uso del sistema.</li>
  <li><code>df</code>: Mostrar el espacio en disco disponible.</li>
  <li><code>free</code>: Mostrar la memoria RAM disponible.</li>
</ul>


Espero que les haya sido de utilidad y agradezco poder aportar a la comunidad








