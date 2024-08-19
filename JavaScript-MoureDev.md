# \<JavaScript> Conceptos | Prácticas | Herramientas

### Introducción  

⏫ [Node.js — Download Node.js® (nodejs.org)](https://nodejs.org/en/download/package-manager)

[Referencia de JavaScript - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference)

#### Comentarios:

````js
// Esto es un comentario simple
/* 
Esto es un 
comentario en 
varias líneas 
*/
````

#### console.log( )

La sentencia console.log() muestra el mensaje que pasemos como parámetro a la llamada en la consola JavaScript del Navegador web.

````js
console.log("¡Hola, JavaScript!") // --> ¡Hola, JavaScript!
console.log('¡Hola, JavaScript!') // --> ¡Hola, JavaScript!
console.log(`¡Hola, JavaScript!`) // --> ¡Hola, JavaScript!

console.log("5")	// --> 5
console.log(5) 		// --> 5
console.log(5 + 2)	// --> 7
console.log(5 - 2)	// --> 3
console.log(5 * 2)	// --> 10
console.log(5 / 2)	// --> 2.5
console.log(5 % 2)	// --> 1
console.log(5 ** 2)	// --> 25
````

#### prompt()

La sentencia prompt() mostrará un cuadro de diálogo para que el usuario ingrese un dato. Se puede proporcionar un mensaje que se colocará sobre el campo de texto. El valor que devuelve es una cadena que representa lo que el usuario ingresó.

````js
let nombreIngresado = prompt("Ingrese su nombre");
````

> El valor que enviará prompt será Null o String.

````js
let edad = Number(prompt("Ingrese su edad: ")); // hay que convertir el string a number
````

#### alert()

La sentencia alert() mostrará una ventana sobre la página web que estemos accediendo mostrando el mensaje que se pase como parámetro a la llamada.

````js
alert("¡Hola Coder!"); 
````

### Términos empleados

- **Declaración**

Es un componente esencial que permite al programa realizar acciones específicas. A través de las declaraciones, se establecen reglas, asignan valores y se ejecutan operaciones fundamentales para el correcto funcionamiento del código.

````js
// Declaración de Variables
var x = 42;	// Declaración EXPLICITA
let y = 13;	//
let z     	// Declaración IMPLICITA
const pi = 3.14159;

// Declarción de Función
function showMessage() {
  alert('¡Hola a todos!');
}
````

- **Inicialización**

En el contexto de la informática, **inicialización** se refiere al proceso de establecer los valores iniciales para la ejecución de un programa.

````js
let name = `Charly`;
let surname = `Ribas`;
const dev = `Desarrollador`;
const nac = `15/02/1987`;
````

- **Reasignación**

Se refiere a cambiar el valor de una variable después de haberla inicializado previamente. Cuando reasignas una variable, le asignas un nuevo valor, sobrescribiendo el valor anterior.

````js
let x = 5; // Inicialización
x = 10;    // Reasignación: ahora x tiene el valor 10

````

- **Hoisting**

Permite usar funciones y variables antes de que se hayan declarado. Imagina el siguiente código:

````js
console.log(foo);
var foo = 'foo';
````

Aunque `foo` se asigna después de la línea `console.log`, este código genera `undefined` en lugar de un error. ¿Por qué? Porque el intérprete de JavaScript **mueve** las declaraciones al principio de su ámbito antes de ejecutar el código. A esto se le llama hoisting.

- **Scope**

Se refiere al alcance o visibilidad de las variables dentro de tu código. Básicamente, determina en qué partes del código una variable es accesible y cuánto tiempo vive.

1. **Scope Global:**

   - Una variable declarada fuera de cualquier función tiene **scope global**.

   - Puede ser accedida desde cualquier parte del programa.

   - Ejemplo:

     ```js
     let carName = "Volvo"; // Variable global
     function myFunction() {
         // Aquí también se puede usar carName
     }
     ```

   

2. **Scope Local (Función):**

   - Las variables declaradas dentro de una función tienen **scope local**.

   - Solo son visibles dentro de esa función.

   - Ejemplo:

     ```js
     function myFunction() {
         let carName = "Volvo"; // Variable local
         // Aquí se puede usar carName
     }
     ```

     

3. **Scope de Bloque (ES6+):**

   - Introducido en ES6 (2015) con las palabras clave `let` y `const`.

   - Las variables declaradas con `let` y `const` tienen **scope de bloque**.

   - Solo son accesibles dentro del bloque `{ ... }` en el que se declaran.

   - Ejemplo:

     ```js
     {
         let x = 2; // Variable con scope de bloque
     }
     // x no se puede usar aquí
     ```

4. **Scope de Cierre (Closure):**

   - Relacionado con funciones anidadas.

   - Las funciones internas pueden acceder a las variables de las funciones externas.

   - Ejemplo:

     ```js
     function outerFunction() {
         let outerVar = "Hello";
         function innerFunction() {
             console.log(outerVar); // Accede a outerVar
         }
         return innerFunction;
     }
     const myClosure = outerFunction();
     myClosure(); // Muestra "Hello"
     ```

​	**Ejemplo general:**

````js
let nombre = 'flora'
let apellido
{
    nombre = 'pepe'
    let apellido = 'argento'
    {
        let nombre = 'juan'
        apellido = 'suarez'
        console.log(nombre);
        console.log(apellido);
    }
    console.log(nombre);
    console.log(apellido);
}
console.log(nombre);
console.log(apellido);
/* por Consola:
juan
suarez
pepe
suarez
pepe
undefined
*/
````

- **Funcion Flecha (Arrow Function)**

Una función de flecha es una forma concisa de escribir una expresión de función. Es una sintaxis abreviada que te permite definir una función sin utilizar la palabra clave `function`.

Aquí hay un desglose del código:

```js
const verificarNumero = (numero) => { return !isNaN(numero) };
```

- `const verificarNumero`: Esto declara una variable constante llamada `verificarNumero`.
- `(numero)`: Esto es la lista de parámetros, que define el parámetro de entrada `numero`.
- `=>`: Esto es el símbolo de flecha, que separa la lista de parámetros del cuerpo de la función.
- `{ return !isNaN(numero) }`: Esto es el cuerpo de la función, que devuelve un valor booleano que indica si el parámetro `numero` es un número o no.

La función de flecha es equivalente a la siguiente expresión de función tradicional:

```js
const verificarNumero = function(numero) {
	return !isNaN(numero);
}
```

Sin embargo, la sintaxis de la función de flecha es más concisa y expresiva, lo que la hace una opción popular para definir funciones pequeñas y de una sola línea.

Algunos beneficios clave de las funciones de flecha incluyen:

- **Sintaxis concisa**: Las funciones de flecha son más breves y fáciles de leer que las expresiones de función tradicionales.
- **Devuelve implícito**: Si el cuerpo de la función es una sola expresión, la palabra clave `return` se implícita, lo que hace que el código sea aún más conciso.
- **`this` léxico**: Las funciones de flecha heredan el contexto `this` de su ámbito circundante, lo que puede simplificar el código y reducir errores.

En general, las funciones de flecha son una característica poderosa y flexible en JavaScript, y se utilizan ampliamente en el desarrollo de JavaScript moderno.

- **Documentacion**





### Principios

#### dry (dont repeat yourself )

> Es un principio de programación que sugiere que cada pieza de conocimiento debe estar representada de manera única en el sistema. En otras palabras, se trata de evitar la duplicación de código o lógica para hacer el software más mantenible y menos propenso a errores.

#### solid



### Tipos de variables

#### Sintaxis

````
<tipo_variable> identificador = dato
````

#### var 

````js
var helloWorld = "¡Hola, JavaScript!"
console.log(helloWorld)

helloWorld = "¡Hola de nuevo, JavaScript!"
console.log(helloWorld)

/* Ámbito */
{
    var nombre = 'pepe'
    console.log(nombre)
}
console.log(nombre)

/*Visto por consola*/
// --> pepe
// --> pepe
````

> - **Ámbito:** Las declaraciones `var` tienen un ámbito global o de función. Si se declara fuera de una función, está disponible en todo el código. Si se declara dentro de una función, solo es accesible dentro de esa función.
> - **Re-declaración y modificación:** Las variables con `var` pueden ser re-declaradas y modificadas dentro de su ámbito.
> - **Hoisting:** Las declaraciones `var` se mueven al principio de su ámbito antes de la ejecución del código.

#### let 

````js
let helloWorld2 = "¡Hola, JavaScript 2!"
console.log(helloWorld2)

helloWorld2 = "¡Hola de nuevo, JavaScript 2!"
console.log(helloWorld2)

/* Ámbito */
{
    let nombre = 'pepe'
    console.log(nombre)
}
console.log(nombre)

/* Visto por consola */
// --> pepe
// --> ReferenceError: nombre is not defined
````

> - **Ámbito:** Las declaraciones `let` tienen un ámbito de bloque. Esto significa que solo están disponibles dentro del bloque en el que se declaran.
> - **Re-declaración y modificación:** Las variables con `let` pueden ser modificadas, pero no re-declaradas.
> - **Hoisting:** Al igual que `var`, las declaraciones `let` también se mueven al principio de su ámbito antes de la ejecución del código.

#### const

````js
const helloWorld3 = "¡Hola, JavaScript 3!"
console.log(helloWorld3)

/* Nos da Error */
// helloWorld3 = "¡Hola de nuevo, JavaScript 2!"
// console.log(helloWorld3)

/* Ámbito */
{
    const nombre = 'pepe'
    console.log(nombre)
}
console.log(nombre)

/* Visto por consola */
// --> pepe
// --> ReferenceError: nombre is not defined
````

> - **Ámbito:** Las declaraciones `const` también tienen un ámbito de bloque. No pueden ser re-declaradas y su valor no puede ser modificado después de la asignación inicial.
> - **Úso:** Utiliza `const` para valores constantes que no cambiarán a lo largo del tiempo. Ej. Arrays, Object, Map

#### En resumen:

- Usa `const` para constantes inmutables.
- Usa `let` para variables cuyo valor puede cambiar.
- Evita `var` debido a sus problemas de alcance y re-declaración.

### Tipos de datos 

https://www.todojs.com/tipos-datos-javascript-es6/

https://es.javascript.info/types

En **JavaScript**, existen varios tipos de datos, y se pueden clasificar en dos categorías principales: **tipos primitivos** y **objetos**.

#### Primitivos

- **Undefined:** Representa una variable que no ha sido declarada o a la cual no se le ha asignado un valor.

````js
// Undefined
let undefinedValue
````

- **Boolean:** Representa un valor lógico y puede ser `true` o `false`.

````js
// Booleanos (boolean)
let isTeacher = true
let isStudent = false
````

- **Number:** Permite representar y manipular valores numéricos, como `37` o `-9.25`.

````js
// Números (number)
let age = 37 // Entero
let height = 1.77 // Decimal
````

- **String:** Representa datos textuales (cadenas de caracteres).

````js
// Cadenas de texto (string)
let myName = "Brais Moure"
let alias = 'MoureDev'
let email = `braismoure@mouredev.com`

````

- **Null:** Representa la ausencia intencional de valor.

````js
// Null
let nullValue = null
````

- **Symbol:** Introducido en ES6, se utiliza para crear identificadores únicos.

````js
// Symbol
let mySymbol = Symbol("mysymbol")

let sym2 = Symbol("foo");
let sym3 = Symbol("foo");

console.log(sym2); // Symbol(foo)
console.log(sym3); // Symbol(foo)

console.log(sym2 === sym3); // false (son distintos)
````

- **BigInt:** También introducido en ES6, permite representar enteros grandes con precisión.

````js
// BigInt
let myBigInt = BigInt(8172371986589716389471628379612983761289376129)
let myBigInt2 = 8172398712389471628379612983761289376129n
````

#### Objetos

- Los objetos son estructuras más complejas que contienen propiedades y métodos. Algunos ejemplos de objetos son `Array`, `Date`, `Promise`, etc.

#### typeof : tipo de dato

```` js
// Mostramos los tipos de datos
console.log(typeof myName) // --> string
console.log(typeof alias) // --> string
console.log(typeof email) // --> string

console.log(typeof age) // --> number
console.log(typeof height) // --> number

console.log(typeof isTeacher) // --> boolean
console.log(typeof isStudent) // --> boolean

console.log(typeof undefinedValue) // --> undefined

console.log(typeof nullValue) // --> object

console.log(typeof mySymbol) // --> symbol

console.log(typeof myBigInt) // --> bigint
console.log(typeof myBigInt2) // --> bigint
````

### Operadores

#### Operadores Aritméticos

````js
let a = 10
let b = 5

console.log(a + b) // Suma --> 15
console.log(a - b) // Resta --> 5
console.log(a * b) // Multiplicación --> 30
console.log(a / b) // División --> 2

console.log(a % b) // Módulo --> 0
console.log(a ** b) // Exponente --> 10^5 = 100000

a++ // Incremento
console.log(a) // --> 11 

b-- // Decremento
console.log(b) // --> 4

/* Conversión automática de tipos (coerción de tipo) */
console.log(8 * null) // null se convierte a 0 --> 0
console.log("5" - 1) // "5" (string) se convierte a 5 (number) --> 4
console.log("5" + 1) // 1 (number) se convierte a "1" (string)--> 51 
console.log("five" * 2) // "five" se convierte a NaN (number)--> NaN
````

#### Operadores de Asignación

````js
let myVariable = 2
console.log(myVariable)
myVariable += 2 // Suma con asignación  --> 2 + 2 = 4
myVariable -= 2 // Resta con asignación --> 4 - 2 = 2
myVariable *= 2 // Multiplicación con asignación --> 2 * 2 = 4
myVariable /= 2 // División con asignación --> 4 / 2 = 2

myVariable = 7
myVariable %= 2 // Módulo con asignación --> 7 % 2 = 1
myVariable **= 2 // Exponente con asignación --> 1^2 = 1
````

#### Operadores de Comparación

````js
let a = 10
let b = 6
console.log(a > b) // Mayor que --> true
console.log(a < b) // Menor que --> false

console.log(a >= b) // Mayor o igual que --> true
console.log(a <= b) // Menor o igual que --> false

console.log(a == b) // Igualdad por valor --> false
console.log(b == 6) // --> true 
console.log(b == "6") // Igualdad por tipo --> true
console.log(a == a) // --> true

console.log(a === a) // Igualdad por identidad (por tipo y valor) o igualdad estricta --> true
console.log(b === 6) // --> true 
console.log(b === "6") // --> false 

console.log(b != 6) // Desigualdad por valor  --> false
console.log(b !== "6") // Desigualdad por identidad (por tipo y valor) o desigualdad estricta  --> true
console.log(0 == false) // --> true
console.log(1 == false) // --> false
console.log(2 == false) // --> false

console.log(0 == "") // --> true
console.log(0 == " ") // --> true
console.log(0 == '') // --> true
console.log(0 == "Hola") // --> false
console.log(0 === "") // --> false

console.log(undefined == null) // --> true 
console.log(undefined === null) // --> false
````

> ❗ Recomiendo usar los operadores de comparación de tres caracteres defensivamente para evitar conversiones de tipo inesperadas que puedan complicarte las cosas.

#### Truthy y Falsy

Convertirán el valor del lado izquierdo a tipo Booleano para decidir qué hacer, pero dependiendo del operador y el resultado de esa conversión, devolverán ya sea el valor original del lado izquierdo o el valor del lado derecho.

- **Truthy values (valores verdaderos)**
  - Todos los **números positivos y negativos** menos el cero
  - Todas las **cadenas de texto** menos las vacías
  - El boolean **true**
- **Falsy values (valores falsos)**
  - **0**
  - **0n**
  - **null**
  - **undefined**
  - **NaN** (Not a Number)
  - El boolean **false**
  - Cadenas de **texto vacías** 

#### Operador Lógico

````js
// or (||) Operador Binario
console.log( 5 > 10 || 15 > 20) // --> (false or false) = false
console.log( 5 > 10 || 15 < 20) // --> (false or true) = true
console.log( 5 < 10 || 15 > 20) // --> (true or false) = true
console.log( 5 < 10 || 15 < 20) // --> (true or true) = true
console.log( 5 > 10 || 15 > 20 || 30 > 40) // --> ((false or false) or false) = false

// and (&&) Operador Binario
console.log( 5 > 10 && 15 > 20) // --> (false and false) = false
console.log( 5 > 10 && 15 < 20) // --> (false and true) = false
console.log( 5 < 10 && 15 > 20) // --> (true and false) = false
console.log( 5 < 10 && 15 < 20) // --> (true and true) = true
console.log( 5 < 10 && 15 > 20 && 30 > 40) // -->  ((true and false) and false) = false

console.log( 5 < 10 && 15 > 20 || 30 < 40) // --> ((true and false) or true) = true

// not (!) Operador Unitario
console.log(!( 5 > 10 && 15 > 20)) // --> !(false and false) = true 
console.log(!( 5 < 10 || 15 < 20)) // --> !(true or true) = false
````

> **or (||)** devolverá el **valor de su izquierda** cuando ese valor pueda convertirse en **true** y devolverá el valor de su derecha de lo contrario. 

> **and (&&)** funciona de manera similar pero en sentido contrario. Cuando el **valor a su izquierda** es algo que se convierte en **false**, devuelve ese valor, y de lo contrario devuelve el valor de su derecha. 

#### Ternario

````js
// (? :) Operador Ternario
const isRaining = true
isRaining ? console.log("esta lloviendo") : console.log("no esta lloviendo"); // --> esta lloviendo

````

> Operador *condicional* (o a veces simplemente *el operador ternario*).
>
> El operador usa el valor a la izquierda del signo de interrogación para decidir cuál de los otros dos valores “elegir”. Si escribes `a ? b : c`, **el resultado será `b` cuando `a` es verdadero** y `c` de lo contrario.

#### Precedencia de Operadores:

La **precedencia de operadores** determina el orden en el cual se evalúan los operadores. Los operadores con mayor precedencia se evalúan primero. 

| Orden                                                        | Ejemplo                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Agrupación y llamadas a funciones** (paréntesis, corchetes y objetos literales). | `Agrupación: `const resultado = (3 + 4) * 5;                 |
|                                                              | `Llamada a función: `function saludar(nombre) { console.log('Hola, ' + nombre); }` |
| **Incremento y decremento** (`++`, `--`).                    | `Incremento: `let contador = 0; contador++;`                 |
|                                                              | `Decremento: `let valor = 10; valor--;`                      |
| **Operadores unarios** (`!`, `~`, `+`, `-`, `typeof`, `void`, `delete`). | `Negación: `const esVerdadero = !false;`                     |
|                                                              | `Tipo de dato: `const tipo = typeof 42;`                     |
| **Multiplicación, división y módulo** (`*`, `/`, `%`).       | `Multiplicación: `const producto = 3 * 4;                    |
|                                                              | ` División: `const cociente = 10 / 2;                        |
|                                                              | ` Módulo: `const resto = 11 % 3;`                            |
| **Suma y resta** (`+`, `-`).                                 | `Suma: `const suma = 5 + 7;                                  |
|                                                              | `Resta: `const resta = 10 - 3;`                              |
| **Desplazamiento de bits** (`<<`, `>>`, `>>>`).              | `Desplazamiento a la izquierda: `const resultado = 8 << 2;`  |
| **Relacionales** (`<`, `<=`, `>`, `>=`, `in`, `instanceof`). | `Mayor que: `const esMayor = 5 > 3;` Instancia de: `const esArray = [1, 2] instanceof Array;` |
| **Igualdad** (`==`, `!=`, `===`, `!==`).                     | `Estrictamente igual: `const esIgual = '5' === 5;`           |
| **Bitwise AND** (`&`).                                       | `const resultado = 5 & 3;`                                   |
| **Bitwise XOR** (`^`).                                       | `const resultado = 5 ^ 3;`                                   |
| **Bitwise OR** (`|`).                                        | `const resultado = 5 | 3;`                                   |
| **Logical AND** (`&&`).                                      | `const resultado = true && false;`                           |
| **Logical OR** (`||`).                                       | `const resultado = true || false;`                           |
| **Operador condicional (ternario)** (`? :`).                 | `const edad = 18; const mensaje = edad >= 18 ? 'Mayor de edad' : 'Menor de edad';` |
| **Asignación** (`=`, `+=`, `-=` y otros).                    | `let x = 10; x += 5;`                                        |
| **Coma** (`,`).                                              | `const resultado = (2 + 3, 4 * 5); // El resultado es 20`    |

Recuerda que los paréntesis pueden anular la precedencia y te permiten controlar el orden de evaluación en expresiones más complejas.

[Precedencia de operadores - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Operator_precedence)

### Cadenas de Texto (String)

Las cadenas se utilizan para representar texto. Se escriben encerrando su contenido entre comillas.

```js
let string = `En el mar`; // Comillas simples
let string1 ="Acostado en el océano"; // Comillas dobles
let string2 ='Flotando en el océano'; // acentos graves
```

#### Concatenación

Las cadenas no se pueden dividir, multiplicar o restar. El operador `+` se puede usar en ellas, no para sumar, sino para *concatenar* —unir dos cadenas.

````js
let myName = "charly"
let myAge = "36"
let greeting = "Hola, " + myName + "!!"
console.log(greeting); // --> "Hola, charly!!
console.log(typeof greeting); // --> string
````

Incluir caracteres especiales:

````js
let text = "primera línea\nsegunda línea" // \ caracter posterior significado especial
									  // n: salto de línea; t: tabulado
text = "Un carácter de nueva línea se escribe como \" \\n \"." // \\: muestra una \
````

#### Acceso a caracteres

````js
let greeting = "Hola, Charlydev!!"

console.log(greeting.length) // Muestra la longuitud de la cadena
console.log(greeting[0]) // --> H
console.log(greeting[11]) // --> l
````

#### Métodos comunes

````js
console.log(greeting.toUpperCase()) // Mayúsculas
console.log(greeting.toLowerCase()) // Minúsculas
console.log(greeting.indexOf("Hola")) // Índice --> 0
console.log(greeting.indexOf("Charlydev"))
console.log(greeting.includes("Hola")) // Incluye
console.log(greeting.includes("Brais"))
console.log(greeting.includes("MoureDev"))
console.log(greeting.slice(0, 10)) // Sección --> Hola, Charl
console.log(greeting.replace("Brais", "MoureDev")) // Reemplazo
console.log(text2.replaceAll(' ','-')); // Reemplaza todos los espacios vacíos por -
console.log(text2.replace(/\s+/g,'-'));
````

#### Template literal

Cadenas de texto que nos permiten utilizar expresiones incrustadas.

1. **Cadenas de caracteres de más de una línea**: Las plantillas literales te permiten crear cadenas de texto que abarcan varias líneas sin necesidad de concatenar manualmente. Por ejemplo:

   JavaScript

   

   ```js
   console.log(`Línea 1 de la cadena de texto
   Línea 2 de la cadena de texto`);
   // Resultado: "Línea 1 de la cadena de texto
   // Línea 2 de la cadena de texto"
   ```

2. **Interpolación de expresiones**: Puedes insertar expresiones dentro de las plantillas literales utilizando `${expresión}`. Esto simplifica la sintaxis en comparación con las cadenas de caracteres normales. Por ejemplo:

   JavaScript

   

   ```js
   let a = 5;
   let b = 10;
   console.log(`Quince es ${a + b} y no ${2 * a + b}.`);
   // Resultado: "Quince es 15 y no 20."
   ```

En resumen, las plantillas literales hacen que trabajar con cadenas de texto sea más legible y expresivo.

### Estructuras del Programa

Estructuras condicionales y de control de flujo en JavaScript:

**Estructuras condicionales**

Las estructuras condicionales se refieren a las instrucciones que permiten tomar decisiones en función de ciertas condiciones o eventos. Estas estructuras permiten evaluar una condición y ejecutar un bloque de código si la condición se cumple. Los ejemplos de estructuras condicionales incluyen:

- If (si)
- Else (si no)
- Switch (seleccionar)
- Ternario (?:)

Las estructuras condicionales se utilizan para:

- Tomar decisiones en función de condiciones específicas
- Evaluar expresiones y ejecutar código en consecuencia
- Realizar acciones diferentes en función de la entrada del usuario o de otros factores

**Estructuras de control de flujo**

Las estructuras de control de flujo se refieren a las instrucciones que permiten controlar el orden en que se ejecutan las instrucciones de un programa. Estas estructuras permiten saltar, repetir o interrumpir la ejecución de un programa en función de ciertas condiciones o eventos. Los ejemplos de estructuras de control de flujo incluyen:

- Bucles (while, for, do-while)
- Condiciones (if, else, switch)
- Saltos (break, continue, return)
- Funciones y procedimientos

Las estructuras de control de flujo se utilizan para:

- Repetir tareas
- Tomar decisiones
- Saltar a diferentes partes del programa
- Interrumpir la ejecución del programa

**Diferencias clave**

Las principales diferencias entre las estructuras de control de flujo y las estructuras condicionales son:

- **Propósito**: Las estructuras de control de flujo se utilizan para controlar el orden en que se ejecutan las instrucciones, mientras que las estructuras condicionales se utilizan para tomar decisiones en función de condiciones específicas.
- **Funcionalidad**: Las estructuras de control de flujo pueden saltar, repetir o interrumpir la ejecución del programa, mientras que las estructuras condicionales solo pueden ejecutar un bloque de código si se cumple una condición.
- **Sintaxis**: Las estructuras de control de flujo suelen tener una sintaxis más compleja que las estructuras condicionales, ya que requieren la especificación de condiciones, bucles o saltos.

En resumen, las estructuras de control de flujo se utilizan para controlar el orden en que se ejecutan las instrucciones, mientras que las estructuras condicionales se utilizan para tomar decisiones en función de condiciones específicas. Ambas son fundamentales en la programación y se utilizan en conjunto para crear algoritmos y programas eficientes.

#### **Estructuras Condicionales**

##### **1. If (Si)**

La estructura `if` se utiliza para ejecutar un bloque de código si se cumple una condición específica. 

Sintaxis:

```js
if (condición) {
// código a ejecutar si se cumple la condición
}
```

Ejemplo:

```js
let edad = 25;
if (edad >= 18) {
	console.log("Eres mayor de edad");
}
```

##### 2. If...Else (Si-No)

La estructura `if...else` se utiliza para ejecutar un bloque de código si se cumple una condición específica. Si la condición no se cumple, se ejecutará el bloque de código dentro de la cláusula `else`.

Sintaxis:

```js
if (condición) {
// código a ejecutar si la condición es verdadera
} else {
// código a ejecutar si la condición es falsa
}
```

Ejemplo:

```js
let edad = 25;
if (edad >= 18) {
	console.log("Eres mayor de edad");
} else {
	console.log("Eres menor de edad");
}
```

##### 2. If...Else If...Else (Si-No-Si-No)

La estructura `if...else if...else` se utiliza para evaluar varias condiciones y ejecutar un bloque de código según la condición que se cumpla.

Sintaxis:

```js
if (condición1) {
// código a ejecutar si la condición1 es verdadera
} else if (condición2) {
// código a ejecutar si la condición1 es falsa y la condición2 es verdadera
} else {
// código a ejecutar si todas las condiciones son falsas
}
```

Ejemplo:

```js
let nota = 7;
if (nota >= 9) {
	console.log("Excelente");
} else if (nota >= 7) {
	console.log("Bueno");
} else {
	console.log("Regular");
}
```

##### 3. Switch (Seleccionar)

La estructura `switch` se utiliza para evaluar una expresión y ejecutar un bloque de código según el valor que tome la expresión.

Sintaxis:

```js
switch (expresión) {
case valor1:
// código a ejecutar si la expresión es igual a valor1
	break;
case valor2:
// código a ejecutar si la expresión es igual a valor2
	break;
default:
// código a ejecutar si la expresión no coincide con ninguno de los valores
}
```

Ejemplo:

```js
// let dia = 2;
switch (dia = 3) {
	case 1:
		console.log("Lunes");
		break;
	case 2:
		console.log("Martes");
		break;
	case 3:
		console.log("Miércoles");
		break;
	default:
		console.log("Día no válido");
		break;
}
```

#### **Estructuras de Control de Flujo**

##### 1. While

La estructura `while` se utiliza para ejecutar un bloque de código mientras se cumpla una condición específica.

Sintaxis:

```js
while (condición) {
// código a ejecutar mientras la condición sea verdadera
}
```

Ejemplo:

```js
let i = 0;
while (i < 5) {
	console.log(i);
	i++;
}
```

##### 2. Do...While

La estructura `do...while` se utiliza para ejecutar un bloque de código al menos una vez y luego repetirlo mientras se cumpla una condición específica.

Sintaxis:

```js
do {
// código a ejecutar al menos una vez
} while (condición);
```

Ejemplo:

```js
let i = 0;
do {
	console.log(i);
	i++;
} while (i < 5);
```

##### 3. For

La estructura `for` se utiliza para ejecutar un bloque de código un número determinado de veces.

Sintaxis:

```js
for (inicialización; condición; incremento) {
// código a ejecutar en cada iteración
}
```

Ejemplo:

```js
for (let i = 0; i < 5; i++) {
	console.log(i);
}
```

##### 4. For-In (Para-En)

La estructura `for-in` se utiliza para iterar sobre las propiedades de un objeto. La sintaxis es la siguiente:

```js
for (variable in objeto) {
// código a ejecutar en cada iteración
}
```

##### 5. For-Of (Para-De)

La estructura `for-of` se utiliza para iterar sobre los valores de un array o un objeto iterable. La sintaxis es la siguiente:

```js
for (variable of iterable) {
// código a ejecutar en cada iteración
}
```

##### 6. Break (Romper)

La instrucción `break` se utiliza para salir de un bucle o una estructura de control de flujo. La sintaxis es la siguiente:

```js
break;
```

##### 7. Continue (Continuar)

La instrucción `continue` se utiliza para saltar a la siguiente iteración de un bucle. La sintaxis es la siguiente:

```js
continue;
```

##### 8. Return (Retornar)

La instrucción `return` se utiliza para salir de una función y devolver un valor. La sintaxis es la siguiente:

```js
return valor;
```

Es importante destacar que las estructuras de control de flujo se utilizan para controlar el orden en que se ejecutan las instrucciones de un programa, lo que permite crear algoritmos más eficientes y escalables.

### Arrays

[Array - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array)

En JavaScript, un array (también conocido como arreglo o matriz) es una estructura de datos que permite almacenar una colección de valores en una sola variable. Los arrays en JavaScript son objetos especiales que tienen propiedades y métodos adicionales para trabajar con ellos.

Aquí hay algunos ejemplos de cómo crear y manipular arrays en JavaScript:

#### Crear un array

Puedes crear un array vacío utilizando el constructor `Array()` o utilizando la sintaxis de corchetes `[]`:

```js
// DECLARACIÓN
const miArray = new Array(); // []
const miArray2 = []; // []

// INICIALIZACIÓN
myArray = [3] // [3]
myArray2 = new Array(3) // [ <3 empty items> ]
```

También puedes crear un array con valores iniciales:

```js
const miArray = [1, 2, 3, 4, 5];
```

También se puede crear una array con un tamaño:

````js
const miArray2 = new Array(3);
console.log(myArray2.length); // 3
console.log(myArray2[0]); // undefined
console.log(myArray2[1]); // undefined
console.log(myArray2[2]); // undefined
````

#### Acceder a elementos del array

Puedes acceder a los elementos del array utilizando su índice (posición en el array). El índice comienza en 0:

```js
const miArray = [1, 2, 3, 4, 5];
console.log(miArray[0]); // 1
console.log(miArray[4]); // 5
```

#### Modificar elementos del array

Puedes modificar los elementos del array asignando un nuevo valor a una posición específica:

```js
const miArray = [1, 2, 3, 4, 5];
miArray[2] = 10;
console.log(miArray); // [1, 2, 10, 4, 5]
```

#### Métodos

> En JavaScript, los métodos de arrays son funciones que se pueden aplicar a un arreglo (array) para realizar diversas operaciones. A continuación, los métodos más comunes y útiles que se pueden hacer con los métodos de arrays en JavaScript:

##### **1. Métodos de manipulación de elementos**

- `push()`: Agrega uno o más elementos al final del arreglo.

````js
let myArray = []
myArray.push("Carlos")
myArray.push("Alberto")
myArray.push("Ribas")
myArray.push(37)
````

- `pop()`: Elimina el último elemento del arreglo y lo devuelve.

````js
console.log(myArray.pop()) 
console.log(myArray)
// 37
// [ 'Carlos', 'Alberto', 'Ribas' ]
````

- `shift()`: Elimina el primer elemento del arreglo y lo devuelve.

````js
console.log(myArray.shift());
console.log(myArray);
// Carlos
// [ 'Alberto', 'Ribas' ]
````

- `unshift()`: Agrega uno o más elementos al principio del arreglo.

````js
myArray.unshift("Carlos","Ribas")
console.log(myArray);
// [ 'Carlos', 'Ribas', 'Carlos', 'Alberto', 'Ribas' ]
````

- `splice()`: Agrega o elimina elementos en una posición específica del arreglo.

````js
// myArray.splice(start, deleteCount, item1, item2, ...)
// [ 'Carlos', 'Ribas', 'Carlos', 'Alberto', 'Ribas' ]
myArray.splice(1, 2, "Nueva entrada")
console.log(myArray)
// [ 'Carlos', 'Nueva entrada', 'Alberto', 'Ribas' ]
myArray.splice(1, 0, "Nueva entrada")
console.log(myArray)
// [ 'Carlos', "Nueva entrada",'Nueva entrada', 'Alberto', 'Ribas' ]
````

`start`: Es el índice donde se iniciará la modificación del array. Puede ser un número positivo o negativo. Si es negativo, se cuenta desde el final del array.

`deleteCount`: Es el número de elementos que se eliminarán a partir de la posición `start`. Si es 0, no se eliminarán elementos.

`item1, item2, ...`: Son los elementos que se agregarán en la posición `start` después de eliminar los elementos especificados por `deleteCount`.

- `length()` : Devuelve el número de elementos que tiene el arreglo.

````js
// [ 'Carlos', 'Alberto', 'Ribas' ]
console.log(myArray.length)
// 3
````

##### **2. Métodos de búsqueda y filtro**

- `indexOf()`: Busca la posición de un elemento en el arreglo y devuelve su índice.

````js
// [ 'Carlos', 'Ribas', 'Carlos', 'Alberto', 'Ribas' ]
console.log(nombres.indexOf('Carlos'))
// 0
````

- `includes()`: Verifica si un elemento está incluido en el arreglo y devuelve un booleano.

````js
// [ 'Carlos', 'Ribas', 'Carlos', 'Alberto', 'Ribas' ]
console.log(nombres.includes('Carlos'))
// true
````

- `find()`: Busca el primer elemento que cumpla con una condición y lo devuelve.
- `findIndex()`: Busca la posición del primer elemento que cumpla con una condición y devuelve su índice.
- `filter()`: Crea un nuevo arreglo con los elementos que cumplen con una condición.

##### **3. Métodos de ordenamiento y clasificación**

- `sort()`: Ordena los elementos del arreglo de manera ascendente o descendente.
- `reverse()`: Invierte el orden de los elementos del arreglo.

##### **4. Métodos de reducción y acumulación**

- `reduce()`: Aplica una función a cada elemento del arreglo y devuelve un valor acumulado.
- `reduceRight()`: Aplica una función a cada elemento del arreglo en orden inverso y devuelve un valor acumulado.

##### **5. Métodos de concatenación y división**

- `concat()`: Combina dos o más arreglos en uno solo.
- `slice()`: Extrae una sección del arreglo y devuelve un nuevo arreglo.

````js
// myArray.slice(start, end)
const myArray = []
myArray.push("carlos","alberto","ribas",37)
console.log(myArray); // [ 'carlos', 'alberto', 'ribas', 37 ]

let myNewArray = myArray.slice(1,3)
console.log(myNewArray); // [ 'alberto', 'ribas' ]
````

`Star`: Es el índice desde donde se tomará los valores del array.

`End`: Es el índice hasta donde se tomara los valores del array, si no se señala toma el array completo.

- `split()`: Divide un arreglo en subarreglos según un separador.

##### **6. Métodos de iteración**

- `forEach()`: Ejecuta una función para cada elemento del arreglo.
- `map()`: Crea un nuevo arreglo con los resultados de aplicar una función a cada elemento del arreglo original.
- `some()`: Verifica si al menos un elemento del arreglo cumple con una condición y devuelve un booleano.
- `every()`: Verifica si todos los elementos del arreglo cumplen con una condición y devuelve un booleano.

### Objetos

**¿Qué es un objeto en JavaScript?**

En JavaScript, un objeto (object) es una colección de propiedades (llamadas también atributos o campos) y métodos que se utilizan para describir y manipular un conjunto de datos. Un objeto es una instancia de una clase, y cada objeto tiene sus propias propiedades y métodos que lo definen.

Un objeto en JavaScript se puede crear de varias maneras:

- Utilizando la sintaxis de objeto literal: 

````js
let persona = { 
    nombre: 'Juan', 
    edad: 30 
}
````

- Utilizando el constructor `Object`: 

````js
let persona = new Object(); 
persona.nombre = 'Juan'; 
persona.edad = 30;
````

- Utilizando una función constructora: 

````js
function Persona(nombre, edad) { 
    this.nombre = nombre; 
    this.edad = edad; 
} 
let persona = new Persona('Juan', 30);
````

**Propiedades de un objeto**

Las propiedades de un objeto son pares clave-valor que se utilizan para describir los atributos del objeto. Las propiedades se pueden acceder utilizando la notación de punto (`.`) o la notación de corchetes (`[]`).

Ejemplo:

```js
const persona = { 
    nombre: 'Juan', 
    edad: 30 
};
console.log(persona.nombre); // "Juan"
console.log(persona['edad']); // 30
```

**Métodos de un objeto**

Los métodos de un objeto son funciones que se utilizan para manipular y interactuar con el objeto. Los métodos se definen como propiedades del objeto que contienen una función.

Ejemplo:

```js
const persona = {
  	nombre: 'Juan',
  	edad: 30,
  	saludar: function() {
    console.log(`Hola, soy ${this.nombre}`)
	}
}
persona.saludar(); // "Hola, soy Juan"
```

#### Array de objetos

un array de objetos es una colección de objetos que se almacenan en una sola variable. Cada objeto dentro del array tiene sus propias propiedades y valores, y se puede acceder a ellos utilizando un índice o clave.

Un array de objetos se declara de la siguiente manera:

```js
const miArray = [
	{ nombre: "Juan", edad: 25 },
	{ nombre: "María", edad: 30 },
	{ nombre: "Pedro", edad: 35 }
]
```

En este ejemplo, `miArray` es un array que contiene tres objetos. Cada objeto tiene dos propiedades: `nombre` y `edad`.

Para acceder a un objeto específico dentro del array, se utiliza el índice del objeto. Por ejemplo, para acceder al primer objeto del array, se utiliza el índice 0:

```js
console.log(miArray[0]); // { nombre: "Juan", edad: 25 }
```

Para acceder a una propiedad específica de un objeto dentro del array, se utiliza la notación de punto. Por ejemplo, para acceder a la propiedad `nombre` del primer objeto del array, se utiliza la siguiente sintaxis:

```js
console.log(miArray[0].nombre); // "Juan"
```

Los arrays de objetos son muy útiles en JavaScript porque permiten almacenar y manipular grandes cantidades de datos de manera eficiente. Algunos ejemplos de uso de arrays de objetos incluyen:

- Almacenar información de usuarios en una aplicación web
- Representar una lista de productos en una tienda en línea
- Guardar información de una base de datos en una aplicación móvil

Algunas operaciones comunes que se pueden realizar con arrays de objetos en JavaScript incluyen:

- Agregar un nuevo objeto al array utilizando el método `push()`
- Eliminar un objeto del array utilizando el método `splice()`
- Buscar un objeto específico dentro del array utilizando el método `find()`
- Filtrar los objetos del array utilizando el método `filter()`
- Ordenar los objetos del array utilizando el método `sort()`

**Métodos built-in de JavaScript**

JavaScript proporciona varios métodos built-in (integrados) que se pueden utilizar con objetos. Algunos de los métodos más comunes son:

- `toString()`: devuelve una representación de cadena del objeto.
- `valueOf()`: devuelve el valor primitivo del objeto.
- `hasOwnProperty(prop)`: devuelve `true` si el objeto tiene una propiedad propia con el nombre especificado.
- `isPrototypeOf(obj)`: devuelve `true` si el objeto es el prototipo de otro objeto.
- `propertyIsEnumerable(prop)`: devuelve `true` si la propiedad es enumerable.

**Métodos de objetos específicos**

Además de los métodos built-in, cada objeto en JavaScript tiene sus propios métodos específicos que dependen del tipo de objeto. Por ejemplo:

- Array:
  - `push()`: agrega un elemento al final del array.
  - `pop()`: elimina el último elemento del array.
  - `indexOf()`: devuelve el índice del primer elemento que coincide con el valor especificado.
- String:
  - `toUpperCase()`: devuelve una copia del string en mayúsculas.
  - `toLowerCase()`: devuelve una copia del string en minúsculas.
  - `trim()`: elimina los espacios en blanco del principio y del final del string.
- Date:
  - `getFullYear()`: devuelve el año del objeto Date.
  - `getMonth()`: devuelve el mes del objeto Date (0-11).
  - `getDate()`: devuelve el día del mes del objeto Date.

Estos son solo algunos ejemplos de los métodos que se pueden utilizar con objetos en JavaScript. Hay muchos más, y cada objeto tiene sus propias características y métodos específicos.

#### Iterar

En JavaScript, existen varias formas de iterar sobre arrays, objetos y otros tipos de datos utilizando los siguientes métodos:

1. `for...in`
2. `for...of`
3. `forEach()`
4. `for...each` (no es un método nativo, pero se puede implementar utilizando otros métodos)

A continuación, se presentan las diferencias entre cada uno de ellos:

##### **1. `for...in`**

El bucle `for...in` itera sobre las propiedades de un objeto, devolviendo el nombre de la propiedad en cada iteración.

Sintaxis: `for (var propiedad in objeto) { ... }`

Ejemplo:

```js
const persona = { nombre: 'Juan', edad: 30, ciudad: 'Madrid' };
for (let propiedad in persona) {
  console.log(propiedad + ': ' + persona[propiedad]);
}
// Output:
// nombre: Juan
// edad: 30
// ciudad: Madrid
```

**Ventajas:**

- Permite iterar sobre objetos y arrays.
- Devuelve el nombre de la propiedad en cada iteración.

**Desventajas:**

- No garantiza el orden de iteración.
- No es compatible con iterables (como arrays o strings).

##### **2. `for...of`**

El bucle `for...of` itera sobre los valores de un iterable (como un array, un string o un objeto que implemente la interfaz `Iterable`), devolviendo el valor en cada iteración.

Sintaxis: `for (var valor of iterable) { ... }`

Ejemplo:

```js
const frutas = ['manzana', 'pera', 'naranja'];
for (var fruta of frutas) {
  console.log(fruta);
}
// Output:
// manzana
// pera
// naranja
```

**Ventajas:**

- Permite iterar sobre iterables (como arrays, strings, etc.).
- Garantiza el orden de iteración.
- Es compatible con iterables que no son objetos.

**Desventajas:**

- No devuelve el nombre de la propiedad en cada iteración.
- No es compatible con objetos que no implementan la interfaz `Iterable`.

##### **3. `forEach()`**

El método `forEach()` itera sobre un array o un objeto que implemente la interfaz `Iterable`, ejecutando una función callback para cada elemento.

Sintaxis: `array.forEach(callback)`

Ejemplo:

```js
const frutas = ['manzana', 'pera', 'naranja'];
frutas.forEach(function(fruta) {
  console.log(fruta);
});
// Output:
// manzana
// pera
// naranja
```

**Ventajas:**

- Permite iterar sobre arrays y objetos que implementen la interfaz `Iterable`.
- Puede ser utilizado con funciones callback.

**Desventajas:**

- No devuelve el nombre de la propiedad en cada iteración.
- No es compatible con objetos que no implementan la interfaz `Iterable`.

##### **4. `for...each` (no es un método nativo)**

El bucle `for...each` no es un método nativo de JavaScript, pero se puede implementar utilizando otros métodos. Por ejemplo, utilizando `for...in` y `Object.keys()`:

```js
const persona = { nombre: 'Juan', edad: 30, ciudad: 'Madrid' };
for (var propiedad in persona) {
  if (Object.prototype.hasOwnProperty.call(persona, propiedad)) {
    console.log(propiedad + ': ' + persona[propiedad]);
  }
}
// Output:
// nombre: Juan
// edad: 30
// ciudad: Madrid
```

**Ventajas:**

- Permite iterar sobre objetos y arrays.
- Devuelve el nombre de la propiedad en cada iteración.

**Desventajas:**

- No garantiza el orden de iteración.
- No es compatible con iterables que no son objetos.

##### **5. `for await`**

El  `for await` es una variante del bucle `for` que se utiliza específicamente para iterar sobre iterables asíncronos, como promesas o generadores asíncronos.

La principal diferencia entre `for await` y los otros bucles es que `for await` permite iterar sobre iterables asíncronos de manera síncrona, es decir, sin necesidad de utilizar callbacks o promesas explícitas.

Aquí hay un ejemplo para ilustrar la diferencia:

```js
// Un arreglo de promesas
const promises = [
  new Promise(resolve => setTimeout(() => resolve(1), 1000)),
  new Promise(resolve => setTimeout(() => resolve(2), 2000)),
  new Promise(resolve => setTimeout(() => resolve(3), 3000)),
];

// Utilizando for await
for await (const value of promises) {
  console.log(value); // 1, 2, 3
}

// Utilizando for...of
for (const promise of promises) {
  promise.then(value => console.log(value)); // 1, 2, 3 (pero no en orden)
}

// Utilizando forEach()
promises.forEach(promise => {
  promise.then(value => console.log(value)); // 1, 2, 3 (pero no en orden)
});
```

En el ejemplo anterior, `for await` permite iterar sobre el arreglo de promesas de manera síncrona, es decir, espera a que cada promesa se resuelva antes de pasar a la siguiente. Por otro lado, `for...of` y `forEach()` no esperan a que las promesas se resuelvan, por lo que el orden de los valores no está garantizado.

En resumen, `for await` es una herramienta útil para iterar sobre iterables asíncronos de manera síncrona, lo que puede simplificar el código y hacerlo más legible. Sin embargo, es importante tener en cuenta que solo se puede utilizar con iterables asíncronos, y no con iterables síncronos.

En resumen, cada método tiene sus ventajas y desventajas, y la elección del método adecuado dependerá del tipo de datos que se esté trabajando y del objetivo específico de la iteración.

### Set

[Set - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Set)

El objeto Set en JavaScript es una colección de valores únicos, que pueden ser de cualquier tipo, ya sean primitivos o referencias a objetos. Permite almacenar y manipular conjuntos de valores de manera eficiente. El objeto Set se utiliza para eliminar duplicados de un conjunto de valores y para verificar si un valor existe en el conjunto.

#### Métodos

> Los métodos de `Set` permiten interactuar con esta colección de valores de manera eficiente y segura.

````js
//DECLARACIÓN
let mySet = new Set() // Set(0) {}

//INICIALIZACIÓN
mySet = new Set("carlos","alberto","ribas",37,"carlos@look.com")
console.log(mySet) // Set(5) { 'carlos', 'alberto', 'ribas', 37, 'carlos@look.com' }
````

- `add(valor)`: Agrega un nuevo elemento al conjunto.

````js
const mySet = new Set(); 
mySet.add(1); 
mySet.add(2); 
console.log(mySet); // Set(2) {1, 2}
````

Los set no admiten duplicar valores:

````js
const miSet = new Set([1, 2, 3]);
miSet.add(4)
miSet.add(4)
miSet.add(4)
console.log(miSet); // Set(4) {1, 2, 3, 4}
````

También se pueden crear objetos Set a partir de arrays utilizando el constructor `Set()` y pasando el array como parámetro:

````js
const myArray = [1, 2, 2, 3, 4, 4, 5];
const mySet = new Set(myArray);
console.log(mySet); // Set {1, 2, 3, 4, 5}
````

- `clear()`: Elimina todos los elementos del conjunto.

````js
const miSet = new Set([1, 2, 3]); 
miSet.clear(); 
console.log(miSet); // Set {}
````

- `delete(valor)`: Elimina un elemento específico del conjunto.

````js
const miSet = new Set([1, 2, 3]); 
miSet.delete(2); 
console.log(miSet); // Set {1, 3}

// Verifica por consola si se elimino el valor indicado
console.log(miSet.delete("2")); // true
console.log(miSet.delete("4")); // false
````

- `has(valor)`: Verifica si un elemento existe en el conjunto.
````js
const miSet = new Set([1, "dos", 3]); 
console.log(miSet.has("dos")); // true
console.log(miSet.has("cuatro")); // false
````
- `from()`: Convierte un set a array

````js
const mySet = new Set([ 'ribas', 37, 'carlos@look.com' ]) 
// Set(3) { 'ribas', 37, 'carlos@look.com' }
let myArray = Array.from(mySet) //[ 'ribas', 37, 'carlos@look.com' ]
````

- `new Set()`: Convierte un array a set

````js
const myArray = [ 'ribas', 37, 'carlos@look.com' ];
mySet = new Set(myArray); // Set(3) { 'ribas', 37, 'carlos@look.com' }
````

- `size`: Devuelve el número de elementos en el conjunto.

````js
const miSet = new Set([1, 2, 3]); 
console.log(miSet.size); // 3
````

- `values()`: Devuelve un objeto iterable que contiene los valores del conjunto.

````js
const miSet = new Set([1, 2, 3]); 
for (let valor of miSet.values()){ 
	console.log(valor); 
} // 1, 2, 3
````

- `keys()`: Devuelve un objeto iterable que contiene los valores del conjunto (similar a `values()`).

````js
const miSet = new Set([1, 2, 3]); 
for (let valor of miSet.keys()) { 
	console.log(valor); 
} // 1, 2, 3
````

- `entries()`: Devuelve un objeto iterable que contiene los pares clave-valor del conjunto.

````js
const miSet = new Set([1, 2, 3]);
for (let entrada of miSet.entries()) { 
	console.log(entrada); 
} // [1, 1], [2, 2], [3, 3]
````
- `forEach(callback)`: Ejecuta una función para cada elemento del conjunto.

````js
const miSet = new Set([1, 2, 3]); 
miSet.forEach(elemento => console.log(elemento)); // 1, 2, 3
````

### Map

En JavaScript, `Map` es una estructura de datos que almacena pares clave-valor, similar a un objeto. Sin embargo, a diferencia de los objetos, `Map` permite utilizar cualquier tipo de valor como clave, no solo cadenas de texto.

La estructura de datos `Map` es parte del estándar ECMAScript 2015 (ES6) y es compatible con la mayoría de los navegadores modernos y Node.js.

**Crear un Map**

Puedes crear un `Map` utilizando la palabra clave `new` y el constructor `Map`:

```js
const miMapa = new Map();
```

**Agregar pares clave-valor**

Puedes agregar pares clave-valor a un `Map` utilizando el método `set()`:

```js
miMapa.set('nombre', 'Juan');
miMapa.set('edad', 30);
```

**Obtener valores**

Puedes obtener un valor de un `Map` utilizando el método `get()`:

```js
const nombre = miMapa.get('nombre'); // devuelve "Juan"
```

**Verificar si una clave existe**

Puedes verificar si una clave existe en un `Map` utilizando el método `has()`:

```js
const tieneNombre = miMapa.has('nombre'); // devuelve true
```

**Eliminar pares clave-valor**

Puedes eliminar un par clave-valor de un `Map` utilizando el método `delete()`:

```js
miMapa.delete('edad');
```

**Iterar sobre un Map**

Puedes iterar sobre un `Map` utilizando el método `forEach()`:

```js
miMapa.forEach((valor, clave) => {
	console.log(`${clave}: ${valor}`);
});
```

**Convertir un Map a un arreglo**

Puedes convertir un `Map` a un arreglo utilizando el método `Array.from()`:

```js
const miArreglo = Array.from(miMapa);
```

**Convertir un Map a un objeto**

Puedes convertir un `Map` a un objeto utilizando el método `Object.fromEntries()`:

```js
const miObjeto = Object.fromEntries(miMapa);
```

**Casos de uso**

`Map` es útil cuando necesitas almacenar pares clave-valor con claves que no son cadenas de texto, como números o objetos. También es útil cuando necesitas iterar sobre los pares clave-valor en un orden específico.

En JavaScript, `Map` es una estructura de datos que almacena pares clave-valor, similar a un objeto. Sin embargo, a diferencia de los objetos, `Map` permite utilizar cualquier tipo de valor como clave, no solo cadenas de texto.

La estructura de datos `Map` es parte del estándar ECMAScript 2015 (ES6) y es compatible con la mayoría de los navegadores modernos y Node.js.

**Crear un Map**

Puedes crear un `Map` utilizando la palabra clave `new` y el constructor `Map`:

```js
const miMapa = new Map();
```

**Agregar pares clave-valor**

Puedes agregar pares clave-valor a un `Map` utilizando el método `set()`:

```js
miMapa.set('nombre', 'Juan');
miMapa.set('edad', 30);
```

**Obtener valores**

Puedes obtener un valor de un `Map` utilizando el método `get()`:

```js
const nombre = miMapa.get('nombre'); // devuelve "Juan"
```

**Verificar si una clave existe**

Puedes verificar si una clave existe en un `Map` utilizando el método `has()`:

```js
const tieneNombre = miMapa.has('nombre'); // devuelve true
```

**Eliminar pares clave-valor**

Puedes eliminar un par clave-valor de un `Map` utilizando el método `delete()`:

```js
miMapa.delete('edad');
```

**Iterar sobre un Map**

Puedes iterar sobre un `Map` utilizando el método `forEach()`:

```js
miMapa.forEach((valor, clave) => {
	console.log(`${clave}: ${valor}`);
});
```

**Convertir un Map a un arreglo**

Puedes convertir un `Map` a un arreglo utilizando el método `Array.from()`:

```js
const miArreglo = Array.from(miMapa);
```

**Convertir un Map a un objeto**

Puedes convertir un `Map` a un objeto utilizando el método `Object.fromEntries()`:

```js
const miObjeto = Object.fromEntries(miMapa);
```

**Casos de uso**

`Map` es útil cuando necesitas almacenar pares clave-valor con claves que no son cadenas de texto, como números o objetos. También es útil cuando necesitas iterar sobre los pares clave-valor en un orden específico.

Aquí hay algunos ejemplos de casos de uso:

- Caché: Puedes utilizar un `Map` para almacenar valores en caché con claves que no son cadenas de texto.
- Configuración: Puedes utilizar un `Map` para almacenar opciones de configuración con claves que no son cadenas de texto.
- Almacenamiento de datos: Puedes utilizar un `Map` para almacenar datos con claves que no son cadenas de texto.

**Diferencias con objetos**

Aquí hay algunas diferencias clave entre `Map` y objetos:

- Claves: `Map` permite utilizar cualquier tipo de valor como clave, mientras que los objetos solo permiten cadenas de texto.
- Orden: `Map` preserva el orden en que se agregaron los pares clave-valor, mientras que los objetos no garantizan un orden específico.
- Iteración: `Map` proporciona una forma integrada de iterar sobre los pares clave-valor, mientras que los objetos requieren que utilices un bucle `for...in` o `Object.keys()`.

En resumen, `Map` es una estructura de datos poderosa que proporciona una forma de almacenar pares clave-valor con claves que no son cadenas de texto, iterar sobre los pares clave-valor en un orden específico y convertir a arreglos u objetos.


----

### Referencias:

- [Eloquent JavaScript en Español (eloquent-javascript-es.vercel.app)](https://eloquent-javascript-es.vercel.app/)
- [Fundamentos de JavaScript - Aprende desarrollo web | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/JavaScript_basics)
- [JavaScript Tutorial (w3schools.com)](https://www.w3schools.com/js/DEFAULT.asp)
- [mouredev/hello-javascript: Curso para aprender el lenguaje de programación JavaScript desde cero y para principiantes. (github.com)](https://github.com/mouredev/hello-javascript)
- [Learn JavaScript  | web.dev](https://web.dev/learn/javascript)
- [The Modern JavaScript Tutorial](https://javascript.info/)
