Git Rebase
==============================
----
## Aplicaciones Moviles
#### Carlos fernando Torres Luna
##### cf.torresluna@gmail.com 
---

#### Rebase utilizado como parametro de pull

Cuando hacemos git pull, nos traemos los cambios del repositorio que elijamos o tengamos configurado, y uno de los parámetros que podemos utilizar es rebase:
```sh
$ git pull --rebase
```
Al realizar un pull estamos haciendo un fetch y justo después un merge, pasándole la opción rebase, git intentará traer todos los cambios y después aplicar nuestras modificaciones encima en lugar de intentar hacer un merge desde el punto en el que estábamos, esto hará que nuestro histórico tenga mucho mejor aspecto. 

![alt text][logo]
[logo]: http://cambrico.net/sites/cambrico.net/files/blog_imagen/spoon-knife_detached_head-1-1.jpg "git-pull"

![alt text][logo]
[logo]: http://cambrico.net/sites/cambrico.net/files/blog_imagen/spoon-knife_detached_head-3.jpg "git-pull --rebase"

#### Comando Rebase

El comando rebase hace algo muy diferente; cuando tenemos una serie de commits que queremos asociar juntos, normalmente por la misma razón que el ejemplo anterior, mantener una historia de commits un poco más limpia, podemos utilizar git rebase.

```sh
$ git rebase -i BRANCH/HASH
```
##### Ejemplo
Tenemos un commit inicial y tres modificaciones para juntar todos estos commits en uno solo, podemos utilizar git rebase, el procedimiento sería localizar la rama o el hash anterior al primer commit que queremos agregar y usarlo como parámetro de git rebase:

```sh
$ git rebase -i bdd3996d
```

![alt text][logo]
[logo]:http://cambrico.net/sites/cambrico.net/files/blog_imagen/spoon-knife_detached_head-4.jpg "git  rebase"

Despues de hacer git rebase nos manda a esta ventana interactiva donde muestra todos los commits que queremos asociar. 

![alt text][logo]
[logo]: http://cambrico.net/sites/cambrico.net/files/blog_imagen/1._vim.jpg "git rebase"

Despues nos manda a un segundo proceso donde muestra las modificaciones entrre los diferentes commits.

![alt text][logo]
[logo]: http://cambrico.net/sites/cambrico.net/files/blog_imagen/1._sh.jpg "git rebase"

![alt text][logo]
[logo]: http://cambrico.net/sites/cambrico.net/files/blog_imagen/spoon-knife_detached_head-5.jpg "git rebase"