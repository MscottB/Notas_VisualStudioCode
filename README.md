# Notas Visual Studio Code (Windows)

## 1.- Tips Basicos

### 1.1-Ordenar Lista ( < li > )

Para ordenar lista Ocupar los siguientes comandos, `Alt + ↑ / ↓` (Flecha direccion Arriba, Flecha Direccion Abajo). Se situa en la linea y se mueve con el comando previamente entregado.

* Antes
```html
<ul>
    <li>Línea 7</li>
    <li>Línea 3</li>
    <li>Línea 6</li>
    <li>Línea 2</li>
    <li>Línea 5</li>| <--lugar cursor y linea a modificar.
    <li>Línea 4</li>       
    <li>Línea 1</li>
</ul>
```
* Despues
```html
<ul>
    <li>Línea 1</li>
    <li>Línea 2</li>
    <li>Línea 3</li>
    <li>Línea 4</li>
    <li>Línea 5</li>
    <li>Línea 6</li>
    <li>Línea 7</li>
</ul>
```
### 1.2-Ordenar multiples Lineas

Para ordenar lista Ocupar los siguientes comandos, `Alt + ↑ / ↓` (Flecha direccion Arriba, Flecha Direccion Abajo). Se selecciona la seccion a mover y se ocupa el comando.

Antes:
```html
<ul>
    <li>
        <span>línea 4</span>
        <span>Nada importante 4</span>
    </li>
    <li>
        <span>línea 3</span>
        <span>Nada importante 3</span>
    </li>
    <li>
        <span>línea 2</span>
        <span>Nada importante 2</span>
    </li>
    <li>
        <span>línea 1</span>
        <span>Nada importante 1</span>
    </li>
</ul>
```
Despues:
```html
<ul>
    <li>
        <span>línea 1</span>
        <span>Nada importante 1</span>
    </li>
    <li>
        <span>línea 2</span>
        <span>Nada importante 2</span>
    </li>
    <li>
        <span>línea 3</span>
        <span>Nada importante 3</span>
    </li>
    <li>
        <span>línea 4</span>
        <span>Nada importante 4</span>
    </li>
</ul>
```

>En caso de que al mover se agregen mas "sangrias" o TAB, se ocupa SHIFT + TAB para quitar los espacios. 

### 1.3-Comentar Codigo

Para comentar una sola línea o cada línea de un bloque: `CTRL+K CTRL+C` (NO requiere que el texto esté seleccionado, por defecto comenta la línea actual)

Para hacer lo opuesto al paso anterior (descomentar): `CTRL+K CTRL+U` (NO requiere que el texto esté seleccionado, por defecto comenta la línea actual)

Para hacer un comentario en bloque: `SHIFT+ALT+A` (Requiere selección)

Antes: 
```html
const a = 10;
const b = 20;
const c = { a, b };
```

Despues:
* Comentar Linea(`CTRL+K CTRL+C`, `CTRL+}`)
```html
// const a = 10;
// const b = 20;
// const c = { a, b };
```
* Comentario Bloque (`SHIFT+ALT+A`)
```html
/* const a = 30;
const b = 40;
const c = { a, b }; */
```

### 1.4-Crear Archivo

Para evitar la creacion de carpetas y archivos de manera manual en un nuevo proyecto, se puede ocupar `CTRL+Click` sobre la direccion de un nuevo archivo;

ejemplo:
```html
<script src="assehtml/js/app.js"></script>
```
Al ocupar el comando sobre el `src`, VSCode mostrara que no existe y permitira crear las carpetas y el archivo requeridos, ademas de abrir el nuevo archivo creado.

### 1.5-Ir a Definicion

Para ver las deficiones de una funcion existen 2 metodos:

* __F12__: Abrira una nueva pestaña mostrando el archivo completo.
* __ALT+F12__: Abrira una pequeña ventana en el archivo que se esta viendo actualmente. En resumen, mostrara la deficion sin salir de la ventana.
* __CTRL+Click__: Abrira una nueva ventana pero mostrara especificamente la funcion a la que hicimos click.
* __CTRL__: permite ir a la linea de codigo donde esta la deficion de una funcion, la cual se estaba llamando.

### 1.6-Borrar Linea

Permite borrar de manera seleccionada las variables establecidas(Un ejemplo).

Antes:
```html
let NoMeBorres = ':)';
let Borrame = ':(';

NoMeBorres = '1';
Borrame    = 'a';
NoMeBorres = '1';
Borrame    = 'a';
```
Despues:

* Borrar Una Linea(CTRL+SHIFT+K)
Borra la linea donde se estepocicionado.
```html
let NoMeBorres = ':)';


NoMeBorres = '1';
Borrame    = 'a';
NoMeBorres = '1';
Borrame    = 'a';
```

* Borrar la seleccionada y sus copias(`CTRL+SHIFT+L`, `CTRL+SHIFT+K`, `ESC`)

Para facilitar la eliminacion de multiples parametros, variables, etc. que posean un mismo nombre pero se selecciona el que se desea eliminar ejemplo `Borrame`, despues se ocupa `CTRL+SHIFT+L` y seleccionara todas las variables que sean identicas a la seleccionada anteriormente, posteriormente ocupa `CTRL+SHIFT+K` para eliminarlas y finalmente `ESC` para salir del multicursor.

Resultado:
```html
let NoMeBorres = ':)';

NoMeBorres = '1';
NoMeBorres = '1';
```
### 1.7-Deshacer/Rehacer.

Para deshacer un cambio realizado `CTRL+Z`, y para reacer un cambio `CTRL+SHIFT+Z`.

*__Deshacer:__`CTRL+Z`
*__Rehacer:__`CTRL+SHIFT+Z`

### 1.8-Zen Mode

El modo cero distracion, se activa `CTRL+K,Z`(Se debe soltar el CTRL y despues apretar Z).Es modo de pantalla Completa.
Para cambiar de archivos en modo Zen, `CTRL+P`.

Para mostrar/ocultar la barra lateral `CTRL+B`.

### 1.9-Terminal Integrada

VScode viene con una terminal propia, con la cual se inicia con `CTRL+Ñ`, mismo comando para minimizar terminal.

Simbologia
* __+__, permite agregar otra pestaña de terminal.
* __Basurero__: Eliminara la terminal, y se detendra todo lo que este ejecutando.


### 1.10-Emmet Wrap / atajos personalizados

Sirve para enmarcar un codigo, con `CTRL+SHIFT+P`,  se ingresa `wrap whith abbreviation` y se agrega el codigo con el con el que se desea enmarcar en este caso `CODE`, pero puede ser cualquier otro. Es postible ocupar los comandos de emmet.

Ejemplo:
```html
// Antes
ng server
// Despues - code
<code>ng server</code>
// Con emmet - ul>li
<ul>
    <li>
        ng server
    </li>
</ul>
```
Para que se aplique se presiona `ENTER` en caso contrario `ESC`

Para evitar todo el proceso anterior es posible asignar un metodo abreviado, este se encuentra en `archivos>preferencias>metodos abreviados de teclado`, se busca `wrap whith abbreviation` y se le asigna un `enlace de teclado`, que no este asignado a otra funcion.

### 1.11-Manejo Tab

Manejo de pestañas en VSCode.
* __Cerrar Pestaña:__`Ctrl + W`
* __Cerrar todas las pestañas:__`Ctrl+K Ctrl+W`
* __Reabrir pestaña cerrada:__`Ctrl+Shift+T`
* __Cambiar a pestaña especifica:__`CTRL+TAB`

Para ver los que se abrieron recientemente `CTRL+P`

## 2.-Multi Cursor / Edicion Rapida

### 2.1-Clonar Lineas

Para copiar una linea multiples veces, se coloca el cursor en la linea deseada y se ejecuta el comando `SHIFT+ALT+FLECHA-ARRIBA`/`SHIFT+ALT+FLECHA-ABAJO`

Ejemplo:

Antes:
```html
<span>hola</span>
```
Despues:
```html
<span>hola</span>
<span>hola</span>
<span>hola</span>
<span>hola</span>
```
>Es posible clonar una linea o una seccion seleccionada.
>
>Se debe revisar el comando, para estar seguro, puede variar. con `CTRL+k CTRL+S` se inicia la pestaña de metodos abreviados.

### 2.2-MultiCursor Arriba/Abajo de Posicion Actual

Sirve para seleccionar mas de una linea y escribir en todas las seleccionadas al mismo tiempo, `Ctrl+Alt+Flecha(↑ / ↓)`.
y posteriormente se apreta `ESC` para salir del multicursor.

### 2.3-Multicursor Copiar

Es similar al punto 2.2, con la diferencia que se le agrega `SHIFT+ALT+FLECHA-DERECHA/FLECHA-IZQUIERDA` asi seleccionara el caracter siuiente al cursor, aunque estes posean diferentes longitudes.

Ejemplo
```html
<span>amarillo</span>
<span>rojo</span>
<span>verde</span>
<span>naranja</span>
<span>morado</span>
<span>negro</span>
<span>blanco</span>
```
### 2.4-MultiCursor Formato

Se ocupa el multicursor para agregar los espacios o tab correspondientes para que todo quede alineado...

### 2.5-MultiCursor Lowcase-Uppercase

Los metodos abreviados de **Lowercase** y **Uppercase** no poseen metodo abreviado por lo tanto se les debera asignar.
En mi caso:
* __LowerCase__: `CTRL+ALT+{`
* __Uppercase__: `CTRL+ALT+}`
>esto es perzonalizazdo, en vscode no estan asigandos.

Para capitalizar una lista de apellidos, aunque tengan diferentes longitudes se ocupa. `CTRL+FLECHA-DERECHA/FLECHA-IZQUIERDA`. esto despues de ocupar el multicursor.
>para seleccionar la primera palabra delante del cursor `ALT+SHIFT+FLECHA-DERECHA`

Ejemplo:
Antes:
```ts
    const hulk       = 'brouce banner';
    const hawkeye    = 'cinton francis';
    const ironman    = 'tony stark';
    const spiderman  = 'peter parker';
    const viudanegra = 'natalia romanova';
```
Despues:
* Capitalizado(Primera letra mayuscula):
```ts
    const Hulk       = 'Brouce Banner';
    const Hawkeye    = 'Cinton Francis';
    const Ironman    = 'Tony Stark';
    const Spiderman  = 'Peter Parker';
    const Viudanegra = 'Natalia Romanova';
```

### 2.6-Multicursor Posicion Especifica(ALT)

para seleccionar de manera especifica secciones de lineas, se debe mantener pulsado la tecla `ALT`, y seleccionar lo que se necesite con doble click o pulsar y selecionar lo deseado con el mouse.

Ejemplo:
```html
<span>amarillo</span>
<p>rojo</p>
<div-personalizado>verde</div-personalizado>
<bold>naranja</bold>
<otro-div-complejo>naranja-azul</otro-div-complejo>
```

### 2.7-Multicursor seleccion de palabra especifica(CTRL+D)

Es posible seleccionar una palabra y sus copias de la siguiente manera, `Doble click` a la palabra deseada y posteriormente `CTRL+D` por cada copia de esa palabra.

## 3.-Definicion & Snipper

### 3.1-Definiciones archivo

para ver las definiciones, o mejor dicho las clases, variables, propiedades y metodos entre otros y poder dirijirse a ellos de manera rapida y simple se ocupa.

* Metodo 1
`CTRL+SHIFT+O`(no es cero/0)
* Metodo 2
`CTRL+P`, despues el signo `@`

Para obetenerlas de manera agrupada, por tipo se agrega __Dos puntos(__:__)__.

### 3.1- Moverse Linea Especifica

Existen dos maneras para moverse a una linea especifica.

* Metodo 1: `CTRL+G` y se escribe el numero.
* Metodo 2: `CTRL+P` y despues se coloca __Dos Puntos(__:__)__.

### 3.2- Ver archivos MarkDown

Para ver como sera la vista de un archivo markdown se ocupa lo siguiente:

* Ctrl+Shift+P : y se escribe `Markdown Open Preview`
* Ctrl+Shift+P : y se escribe `Markdown Open Preview to the side`

### 3.3- ReNombrar

#### Cambiar de Manera Local
Para reemplazar una seccion y no romper el codigo, se preciona la variable deseada y apreta `F2`, posteriormente se agrega el reemplazo y `ENTER`.

Ejemplo

* Antes:
```ts
import { SuperHeroe } from './extra/classes';

const wolverine = new SuperHeroe();
const ironman   = new SuperHeroe();
const spiderman = new SuperHeroe();

function saludar() {
    return 'El SuperHeroe Wolverine es genial!';
}

function gritar() {
    return 'El SuperHeroe en este string no se debe de cambiar';
}
```
Despues:
```ts
import { SuperHeroe as Heroe } from './extra/classes';

const wolverine = new Heroe();
const ironman   = new Heroe();
const spiderman = new Heroe();

function saludar() {
    return 'El SuperHeroe Wolverine es genial!';
}

function gritar() {
    return 'El SuperHeroe en este string no se debe de cambiar';
}
```
Cambio las Constantes/variables desde __SuperHeroe__ a __Heroe__, sin romper el codigo.

#### Cambiar de manera Global

Para hacerlo se cambia el nombre de la clase con `F2` y VSCode cambiara el nombre en todos los archivos donde se use dicha clase.

### 3.4-Snippets básicos

Para crear un Snippets es `Archivo>Preferencias>Fragmentos de codigo de usuario`, mostrara los que tengan instalados y seleciona el lenguaje. mostrar un nuevo archivo JSON y podra agregar el snippet que desee.

Ejemplo
```json
{
    "import from module": {
        "prefix": "impx",
        "body": ["import { $2 } from '$1';"],
        "description": "Import en typescript"
    }
}
```
>Para pasar de el punto $1 al punto $2 que se ha asignado en el snippet, se realiza con el `TAB`, y no con el `ENTER`.
>
>En caso de no mostrar los snippets, ocupar `CTRL+ESPACIO` y buscar el snippet deseado.

## 4.-Extensiones

### 4.1-Paste JSON as CODE

Esta extension sirve para analizar la respuesta de una API, y generar las clases/interfaces necesarias para trabajar con dicha API.

para ocupar `CTRL+SHIFT+P` y escribir `paste jason as code` o parte de este, analizara el respuesta de la api que copiamos(si no copiamos no puede analisar nada y mostrar un mensaje), y perdira un nombre para la interface(posteriormente se le puede cambiar a clase de ser necesario).

### 4.2-TODO Tree

Sirve para agregar anotaciones dentro de los archivos, maneja dos prefijos `TODO` y `FIXME`, los cuales apareceran en el nuevo icono(tiene forma de arbol) en la barra lateral, Lo puede mostrar de multiples maneras, como "arbol", por tag, o filtrar.

Ejemplo
```ts
// TODO: Anotacion.

// FIXME: arreglar o corregir.
```

#### 4.2.1-Ignorar carpetas en Todo Tree
Para ignorar los `TODO/FIXME`, que puedan estar en node_module, se ingresa a `archivo>preferencias>configuracion`, en la seccion `extensiones` se busca `TODO tree` y se hace click en `edit in setting.json` del modulo __Exclude Globs__. No aparecera la opcion necesaria por eso se agrega el siguiente codigo.
```js
    "todo-tree.excludeGlobs": [
        "**/node_modules/**",
        "**/dist/**"
    ]
```

#### 4.2.2-Agregar nuevas Etiquetas

Para agregar nuevos tipos de etiquetas ademas de las que estan por defecto que son `TODO/FIXME`, en el mismo archivo de configuracion anterior(el de ignorar carpetas, el 4.2.2), se agrega el siguiente codigo.
```json
    "todo-tree.tags": [
        "TODO",
        "FIXME",
        "PENDIENTE",
        "ARREGLAR",
        "INCOMPLETO",
        "NOTA"
    ]
```
Para agregar color para remarcar la palabra, se agrega el siguiente codigo.
```ts
    "todohighlight.keywords": [
        {
            "text": "TODO:",
            "color": "red",
            "border": "1px solid red",
            "borderRadius": "2px", 
            "backgroundColor": "rgba(0,0,0,.2)",

        },
        {
            "text": "FIXME:",
            "color": "white",
            "border": "1px solid white",
            "borderRadius": "2px", 
            "backgroundColor": "blue",

        },
        {
            "text": "PENDIENTE:",
            "color": "black",
            "border": "1px solid black",
            "borderRadius": "2px", 
            "backgroundColor": "rgb(235, 235, 52)",

        },
        {
            "text": "ARREGLAR:",
            "color": "black",
            "border": "1px solid black",
            "borderRadius": "2px", 
            "backgroundColor": "rgb(0, 255, 21)",

        },
        {
            "text": "INCOMPLETO:",
            "color": "black",
            "border": "1px solid white",
            "borderRadius": "2px", 
            "backgroundColor": "rgb(252, 186, 3)",

        },
        {
            "text": "NOTA:",
            "color": "black",
            "border": "1px solid white",
            "borderRadius": "2px", 
            "backgroundColor": "rgb(221, 0, 255)"

        }
    ]
```

### 4.3-Bookmarks

Para agregar marcadores en el codigo, ya que puede ser necesario ver multiples veces una seccion de codigo. se realiza con `CTRL+ALT+K`, o se busca con `CTRL+SHIFT+P` y la palabra `bookmarks toggle` para confirmar el comando. Estos apareceran en la barra lateral de VSCode.

### 4.4-Color Highlight

Sirve para agregar color a los codigos relacionados a este tales como `#fafafa` que seria blanco, en su configuracion, esta si se desea colocar el color que representa en un cuadrao antes o despues del cofigo asi como otras opciones por defecto esta de fondo.

### 4.5-Bracket Pair Colorizer 2

Permite tener una mejor vista de las llaves en los codigos, con sus respectivos colores y en orden.
En configuracion se agrega el siguiente codigo:
```json
"bracket-pair-colorizer-2.colors": [
        "Gold",
        "Orchid",
        "LightSkyBlue"
    ]
```
Este es por defecto, pero es posible perzonalizarlo, los colores se mostraran en el siguiente orden
* Primer color - Primera llave
* Segundo color - Segunda llave
* Tercer color - Tercera llave