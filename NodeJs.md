[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight750&size=35&pause=150&random=false&width=435&lines=APUNTES:;NodeJs)](https://git.io/typing-svg)

------

| antes                                                        | después                                              | info                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![image-20240709080606812](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240709080606812.png) | ![image-20240709080938950](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240709080938950.png) | separacion entre los elementos. |

```scss
display: flex;
gap: 2rem;
//otra alternativa
display: grid;
grid-template-columns: repeat(3,1fr);
column-gap: 2rem;
```

| antes                                                        | después                                                      | info                                                        |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------------- |
| ![image-20240709080938950](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240709080938950.png) | ![image-20240709082927282](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240709082927282.png) | Nos permite resaltar donde estamos apuntando con el cursor. |

 ```scss
 a {
 	color: $blanco;
 	font-size: 2.2rem;
 	&:hover { //hace referencia a su elemento padre a
 		color: $amarillo;
 	}
 }
 ```



### MIXINS

````scss
// Definición de mixin con argumentos
@mixin nuevoMixin($argumento1, $argumento2) {
	// Código del mixin aquí
}
// Definición de mixin sin argumentos
@mixin nuevoMixin {
  // Código del mixin aquí
}
````



````scss
//_header.scss
h1 {
        color: $blanco;
        @include nuevoMixin; 
    }
````

> Mixins tiene de ventaja su reutilización en diferentes puntos.

````scss
@mixin nuevoMixin($transform,$size) {
	font-size: $size;
	color: $morado;
	text-transform: $transform;//pasamos la variable $transform a la propiedad text-transform
}

 a {
     color: $blanco;
     font-size: 2.2rem;
     &:hover {
         color: $amarillo;
         @include nuevoMixin(uppercase,size);
}
    }
 h1 {
     color: $blanco;
     @include nuevoMixin(lowercase);
    }


````

> @include nuevoMixin(valor); nos permite traer del archivo mixins los parametros definidos 

````scss
//_mixins.scss
@mixin telefono {
    @media (min-width: 480px) {
        @content;
    }
}
//_header.scss
.contenido-header {
    padding: calc($separacion / 2) 0;
    @include telefono {
        display: flex;
        justify-content: space-between;
        align-items: center;
        }
}
.navegacion-principal {
    display: flex ;
    gap: 2rem;
    @include telefono {
        display: none;
    }
    a{}
}

````

> @include telefono{...} nos permite pasarle mucha info al mixins.
>
> @content; permitirá que soporte un bloque de código (dinámico y variable), se la denomina directiva. O sea, inyecta todo lo que esta en las {} del @include 
>
> se observan dos dos @include con contenidos diferentes.

````scss
 h1 {
        color: $blanco;
        margin-bottom: 1rem;
        @include tablet {
            margin-bottom: 0;
        }
    }
````

| antes                                                        | después                                                      | info                                             |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------ |
| ![image-20240709103824554](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240709103824554.png) | ![image-20240709103908329](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240709103908329.png) | Ajuste de margin,   enviamos el valor a cambiar. |
