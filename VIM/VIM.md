[[Vimum]]
[[NerdTree - vim plugin]]
[[settings_idea/ideavimrc.txt]]

con d +w borras el caracter en el que estás 

---
### Repasar 
`<` y `>` sirven para identar

---
---
**`n` y `N`**:

- **Uso**: Funcionan después de realizar una búsqueda con `/`

con `/` busca la primera palabra que coincida 
*  `n` = busca esa palabra por todo el código = para ir al revés usar `N` 

---
---

 
**`*` y `#`**:

- **Uso**: Se utilizan directamente sin iniciar una búsqueda, simplemente colocando el cursor sobre una palabra.

---


`y` + `{` para copiar bloque de código 

-----

`A` insert al final de la línea
`I` insert al Inicio de la línea
`O` insert encima de la línea
 
----
----
**Puedes usar números: 5 w** 
`w` Inicio palabra derecha 
`b` Inicio palabra izquierda

- `d + w` borrar hacia la derecha   
- `d + b` borrar hacia la izquierda
- `d + t +` *x*  borra hasta que se tope con el caracter (*x*)  

---
`e` Final palabra izquierda
###  Vim ecosystem 
- Vim Editor
- Vim plugins
	-  plugins para el Vim editor
- Vim Motions
	- modos y comandos para navegar y editar 

### VIM Plugins
**esc**: activar el modo
**i-a-o** : desactivar el modo

 **h-j-k-l**: (navegar) 
	 podemos navegar con prefijos, 5 + L : 5 espacios a la derecha

---

**w-b-e** (Moverse por las las palabras) b y w panas 
	**la e es de end**
	w:  Mover al inicio de la siguiente palabra.
	b: moverse al inicio de la palabra anterior
	
 ---
	e: Mover al final de la siguiente palabra
	ge mover al final de la palabra anterior
	
**gg-G** (inicio y final del archivo.)
	gg: final archivo
	G: inicio archivo

### Modes
#### Normal
#### Insert
#### Visual y Visual Block
- Visual: modo por defecto para editar
- Visual Block lo mismo pero para editar bloques 
- ---
se activa con la **v** y sirve para seleccionar texto de varias maneras,
ya sea carácter por carácter, línea por línea o en bloques.

#### 10. **Comandos ex**:
- `:w` - Guardar el archivo.
- `:q` - Salir de Vim.
- `:wq` - Guardar y salir.
- `:q!` - Salir sin guardar.

### LOS TOPS
- `d` + `d` - Borrar la línea actual.
- `d` + `w` - Borrar desde el cursor hasta el inicio de la siguiente palabra.
- `d` + `$` - Borrar desde el cursor hasta el final de la línea.
- `x` - Eliminar el carácter bajo el cursor.
- `r` - Reemplazar el carácter bajo el cursor.

### 1. **Movimientos básicos**:
- `h` - Mover el cursor a la izquierda.
- `j` - Mover el cursor hacia abajo.
- `k` - Mover el cursor hacia arriba.
- `l` - Mover el cursor a la derecha.
- `w` - Mover al inicio de la siguiente palabra.
- `e` - Mover al final de la palabra actual.
- `b` - Mover al inicio de la palabra anterior.
- `0` - Ir al inicio de la línea.
- `$` - Ir al final de la línea.
- ---
- `Ctrl` + `d` - Desplaza media página
- `Ctrl` + `u` - Desplaza media página
- `gg` - Ir al inicio del archivo.
- `G` - Ir al final del archivo.
  
### 2. **Edición de texto (Inset Mode)** :
- `i` - Insertar antes del cursor.
- `I` - Insertar al inicio de la línea.
- `a` - Insertar después del cursor.
- `A` - Insertar al final de la línea.
- `o` - Insertar una nueva línea debajo.
- `O` - Insertar una nueva línea arriba.
---
### 3. **Copiar y pegar (yank y paste)**:
- `y` + `y` - Copiar (yank) la línea actual.
- `y` + `w` - Copiar la palabra desde el cursor.
- `y` + `$` - Copiar desde el cursor hasta el final de la línea.
- `p` - Pegar después del cursor.
- `P` - Pegar antes del cursor.
- ``gg+V+G+y`` == Ctrl + a 

  
### 4. **Deshacer y rehacer**:
- `u` - Deshacer la última acción.
- `Ctrl` + `r` - Rehacer la última acción deshecha.

### 5. **Visual Mode (modo visual para selección)**:
- `v` - Iniciar selección visual de caracteres.
- `V` - Iniciar selección visual de líneas.
- `Ctrl` + `v` - Iniciar selección visual en bloque (modo visual por columna).
- `d` - Cortar el texto seleccionado.
- `y` - Copiar el texto seleccionado.
  
### 6. **Navegación rápida**:
- `f` + `carácter` - Mover el cursor al siguiente carácter en la línea.
- `F` + `carácter` - Mover el cursor al anterior carácter en la línea.
- `t` + `carácter` - Mover el cursor justo antes del siguiente carácter.
- `T` + `carácter` - Mover el cursor justo antes del anterior carácter.
### 7.**Navegación vertical**
5j y 5k 
{}
()   

---
- **Ctrl+u**: Subir media página.
- **Ctrl+d**: Bajar media página.
----
- **Ctrl+b**: Subir una página completa.
- **Ctrl+f**: Bajar una página completa.
---
- **H**: Ir al principio de la pantalla visible.
- **M**: Ir al medio de la pantalla visible.
- **L**: Ir al final de la pantalla visible.
- **{**: Saltar al comienzo del párrafo anterior.
- **}**: Saltar al comienzo del siguiente párrafo.
 
### 8. **Buscar y reemplazar**:
- `/` + `palabra` - Buscar hacia adelante.
- `?` + `palabra` - Buscar hacia atrás.
- `n` - Ir al siguiente resultado de búsqueda.
- `N` - Ir al resultado anterior de búsqueda.
- `:%s/viejo/nuevo/g` - Reemplazar todas las ocurrencias de "viejo" con "nuevo".



### 9. Borrar 
- `x`  Eliminar el carácter bajo el cursor.
- `X` Borra el carácter antes del cursor (similar a la tecla de retroceso).
- ---
- db 
- dw


-  `d` + `d` - Borrar la línea actual.
- `d` + `w` - Borrar desde el cursor hasta el inicio de la siguiente palabra.
- `d` + `$` - Borrar desde el cursor hasta el final de la línea.

- `r` - Reemplazar el carácter bajo el cursor.


### 10. **Macros (automatización)**:
- `q` + `carácter` - Iniciar grabación de macro (usa un carácter para el nombre).
- `q` - Detener grabación de macro.
- `@` + `carácter` - Ejecutar macro guardada en el carácter.

### 11. **Guardar y salir:**:

`:w` : Guardar el archivo (write).
`:q` : Salir de Vim (quit).
`:wq` o ZZ : Guardar y salir.
`:q!` : Salir sin guardar los cambios (force quit).
`:x` : Guardar y salir, equivalente a :wq.
![[Pasted image 20241107142826.png]]
