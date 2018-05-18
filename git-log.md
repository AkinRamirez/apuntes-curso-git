### git log
Muestra todo el historial de commits del proyecto

`git log --pretty=format:"%h - %an, %ar : %s"`
Muestra el historial con el formato que indicamos. 

#### Limitar la salida del historial
`git log -n` : Cambiamos n por cualquier numero entero, por ejemplo: `git log -2` nos mostrara los 2 commit mas recientes.

`git log --after="2018-05-16 00:00:00"` : Muestra los commit realizados despues de la fecha especificada.

`git log --before="2018-05-17 00:00:00"` : Muestra los commit realizados antes de la fecha especificada.

Las banderas del comando `git log` se pueden usar juntas segun convenga, por ejemplo:
`git log --after="2018-05-16 23:00:00" --before="2018-05-17 22:00:00"`