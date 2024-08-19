[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=30&pause=1000&random=false&width=435&lines=Apuntes+Dev+Full+Stack)](https://git.io/typing-svg)

----

## Visual Studio Code

#### Orden de las carpetas

![image-20240710092740896](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240710092740896.png)

#### Responsible Dimensiones

- Teléfonos móviles (landscape): 320px y más
- Tabletas: 768px y más
- Computadoras de escritorio (desktops): 992px y más
- Computadoras de escritorio grandes (large desktops): 1200px y más

## HTML BÁSICO

#### Estructura de una etiqueta

heading h1 h2 h3 ... h6 

Contenedores: div span

#### Estructura de una página WEB

- Elementos:

  - inline (en línea)
  - block (en bloque)

  | Elemento                                                     | inline | block | inline-bock |
  | ------------------------------------------------------------ | ------ | ----- | ----------- |
  | hx - p - div - ul - ol - main - aside - footer - header - section -nav ... |        | ❌     |             |
  | span - a - label - b - strong - i - em                       | ❌      |       |             |
  | img -button - iframe - textarea - audio - video - select - ... |        |       | ❌           |
  
  > Los elementos de linea no pueden ser modificados facilmente por code  margin❗❗

#### Párrafos y encabezados

> `<p> ... </p> | <h1> TITULO</h1> al <h#>Subtitulo</h#>`

#### Listas

| Con Orden    | Sin Orden    |
|--------------|--------------|
| `<ol>`       | `<ul>`       |
| `<li> </li>` | `<li> </li>` |
| `</ol>`      | `</ul>`      |

#### Enlaces (Hipervínculo)

> `<a href="atributo">...</a>`

| Atributos | Valores                                  | Función      |
|-----------|------------------------------------------|--------------|
| href=     | https://\*.com/ (ruta)                   | hipervínculo |
| target=   | \_self \_blanck \_parent \_top framename | pestañas     |
| title=    |                                          | Títulos      |

#### Imágenes

> `<img src="*.png">`

| Atributos | Valores | Función |
|-----------|---------|---------|
| src       | \*.png  | ruta    |
| alt       |         | texto   |
| title     |         | Título  |

#### Videos

````html
<video src="video/concierto.mp4" controls ... alt="Video de webs accesibles">
	Video no Soportado por el Navegador <!--Si no se reproduce aparece el siguiente texto-->
</video>
````

| Atributos | Valores | Función |
| --------- | ------- | ------- |
| src       | */ *.mp4 | ruta de video |
| controls |  | controles videos |
| autoplay |         | reproducción automática |
| mute | | silencia audio / reproducción automático |
| loop | | búcleo |
| poster | */ *.jpg | ruta de imagen |

[video - HTML: Lenguaje de etiquetas de hipertexto | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/HTML/Element/video)

````html
<video controls autoplay mute loop>
	<source src="video/concierto.mp4" type="video/mp4">
	<source src="video/concierto.ogg" type="video/ogg">
	<source src="video/concierto.webm" type="video/webm">
</video>
````

| Atributos | Valores                   | Función |
| --------- | ------------------------- | ------- |
| src       | */ *.mp4                  | ruta    |
| type      | "video/mp4 o ogg o webm " |         |

[ Source - HTML: Lenguaje de etiquetas de hipertexto | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/HTML/Element/source)

#### Rutas

-   Absolutas
-   Relativas

| Valor     | dirección                                               |
|-----------|---------------------------------------------------------|
| \*        | carpeta                                                 |
| ../\*     | volver una carpeta atrás                                |
| ../../\*  | volver dos carpetas atrás                               |
| \* /      | entramos una carpeta adelante                           |
| \* / \* / | entramos dos carpeta adelante                           |
| ../ \* /  | volver una carpeta atrás, entramos una carpeta adelante |

#### Formularios

````html
<form>
    <label for="...">...</label>
		<input type="..." name="..." required="..." ...>
	<label>
</form>
````


| Atributos   | Valores  | Función                 |
| ----------- | -------- | ----------------------- |
| type        | text     | <input type="text">     |
|             | color    | <input type="color">    |
|             | email    | <input type="email">    |
|             | password | <input type="password"> |
|             | checkbox | <input type="checkbox"> |
|             | radio    | <input type="radio">    |
|             | file     | <input type="file">     |
|             | date     | <input type="date">     |
|             | submit   | <input type="submit">   |
|             | number   | <input type="number">   |
| required    |          | campo requerido         |
| name        |          | id para el servidor     |
| placeholder |          | texto ejemplificador    |
| value       |          | recibe servidor         |
| minlength   |          | números min caracteres  |
| maxlength   |          | números max caracteres  |
| list        |          |                         |
| for         |          | Control de elemento     |
| id          |          | Identificador único     |

##### Datalist

https://developer.mozilla.org/es/docs/Web/HTML/Element/datalist

#### Iframe

| Atributos | Valores | Función |
| --------- | ------- | ------- |
| id        |         |         |
| title     |         |         |
| width     |         |         |
| height    |         |         |
| src       |         |         |

````html
<iframe src="https://..." id="..." ...>...</iframe>
````

https://developer.mozilla.org/es/docs/Web/HTML/Element/iframe

------------------------------------------------------------------------

## CSS BÁSICO

#### Introducción a CSS

- Variable

  ````css
  <!-- Codigo escalable-->
  :root{
  	--font-color: white;
      --width-container-1:936px;
  }
  body{
      <-- uso var para llamar la cariable definida-->
      font-color:var(--font-color);
      width:var(--width-container);
  }
  ````

  

-   Línea. Atributo

`ej. <p style= "color: red;font-size: 20px;...">lorem</p>`

> Poco escalable. | Mala práctica.💥

-   Etiqueta:

```html
<head>
    <style>
        h1 {color: red;} <!--Selector de elemento-->
        .clase {color:pink;} <!--Selector de clase-->
        #id {color:violeta;} <!--Selector de identificador-->
    </style>
</head>	
```

> Necesita de selectores.

-   Link:

```html
<head>
	<link rel="stylesheet" href="./style.css">
<head>
```

> href="./style.css" en algunos servidores no toma sin el punto y la barra.

#### Selectores (Básico)

-   Elemento

    `HTML: <body></body>`

    `CSS: body {propiedades:valores;...}`

    -   Clases (para varios elementos)

    `HTML: <body class= "clase"></body>`

    `CSS: .clase {propiedades:valores;...}`

    -   Id (para 1 elemento)

    `HTML: <body id= "identificador"></body>`

    `CSS: #identificador {propiedades:valores;...}`

-   Nomenclatura

    ```html
    <!-- EJEMPLO 1 -->
    <div class="block">
        <div class="block__element">Elem 1</div>
        <div class="block__element">Elem 2</div>
        <div class="block__element block__element--modifier">Elem 3</div>
    </div>
    
    <!-- EJEMPLO 2 -->
    <div class="item item--modifier">
        <div class="item__element">Elem 1</div>
        <div class="item__element">
            <div class="item__another-element">Elem 2</div>
            <div class="item__another-element">Elem 3</div>
        </div>
        <div class="item__element item__element--modifier">Elem 4</div>
    </div>
    ```

#### BEM

BEM significa *Modificador de Bloques de Elementos (Block Element Modifier)* por sus siglas en inglés. Sugiere una manera estructurada de nombrar tus clases, basada en las propiedades del elemento en cuestión.

Se centra en tres parámetros o variables posibles: **bloques** (div, section, article, ul, ol, etc.), **elementos** (a, button, li, span, etc.) y **modificadores**.

````css
.bock{
}
.block--modifier {
}
.block__element--modifier {
}
````

#### Especificidad

https://developer.mozilla.org/es/docs/Web/CSS/Specificity

| Selectores   | Formas                                   | Prioridad |
| ------------ | ---------------------------------------- | --------- |
| universal    | *{}                                      | Bajo      |
| elemento     | ej. div {}                               |           |
| clase        | ej. .class{}                             |           |
| id           | ej. #in{}                                |           |
| inline style | < h1 class="" id="" style = "color:red"> |           |
| !important   | ej. color: red !important;               | Muy Alto  |

- Herencia

  https://developer.mozilla.org/es/docs/Web/CSS/Inheritance

  ````html
   p { color: green }
  
   <p>Este párrafo tiene <em>texto enfatizado</em> en su interior.</p>
  
  ````
  
  ````css
  input, textarea {
      box-sizing: border-box;
      width: 100%;
      padding: 6px 12px;
      border: none;
      border: 1px solid #666;
      box-shadow: 0 0 15px #0003;
      background-color: transparent;
      border-radius: 4px;
      color: #eee;
  }
  ````
  
  > forma que de se herede 2 o tag las mismas propiedades


#### Propiedades de texto y fuente

| Tipo  | Propiedades      | Valores                         | Función                 |
| ----- | ---------------- | ------------------------------- | ----------------------- |
| text  | color            | rgb/rgba                        | color texto             |
|       | font-family      |                                 | tipografía              |
|       | font-size        | X px/X rem/X %                  | tamaño                  |
|       | font-weight      | bold/bolder                     | grosor                  |
|       | font-style       | italic/normal                   | estilo                  |
|       | text-align       | left/right/center/Justify       | alineación              |
|       | text-decoration  | underline/overline/line-through | subrayado               |
|       | line-height      | X px/X rem/X %                  | alto de la línea        |
|       | letter-spacing   | X px/X rem/X %                  | espacio entre letras    |
|       | text-transform   | uppercase/lowercase/capitalize  | formato                 |
|       | text-shadow      |                                 | sombra                  |
| color | background       | rgb/rgba/\#/                    | color del fondo         |
|       | background-color | rgb/rgba/\#/                    | color de fondo elemento |

#### Tipografías externas

-   Link:

    -   Alternativa A

    > `<head>`
    >
    > `<link rel="preconnect"> href="https://fonts.....">(Extraído de google fonts)`
    >
    > `<head>`

    > `Propiedades: font-family/font-weigth`

    -   Alternativa B

    `HTML: <link rel="preconnect"> href="fonts.css">`

    `(Definimos un valor para una nueva propiedad)`

    `CSS:(fonts.css)`

    > `@font-face{`
    >
    > `font-family:;`
    >
    > `src: url(dirección de la carpeta) format(truetype);`
    >
    > `font-weigth: #;`
    >
    > `}`

    > `(Definimos tantas como tipografías se tenga y usemos)`

-   Importar

    ````css
    @import url('https://fonts.googleapis.com/css2?family=Playwrite+PE:wght@100..400&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    ````

#### Icons

- link

- Importar

````css
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css");
````

> ❗ cada import (de las APIs que usemos) tienen un tiempo de demora. La pagina se pone pesada.

> por cada import que se realice se esta haciendo una peticion.

#### Modelo de caja (box model)

| Propiedades            | Valores  | Funciones                                                    |
| ---------------------- | -------- | ------------------------------------------------------------ |
| width                  | px/%/rem | ancho                                                        |
| height                 | px/%/rem | alto                                                         |
| max-height o max-width |          | valor máximo, la propiedad width o height no pueden ser mayores.- |
| min                    |          | iden.                                                        |

> Definir % es establecer una porción o total de la caja que lo contiene. Esta también se verá influenciada de la caja que lo contenga.

##### Estructura de una página WEB

- Elementos:

  - inline (en línea)
  - block (en bloque)

  | Elemento                                                     | inline | block | inline-bock |
  | ------------------------------------------------------------ | ------ | ----- | ----------- |
  | hx - p - div - ul - ol - main - aside - footer - header - section -nav ... |        | ❌     |             |
  | span - a - label - b - strong - i - em                       | ❌      |       |             |
  | img -button - iframe - textarea - audio - video - select - ... |        |       | ❌           |

  | Propiedades | block           | inline            | inline-bock |
  | ----------- | --------------- | ----------------- | ----------- |
  | width       | ✅ (modificable) | ❌ (no modif)      | ✅           |
  | height      | ✅               | ❌                 | ✅           |
  | margin      |                 | ❎ solo horizontal | ✅           |
  | padding     |                 | ❎ solo horizontal | ✅           |

  > alto y ancho modifican el contenido

  ````css
  span {
      display: inline-block;
   }
  ````

[El modelo de caja - Aprende desarrollo web | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/The_box_model)

![clipboard](https://i.imgur.com/EdeRxYG.png)

> La caja esta formada por el CONTENIDO - PADDING - BORDER. No así el
> MARGIN.

##### Relleno y Margen (padding and margin)

| Propiedades    | Valores  | Funciones                                           |
|----------------|----------|-----------------------------------------------------|
| padding        | X px/rem | (ShortHand) separa en los 4 sentidos misma cantidad |
| padding-top    | px/rem   | separa contenido con el border parte arriba         |
| padding-left   | px/rem   | separa contenido con el border parte izquierda      |
| padding-right  | px/rem   | separa contenido con el border parte derecha        |
| padding-bottom | px/rem   | separa contenido con el border parte de abajo       |

https://developer.mozilla.org/es/docs/Web/CSS/padding

> Shorthand: padding: top right botton left;

| Propiedades   | Valores  | Funciones                                           |
| ------------- | -------- | --------------------------------------------------- |
| margin        | X px/rem | (ShortHand) separa en los 4 sentidos misma cantidad |
|               | auto     | ajuste automatico en el centro                      |
| margin-top    | px/rem   | separa la caja de la parte arriba                   |
| margin-left   | px/rem   | separa la caja de la parte izquierda                |
| margin-right  | px/rem   | separa la caja de la parte derecha                  |
| margin-bottom | px/rem   | separa la caja de la parte de abajo                 |

https://developer.mozilla.org/es/docs/Web/CSS/margin

> Shorthand: margin: top right botton left;

> Margin collaps: toma el margen más grande. Esto sucede entre la
> combinación entre el margen top y bottom.
>
> 

<a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_box_model/Mastering_margin_collapsing" class="uri">https://developer.mozilla.org/en-US/docs/Web/CSS/CSS\_box\_model/Mastering\_margin\_collapsing</a>

##### Bordes

| Propiedades                | Valores                           | Función                      |
| -------------------------- | --------------------------------- | ---------------------------- |
| border                     |                                   |                              |
| border-width               | X px/rem                          | grosor                       |
| border-style               | solid/dashed/doblue/groove/hidden | tipo/estilo                  |
| border-color               | color/rgb/\#                      | color                        |
| border-radius              | X px/%                            | redondeo bordes              |
| border-top                 |                                   | bordes arriba                |
| border-left                |                                   | bordes izquierda             |
| border-bottom              |                                   | bordes abajo                 |
| border-right               |                                   | bordes derecha               |
| border-top-width           |                                   | grosor bordes arribo         |
| border-bottom-right-radius |                                   | redondeo borde abajo derecha |

https://developer.mozilla.org/es/docs/Web/CSS/border-top-left-radius

> Shorthand:
>
> -   **border: width style color;**
> -   **border: top right botton left;**
> -   border-top-width:...;
> -   border-bottom-right-radius:...;

> Existe un diferencia cuando se usa px o %. el redondeo por px solo lo
> realiza desde las equinas. el redondeo por % lo realiza desde su
> radio.

##### Tamaño de caja (box sizing)

| Propiedad  | Valores     | Funciones                                             |
| ---------- | ----------- | ----------------------------------------------------- |
| box-sizing | content-box | contenido fijo                                        |
|            | border-box  | contenido se adapta al valor de caja (width & leigth) |



https://developer.mozilla.org/es/docs/Web/CSS/box-sizing

![image-20240708075044034](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240708075044034.png)![image-20240708075058152](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240708075058152.png)

![image-20240708072515099](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240708072515099.png)![image-20240708072540117](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240708072540117.png)

> **content-box**
>
> Las propiedades [`width`](https://developer.mozilla.org/es/docs/Web/CSS/width) and [`height`](https://developer.mozilla.org/es/docs/Web/CSS/height) no incluyen el borde, relleno o margen. Por ejemplo, `.box {width: 350px; border: 10px solid black;}` despliega una caja con un ancho de 370 pixeles.

![image-20240708072631238](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240708072631238.png)![image-20240708072640237](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240708072640237.png)

> **border-box**
>
> Las propiedad de [`width`](https://developer.mozilla.org/es/docs/Web/CSS/width) y [`height`](https://developer.mozilla.org/es/docs/Web/CSS/height) incluyen el contenido, relleno y borde pero no incluyen el margén.  Tenga en cuenta que el relleno y borde estarán dentro de la caja. Por  ejemplo, `.box {width: 350px; border: 10px solid black;}` despliega una caja con un ancho de 350 pixeles.

#### Colores

https://developer.mozilla.org/es/docs/Web/CSS/color

| Tipos                                     | Formas                         |
| ----------------------------------------- | ------------------------------ |
| colores básico                            | red,blue,green,black,oragen... |
| rgb (RED GREEN BLUE)                      | rgb (0,255,125);               |
| rgba (con opacidad)                       | rgb (255,100,0,0 - 1)          |
| Hexadecimal                               | #00FF00                        |
|                                           | #7700FF 0-F                    |
| hsl (hue (rueda), saturacion, luminancia) | hsl (0-360,0-100%,0-100%)      |

> colores pastel: poca saturación | mucha luminancia

#### Unidades

https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Values_and_units

- Unidades fisicas: 

  - cm, in, px, etc. 

- Unidades absolutas:

  - px img(ancho y alto), tipografia, margen y padding

  ![image-20240708083129254](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240708083129254.png)

- Unidades relativas: (reposive design)

  - % se define nuestra caja con respecto a lo que lo contiene.

  ![image-20240708083219590](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240708083219590.png)

- Tamaño fuente, espaciado o tipografia gral. em y rem.

  > nota: si no se tuviera definido al elemento padre, el contenido buscaría mas arriba.

- Layout y dimension de elementos em, rem, %, vw y vh. (diseño responsible). 

- para evitar tener scroll podemos definir los viewport height y width (vh, vw) que delimitaria la pantalla

  

#### Fondos, Gradientes y Sombras

##### Fondos (Background)

  - background: 
    - (parametros) [ url position / size repeat attachment color]

  - (propiedad) background-size: 
    - (valor) contain; obliga al contenedor que la imagen entre por lo menos una vez de manera entera.
    - (valor) cover; obliga que se ajuste a la resolucion y no tanto al tamaño.
  - background-position: 
    - center; left; rigth; top; estable una posicion a la imagen
  - background-repeat: 
    - no-repeat; no repite laimagen en la caja, se puede apreciar el fondo.
  - background-attachment: 
    - fixed; mien tras hago scroll la imagen se desplaza

##### Gradientes

  - background:
    - (funcion) linear-gradient(direcion, color1, color2, color...) ; gradiente linea. Transparent x%
    - radial-gradient();
    - conic-gradient();
    
    

  ##### Sombras

[box-shadow - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/box-shadow)

  - box-shadow: para las cajas
    - (parametro) : right bottom desenfoque expansion color; 
    
  - text-shadow: par el texto

  - filter : drop-shadow(); para imagenes *.png 

    > box-shadow: horizontal vertical difuminado color;
    >
    > valor: inset
    
    [Box Shadow CSS Generator](https://cssgenerator.org/box-shadow-css-generator.html#google_vignette)
    
    [Neumorphism/Soft UI CSS shadow generator](https://neumorphism.io/#e1dfdf)

#### Position

> Complementa a flex-box

[position - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/position)

##### Static

El elemento es posicionado de acuerdo al flujo normal del documento. Las propiedades [`top`](https://developer.mozilla.org/es/docs/Web/CSS/top), [`right`](https://developer.mozilla.org/es/docs/Web/CSS/right), [`bottom`](https://developer.mozilla.org/es/docs/Web/CSS/bottom), [`left`](https://developer.mozilla.org/es/docs/Web/CSS/left), and [`z-index`](https://developer.mozilla.org/es/docs/Web/CSS/z-index) *no tienen efecto*. Este es el valor por defecto.

**Desactivado:** Position:static; (Por defecto) 

**Activo:** position: relative/absolute/sticky/fixed;

| Propiedades | Funciones                            |
| :---------- | :----------------------------------- |
| top         | (vale mas que bottom, más prioridad) |
| bottom      |                                      |
| left        | (vale mas que right, más prioridad)  |
| right       |                                      |

| Propiedades              | Valores      | Función                                                      |
| ------------------------ | ------------ | ------------------------------------------------------------ |
| Position                 | static       |                                                              |
|                          | relative     | (tiene mas prioridad que static)                             |
|                          | absolute     | ()                                                           |
|                          | sticky       |                                                              |
|                          | fixed        |                                                              |
| top, left, bottom, right | px, rem, ... | Desplazamiento                                               |
| z-index                  | # capa       | Orden de posicionamiento de superposicion, tanto para relative, static... |

##### Relative

El elemento es posicionado de acuerdo al flujo normal del documento, y luego es desplazado *con relación a sí mismo*, con base en los valores de `top`, `right`, `bottom`, and `left`. El desplazamiento no afecta la posición de ningún otro elemento; por lo que, el espacio que se le da al elemento en el esquema de la página es el mismo como si la posición fuera `static`. Este valor crea un nuevo [contexto de apilamiento](https://developer.mozilla.org/es/docs/Web/CSS/CSS_positioned_layout/Understanding_z-index/Stacking_context), donde el valor de `z-index` no es `auto`.

````css
position: relative;
top: 40px; left: 40px;
````

![image-20240711094207245](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240711094207245.png)

Aquellos que tengan position static se encontraran detrás de los que tengan position relative.

Recomendación:

> **Usar bottom o top❗**
>
> **Usar left o rigth❗**
>
> no usar al mismo tiempo ya que elque tiene menos prioridad no afecta al code y prevalece el de mas prioridad, reemplazar con valores negativos.

````css
.hijo:nth-child(2){
    background-color: red;
    position: relative;
    top: 10px;
    left: 10%;
}
````

![image-20240722112146270](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240722112146270.png)

````css
.hijo:nth-child(2){
    background-color: red;
    position: relative;
    top: -10px;
    left: -10%;
}
````

![image-20240722112119888](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240722112119888.png)

````css
.hijo:nth-child(1){
    background-color: aqua;
    position: relative;
}
.hijo:nth-child(2){
    background-color: red;
    position: relative;
    right: 50px;
    top: 50px;
}
.hijo:nth-child(3){
    background-color: blueviolet;
    position: relative;
    right: 100px;
    top: 100px;
}
````

![image-20240723171517235](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723171517235.png)

> ❗ cuando todos sean relativos el orden del html define la superposicion de uno sobre el otro.
>
> para evitar este tipo de prioridad o orden se puede recurrir a la propiedad **z-index**.

````css
.hijo:nth-child(2){
    background-color: red;
    position: relative;
    left: 100px;
    bottom: -100px;
    z-index: 2;
}
.hijo:nth-child(3){
    background-color: blueviolet;
    position: relative;
    z-index: 1;
}
````

![image-20240723180021113](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723180021113.png)

> segun html el hijo3 tiene mas prioridad que el 2, pero el uso de z-index se cambia el orden de superposicion.

> z-index no acepta valores negativos, pero si se usa queda el elemento detras del body

![image-20240711114034320](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240711114034320.png)

##### Absolute

El elemento es removido del flujo normal del documento, sin crearse espacio alguno para el elemento en el esquema de la página. Es posicionado relativo a su ancestro posicionado más cercano, si lo hay; de lo contrario, se ubica relativo al [bloque contenedor](https://developer.mozilla.org/en-US/docs/Web/CSS/Containing_block) inicial. Su posición final está determinada por los valores de `top`, `right`, `bottom`, y `left`.

Este valor crea un nuevo [contexto de apilamiento](https://developer.mozilla.org/es/docs/Web/CSS/CSS_positioned_layout/Understanding_z-index/Stacking_context) cuando el valor de `z-index` no es `auto`. Elementos absolutamente posicionados pueden tener margen, y no colapsan con ningún otro margen.

````css
position: absolute;
top: 40px; left: 40px;
````

![image-20240711093733754](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240711093733754.png)

````css
.hijo:nth-child(1){
    background-color: aqua;
}
.hijo:nth-child(2){
    background-color: red;
}
.hijo:nth-child(3){
    background-color: blueviolet;
    position: absolute;
}
````

![image-20240723183422746](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723183422746.png)

````css
.padre{
    width: 100vw;
    height: 100vh;
    background-color: greenyellow;
    display: flex;
    justify-content: start;
    align-items: start;
    margin-top: 25vh;
}
.hijo:nth-child(1){
    background-color: aqua;
}
.hijo:nth-child(2){
    background-color: red;
}
.hijo:nth-child(3){
    background-color: blueviolet;
    position: absolute;
    top: 0;
    left: 0;
}
````

![image-20240723184056821](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723184056821.png)

> se puede observar que pierde todas las propiedades del *padre mas cercano con position static*, incluido la propiedad flexbox.
>
> pasa a ser hijo del antecesor a su padre (body,html,...)

````css
.hijo:nth-child(3){
    background-color: blueviolet;
    position: absolute;
    top: 10px;
    left: 0;
}
````

![image-20240723190328767](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723190328767.png)

cuando el padre tiene position distinto a static, su hijo se posiciona sobre este.

![image-20240723191151252](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723191151252.png)

##### Combinacion de flexbox-position

![image-20240723203203742](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723203203742.png)

````css
header .search-container {
    width: 500px;
    font-size: 15px;
    border: none;
    display: flex;
    align-items: center;
    position: relative;
}
header .search-container button {
    position: absolute;
    right: 0;
}
````

> contenedor (padre): position relative + display flex
>
> button (hijo): position absolute s/top c/left (centrado a la derecha sin movimiento vertical)

![image-20240723205532633](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723205532633.png)

````css
header .search-container button {
    position: absolute;
    right: 0;
    /* centrado don flexbox*/    
    display: flex;
    justify-content: center;
    align-items: center;
    /* ajuste tamaño*/
    width: 40px;    /* padding: 0 10px; */
    height: 70%;/*de la altura total toma el 70% de la caja */
    /* apariencia del button*/
    background-color: transparent;
    border: none;
    border-left: 1px solid #e6e6e6;
    color: #e6e6e6;
}
````

##### Fixed

El elemento es removido del flujo normal del documento, sin crearse espacio alguno para el elemento en el esquema de la página. Es posicionado con relación al [bloque contenedor](https://developer.mozilla.org/en-US/docs/Web/CSS/Containing_block) inicial establecido por el [viewport](https://developer.mozilla.org/es/docs/Glossary/Viewport), excepto cuando uno de sus ancestros tiene una propiedad `transform`, `perspective`, o `filter` establecida en algo que no sea `none` (ver [CSS Transforms Spec](https://www.w3.org/TR/css-transforms-1/#propdef-transform)), en cuyo caso ese ancestro se comporta como el bloque contenedor. (Notar que hay inconsistencias del navegador con `perspective` y `filter` contribuyendo a la formación del bloque contenedor.) Su posición final es determinada por los valores de `top`, `right`, `bottom`, y `left`.

Estos valores siempre crean un nuevo [contexto de apilamiento](https://developer.mozilla.org/es/docs/Web/CSS/CSS_positioned_layout/Understanding_z-index/Stacking_context). En documentos impresos, el elemento se coloca en la misma posición en *cada página*.

![image-20240723212754465](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723212754465.png)

````css
position: sticky;
top: 20px;
````



![image-20240723212556230](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240723212556230.png)

````css
body {
    height: 500vh;
}
header {
    background-color: #fee600;
    padding: 40px 20px;
    position: fixed;
    width: 100%;
}
````

> El buscador permanece fijo apesar de realizar scroll

#### Overflow (excedente)

[overflow (excedente) - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/overflow)

| Propiedad | Valores | Función                                |
| --------- | ------- | -------------------------------------- |
| Overflow  | visible | no recorta contenido. c/barra scroll.  |
|           | hidden  | recorta (oculta), s/barra de posición. |
|           | scroll  | recorta, c/barra de posición.          |
|           | auto    | depende del usuario.                   |

<img src="C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240810084957540.png" alt="image-20240810084957540" style="zoom:50%;" /> S/overflow: hidden; Sobre sale el video.

<img src="C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240810085112411.png" alt="image-20240810085112411" style="zoom:75%;" /> C/overflow: hidden; Recorto el video que se sobre salia.



---

## HTML AVANZADO

#### Metatags, Comentarios e Iconos

````html
<!-- COMENTARIOS -->
<body>
    <!-- Elementos Heading -->
    <h1>Titulo</h1>
    <h2>Subtitulos</h2>
    <!-- <h3>Subtitulos</h3> -->
</body>
````

![image-20240713110542861](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240713110542861.png)

````html
<head>
    <link rel="icon" href="/img/mi-foto-(32x32)px.jpg" type="icon/jpg">
    <!-- favicon -->
    <title>iMAGENES</title>
</head>
````

> Iconos en pestañas (favicons) : (32 x 32) px (64 x 64)px

````html
<head>
    <meta charset="UTF-8">
    <!-- viewport:contenido adaptado a todo dispositivo -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="descripcion de la pagina (+/- 100 caracteres)">
    <!-- Mejora el posicionamiento pagina web-->
    <meta name="keywords" content="(palabras claves:dev,desarrollador,ux,ui,etc)">
    <meta name="author" content="Carlos A Ribas">
    <meta name="OG: TITLE" content="titulo">
    <meta name="OG: IMAGE" content="imagen.png">
    <meta name="OG: descripcion" content="descripcion">
    <meta name="OG: url" content="127.0.0.1:5000/index.html">
    <!--Anti SEO-->
    <meta name="robots" content="noflow/nosnippet/noarchive/noimageindex"> 
<!--(no ingresar pag. motores de busqueda/no mostrar fragmento en mb/no guarde en cache/no se indexan las imagnes)-->
</head>
````


> Metatags: info seo, accesiblidad,etc.

#### Textarea

````html
<textarea name="" id="" cols="30" rows="10">Textarea</textarea>
````

> el Textarea tiene predefinido 100

| Propiedades | Valores  | Funciones                           |
| ----------- | -------- | ----------------------------------- |
| min-width   | 100%     |                                     |
| min-height  | px/rem   | Textarea tiene una altura min fija  |
| max-height  | px/rem   | Textarea tiene una altura max fija  |
| resize      | both     | desplazarse en eje x e y            |
|             | vertical | desplazarse eje y                   |
|             | none     | no hay desplazamiento de la ventana |
| form-sizing | content  | la ventana se ajusta al contenido   |
| font-family |          |                                     |

| Atributo    | Valores             | Funciones                                                    |
| ----------- | ------------------- | ------------------------------------------------------------ |
| placeholder | "Texto..."          |                                                              |
| required    | s/valor (booleanos) |                                                              |
| disabled    | s/valor (booleanos) | Texto fijo predefinido, nose puede sobreescribir ni borrar. (**NO** permite hacer **focus** y enviar el dato) |
| readonly    | s/valor (booleanos) | Texto fijo predefinido, nose puede sobreescribir ni borrar. (permite hacer **focus** y enviar el dato) |
| maxlength   | #                   | cantidad de caracteres predefinidos                          |
| cols        | #                   | cantidad de columnas                                         |
| row         | #                   | cantidad de filas. (># se activa el scroll)                  |

> los valores booleanos si estan es true, sino se los escribe son false.

#### Labels

| Atributo | Valores | Funciones       |
| -------- | ------- | --------------- |
| for      | text    | enlaza elemento |

> id(input) = for(lebel) esto permite que al clickear el texto (label) hace focu en el input (enlazar)

````html
/*Formas de enlazar*/
<div class="form_input">
	<label for="nombre">Nombre Completo</label>
    <input id="nombre" type="text"  placeholder="Jhon Doe">
</div>
/*Sin conectar for con id*/
<div class="form_input">
	<label for="email">Email
    	<input type="email" placeholder="ejemplo@outlook.com">
	</label>
</div>
````

> buscar que los textos del label no sean reduntante con el placeholder del imput

#### Select, Datalist y Option

Select tipo de campo de entrada permite seleccionar una option. Aspecto de barra desplegable.

| Atributo | Valores | Funciones                              |
| -------- | ------- | -------------------------------------- |
| value    | text    | valor que recibe el usuario. (Backend) |

> en css option solo tiene propiedad color y background-color.

````html
<!-- Select & Option -->
            <div class="form_input">
                <label for="asunto">Asunto
                    <select name="type-of-user" id="">
                        <option value="">Selecciona tu país</option>
                        <option value="user1">Argentina</option>
                        <option value="user2">Brasil</option>
                        <option value="user3">Chile</option>
                    </select>
                </label>
            </div>
````

Datalist es un input que selecciona las option que marcamos.

| Atributo | Valores | Funciones |
| -------- | ------- | --------- |
|          |         |           |

````html
<!-- Datalist & Option -->
            <div class="form_input">
                <label for="asunto">Asunto
                    <input list="reference" name="type-of-user">
                    <datalist  name="type-of-user" id="reference">
                        <option value="user0">Selecciona tu país</option>
                        <option value="user1">Argentina</option>
                        <option value="user2">Brasil</option>
                        <option value="user3">Chile</option>
                    </datalist>
                </label>
            </div>
````

#### Fieldset y Legend

[fieldset - HTML: Lenguaje de etiquetas de hipertexto | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/HTML/Element/fieldset)

El elemento *fieldset* (grupo de campos) permite organizar en grupos los campos de un formulario.

````html
<form action="">
        <fieldset>
            <legend>Información Básica</legend>
            <input type="text" placeholder="Nombre">
            <input type="text"  placeholder="Apellido">
            <input type="number" placeholder="Edad">
        </fieldset>
        <fieldset>
            <legend>Información de Contacto</legend>
            <input type="email" placeholder="Email">
            <input type="text" placeholder="Telefono">
        </fieldset>
    </form>
````

#### Details y Summary

Summary es elemento que titularia la etiqueta.

Details  seria el elemento que representa el desglose de un contenido, lista, etc....

````html
<details>
	<Summary>Details y Summary</Summary>
    <ul>
    	<li>pensar que comer</li>
    	<li>ver heladera</li>
    	<li>cocinar💥💥</li>
	</ul>
</details>
````

[<details>: The Details disclosure element - HTML: HyperText Markup Language | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details)

#### Enlaces (Avanzado)

| Atributos | Tipo                         | Función                                                      |
| --------- | ---------------------------- | ------------------------------------------------------------ |
| href      | #*enlace-elemento*           | enlace de elementos                                          |
|           | "mailto:*namemail@mail.com"* | inicia un mail                                               |
|           | "tel:+542991234567"          |                                                              |
| download  |                              | descarga lo que indique href                                 |
| target    | _blank                       | abre otra ventana hija. ❗                                    |
| rel       | noopener                     | Evita que se tenga acceso a windw.opener. Evitamos redireccionamiento malicioso. |
|           | noreferrer                   | Evita acceso al objeto window.opener y encabezados (pagina padre) |
|           | nofollow                     | Evita que los motores de busqueda le den seguimiento.        |

````css
<div>
	<a href="#buy-process">Ir a Proceso de Compra</a>
</div>
<div>
	<a href="#privacy">Politica de privacidad</a>
</div>
<div>
    <a href="terms.html" download>Descargar Terminos y Condiciones</a>
</div>
<div>
	Inverti en: 
    <a href="binance.com" target="_blank" rel="noopener norereferrer nofollow">Binance.com</a>
</div>
...
<h2 id="privacy">3. Politica</h2>
<h2 id="buy-process">4. Proceso de compra</h2>

````

> Permite vincular/enlazar elemento en disitintos puntos de la página web.

>❗ window.opener () el acceso a una ventana hija. ya que la nueva pagina tiene acceso a la ventana original a traves de window.opener. Consecuencias:
>
>- **Reverse Tabnabbing**
>- **Ejecutar JavaScript Malicioso**
>
>Mitiga riesgo. Evita que la nueva página tenga acceso a window.opener, protege a la página original.

#### Tablas

````html
<table cellspasing><!--Tabla-->
        <thead>
            <tr>
                <th>Fila 1</th>
                <th>Fila 2</th>
                <th>Fila 3</th>
            </tr>
        </thead>
</table>        
````

Dentro de la etiqueta table se configura

| Etiqueta | Tipo                                 | Función |
| -------- | ------------------------------------ | ------- |
| table    | representacion de elementos de tabla | tabla   |
| thead    | elemento de encabezado               | bloque  |
| tbody    | elemento de cuerpo                   | bloque  |
| tfoot    | elelmento de pie                     | bloque  |
| th       | elemento representa una columna      |         |
| tr       | elemento representa una fila         |         |
| td       | elemento representa in dato          |         |

| Atributos | Tipo | Funcion       |
| --------- | ---- | ------------- |
| colspan   | #    | Combina #dato |

#### Audio y Video



#### Lazy Loading

#### HTML Obsoleto

#### HTML Semántico

#### Accesibilidad WEB

-----

## CSS AVANZADO

#### Padres e Hijos

##### Pseudoclase: 

nth-child(#) llama de manera especifica a una clase hijo. dependiendo la posicion que tenga el hijo #.

````html
<div class="padre">
        <div class="hijo"></div>
        <div class="hijo"></div>
        <div class="hijo">
            
````

dependiendo la posicion que tenga el hijo #.

````css
.hijo:nth-child(#){
    background-color:blue ;
}
````

#### Pseudo Selectores

Los **pseudoselectores** y **pseudoelementos** son parte importante de CSS y nos permiten seleccionar elementos en estados específicos o agregar contenido adicional a los elementos. Aquí tienes algunos ejemplos:

1. **Pseudoclases**:

   - `:hover`: Se aplica cuando el cursor está sobre un elemento.

     ````css
     a:hover {
       color: blue;
       text-decoration: underline;
     }
     ````

   - `:first-child`: Selecciona el primer hijo de un elemento.

     ````css
     ul li:first-child {
       font-weight: bold;
     }
     ````

   - `:last-child`: Selecciona el último hijo de un elemento.

     ````css
     ul li:last-child {
       font-style: italic;
     }
     ````

   - `:nth-child(n)`: Selecciona el enésimo hijo de un elemento (por ejemplo, `:nth-child(2)` selecciona el segundo hijo).

     ````css
     li:nth-child(odd) {
       background-color: #f5f5f5;
     }
     ````

   - `:not(selector)`: Excluye elementos que coinciden con el selector especificado.

     ````css
     p:not(.important) {
       opacity: 0.8;
     }
     ````

   - `:focus`: Selecciona un elemento cuando está enfocado (por ejemplo, cuando se hace clic en él o se navega a él mediante el teclado).

     ````css
     input:focus {
       border: 2px solid #0078d4;
     }
     ````

   - `:focus-within`: Selecciona un elemento cuando alguno de sus descendientes está enfocado.

     ````css
     form:focus-within {
       border: 1px solid #ddd;
     }
     ````

   - `:focus-visible`: Se aplica cuando el elemento es enfocado por el usuario de manera visible (útil para mejorar la accesibilidad).

     ````css
     button:focus-visible {
       outline: 2px solid #4caf50;
     }
     ````

   - `:active`: Se aplica cuando el usuario interactúa con un elemento (por ejemplo, al hacer clic en un enlace).

     ````css
     button:active {
       background-color: #ff5722;
     }
     ````

   - `:visited`: Selecciona enlaces visitados.

     ````css
     a:visited {
       color: purple;
     }
     ````

   - `:target`: Selecciona un elemento que es el destino de una URL de anclaje (por ejemplo, `#sección`).

     ````css
     #section1:target {
       background-color: #ffeeba;
     }
     ````

2. **Pseudoelementos**:

   - `::before` y `::after`: Agregan contenido antes o después del contenido real de un elemento.

     ````css
     .quote::before {
       content: "“";
     }
     ````

   - `::first-line`: Selecciona la primera línea de un bloque de texto.

     ````css
     p::first-line {
       font-weight: bold;
     }
     ````

   - `::first-letter`: Selecciona la primera letra de un elemento de texto.

     ````css
     h1::first-letter {
       font-size: 2em;
     }
     ````

[Por ejemplo, si quieres aplicar estilos al primer párrafo de un artículo, puedes usar `:first-child` en lugar de añadir una clase específica](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Selectors/Pseudo-classes_and_pseudo-elements)

#### Display FlexBox

- Tecnología **unidimensional**, eje X o Y.

- display : flex; se coloca en el elemento **PADRE**.

  - ❗ configuraciones (propiedades) por defecto:
    - flex-direction: row;
    - justify-content: flex-star;
    - flex-wrap: none;

- en el padre determino todas las alineaciones del hijo.

  [display - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/display)

  [Conceptos Básicos de flexbox - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox)
  
  [flex - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/flex)
  
  
  
  **Activo:** display:flex;

| Propiedad                    | Valores       | Funciones                                            |
| ---------------------------- | ------------- | ---------------------------------------------------- |
| display                      | flex          | Activamos sus propiedades                            |
| flex-direction               | row / column  | Alinea los elementos en el Eje x / Eje y             |
| **justify-content (row)**    |               | **ajuste de contenido sobre eje x**                  |
|                              | center        | elementos centro                                     |
|                              | flex-end      | elementos al final (ajuste derecha)                  |
|                              | flex-star     | elementos al inicio (ajuste izquierda)               |
|                              | space-between | espaciado max entre los hijos                        |
|                              | space-evenly  | espaciado max alrededor de los hijos                 |
|                              | space-around  | espaciado max entre hijo y y min fuera de los hijos. |
| **aling-items (row)**        |               | **alinea contenido sobre eje y**                     |
|                              | center        | elementos centrados                                  |
|                              |               |                                                      |
| j**ustify-content (column)** |               | **ajuste de contenido sobre eje y**                  |
| **aling-items (column)**     |               | **alinea contenido sobre eje x**                     |
| flex-wrap                    | nowrap / wrap | hijo en 1 linea/ en + lineas                         |
| gap                          | px /          | espaciado entre hijos.                               |
| row-gap                      |               | espaciado entre filas                                |
| column-gap                   |               | espaciado entre columnas                             |
| flex (Solo para hijos)       |               | fraccion del flex (padre)                            |
| order (Solo para hijos)      |               | orden de los hijos                                   |

> si se modifica la ventana de la pantalla el **gap** no se modifica solo los hijos de manera equitativa.
>
> factor de crecimiento. padre mantiene tamaño, los que se modifican los hijos.

>*Cuando haya un cambio de direccion de row a column (o visceversa) debe generarse un contenedor padre (otro flex)*

[justify-content - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/justify-content)

[align-items - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/align-items)

````css
.padre {
    background-color: greenyellow;
    height: 100vh;
    width: 100vw;
    display: flex;
    gap: 15px;
    flex-direction: row;
    <!-- estas dos propiedades centra el elemento en pantalla-->
    align-items: center;
    justify-content: center;
}
````

#### Display Block

[display - CSS | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/CSS/display)

````css
video {
	display: block; /*Toma todo el ancho disponible de la pantalla*/
	width: 100%; /*Se ajusta a la padre*/
}
````



----

## JavaScript

````html
/*dos alternativas para cargar script*/

/*script en head*/
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script async src="./script.js" defer></script>
    <script src="./script.js" defer></script>
    <script async>
</head>
/*script en body*/
<body>
    /*escribir code al final script*/
    <script src="./script.js"></script>
</body>
````

####   Tipos de Datos

> Nos permite ver el tipo de dato: typeof(nombre)

| Tipos     | Formas                                       | Funcion   |
| --------- | -------------------------------------------- | --------- |
| String    | 'tipo1' "tipo2" ´tipo3´  `tipo4`             |           |
| Number    | 1, 2, 5.2, -10, Infinity, NaN (Not a Number) |           |
| Booleans  | true, false                                  |           |
| Null      |                                              | exception |
| Undefined |                                              |           |

**![image-20240729120531655](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240729120531655.png)**

#### Truthy y Falsy

https://developer.mozilla.org/en-US/docs/Glossary/Truthy

| Falsy     |
| --------- |
| false     |
| 0         |
| -0        |
| null      |
| undefined |
| NaN       |
| ' '       |

> todos los valores distintos a los mencionados al Falsy son Truthy

#### Operadores Aritméticos

| Tipo       | Funcion        |
| ---------- | -------------- |
| + (string) | Concatenacion  |
| + (number) | Suma           |
| - (number) | Resta          |
| * (number) | Multiplicacion |
| / (number) | Division       |
| % (number) | Resto          |

> /* Operadores artitmeticos */
> /* 
> +: Concatenacion 
> La concatenacion ocurre cuando HAY un string o mas en una operacion
> Pasa el dato distinto de string a string y los une
> Devuelve SIEMPRE un string
> +: Suma
> La suma ocurre cuando NO hay string en una operacion
> Pasa el dato distinto de numero a numero
> Devuelve siempre NUMBER
> \- Resta
> Pasa el dato distinto de numero a numero
> Devuelve siempre NUMBER
> \* Multiplicacion
> Pasa el dato distinto de numero a numero
> Devuelve siempre NUMBER
> / Division
> Pasa el dato distinto de numero a numero
> Devuelve siempre NUMBER
> % modulo/resto de la division
> Pasa el dato distinto de numero a numero
> Devuelve siempre NUMBER
>
> REGLAS:
> Cualquier dato operado con NaN exepto la concatenacion da como resultado un NaN
> */

#### Comparadores

> siempre devuelven booleanos

| Tipos | Funciones                                           |
| ----- | --------------------------------------------------- |
| ==    | igualdad (compara solo valores)                     |
| ===   | estricta igualdad (compara valor y  tipo de dato) ✅ |
| !=    | diferencia (entre valores)                          |
| !==   | estricta diferencia ✅                               |
| >     | mayor                                               |
| <     | menor                                               |
| >=    | mayor igual                                         |
| <=    | menor igual                                         |

#### Operadores Logicos

| Tipos | Funciones                                                    |
| ----- | ------------------------------------------------------------ |
| !     | negacion                                                     |
| \|\|  | or (verdadero devuelve el primer valor/ falso devuelve el segundo valor) |
| &&    | and (verdadero devuelve el segundo valor/ falso devuelve el primer valor) |

#### Variables

| Tipos | Funciones                                                    |
| ----- | ------------------------------------------------------------ |
| var   | Declarar, Asignar c/valor y s/valor (se puede redeclarar)    |
| let   | Declarar, Asignar c/valor y s/valor (NO se puede redeclarar) |
| const | Declarar, Asignar c/valor (NO se puede redeclarar)           |

![image-20240731112631035](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240731112631035.png)

![image-20240731112533791](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240731112533791.png)

![image-20240731114047578](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240731114047578.png)

#### alert() y prompt()



#### Condiciones

#### Ambitos



