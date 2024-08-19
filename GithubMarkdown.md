[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=35&pause=500&random=false&width=435&lines=Curso+de+Full+Stack;Dev+Charlybio87)](https://git.io/typing-svg)

------

# HTML

## Esquema de HTML
![image](https://github.com/Charlybio87/CursoDFullStack/assets/142097962/a91a2c95-d937-4cc9-9719-7c7c2f3dae2b)

#### <i>Nuevas etiquetas HTML5
> \<section>: Define una sección en un documento.
>
> \<nav>: Define un bloque que contiene enlaces de navegación, como por ejemplo el menú.
>
> \<article>: Define contenido autónomo que podría existir independientemente del resto del contenido.
>
> \<aside>: Define contenidos vagamente relacionados con el resto del contenido de la página.
>
> \<main>: Define el contenido principal o importante en el documento. Solamente existe un elemento \<main> en el documento.
>
> \<header>:  Define la cabecera de una página o sección.
>
> \<footer>:  Define el pie de una página o sección.
>

### Atajos:
ctrl + shif + p --> nos permite escribir o seleccionar el comando. (CMDG)

alt + z o entro CMDG --> Toggle Word Wrap, ajuste de la lineas en ventana.

ctrl + D --> nos permite escribir en varios lugares a la vez donde se repita el caracter seleccionado.

### Atajos Codigos:
h$*6 --> me crea 6 elementos de h del 1 al 6. (Emmet, escribir mas rápido)

#### RECURSOS:
<b><https://www.youtube.com/watch?v=ELSm-G201Ls&t=2705s></b>
* Parrafos y encabezados: <https://www.youtube.com/watch?v=ELSm-G201Ls&t=3118s>

#### Temas claves:
- 
##### NOTAS: 
* Cuando estemos manejando con *RUTAS RELATIVAS* las carpetas deben estar presente en el servidor.
* Accesibilidad para paginas web.
* modificaciones en el Visual hacerlo en el settings.json. CMDG --> preferences: Open User Setting



------


# CSS
Hoja de estilo en cascada.
#### Selectores
- elementos: <ul>   <il>   <h1> (selecciona a todos los mismos elementos) 
- .clase: <contenedor> <heading> (varios elementos en la misma pagina)
- #id: (solo un elemento en toda la pagina)

#### Tipografia
- tipografia preestablecida

- tipografia externa (google fonts) pego link al head

- tipografia externa configurable creo carpeta fonts.css

#### Box Model (Modelo de Caja)
- Propiedades: Content (contenido), Padding (relleno), Border (borde) y Margin (margen). El margin no forma parte de la caja.
- border-radius son diferente cuando se usan en px (redondea las esquinas) y % (radio en X y radio en Y, en relacion con el contenedor). ej.  border-bottom: 1*px* solid greenyellow;

#### Tamaño de caja (box sizing)
- se fija tamaño de contenido o borde, entonces, el resto se ira ajustando sin modificar lo fijado.
  ej.
  box-sizing: content-box; /*fijo el tamaño del contenido (100x100px)/
  box-sizing: border-box;  /*fijo el tamaño box (100x100)px/

#### Color
- RGB: (0,128,256); #0077FF; #07F;(menos exacto) 

- RGBA: #FFFF; (ultimo digito: Opacidad)

- HSl (hue, saturation,lightness): hlsa()

  > Fondo: Claro --> Texto: Oscuro.
  >
  > Fondo: Oscuro --> Texto: Claro.

#### Unidades de Medidas
- Unidades fisicas: 
  - cm, in, px, etc. 

- Unidades absolutas:
  - px img(ancho y alto), tipografia, margen y padding

- Unidades relativas: (reposive design)
  - % se define nuestra caja con respecto a lo que lo contiene.
  - em tomo de referencia al elemento padre
  - rem tomo al elemento raiz (html)
  - vw ancho disponible en la ventana. 
  - vh alto disponible en la ventana.
- Tamaño fuente, espaciado o tipografia gral. em y rem.
- Layout y dimension de elementos em, rem, %, vw y vh. (diseño responsible). 

> nota: si no se tuviera definido al elemento padre, el contenido buscaría mas arriba.

#### Fondos (BACKGROUND)

- background: 
  - (parametros) [ url position / size repeat attachment color]

- (propiedad) background-size: 
  - (valor) contain; obliga al contenedor que la imagen entre por lo menos una vez de manera entera.
  - (valor) cover; obliga que se ajuste a la resolucion y no tanto al tamaño.
- background-position: 
  - center; left; rigth; top; estable una posicion a la imagen
-  background-repeat: 
  - no-repeat; no repite laimagen en la caja, sepuede apreciar el fondo.
-  background-attachment: 
  - fixed; mien tras hago scroll la imagen se desplaza

#### Gradientes
- background:
  - (funcion) linear-gradient(direcion, color1, color2, color...) ; gradiente linea. Transparent x%
  - radial-gradient();
  - conic-gradient();

#### Sombras
- box-shadow: para las cajas
  - (parametro) : right bottom desenfoque expansion color; 
- text-shadow: par el texto
- filter : drop-shadow(); para imagenes *.png 

------

### Curso Completo HTML y CSS: (Prop. Soy Dalton)   😎

#### <u>TEMARIO:</u>  

[00:00](https://www.youtube.com/watch?v=ELSm-G201Ls&t=0s) - Introducción [02:35](https://www.youtube.com/watch?v=ELSm-G201Ls&t=155s) - Entendiendo la WEB [13:38](https://www.youtube.com/watch?v=ELSm-G201Ls&t=818s) - Entendiendo HTML y CSS [26:10](https://www.youtube.com/watch?v=ELSm-G201Ls&t=1570s) - Editor de código 

~~--- HTML BÁSICO ---~~ [35:02](https://www.youtube.com/watch?v=ELSm-G201Ls&t=2102s) - Estructura de una etiqueta [45:48](https://www.youtube.com/watch?v=ELSm-G201Ls&t=2748s) - Estructura de una página WEB [51:58](https://www.youtube.com/watch?v=ELSm-G201Ls&t=3118s) - Párrafos y encabezados [1:00:09](https://www.youtube.com/watch?v=ELSm-G201Ls&t=3609s) - Listas [1:10:45](https://www.youtube.com/watch?v=ELSm-G201Ls&t=4245s) - Enlaces (Básico) [1:26:09](https://www.youtube.com/watch?v=ELSm-G201Ls&t=5169s) - Imágenes y Rutas [1:41:40](https://www.youtube.com/watch?v=ELSm-G201Ls&t=6100s) - Formularios 

~~--- CSS BÁSICO ---~~ [1:56:45](https://www.youtube.com/watch?v=ELSm-G201Ls&t=7005s) - Introducción a CSS [2:08:24](https://www.youtube.com/watch?v=ELSm-G201Ls&t=7704s) - Selectores (Básico) [2:18:04](https://www.youtube.com/watch?v=ELSm-G201Ls&t=8284s) - Propiedades de texto y fuente [2:44:56](https://www.youtube.com/watch?v=ELSm-G201Ls&t=9896s) - Tipografías externas [2:55:25](https://www.youtube.com/watch?v=ELSm-G201Ls&t=10525s) - Modelo de caja (box model) [3:07:04](https://www.youtube.com/watch?v=ELSm-G201Ls&t=11224s) - Relleno y Margen (margin y padding) [3:37:57](https://www.youtube.com/watch?v=ELSm-G201Ls&t=13077s) - Bordes [3:53:43](https://www.youtube.com/watch?v=ELSm-G201Ls&t=14023s) - Tamaño de caja (box sizing) [4:02:09](https://www.youtube.com/watch?v=ELSm-G201Ls&t=14529s) - Colores [4:25:16](https://www.youtube.com/watch?v=ELSm-G201Ls&t=15916s) - Unidades [4:50:29](https://www.youtube.com/watch?v=ELSm-G201Ls&t=17429s) - Fondos, Gradientes y Sombras [5:31:15](https://www.youtube.com/watch?v=ELSm-G201Ls&t=19875s) - Ejercicio práctico 

~~--- HTML AVANZADO ---~~ [5:38:02](https://www.youtube.com/watch?v=ELSm-G201Ls&t=20282s) - Metatags, Comentarios e Iconos [5:57:18](https://www.youtube.com/watch?v=ELSm-G201Ls&t=21438s) - Textarea y Labels [6:24:18](https://www.youtube.com/watch?v=ELSm-G201Ls&t=23058s) - Select, Datalist y Option [6:33:02](https://www.youtube.com/watch?v=ELSm-G201Ls&t=23582s) - Fieldset y Legend [6:44:35](https://www.youtube.com/watch?v=ELSm-G201Ls&t=24275s) - Details y Summary [6:51:34](https://www.youtube.com/watch?v=ELSm-G201Ls&t=24694s) - Enlaces (Avanzado) [7:04:12](https://www.youtube.com/watch?v=ELSm-G201Ls&t=25452s) - Tablas [7:22:25](https://www.youtube.com/watch?v=ELSm-G201Ls&t=26545s) - Audio y Video [7:34:10](https://www.youtube.com/watch?v=ELSm-G201Ls&t=27250s) - Lazy Loading [7:39:37](https://www.youtube.com/watch?v=ELSm-G201Ls&t=27577s) - HTML Obsoleto [7:49:10](https://www.youtube.com/watch?v=ELSm-G201Ls&t=28150s) - HTML Semántico [7:57:42](https://www.youtube.com/watch?v=ELSm-G201Ls&t=28662s) - Accesibilidad WEB 

~~--- CSS INTERMEDIO ---~~ [8:19:58](https://www.youtube.com/watch?v=ELSm-G201Ls&t=29998s) - Selectores (Avanzado) [8:36:14](https://www.youtube.com/watch?v=ELSm-G201Ls&t=30974s) - Herencia, Cascada y Especificidad [9:04:51](https://www.youtube.com/watch?v=ELSm-G201Ls&t=32691s) - Pseudoclases [9:30:38](https://www.youtube.com/watch?v=ELSm-G201Ls&t=34238s) - Pseudoelementos [9:37:51](https://www.youtube.com/watch?v=ELSm-G201Ls&t=34671s) - Metodología BEM [9:49:33](https://www.youtube.com/watch?v=ELSm-G201Ls&t=35373s) - Display [10:03:21](https://www.youtube.com/watch?v=ELSm-G201Ls&t=36201s) - Posición Relativa y Absoluta [10:26:36](https://www.youtube.com/watch?v=ELSm-G201Ls&t=37596s) - Ventanas Modal [10:35:20](https://www.youtube.com/watch?v=ELSm-G201Ls&t=38120s) - Posición Fixed y Sticky [10:43:28](https://www.youtube.com/watch?v=ELSm-G201Ls&t=38608s) - Transiciones [10:56:53](https://www.youtube.com/watch?v=ELSm-G201Ls&t=39413s) - Desbordamiento (overflow) [11:01:49](https://www.youtube.com/watch?v=ELSm-G201Ls&t=39709s) - Control de flujo del texto [11:11:54](https://www.youtube.com/watch?v=ELSm-G201Ls&t=40314s) - Object fit y Object position [11:16:34](https://www.youtube.com/watch?v=ELSm-G201Ls&t=40594s) - Contorno (outline) [11:25:13](https://www.youtube.com/watch?v=ELSm-G201Ls&t=41113s) - Emmet (material re-usado) 

~~--- CSS FLEXBOX ---~~ [11:43:11](https://www.youtube.com/watch?v=ELSm-G201Ls&t=42191s) - Introducción a Flexbox [11:56:29](https://www.youtube.com/watch?v=ELSm-G201Ls&t=42989s) - Flex Direction, Flex Wrap y Flex Flow [12:17:33](https://www.youtube.com/watch?v=ELSm-G201Ls&t=44253s) - Alineación en los ejes [12:34:59](https://www.youtube.com/watch?v=ELSm-G201Ls&t=45299s) - Order [12:41:37](https://www.youtube.com/watch?v=ELSm-G201Ls&t=45697s) - Flex Básis, Shrink y Grow [12:59:10](https://www.youtube.com/watch?v=ELSm-G201Ls&t=46750s) - Align Self  [13:02:42](https://www.youtube.com/watch?v=ELSm-G201Ls&t=46962s) - Layout con Flexbox --- RESPONSIVE DESIGN --- [13:35:25](https://www.youtube.com/watch?v=ELSm-G201Ls&t=48925s) - Bloques y Multimedia flexible [13:56:07](https://www.youtube.com/watch?v=ELSm-G201Ls&t=50167s) - Atributos SRCSET y SIZES [14:10:17](https://www.youtube.com/watch?v=ELSm-G201Ls&t=51017s) - Picture, Source y Media [14:21:18](https://www.youtube.com/watch?v=ELSm-G201Ls&t=51678s) - Media Queries [14:29:57](https://www.youtube.com/watch?v=ELSm-G201Ls&t=52197s) - Ejercicio "Holy Grail" con Flexbox [14:48:36](https://www.youtube.com/watch?v=ELSm-G201Ls&t=53316s) - Mobile First [14:55:08](https://www.youtube.com/watch?v=ELSm-G201Ls&t=53708s) - Feature Queries [14:59:01](https://www.youtube.com/watch?v=ELSm-G201Ls&t=53941s) - Container Queries 

~~--- CSS GRID ---~~ [15:05:11](https://www.youtube.com/watch?v=ELSm-G201Ls&t=54311s) - Introducción a Grid [15:12:50](https://www.youtube.com/watch?v=ELSm-G201Ls&t=54770s) - Creando un Grid [15:24:54](https://www.youtube.com/watch?v=ELSm-G201Ls&t=55494s) - Unidades "auto" y "fr" [15:34:24](https://www.youtube.com/watch?v=ELSm-G201Ls&t=56064s) - Repeat y Minmax [15:42:18](https://www.youtube.com/watch?v=ELSm-G201Ls&t=56538s) - Grid implícito y explícito [15:53:34](https://www.youtube.com/watch?v=ELSm-G201Ls&t=57214s) - Grid dinámico (y responsive) [16:04:54](https://www.youtube.com/watch?v=ELSm-G201Ls&t=57894s) - Grid column y Grid row [16:14:52](https://www.youtube.com/watch?v=ELSm-G201Ls&t=58492s) - Grid flow: Dense [16:19:34](https://www.youtube.com/watch?v=ELSm-G201Ls&t=58774s) - Grid areas [16:35:06](https://www.youtube.com/watch?v=ELSm-G201Ls&t=59706s) - Alineacion con grid [16:53:28](https://www.youtube.com/watch?v=ELSm-G201Ls&t=60808s) - Subgrid [17:02:14](https://www.youtube.com/watch?v=ELSm-G201Ls&t=61334s) - Creando una página WEB --- ANIMACIONES --- [18:02:13](https://www.youtube.com/watch?v=ELSm-G201Ls&t=64933s) - Transiciones (Repaso) [18:13:13](https://www.youtube.com/watch?v=ELSm-G201Ls&t=65593s) - Animaciones [18:29:19](https://www.youtube.com/watch?v=ELSm-G201Ls&t=66559s) - Botones Animados y Efecto Typewriter [18:52:42](https://www.youtube.com/watch?v=ELSm-G201Ls&t=67962s) - Animaciones basadas en Scroll [19:07:35](https://www.youtube.com/watch?v=ELSm-G201Ls&t=68855s) - Rango de animaciones [19:17:33](https://www.youtube.com/watch?v=ELSm-G201Ls&t=69453s) - Integrando animaciones en una WEB [19:29:14](https://www.youtube.com/watch?v=ELSm-G201Ls&t=70154s) - Animaciones, cumpliendo la promesa --- WEB HOSTING --- [19:31:07](https://www.youtube.com/watch?v=ELSm-G201Ls&t=70267s) - Introducción al WEB HOSTING [19:57:59](https://www.youtube.com/watch?v=ELSm-G201Ls&t=71879s) - Subir tu WEB a INTERNET 

~~---- SECCIÓN AVANZADA ----~~ [20:09:16](https://www.youtube.com/watch?v=ELSm-G201Ls&t=72556s) - Filter y Backdrop Filter [20:29:30](https://www.youtube.com/watch?v=ELSm-G201Ls&t=73770s) - Transform [20:40:54](https://www.youtube.com/watch?v=ELSm-G201Ls&t=74454s) - Min, Max y Clamp [20:54:26](https://www.youtube.com/watch?v=ELSm-G201Ls&t=75266s) - Variables (custom properties) [21:05:50](https://www.youtube.com/watch?v=ELSm-G201Ls&t=75950s) - Función Calc [21:14:58](https://www.youtube.com/watch?v=ELSm-G201Ls&t=76498s) - Propiedades del Scroll [21:22:31](https://www.youtube.com/watch?v=ELSm-G201Ls&t=76951s) - Initial Letter [21:27:28](https://www.youtube.com/watch?v=ELSm-G201Ls&t=77248s) - Unidades del Viewport (Large, Small y Dynámic) [21:32:45](https://www.youtube.com/watch?v=ELSm-G201Ls&t=77565s) - Min-content, Max-content y Fit-content [21:39:19](https://www.youtube.com/watch?v=ELSm-G201Ls&t=77959s) - Función Color Mix 

~~---- PROYECTOS FINALES ----~~ [21:49:41](https://www.youtube.com/watch?v=ELSm-G201Ls&t=78581s) - Sidebar Menu & Chatbox (proyecto 1 y 2) [22:43:47](https://www.youtube.com/watch?v=ELSm-G201Ls&t=81827s) - Flip Card & One-Page View (proyecto 3 y 4) [23:21:42](https://www.youtube.com/watch?v=ELSm-G201Ls&t=84102s) - Menú Acordeón (proyecto 5) 

~~---- COMO SEGUIR ---~~ [23:42:39](https://www.youtube.com/watch?v=ELSm-G201Ls&t=85359s) - Como seguir aprendiendo 

--- FIN ---























