# Chuleta GIT #
---

### Vamos a detallar posibles situaciones de GIT y qué hacer en cada caso ###

## Subir contenido nuevo de nuestra rama local a nuestra rama en el repositorio ##
	- Abrimos una consola desde nuestro IDE `control + shift + C`
	- `git status`. Esto nos ayudará a ver que ficheros han sido modificados (aparecerán en rojo) y cuales están ya trackeados (aparecerán en verde). 
	- `git add .`. Este comando nos trackea todos los ficheros que han sido modificados y los añade a la cola para poder subirlos mas tarde. Si tras esto hacemos `git status` de nuevo, aparecerán todos los ficheros "añadidos", es decir, en color verde. 
	- `git commit -m "feat|fix(frontend|backend|chatbotai|db...): mensaje intuitivo de los cambios realizados"`. Esto nos ayudará a identificar fácilmente que hemos hecho (feat|fix) a una determinada zona del proyecto (frontend|backend...). Por tanto un commit tipo seria algo asi como: `feat(frontend): update chatbotai cards`.
	-  Este comando lo que hace es subir a nuestra rama remota todos los cambios que hayamos añadido previamente. 

#### Si hay algun otro compañero trabajando en la misma rama y ha subido cosas, debemos verificar previamente si hay algún cambio en el repositorio remoto y también  resolver conflictos en caso de que los haga. ####
	
	- `git pull`. Nos trae todos los cambios que haya en el repositorio remoto actual. Es decir, trabajamos con el repositorio actualizado. 
	- `git push`. Una vez hayamos resuelto los conflictos debemos volver a subir los cambios actualizados. 

---

## Una vez hemos terminado con nuestra rama ##

	- `git switch main`. Una vez hayamos terminado con nuestra rama, debemos actualizar nuestro repositorio local respecto al de la nube. Esto solo lo podemos hacer cuando no haya ningún fichero modificado en nuestro repositorio local. 
	- `git fetch`. Esto actualizará todo el contenido de main y estaremos trabajando en un repositorio actualizado. 
	- `git merge main`. Esto nos juntara el contenido que acabamos de obtener de main con el paso anterior con el contenido actual de nuestra rama local. 

---

## STASH ##

#### Esto nos ayudara a hacer pequeñas modificaciones y cuando queramos ocultarlas, usarlas para más tarde, o simplemente no perderlas.  ####

	- `git status`. Para ver que cosas vamos a stashear, siempre es útil hacerlo. 
	- `git stash -m "nombre del stash"`. Aqui no hace falta usar conventional commits, ya que es algo nuestro, de nuestro repositorio local y por tanto es un mero nombre identificativo. 
	- `git stash list`. Esto nos servirá para ver el listado de las cosas a la que hemos hecho stash, numeradas con su número identificativo y el nombre que les hayamos puesto. 
	- `git stash apply stash@{id}`. Con este comando seremos capaces de aplicar, sin perder nada en el stash list, los cambiamos que teníamos stasheados.
	- `git stash drop`. Con este comando lo que consigo es eliminar el stash@{0} sin aplicar, por lo que liberamos stash del stash list. 
	- `git stash drop stash@{id}`. Hacemos lo mismo que en git stash drop pero le pasamos un determinado id, por lo tanto eliminamos por ejemplo el stash@{3}
	- `git stash pop`. Con este comando lo que consigo es eliminar el stash@{0} pero aplicándolo. Asi lo tenemos en nuestra rama pero lo eliminamos del stash list
	- `git stash pop stash@{id}` -> Hacemos lo mismo que en git stash pop pero le pasamos un determinado id, por lo tanto eliminaríamos por ejemplo el stash@{3}. 

---
## CHERRY PICK ##

#### Esto es un comando que se utiliza cuando necesito algo de otra rama pero aún no está en main. Por tanto tenemos que coger los commits que necesitemos dentro del repositorio `http://192.168.2.71/implemental/gis-is`, buscamos el hash de cada commit que necesitemos y seguimos esta guia. ####

	- Normalmente esto solamente lo haremos cuando se haya creado una nueva funcionalidad, por tanto no deberia generar muchos conflictos. 
	- `git cherry-pick {numero del commit} ... {n-avo - numero del commit }`. Ahora en nuestra rama A tendremos contenido de rama B sin haber pasado por main. 