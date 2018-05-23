### Situacion al momento de hacer `git push origin master`
! [rechazado] maestro -> maestro (buscar primero)
https://stackoverflow.com/questions/28429819/rejected-master-master-fetch-first

¿Hay alguna manera de explicar cómo resolver " ! [rejected] master -> master (fetch first)' " en Git?

Cuando uso este comando `$ git push origin master` muestra un mensaje de error.

```
! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'git@github.com:zapnaa/abcappp.git'
```

La respuesta está ahí, git te dice que busques primero.

Probablemente alguien más haya empujado a dominarlo, y tu compromiso está atrasado. Por lo tanto, debe buscar, fusionar el conjunto de cambios y luego podrá volver a presionar.

Si no lo hace (o incluso peor, si lo fuerza mediante el uso de la opción `--force`), puede estropear el historial de confirmaciones.

EDITAR: Obtengo más detalles sobre el último punto, ya que un tipo aquí acaba de dar el Muy Mal Consejo de usar la opción `--force ` .

Como git es un DVCS, idealmente muchos otros desarrolladores están trabajando en el mismo proyecto que tú, usando el mismo repositorio (o un tenedor). 

Si sobrescribe a la fuerza con su conjunto de cambios, su repositorio no coincidirá con el de otras personas, porque "reescribió el historial". Harás a otras personas infelices y el repositorio sufrirá. Probablemente un gatito en el mundo llorará también.

1. Si quiere resolver, busque primero (y luego fusione).
2. Si quiere hackear, use la opción `--force` .

Siempre ir por la opcion 1, incluso si usará git usted mismo, porque es una buena práctica.


