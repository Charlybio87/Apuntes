# \<JavaScript> Conceptos | Prácticas | Herramientas

---

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

---

### Términos

#### **Declaración**

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

#### **Inicialización**

En el contexto de la informática, **inicialización** se refiere al proceso de establecer los valores iniciales para la ejecución de un programa.

````js
let name = `Charly`;
let surname = `Ribas`;
const dev = `Desarrollador`;
const nac = `15/02/1987`;
````

#### **Reasignación**

Se refiere a cambiar el valor de una variable después de haberla inicializado previamente. Cuando reasignas una variable, le asignas un nuevo valor, sobrescribiendo el valor anterior.

````js
let x = 5; // Inicialización
x = 10;    // Reasignación: ahora x tiene el valor 10

````

#### **Hoisting**

Permite usar funciones y variables antes de que se hayan declarado. Imagina el siguiente código:

````js
console.log(foo);
var foo = 'foo';
````

Aunque `foo` se asigna después de la línea `console.log`, este código genera `undefined` en lugar de un error. ¿Por qué? Porque el intérprete de JavaScript **mueve** las declaraciones al principio de su ámbito antes de ejecutar el código. A esto se le llama hoisting.

#### **Scope**

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

#### **Funcion**

Una función es un bloque de código que se puede ejecutar varias veces desde diferentes partes del programa. Las funciones son una forma de organizar y reutilizar el código, lo que hace que el programa sea más eficiente y fácil de mantener.

Es un bloque de código que se puede ejecutar varias veces desde diferentes partes del programa. Las funciones son una forma de organizar y reutilizar el código, lo que hace que el programa sea más eficiente y fácil de mantener.

**Características de las funciones en JavaScript**

1. **Nombre**: Las funciones tienen un nombre que se utiliza para llamarlas.
2. **Parámetros**: Las funciones pueden recibir parámetros, que son valores que se pasan a la función cuando se llama.
3. **Cuerpo**: El cuerpo de la función es el código que se ejecuta cuando se llama a la función.
4. **Return**: Las funciones pueden devolver un valor utilizando la palabra clave `return`.

**Tipos de funciones en JavaScript**

1. **Funciones declaradas**: Son funciones que se declaran utilizando la palabra clave `function`.
2. **Funciones expresadas**: Son funciones que se asignan a una variable o propiedad.
3. **Funciones anónimas**: Son funciones que no tienen un nombre y se utilizan como callbacks o como argumentos de otras funciones.
4. **Funciones flecha**: Son funciones que se declaran utilizando la sintaxis de flecha (`=>`) y son más concisas que las funciones declaradas.

1. **Función declarada**

```js
// saludar(recibe un valor: nombre)
function saludar(nombre) {
	console.log(`Hola, ${nombre}!`);
}
saludar('Juan'); // Output: Hola, Juan!
```

2. **Función expresada**

```js
const saludar = function(nombre) {
	console.log(`Hola, ${nombre}!`);
};
saludar('Juan'); // Output: Hola, Juan!
```

3. **Función anónima**

```js
setTimeout(function() {
	console.log('Hola, mundo!');
}, 2000);
```

4. **Función flecha**

```js
const saludar = (nombre) => {
	console.log(`Hola, ${nombre}!`);
};
saludar('Juan'); // Output: Hola, Juan!
```

#### **Funcion Flecha (Arrow Function)**

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

#### **Documentación**



---

### Principios

#### dry (dont repeat yourself )

> Es un principio de programación que sugiere que cada pieza de conocimiento debe estar representada de manera única en el sistema. En otras palabras, se trata de evitar la duplicación de código o lógica para hacer el software más mantenible y menos propenso a errores.

#### solid



---

### Tipos de variables

#### Sintaxis

````js
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

---

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

#### Diferencias entre primitivos y objetos

**Primitivos**

En JavaScript, los primitivos son valores simples que no son objetos. Los primitivos son:

- Números (number)
- Cadenas de texto (string)
- Booleanos (boolean)
- Null
- Undefined

Los primitivos no tienen métodos ni propiedades, solo valor.

**Objetos**

Los objetos en JavaScript son colecciones de pares clave-valor. Un objeto puede tener métodos y propiedades. Los objetos son instancias de la clase Object.

**Diferencias clave**

- **Inmutabilidad**: Los primitivos son inmutables, lo que significa que no se pueden cambiar una vez creados. Los objetos son mutables, lo que significa que se pueden cambiar después de ser creados.
- **Métodos y propiedades**: Los primitivos no tienen métodos ni propiedades, mientras que los objetos sí.
- **Comparación**: Los primitivos se comparan por valor, mientras que los objetos se comparan por referencia.

**Métodos y propiedades de objetos**

Los objetos en JavaScript pueden tener métodos y propiedades. Los métodos son funciones que se pueden llamar en un objeto, mientras que las propiedades son valores que se almacenan en un objeto.

- **Métodos**: Los métodos se definen usando la palabra clave `function` dentro de un objeto. Por ejemplo:

```js
const persona = {
  nombre: 'Juan',
  edad: 30,
  saludar: function() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }
};
```

- **Propiedades**: Las propiedades se definen usando la sintaxis `clave: valor` dentro de un objeto. Por ejemplo:

```js
const persona = {
  nombre: 'Juan',
  edad: 30
};
```

**Funcionalidad de objetos**

Los objetos en JavaScript tienen varias funcionalidades, como:

- **Prototipos**: Los objetos pueden heredar propiedades y métodos de otros objetos mediante la cadena de prototipos.
- **Constructores**: Los objetos pueden ser creados usando constructores, que son funciones especiales que retornan un objeto nuevo.
- **Métodos de instancia**: Los objetos pueden tener métodos de instancia, que son métodos que se llaman en una instancia específica de un objeto.

**Ejemplo de código**

Aquí te dejo un ejemplo de código que muestra la diferencia entre primitivos y objetos:

```js
// Primitivo
const nombre = 'Juan';
console.log(nombre); // "Juan"

// Objeto
const persona = {
  nombre: 'Juan',
  edad: 30
};
console.log(persona); // { nombre: "Juan", edad: 30 }

// Método de objeto
persona.saludar = function() {
  console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
};
persona.saludar(); // "Hola, mi nombre es Juan y tengo 30 años."
```

---

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

---

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

---

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
for (inicialización; condición; incremento (o decremento)) {
// código a ejecutar en cada iteración
}
```

Ejemplo:

```js
for (let i = 0; i < 5; i++) {
	console.log(i);
}
// 0
// 1
// 2
// 3
// 4
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

##### 6. ForEach()

La estructura `forEach` se puede considerar como una forma de loop que se ejecuta automáticamente para cada elemento del array, sin necesidad de escribir explícitamente un bucle `for` o `while`.

Es un tipo de iterador conocido como "callback-based iterator" (iterador basado en callbacks), o sea,  función que se va a ejecutar para cada elemento del array.

````js
//array.forEach(callbackFunction => {})
const arrayNum = [1,20,45]
arrayNum.forEach(numero => {
    if (numero >= 10){
    	console.log(`# mayor de 10: ${numero}`)	
    } 
}) 	
	// # mayor de 10: 20
	// # mayor de 10: 45

const resultado = productos.forEach(
    (producto) => {
        console.log('hola ' + producto.nombre)
    }
)
console.log(resultado)
````

##### 7.Break (Romper)

La instrucción `break` se utiliza para salir de un bucle o una estructura de control de flujo. La sintaxis es la siguiente:

```js
break;
```

##### 8. Continue (Continuar)

La instrucción `continue` se utiliza para saltar a la siguiente iteración de un bucle. La sintaxis es la siguiente:

```js
continue;
```

##### 9. Return (Retornar)

La instrucción `return` se utiliza para salir de una función y devolver un valor. La sintaxis es la siguiente:

```js
return valor;
```

Es importante destacar que las estructuras de control de flujo se utilizan para controlar el orden en que se ejecutan las instrucciones de un programa, lo que permite crear algoritmos más eficientes y escalables.

---

### Funciones

Una función es un bloque de código que se puede ejecutar varias veces desde diferentes partes del programa. Las funciones son fundamentales en la programación y sirven para:

**¿Para qué sirven las funciones?**

1. **Reutilización de código**: Las funciones permiten reutilizar código, evitando la duplicación de código y reduciendo la cantidad de líneas de código.
2. **Organización del código**: Las funciones ayudan a organizar el código en bloques lógicos y fáciles de entender.
3. **Abstracción**: Las funciones pueden abstraer complejidad, permitiendo que el código sea más fácil de entender y mantener.
4. **Reutilización de lógica**: Las funciones pueden ser reutilizadas en diferentes partes del programa, reduciendo la cantidad de código que se necesita escribir.

#### **Tipos de funciones **

- Funciones declaradas (Function Declaration):  Se definen utilizando la palabra clave `function` seguida del nombre de la función y los parámetros entre paréntesis.

```js
function suma(a, b) {
	return a + b;
}
```

- Funciones expresadas (Function Expression): Se definen asignando una función a una variable.

```js
const suma = function(a, b) {
	return a + b;
};
```

- Funciones flecha (Arrow Function): Se definen utilizando la sintaxis `=>` y son más concisas que las funciones declaradas y expresadas.

```js
const suma = (a, b) => a + b;

const resultado = productos.filter( (producto) => { 
    return producto.nombre.includes('TV')
	}
)
const resultado_3 = productos.filter( producto => producto.nombre.includes('TV') ) // S/parentesis cdo tiene un solo paramentro

const filtrar = (array, condicion) => {  // CallBack: condicion
    const resultado = []
    for(const elemento of array){
        if(condicion(elemento)){
            resultado.push(elemento)
        }
    }
    return resultado
}
const filtroPorNombre = (producto) => producto.nombre.includes('TV')
console.log(filtrar(productos, filtrarPorNombre))
```

- Funciones anónimas (Anonymous Function): Se definen sin un nombre y se utilizan como argumentos de otras funciones o como valores de variables.

```js
const saludo = function() {
  return "Hola";
};

setTimeout(function() {
  console.log("Hola después de 3 segundos");
}, 3000);

// Lista de personas
const personas = [
  { nombre: "Juan", edad: 25 },
  { nombre: "Ana", edad: 17 },
  { nombre: "Luis", edad: 30 },
  { nombre: "María", edad: 15 }
];

// Usamos una función anónima para filtrar a las personas mayores de 18 años
const mayoresDeEdad = personas.filter(function(persona) {
  return persona.edad > 18;
});
console.log(mayoresDeEdad);

console.log(filter(personas, (persona) => persona.edad > 25))
// Funcion Normal S/Nombre
const resultado_2 = productos.filter(
    function(producto){
        return producto.nombre.includes('TV') 
    }
) 
```

- Funciones asíncronas (Async Function): Se definen utilizando la palabra clave `async` y permiten trabajar con código asíncrono de manera más sencilla.

```js
async function suma(a, b) {
	return a + b;
}
```

- Funciones generadoras (Generator Function): Se definen utilizando la palabra clave `function*` y permiten crear iteradores que pueden ser utilizados para generar secuencias de valores.

```js
function* suma(a, b) {
	yield a + b;
}
```

En resumen, las funciones en JavaScript son fundamentales para la programación y se utilizan para reutilizar código, organizar el código y abstraer complejidad. Hay diferentes tipos de funciones, cada una con sus propias características y usos.

#### **Declaraciones**

En JavaScript, las funciones pueden ser declaradas antes o después de ser llamadas, dependiendo del tipo de declaración y del alcance de la función.

**Declaración de función con `function`**

Cuando se declara una función con la palabra clave `function`, se puede llamar antes o después de su declaración. Esto se debe a que las declaraciones de función con `function` son "hoisted" (elevadas) al principio del ámbito de la función, lo que significa que la función se define antes de que se ejecute cualquier código.

Ejemplo:

```js
console.log(miFuncion()); // "Hola, mundo!"

function miFuncion() {
	return "Hola, mundo!";
}
```

En este ejemplo, la función `miFuncion` se declara después de ser llamada, pero debido a la "hoisting", la función se define antes de que se ejecute el código.

**Declaración de función con `let` o `const`**

Cuando se declara una función con `let` o `const`, la función no se puede llamar antes de su declaración. Esto se debe a que las declaraciones con `let` y `const` no son "hoisted" al principio del ámbito de la función.

Ejemplo:

```js
console.log(miFuncion()); // Error: miFuncion is not defined

let miFuncion = function() {
	return "Hola, mundo!";
}
```

En este ejemplo, la función `miFuncion` se declara con `let`, por lo que no se puede llamar antes de su declaración.

**Declaración de función con expresión de función**

Cuando se declara una función con una expresión de función (es decir, una función anónima asignada a una variable), la función no se puede llamar antes de su declaración.

Ejemplo:

```js
console.log(miFuncion()); // Error: miFuncion is not defined

const miFuncion = () => {
	return "Hola, mundo!";
}
```

En este ejemplo, la función `miFuncion` se declara con una expresión de función, por lo que no se puede llamar antes de su declaración.

En resumen:

- Las declaraciones de función con `function` pueden ser llamadas antes o después de su declaración.
- Las declaraciones de función con `let` o `const` no pueden ser llamadas antes de su declaración.
- Las declaraciones de función con expresión de función no pueden ser llamadas antes de su declaración.

Es importante tener en cuenta que, aunque las declaraciones de función con `function` pueden ser llamadas antes de su declaración, es una buena práctica declarar las funciones antes de usarlas para evitar confusiones y errores.

#### **Anidadas**

Las funciones anidadas se llaman de la misma manera que las funciones normales, pero con una pequeña diferencia. La función anidada se llama desde dentro de la función externa que la contiene.

Aquí hay un ejemplo:

```js
function externa() {
	function interna() {
		console.log("Soy la función interna");
	}
	interna(); // Llamada a la función interna desde dentro de la función externa
}
externa(); // Llamada a la función externa
```

En este ejemplo, la función `interna` se llama desde dentro de la función `externa` utilizando el nombre de la función `interna`. La función `externa` se llama desde fuera utilizando el nombre de la función `externa`.

Si intentamos llamar a la función `interna` desde fuera de la función `externa`, obtendremos un error, porque la función `interna` no está en el ámbito global:

```js
function externa() {
	function interna() {
		console.log("Soy la función interna");
	}
}
interna(); // Error: interna is not defined
```

Para llamar a una función anidada desde fuera de la función externa, debemos devolver la función anidada desde la función externa y asignarla a una variable. Luego, podemos llamar a la función anidada utilizando la variable:

```js
function externa() {
	function interna() {
		console.log("Soy la función interna");
	}
	return interna;
}
const miFuncionInterna = externa();
miFuncionInterna(); // Llamada a la función interna
```

En este ejemplo, la función `externa` devuelve la función `interna` y se asigna a la variable `miFuncionInterna`. Luego, podemos llamar a la función `interna` utilizando la variable `miFuncionInterna`.

#### **Función c/Orden Superior**

**¿Qué son las funciones de orden superior?**

Una función de orden superior es una función que toma otra función como parámetro o devuelve una función como resultado. En otras palabras, una función de orden superior es una función que se puede utilizar como una función "normal" pero que también puede ser utilizada como un argumento o un valor de retorno de otra función.

**Ejemplos de funciones de orden superior**

1. **Arrow Function**

````js
function applyFunc(func, param) {
    func(param)
}
const myFunc4 = (name) => console.log(`Hola, ${name}!!`)
applyFunc(myFunc4,"Funcion de Orden Superior")
// Hola, Funcion de Orden Superior
````

2. **Filter**: La función `filter()` es un ejemplo clásico de una función de orden superior. Toma una función como parámetro y devuelve un nuevo array con los elementos que cumplen con la condición especificada por la función pasada como parámetro.

```js
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(x => x % 2 === 0); // [2, 4]
```

En este ejemplo, la función `filter()` toma una función anónima como parámetro, que se utiliza para determinar si un elemento del array es par o no.

3. **Map**: La función `map()` es otra función de orden superior que toma una función como parámetro y devuelve un nuevo array con los resultados de aplicar la función a cada elemento del array original.

```js
const numbers = [1, 2, 3, 4, 5];
const doubleNumbers = numbers.map(x => x * 2); // [2, 4, 6, 8, 10]
```

En este ejemplo, la función `map()` toma una función anónima como parámetro, que se utiliza para doblar cada elemento del array.

4. *Reduce**: La función `reduce()` es una función de orden superior que toma una función como parámetro y devuelve un valor que es el resultado de aplicar la función a cada elemento del array, de izquierda a derecha.

```js
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((acc, current) => acc + current, 0); // 15
```

En este ejemplo, la función `reduce()` toma una función anónima como parámetro, que se utiliza para sumar cada elemento del array.

**Ventajas de las funciones de orden superior**

Las funciones de orden superior ofrecen varias ventajas, como:

- **Modularidad**: Las funciones de orden superior permiten separar la lógica de la aplicación en pequeñas funciones reutilizables.
- **Flexibilidad**: Las funciones de orden superior permiten cambiar la lógica de la aplicación sin modificar el código existente.
- **Reutilización**: Las funciones de orden superior permiten reutilizar el código en diferentes contextos.

**Conclusión**

En resumen, las funciones de orden superior son una característica fundamental en JavaScript que permiten crear funciones más flexibles y reutilizables. Al entender cómo funcionan las funciones de orden superior, podrás escribir código más eficiente y escalable.

#### Import () and Export()

````html
<head>
    <script src="script.js" type="module"></script>
</head>
````

````js
// math.js
export function sumar(a,b){
    return a + b
}
export function name(alumno){
    return 'Hola ${alumno}'
}
````

````js
// script.js
import {sumar as add, nombre as name} from './math.js'
console.log(add(1,2));
console.log(name('Carlos'));
````

---

### CallBack

[Función Callback - Glosario de MDN Web Docs: Definiciones de términos relacionados con la Web | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Glossary/Callback_function)

Una callback (también conocida como función de devolución de llamada) es una función que se pasa como argumento a otra función, y se ejecuta cuando se produce un evento o se completa una tarea específica.

**Función:**

La función de una callback es permitir que una función se comunique con otra función después de que se haya completado una tarea o se haya producido un evento. De esta manera, la función que llama a la callback puede continuar ejecutándose sin bloquearse, mientras que la callback se encarga de manejar el resultado o el evento.

**Descripción en JavaScript:**

En JavaScript, una callback es una función que se pasa como argumento a otra función, utilizando el siguiente patrón:

```JS
function funcionPrincipal(callback) {
// Código que se ejecuta antes de llamar a la callback
callback(); // Llamada a la callback
// Código que se ejecuta después de llamar a la callback
}

function callback() {
// Código que se ejecuta cuando se llama a la callback
}
```

Por ejemplo, supongamos que queremos hacer una solicitud de Datos y  procesar la respuesta cuando se recibe. Podemos utilizar una callback para manejar la respuesta y validación :

```js
/*Funciones*/
const solicitarDato = (mensaje, errorMensaje, validacion) => {
    let dato = prompt(mensaje)
    while( !validacion(dato) ){
        dato = prompt(errorMensaje)
    }
    return dato
} 

// CallBack --> Validaciones
const validacionNombre = (valor) => {
    return Boolean(valor && isNaN(valor) && !valor.includes('*'))
}
const validacionEdad = (valor) => {
    return Boolean(valor && !isNaN(valor))
}

/*LLamado a funciones:*/
let nombre = solicitarDato(
    'Ingrese el nombre', 
    'Error al ingresar nombre, recuerda que no se permiten numeros o asteriscos',
    validacionNombre // funcion pasada por argumento (referencia de la funcion)
)
let edad = solicitarDato(
    'Ingrese su edad',
    'Error al ingresar la edad',
    validacionEdad // funcion pasada por argumento
) 
```

En este ejemplo, primero se realizo la customización de los mensaje que recibirán los `prompt(mensaje)`, en segundo lugar se realiza las validaciones correspondientes a través de la CallBack.

La función pasada por argumento se la conoce como `Referencia de la Función`. Se puede observar que no se le coloca el ( ) porque sino se estaría `invocando` y estaría entregando un valor en este caso un booleano.  La invocación de la función se realiza por detrás (por eso se lo conoce por CALLBACK)  dentro de la función solicitarDato().

**Ventajas:**

1. **Asincronía**: Las callbacks permiten que el código se ejecute de manera asincrónica, lo que significa que no se bloquea la ejecución del código mientras se espera a que se complete una tarea.
2. **Flexibilidad**: Las callbacks permiten que se puedan manejar diferentes resultados o eventos de manera personalizada.
3. **Reutilización del código**: Las callbacks permiten reutilizar el código y evitar la duplicación de lógica.

**Desventajas:**

1. **Complejidad**: Las callbacks pueden hacer que el código sea más complejo y difícil de leer.
2. **Callback hell**: Cuando se utilizan demasiadas callbacks anidadas, puede generar un "callback hell" que hace que el código sea difícil de entender y mantener.

En resumen, las callbacks son una herramienta poderosa en JavaScript que permiten manejar eventos y resultados de manera asincrónica y flexible, pero requieren cuidado y atención para evitar la complejidad y el "callback hell".

---

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

- `find()`: Busca el primer elemento que cumpla con una condición y lo devuelve. Sino cumple con la condición devuelve undefined.

````js
const resultado = personas.find((persona) => {
    return persona.nombre === 'pepe'
})
console.log(resultado)

const producto_70 = productos.find(producto => producto.id === 70)
console.log(producto_70) //no cumple con la condicion: UNDEFINED.
````

> Find() siempre devuelve "un" objeto.

- `findIndex()`: Busca la posición del primer elemento que cumpla con una condición y devuelve su índice. Sino cumple con la condición devuelve -1.

````js
const posicionProducto = producto.findIndex(producto => producto.id === 1)
console.log(prosicionProducto)

````

- `filter()`: Crea un nuevo arreglo con los elementos que cumplen con una condición.

````js
const resultado = productos.filter((producto) => producto.nombre.includes('TV'))

console.log(resultado)
````

> Filter() siempre retorna un array, el array estará compuesto por los elementos que hayan cumplido con la callback.

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

---

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

#### **Propiedades**

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

````js
// Modificación de propiedades

person.name = "Brais Moure"
console.log(person.name)

console.log(typeof person.age)
person.age = "37"
console.log(person.age)
console.log(typeof person.age)

// Eliminación de propiedades

delete person.age
console.log(person)

// Nueva propiedad

person.email = "braismoure@mouredev.com"
person["age"] = 37

console.log(person)
````

#### **Métodos (Funciones)**

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

let person2 = {
    name: "Brais",
    age: 37,
    alias: "MoureDev",
    walk: function () {
        console.log("La persona camina.")
    }
}
person2.walk()
```

##### Anidación de Objetos

````js
let person3 = {
    name: "Brais",
    age: 37,
    alias: "MoureDev",
    walk: function () {
        console.log("La persona camina.")
    },
    job: {
        name: "Programador",
        exp: 15,
        work: function () {
            console.log(`La persona de ${this.exp} años de experiencia trabaja.`)
        }
    }
}

console.log(person3)
````

##### Igualdad de objetos

````js
let person4 = {
    name: "Brais Moure",
    alias: "CharlyDev",
    email: "braismoure@mouredev.com",
    age: 37
}

console.log(person)
console.log(person4)

console.log(person == person4) // false
console.log(person === person4) // false
// se comparan dos valores de direccion de memoria distintas.

console.log(person.name == person4.name) // true
````

> Los valores como se guardan en memoria no son como el valor  asociado en si en los objetos, sino que es un valor de referencia , es decir, es una dirección de memoria.

##### Funciones como objetos

````js
function Person(name, age) { // Debería ser una clase
    this.name = name
    this.age = age
}
let person5 = new Person("Brais", 37)
console.log(person5)
console.log(typeof person5) // object
````

> Esta función actúa como un constructor. Se crea un objeto. Este tipo de función es útil cuando se desea construir múltiples instancias. 

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

#### Iteración

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
frutas.forEach(fruta => {console.log(fruta)})
```

> ❗Recordar: que no se puede iterar sobre un objeto de manera directa. Los métodos forEach se usan para iterar sobre arreglos (arrays), no sobre objetos.

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

Object.keys(persona).forEach(key => {
    console.log(`${key}: ${persona[key]}`);
});
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

----

### Destructuring y Spreading

Destructuring y spreading son dos conceptos relacionados en JavaScript que permiten manipular y trabajar con objetos y arreglos de manera más eficiente y concisa.

#### **Destructuring (Desestructuración)**

La desestructuración es una sintaxis especial que permite extraer valores de arreglos o propiedades de objetos y asignarlos a variables individuales de manera más concisa y legible. Fue introducida en ECMAScript 6 (ES6) y simplifica el proceso de extracción de datos.

La desestructuración se utiliza principalmente para:

- Asignar múltiples variables de manera concisa
- Intercambiar valores de dos variables sin necesidad de una variable temporal
- Extraer propiedades de objetos y elementos de un arreglo

**Ejemplos de Destructuring**

Trabajando con Arrays:  se emplea [ ]

```js
const array = [1, 2, 3, 4, 5];
const [first, second, third] = array;
console.log(first);  // 1
console.log(second); // 2
console.log(third);  // 3
console.log(four);   // undefined
```

````js
const myArray = [1, 2, 3, 4]

// Sintaxis arrays

let [myValue0, myValue1, myValue2, myValue3, myValue4] = myArray
console.log(myValue0)
console.log(myValue1)
console.log(myValue2)
console.log(myValue3)
console.log(myValue4)

// Sintaxis arrays con valores predeterminados

let [myValue5 = 0, myValue6 = 0, myValue7 = 0, myValue8 = 0, myValue9 = 0] = myArray
console.log(myValue5)
console.log(myValue6)
console.log(myValue7)
console.log(myValue8)
console.log(myValue9)

// Ignorar elementos array

let [myValue10, , , myValue13] = myArray
console.log(myValue10)
console.log(myValue13)
````

Trabajando con Objetos: se emplea { }

```js
const person = { name: 'Alice', age: 25 };
const { name, age } = person;
console.log(name);  // Alice
console.log(age);   // 25
```

````js
let person = {
    name: "Brais",
    age: 37,
    alias: "MoureDev"
}

// Sintaxis objects

let { name, age, alias } = person
console.log(name)
console.log(age)
console.log(alias)
console.log(person) // { name: 'Brais', age: 37, alias: 'MoureDev' }

// Sintaxis objects con valores predeterminados

let { name2, age2, alias2, email = "email@email.com" } = person
console.log(name2) // No existe
console.log(age2)  // No existe
console.log(alias2)  // No existe
console.log(email)

// Sintaxis objects con nuevos nombres de variables

let { alias: alias3, name: name3, age: age3 } = person
console.log(name3)
console.log(age3)
console.log(alias3)
````

````js
// Objects anidados

let person3 = {
    name: "Brais",
    age: 37,
    alias: "MoureDev",
    walk: function () {
        console.log("La persona camina.")
    },
    job: {
        name: "Programador",
        exp: 15,
        work: function () {
            console.log(`La persona de ${this.age} años de experiencia trabaja.`)
        }
    }
}

let { name: name4, job: { name: jobName } } = person3

console.log(name4)
console.log(jobName)
````

#### **Spreading (Expansión)**

La expansión es una sintaxis que permite a un elemento iterable (como un arreglo o cadena) ser expandido en lugares donde cero o más argumentos (para llamadas de función) o elementos (para literales de arreglo) son esperados, o a un objeto ser expandido en lugares donde cero o más pares de valores clave (para literales de objeto) son esperados.

**Ejemplos de Spreading**

Trabajando con Funciones:

```js
function myFunction(x, y, z) {}
var args = [0, 1, 2];
myFunction(...args);
```

Trabajando con Arreglos:

```js
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
arr1 = [...arr2, ...arr1]; // arr1 is now [3, 4, 5, 0, 1, 2]
```

````js
const myArray = [1, 2, 3, 4]

// Sintaxis arrays

let myArray2 = [...myArray, 5, 6]

console.log(myArray2)

// Copia de arrays

let myArray3 = [...myArray]

console.log(myArray3)

// Combinación de arrays

let myArray4 = [...myArray, ...myArray2, ...myArray3]

console.log(myArray4)
````

Trabajando con Objetos:

```js
var obj1 = { foo: "bar", x: 42 };
var obj2 = { foo: "baz", y: 13 };
var mergedObj = { ...obj1, ...obj2 }; // mergedObj is now { foo: "baz", x: 42, y: 13 }
```

````js
let person = {
    name: "Brais",
    age: 37,
    alias: "MoureDev"
}

// Sintaxis objects

let person4 = { ...person, email: "braismoure@mouredev.com" }

console.log(person4)

// Copia de objects

let person5 = { ...person }

console.log(person5)
````

**Comparación entre Destructuring y Spreading**

Ambas sintaxis son utilizadas para trabajar con objetos y arreglos, pero tienen objetivos diferentes:

- La desestructuración se utiliza para extraer valores de objetos y arreglos y asignarlos a variables individuales.
- La expansión se utiliza para expandir objetos y arreglos en lugares donde se esperan argumentos o elementos.

**Métodos y Propiedades**

No hay métodos específicos para la desestructuración y la expansión, ya que son sintaxis especiales que se utilizan en el lenguaje. Sin embargo, hay algunas propiedades y métodos relacionados que se pueden utilizar en combinación con la desestructuración y la expansión:

- `Object.assign()`: se utiliza para copiar propiedades de un objeto a otro.
- `Array.prototype.concat()`: se utiliza para concatenar arreglos.
- `Array.prototype.unshift()`: se utiliza para insertar elementos al inicio de un arreglo.

---

### Clases

una clase (class) es una plantilla para crear objetos que comparten una estructura y comportamiento comunes. Las clases se introdujeron en JavaScript con la versión ECMAScript 2015 (ES6).

**Diferencia con primitivos**

Los primitivos (primitive types) son tipos de datos básicos en JavaScript, como números (Number), cadenas de texto (String), booleanos (Boolean), null y undefined. Estos tipos de datos no tienen propiedades ni métodos asociados.

Por otro lado, las clases y objetos son instancias de una plantilla que define una estructura y comportamiento específicos. Las clases y objetos tienen propiedades (datos) y métodos (funciones) asociados.

**Diferencia con objetos**

En JavaScript, un objeto (object) es una instancia de una clase o una colección de pares clave-valor. Los objetos pueden ser creados utilizando la sintaxis de objeto literal `{}` o mediante la creación de una instancia de una clase utilizando el operador `new`.

La principal diferencia entre una clase y un objeto es que una clase es una plantilla para crear objetos, mientras que un objeto es una instancia específica de esa plantilla.

**Descripción de métodos, propiedades y funcionalidad**

**Métodos**: Son funciones que se definen dentro de una clase y se utilizan para realizar acciones específicas en objetos instanciados de esa clase. Los métodos pueden acceder y modificar las propiedades del objeto.

**Propiedades**: Son los datos asociados a un objeto. Las propiedades pueden ser de tipo primitivo o ser objetos complejos.

**Funcionalidad**: La funcionalidad de una clase se refiere a la capacidad de crear objetos que pueden realizar acciones específicas y tener un comportamiento determinado.

**Ejemplo de clase en JavaScript**

```js
class Persona {
  // Propiedades
  nombre;
  edad;

  // Constructor
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }

// Método
  saludar() {
    console.log(`Hola, soy ${this.nombre} y tengo ${this.edad} años.`);
  }
}

// Crear objeto instancia de la clase Persona
const persona = new Persona('Juan', 30);
persona.saludar(); // Output: Hola, soy Juan y tengo 30 años.
```

En este ejemplo, la clase `Persona` tiene dos propiedades (`nombre` y `edad`) y un método (`saludar`). El constructor se utiliza para inicializar las propiedades cuando se crea un objeto instancia de la clase. El método `saludar` utiliza las propiedades del objeto para generar un mensaje de saludo.

La palabra reservada `this` suele apuntar a la instancia de la clase, no a la clase en sí. Cuando crea una nueva instancia de una clase, `this` se enlaza a esa instancia, permitiéndole acceder a sus propiedades y métodos.

#### **Estructura básica de una clase**

```js
class NombreClase {
  // Propiedades y métodos de la clase
}
```

Donde `NombreClase` es el nombre de la clase.

**Estructura de una clase**

La estructura de una clase en JavaScript puede incluir:

- **Propiedades**: variables que se definen dentro de la clase y se utilizan para almacenar valores.
- **Métodos**: funciones que se definen dentro de la clase y se utilizan para realizar acciones.
- **Constructor**: un método especial que se llama cuando se crea un objeto a partir de la clase.

#### **Constructor**

Un constructor en JavaScript es un método especial que se llama cuando se crea un objeto a partir de una clase. El constructor se utiliza para inicializar las propiedades de la clase y se define con la palabra clave `constructor`. La estructura básica de un constructor es la siguiente:

```js
class NombreClase {
  constructor(parametros) {
    // Inicialización de propiedades
  }
}
```

Donde `parametros` son los parámetros que se pasan al constructor cuando se crea un objeto.

````js
// Plantilla (Clase)
class Person {
    constructor(name, age, alias) {
        this.name = name
        this.age = age
        this.alias = alias
    }
}
````

#### Instanciación

````js
// Sintaxis

let person = new Person("Brais", 37, "MoureDev")
let person2 = Person("Brais", 37, "MoureDev")

console.log(person)  // Person { name: 'Brais', age: 37, alias: 'MoureDev' }
console.log(person2) // Error
````

en otro caso, si se desea generar un nueva clase. En el constructor se puede asignar valores predefinidos a los parámetros en el caso que se instancie sin un parámetro. 

````js
// Valores por defecto

class DefaultPerson {
    constructor(name = "Sin nombre", age = 0, alias = "Sin alias") {
        this.name = name
        this.age = age
        this.alias = alias
    }
}
let person3 = new DefaultPerson("Brais", 37)
console.log(person3) // DefaultPerson { name: 'Brais', age: 37, alias: 'Sin alias' }

// Acceso a propiedades

console.log(person3.alias)
console.log(person3["alias"])
person3.alias = "MoureDev"
console.log(person3.alias)
````

#### Funciones

````js
// Funciones en clases

class PersonWithMethod {
    constructor(name, age, alias) {
        this.name = name
        this.age = age
        this.alias = alias
    }
    walk() {
        console.log("La persona camina.")
    }
}
let person4 = new PersonWithMethod("Brais", 37, "MoureDev")
person4.walk()
````

#### Propiedades Publicas y Privadas

##### **Propiedades públicas**

Las propiedades públicas, son propiedades que se pueden acceder directamente desde una instancia de una clase. Se definen utilizando la palabra clave `this` dentro del constructor de la clase o utilizando un inicializador de propiedades.

Ejemplo:

```js
class Persona {
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }
}

const persona = new Persona('Juan', 30);
console.log(persona.nombre); // Juan
console.log(persona.edad); // 30
```

En este ejemplo, `nombre` y `edad` son propiedades normales que se pueden acceder directamente desde la instancia `persona`.

La desventaja de las clases publicas es que son de fácil acceso a las propiedades lo cual pueden ser modificarlas o impresas, no resguardando la integridad de la información.  

##### **Propiedades Privadas**

Las propiedades privadas, por otro lado, son propiedades que no se pueden acceder directamente desde una instancia de una clase. Se definen utilizando un símbolo de hash `#` antes del nombre de la propiedad, o sea, debe inicializarse.

Ejemplo:

```js
class Persona {
    #contraseña;
  
    constructor(nombre, edad, contraseña) {
      this.nombre = nombre;
      this.edad = edad;
      this.#contraseña = contraseña;
    }
  
    autenticar(contraseña) {
      return this.#contraseña === contraseña;
    }
  }
  
  const persona = new Persona('Juan', 30, 'miclave secreta');
  console.log(persona.contraseña); // undefined
  console.log(persona.autenticar('miclave secreta')); // true
  console.log(persona);
// Persona { nombre: 'Juan', edad: 30 }
  persona.contraseña = "new clave Secreta" // nuevo prametro
  console.log(persona);
// Persona { nombre: 'Juan', edad: 30, 'contraseña': 'new clave Secreta' }
```

En este ejemplo, `contraseña` es una propiedad privada que no se puede acceder directamente desde la instancia `persona`. En su lugar, solo se puede acceder a través del método `autenticar`. Al intentar modificar la propiedad `contraseña`, lo que se genero fue agregar un nuevo parámetro, por lo que **`contraseña` no es lo mismo que `#contraseña`**.

Nota que las propiedades privadas no están completamente soportadas en todos los navegadores y entornos, y actualmente son una propuesta de fase 3 en el estándar ECMAScript.

**Propiedades Privadas en Clases de JavaScript**

Las propiedades privadas en JavaScript son una forma de encapsular datos dentro de una clase, de manera que solo puedan ser accedidos a través de métodos específicos. Esto ayuda a proteger la integridad de los datos y a prevenir accesos no autorizados.

**Definir Propiedades Privadas**

Para definir una propiedad privada en una clase de JavaScript, se utiliza el símbolo de hash `#` antes del nombre de la propiedad. Por ejemplo:

```js
class Persona {
  #nombre;
  #edad;

  constructor(nombre, edad) {
    this.#nombre = nombre;
    this.#edad = edad;
  }
}
```

En este ejemplo, `nombre` y `edad` son propiedades privadas que no pueden ser accedidas directamente desde fuera de la clase.

##### Getters y Setters

````js
class GetSetPerson {
    #name
    #age
    #alias
    #bank
    constructor(name, age, alias, bank) {
        this.#name = name
        this.#age = age
        this.#alias = alias
        this.#bank = bank
    }
}

person6 = new GetSetPerson("Brais", 37, "MoureDev", "IBAN123456789")
console.log(person6) // GetSetPerson {}
````

Como se observa en el siguiente caso el acceso a las propiedades `person6` nos muestra por console {} vacías. Para ello se recurre a ciertos métodos,

**Acceder a Propiedades Privadas**

Para acceder a una propiedad privada, se debe utilizar un método que esté definido dentro de la clase. Por ejemplo:

```js
class Persona {
  #nombre;
  #edad;

  constructor(nombre, edad) {
    this.#nombre = nombre;
    this.#edad = edad;
  }

  getNombre() {
    return this.#nombre;
  }

  getEdad() {
    return this.#edad;
  }
}

const persona = new Persona('Juan', 30);
console.log(persona.getNombre()); // Juan
console.log(persona.getEdad()); // 30
```

En este ejemplo, los métodos `getNombre()` y `getEdad()` permiten acceder a las propiedades privadas `nombre` y `edad`, respectivamente.

**Modificar Propiedades Privadas**

Para modificar una propiedad privada, se debe utilizar un método que esté definido dentro de la clase. Por ejemplo:

```js
class Persona {
  #nombre;
  #edad;

  constructor(nombre, edad) {
    this.#nombre = nombre;
    this.#edad = edad;
  }

  setNombre(nombre) {
    this.#nombre = nombre;
  }

  setEdad(edad) {
    this.#edad = edad;
  }
}

const persona = new Persona('Juan', 30);
persona.setNombre('Pedro');
persona.setEdad(31);
console.log(persona.getNombre()); // Pedro
console.log(persona.getEdad()); // 31
```

En este ejemplo, los métodos `setNombre()` y `setEdad()` permiten modificar las propiedades privadas `nombre` y `edad`, respectivamente.

#### Herencia

La herencia se refiere a la capacidad de una clase para heredar propiedades y métodos de otra clase. 

##### **Herencia de propiedades públicas**

En JavaScript, las propiedades públicas se definen directamente en el objeto o clase. Cuando una clase hereda de otra, automáticamente hereda todas las propiedades públicas de la clase padre.

Aquí hay un ejemplo:

```js
class Persona {
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }

  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre} y tengo ${this.edad} años.`);
  }
}

class Estudiante extends Persona {
  constructor(nombre, edad, carrera) {
    super(nombre, edad);
    this.carrera = carrera;
  }

  estudiar() {
    console.log(`Estoy estudiando ${this.carrera}.`);
  }
}

const estudiante = new Estudiante('Juan', 20, 'Ingeniería');
estudiante.saludar(); // "Hola, mi nombre es Juan y tengo 20 años."
estudiante.estudiar(); // "Estoy estudiando Ingeniería."
```

La palabra reservada `extends` se utiliza para crear una clase que es una subclase de otra clase. Esto permite heredar las propiedades y métodos de la clase padre y agregar nuevos o sobre escribir los existentes .

La palabra reservada `super` se utiliza para acceder a las propiedades y métodos de una clase padre (o clase base) desde una clase hija (o clase derivada).

Cuando se utiliza `super` en una clase hija, permite llamar a los métodos y acceder a las propiedades de la clase padre. Esto es especialmente útil cuando se quiere sobre escribir un método de la clase padre en la clase hija, pero aún se necesita llamar al método original de la clase padre.

En este ejemplo, la clase `Estudiante` hereda las propiedades `nombre` y `edad` de la clase `Persona`, y también define su propia propiedad `carrera`. O sea, la clase `Estudiante` extiende la clase `Persona` y sobre escribe el método `estudiar`.

````js
// Clase Padre
class Persona {
  constructor(nombre) {
    this.nombre = nombre;
  }

  saludar() {
    console.log(`Hola, mi nombre es ${this.nombre}`);
  }
}

// Clase Hija
class Empleado extends Persona {
  constructor(nombre, cargo) {
    super(nombre); // Llama al constructor de la clase padre
    this.cargo = cargo;
  }

  saludar() {
    super.saludar(); // Llama al método saludar de la clase padre
    console.log(`Mi cargo es ${this.cargo}`);
  }
}

const empleado = new Empleado('Juan', 'Desarrollador');
empleado.saludar();

// Hola, mi nombre es Juan
// Mi cargo es Desarrollador
````

En este ejemplo, la clase `Empleado` hereda de la clase `Persona` y utiliza `super` para llamar al constructor y al método `saludar` de la clase padre.

##### **Herencia de propiedades privadas**

En JavaScript, las propiedades privadas se definen utilizando el símbolo `#` antes del nombre de la propiedad. Estas propiedades solo son accesibles dentro de la clase que las define y no se heredan automáticamente.

Aquí hay un ejemplo:

```js
class Persona {
  #dni;
  constructor(nombre, edad, dni) {
    this.nombre = nombre;
    this.edad = edad;
    this.#dni = dni;
  }

  getDni() {
    return this.#dni;
  }
}

class Estudiante extends Persona {
  constructor(nombre, edad, carrera, dni) {
    super(nombre, edad, dni);
    this.carrera = carrera;
  }

  estudiar() {
    console.log(`Estoy estudiando ${this.carrera}.`);
  }
}

const estudiante = new Estudiante('Juan', 20, 'Ingeniería', '12345678');
console.log(estudiante.getDni()); // "12345678"
```

En este ejemplo, la clase `Persona` define una propiedad privada `#dni`, que solo es accesible a través del método `getDni()`. La clase `Estudiante` hereda de `Persona`, pero no tiene acceso directo a la propiedad `#dni`. Sin embargo, puede llamar al método `getDni()` para obtener el valor de la propiedad privada.

Otro ejemplo:

```js
class Animal {
  #nombre;

  constructor(nombre) {
    this.#nombre = nombre;
  }

  getNombre() {
    return this.#nombre;
  }
}

class Perro extends Animal {
  #raza;

  constructor(nombre, raza) {
    super(nombre);
    this.#raza = raza;
  }

  getRaza() {
    return this.#raza;
  }
}

const perro = new Perro('Fido', 'Golden Retriever');
console.log(perro.getNombre()); // Fido
console.log(perro.getRaza()); // Golden Retriever
```

En este ejemplo, la clase `Perro` hereda de la clase `Animal` y utiliza la propiedad privada `nombre` de la clase `Animal`. La clase `Perro` también define su propia propiedad privada `raza`.

**Conclusión**

Las propiedades privadas en JavaScript son una forma de encapsular datos dentro de una clase, de manera que solo puedan ser accedidos a través de métodos específicos. Esto ayuda a proteger la integridad de los datos y a prevenir accesos no autorizados. Las propiedades privadas se pueden utilizar en clases que heredan de otras clases y se pueden acceder y modificar a través de métodos definidos dentro de la clase.

#### Métodos Estáticos

Los métodos estáticos son métodos que se definen en una clase, pero no se instancian con cada objeto creado a partir de esa clase. En otras palabras, los métodos estáticos se llaman directamente en la clase, no en una instancia de la clase.

Para definir un método estático en una clase JavaScript, se utiliza la palabra clave `static` antes del nombre del método. Por ejemplo:

```js
class MyClass {
  static myStaticMethod() {
    console.log("Este es un método estático");
  }
}
```

Luego, para llamar al método estático, se utiliza el nombre de la clase, no una instancia de la clase:

```js
MyClass.myStaticMethod(); // Output: "Este es un método estático"
```

Notar que no se necesita crear una instancia de la clase para llamar al método estático.

Los métodos estáticos son útiles cuando se necesita una función que no dependa de una instancia específica de la clase, como una función de utilidad o una función que devuelve un valor constante.

````js
// Métodos estáticos

class MathOperations {
    static sum(a, b) {
        return a + b
    }
}
console.log(MathOperations.sum(5, 10)) //15
````

---

### Set

[Set - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Set)

El objeto Set en JavaScript es una colección de valores únicos, que pueden ser de cualquier tipo, ya sean primitivos o referencias a objetos. Permite almacenar y manipular conjuntos de valores de manera eficiente. El objeto Set se utiliza para eliminar duplicados de un conjunto de valores y para verificar si un valor existe en el conjunto.

#### Métodos

> Los métodos de `Set` permiten interactuar con esta colección de valores de manera eficiente y segura.

- `new Set()`: Declara e inicializa. 

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

#### Iterar

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

---

### Map

En JavaScript, `Map` es una estructura de datos que almacena pares clave-valor, similar a un objeto. Sin embargo, a diferencia de los objetos, `Map` permite utilizar cualquier tipo de valor como clave, no solo cadenas de texto.

````js
const myMap = new Map([
	[clave1, valor1],
	[clave2, valor2],
	[clave3, valor3]
])
````

La estructura de datos `Map` es parte del estándar ECMAScript 2015 (ES6) y es compatible con la mayoría de los navegadores modernos y Node.js.

#### Métodos

- `new Map()`: crear un `Map` utilizando la palabra clave `new` y el constructor `Map`.

```js
// DECLARACIÓN
const miMapa = new Map(); // Map(0) {}

// INICIALIZACIÓN
myMap = new Map([
    ["name","Charly"],
    ["email","charlybio87@outlook.com"],
    ["age", 25],
])
// Map(3) {
//  'name' => 'Charly',
//  'email' => 'charlybio87@outlook.com',
//  'age' => 25
// }

```

- `set()` :  agregar pares clave-valor a un `Map`.

```js
miMapa.set('alias', 'charlyDev');
miMapa.set('name', 'Juan');
miMapa.set('age', 30);
// Map(3) {
//  'name' => 'Juan',
//  'email' => 'charlybio87@outlook.com',
//  'age' => 20,
//	'alias' => charlyDev
// }
```

- `get()`: obtener un valor de un `Map`.

```js
const nombre = miMapa.get('name'); // devuelve "Juan"
```

- `has()`: verificar si una clave existe en un `Map`.

```js
const tieneNombre = miMapa.has('name'); // devuelve true
```

- `delete()`: eliminar un par clave-valor de un `Map`.

```js
miMapa.delete('age');
```

-  `keys() and values()`: devuelve un objeto `MapIterator` que contiene las claves (o llaves) o valor del mapa (o map).

````js
console.log(myMap.keys()); 
// [Map Iterator] { 'name', 'age', 'alias' }
console.log(myMap.values()); 
// [Map Iterator] { 'Charly Dev', 25, 'Charly Bio' }

const keysIterator = myMap.keys()
console.log(keysIterator.next().value); // name
console.log(keysIterator.next().value); // age
console.log(keysIterator.next().value); // alias
````

- `entries()`: Este método devuelve un objeto `Iterator` que contiene los pares clave-valor.

````js
console.log(myMap.entries())
// [Map Entries] {
// 	[ 'name', 'Charly Dev' ],
// 	[ 'age', 25 ],
// 	[ 'alias', 'Charly Bio' ]
// }
````

- `size`:  nos devuelve la cantidad de keys que guarda.

````js
myMap.size // 3
````

- `Array.from()`: convertir un `Map` a un arreglo.

```js
const miArreglo = Array.from(myMap);
// [ [ 'name', 'Charly Dev' ], [ 'age', 25 ], [ 'alias', 'Charly Bio' ] ]
```

- `Object.fromEntries()`: convertir un `Map` a un objeto utilizando el método 

```js
const miObjeto = Object.fromEntries(myMap);
// { name: 'Charly Dev', age: 25, alias: 'Charly Bio' }
```

- `clear()`: elimina el key-value del `map`.

````js
myMap.clear() // Map(0) {}
````

#### Iterar 

Puedes iterar sobre un `Map` utilizando el método `forEach()`:

```js
const miMapa.forEach((valor, clave) => {
	console.log(`${clave}: ${valor}`);
});
```

**Casos de uso**

`Map` es útil cuando necesitas almacenar pares clave-valor con claves que no son cadenas de texto, como números o objetos. También es útil cuando necesitas iterar sobre los pares clave-valor en un orden específico.

En JavaScript, `Map` es una estructura de datos que almacena pares clave-valor, similar a un objeto. Sin embargo, a diferencia de los objetos, `Map` permite utilizar cualquier tipo de valor como clave, no solo cadenas de texto.

La estructura de datos `Map` es parte del estándar ECMAScript 2015 (ES6) y es compatible con la mayoría de los navegadores modernos y Node.js.

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

---

### DOM

El DOM (Document Object Model) es una representación en memoria del documento HTML, que permite a los desarrolladores acceder y manipular los elementos del documento utilizando JavaScript.

Cuando un navegador carga un documento HTML, crea un objeto en memoria que representa la estructura del documento, incluyendo todos los elementos HTML, sus atributos y contenido. Este objeto se conoce como el DOM.

El DOM es una interfaz de programación que permite a los desarrolladores acceder y manipular los elementos del documento utilizando métodos y propiedades. De esta manera, los desarrolladores pueden crear scripts que interactúen con el documento, como por ejemplo:

- Agregar o eliminar elementos del documento
- Modificar el contenido o los atributos de los elementos
- Agregar eventos a los elementos para responder a acciones del usuario
- Realizar búsquedas y selecciones de elementos en el documento

El DOM es una parte fundamental de la programación web, ya que permite a los desarrolladores crear aplicaciones web dinámicas y interactivas.

Algunos conceptos clave relacionados con el DOM son:

- **Nodos**: Los elementos del documento se representan como nodos en el DOM. Cada nodo tiene una serie de propiedades y métodos que permiten acceder y manipular el elemento.
- **Elementos**: Los elementos HTML se representan como nodos en el DOM. Cada elemento tiene una serie de propiedades y métodos que permiten acceder y manipular el elemento.
- **Atributos**: Los atributos de los elementos HTML se representan como propiedades en el DOM.
- **Eventos**: Los eventos se utilizan para responder a acciones del usuario, como clicks o cambios en los formularios.

#### DOM HTML & JavaScript

La diferencia entre el DOM en HTML y JavaScript es fundamentalmente una cuestión de perspectiva y de cómo se accede y se manipula el DOM.

**HTML:**

En HTML, el DOM se refiere a la estructura de elementos que componen el documento HTML. Los elementos HTML, como `<html>`, `<body>`, `<p>`, `<img>`, etc., se organizan en una estructura de árbol, donde cada elemento es un nodo en el árbol. El DOM en HTML se enfoca en la estructura y el contenido del documento, y se utiliza para definir la presentación y el contenido de la página.

En otras palabras, el DOM en HTML es la representación estática del documento, que se carga en la memoria del navegador cuando se carga la página.

**JavaScript:**

En JavaScript, el DOM se refiere a la representación dinámica del documento HTML en memoria. Cuando se carga una página web, el navegador crea un objeto DOM que representa la estructura y el contenido del documento HTML. El DOM en JavaScript es una representación en vivo del documento, que se puede acceder y manipular mediante código JavaScript.

El DOM en JavaScript se utiliza para interactuar con el contenido de la página, realizar cambios dinámicos, responder a eventos del usuario, y mucho más. Los desarrolladores pueden acceder y manipular el DOM utilizando métodos y propiedades de JavaScript, como `document.getElementById()`, `element.innerHTML`, `addEventListener()`, etc.

En resumen, la principal diferencia entre el DOM en HTML y JavaScript es que:

- El DOM en HTML se enfoca en la estructura y el contenido estático del documento.
- El DOM en JavaScript se enfoca en la representación dinámica del documento en memoria, que se puede acceder y manipular mediante código JavaScript.

Ambas perspectivas del DOM son importantes y se complementan entre sí. El DOM en HTML proporciona la estructura y el contenido básico de la página, mientras que el DOM en JavaScript permite interactuar y personalizar la página de manera dinámica.

**Cómo acceder al DOM en JavaScript**

En JavaScript, puedes acceder al DOM mediante la variable `document`. Esta variable es un objeto que representa el documento HTML actual y proporciona métodos y propiedades para interactuar con él.

````js
console.dir(document)
````

El `console.dir(document)` es un comando de depuración en JavaScript que nos permite visualizar la estructura y contenido del objeto `document` en la consola del navegador.

Cuando se ejecuta `console.dir(document)`, se muestra una representación en forma de árbol del objeto `document`, que incluye sus propiedades y métodos. Esto puede ser útil para:

- Inspeccionar la estructura del documento HTML
- Verificar las propiedades y atributos de los elementos del documento
- Depurar problemas relacionados con el acceso a elementos del documento

#### Métodos y propiedades

Métodos y propiedades más empleados:

- `document.getElementById()`: Devuelve un elemento con el ID especificado.
- `document.querySelector()`: Devuelve el primer elemento que coincide con el selector especificado.
- `element.innerHTML`: Establece o devuelve el contenido HTML de un elemento.
- `element.addEventListener()`: Agrega un evento a un elemento.
- `element.style`: Establece o devuelve el estilo CSS de un elemento.

#### **Ejemplos de uso del DOM**

1. `document.getElementById(id)`: devuelve el elemento con el id especificado.

````html
<!-- HTML -->
<div id="miId">Este es mi id</div>
<div id="miDiv">Este es mi div</div>
````

```js
const elemento = document.getElementById('miId');
console.log(elemento); // imprime el elemento con el id "miId"

const elemento = document.getElementById('miId');
elemento.innerHTML = '<p>Hola, mundo!</p>';

<!-- JavaScript -->
const miDiv = document.getElementById('miDiv');
console.log(miDiv); // <div id="miDiv">Este es mi div</div>
```

> si no se encuentra el id en HTML el cual llamamos desde JS, por console nos muestra un null sino el document del elemento que nombramos.

2. `document.getElementsByClassName(clase)`: devuelve una lista de elementos con la clase especificada.

````html
<!-- HTML -->
<div class="miClase">Este es mi div 1</div>
<div class="miClase">Este es mi div 2</div>
````


```js
const elementos = document.getElementsByClassName('miClase');
console.log(elementos); // imprime una lista de elementos con la clase "miClase"

<!-- JavaScript -->
const misDivs = document.getElementsByClassName('miClase');
console.log(misDivs); // HTMLCollection [div.miClase, div.miClase]
```

3. `document.getElementsByTagName(etiqueta)`: devuelve una lista de elementos con la etiqueta especificada.

````html
<!-- HTML -->
<p>Este es mi párrafo 1</p>
<p>Este es mi párrafo 2</p>

````

````js
<!-- JavaScript -->
const misParrafos = document.getElementsByTagName('p');
console.log(misParrafos); // HTMLCollection [p, p]

````

4. `document.querySelector(selector)`: devuelve el primer elemento que coincide con el selector CSS especificado.

````html
<!-- HTML -->
<div class="miClase">Este es mi div</div>
````

````js
<!-- JavaScript -->
const miDiv = document.querySelector('.miClase');
console.log(miDiv); // <div class="miClase">Este es mi div</div>
````

- `document.querySelectorAll(selector)`: devuelve una lista de elementos que coinciden con el selector CSS especificado.

````html
<!-- HTML -->
<div class="miClase">Este es mi div 1</div>
<div class="miClase">Este es mi div 2</div>
````

````js
<!-- JavaScript -->
const misDivs = document.querySelectorAll('.miClase');
console.log(misDivs); // NodeList [div.miClase, div.miClase]
````
5. `element.addEventListener(evento, función)`: agrega un evento al elemento.

```js
<!-- HTML -->
<button id="miBoton">Click me</button>

<!-- JavaScript -->
const miBoton = document.getElementById('miBoton');
miBoton.addEventListener('click', function() {
  console.log('Botón clickeado!');
});

const elemento = document.getElementById('miId');
elemento.addEventListener('click', function() {
  console.log('Se ha hecho clic en el elemento');
});
```

6. `document.createElement()`:

```js
const nuevoElemento = document.createElement('p');
nuevoElemento.textContent = 'Hola, mundo!';
document.body.appendChild(nuevoElemento);
```

7. `element.innerHTML`: devuelve o establece el contenido HTML del elemento. O sea, que lo interpreta el string y devolver hasta un elemento html.

````html
<!-- HTML -->
<div id="miDiv">Este es mi div</div>
````

```js
<!-- JavaScript -->
const miDiv = document.getElementById('miDiv');
miDiv.innerHTML = 'Este es mi nuevo contenido';
console.log(miDiv.innerHTML); // "Este es mi nuevo contenido"
```

Otro ejemplo:

````html
<h1 id="titulo">TITULO</h1>
<div id="caja"></div>
````

````js
const productos = [...]

let listaDeProductosHTML = ''
productos.forEach(producto => 
    listaDeProductosHTML = listaDeProductosHTML +  `
        <div class="producto">
            <h2>${producto.nombre}</h2>
            <img src="${producto.thumbnail}" alt="${producto.nombre}">
            <br>
            <span>Precio: $${producto.precio}</span>
            <br>
            <span>Stock Disponible: ${producto.stock}</span>
            <br>
            <button>comprar</button>
            <hr>
        </div>
    `
)
caja.innerHTML = listaDeProductosHTML

/*Optimizacion. Se arma una lista de string y se guarda (reasigna) una sola veces en caja.innerHTML*/
````

> En el elemento div del HTML se incorporaría este forEach armado en JS. este se repetirá tantos elementos haya en el array productos.

8. `element.innerText`:  devuelve o establece el contenido de texto del elemento y todos sus hijos.

````html
<!-- HTML -->
<div id="miDiv">
  <p>Hola, mundo!</p>
  <span>Este es un texto dentro de un span</span>
</div>
````

````js
<!-- JavaScript -->
// Seleccionamos el elemento con id "miDiv"
const miDiv = document.getElementById('miDiv');

// Accedemos al texto contenido dentro del elemento
const texto = miDiv.innerText;

//Establece nuevo contenido
miDiv.innerText = 'Establecemos contenido'

// Mostramos el texto en la consola
console.log(texto);
````

9. `element.textContent`: devuelve o establece el contenido de texto del elemento.

```js
<!-- HTML -->
<div id="miDiv">Este es mi div</div>

<!-- JavaScript -->
const miDiv = document.getElementById('miDiv');
miDiv.textContent = 'Este es mi nuevo contenido';
console.log(miDiv.textContent); // "Este es mi nuevo contenido"
```

10. `element.setAttribute(atributo, valor)`: establece el valor de un atributo del elemento.

```js
<!-- HTML -->
<div id="miDiv">Este es mi div</div>

<!-- JavaScript -->
const miDiv = document.getElementById('miDiv');
miDiv.setAttribute('class', 'miNuevaClase');
console.log(miDiv.getAttribute('class')); // "miNuevaClase"
```

11. `element.getAttribute(atributo)`: devuelve el valor de un atributo del elemento.

```js
<!-- HTML -->
<div id="miDiv" class="miClase">Este es mi div</div>

<!-- JavaScript -->
const miDiv = document.getElementById('miDiv');
console.log(miDiv.getAttribute('class')); // "miClase"
```


12. `element.removeEventListener(evento, función)`: elimina un evento del elemento

```js
<!-- HTML -->
<button id="miBoton">Click me</button>

<!-- JavaScript -->
const miBoton = document.getElementById('miBoton');
const handleClick = function() {
  console.log('Botón clickeado!');
};
miBoton.addEventListener('click', handleClick);
// ...
```

Estos son solo algunos ejemplos básicos de cómo usar y emplear el DOM en JavaScript. El DOM es una herramienta muy poderosa que te permite interactuar con la estructura y el contenido de un documento de manera programática.

#### Iteración 

Iterar sobre los elementos del DOM (Document Object Model) utilizando varios métodos. Ejemplos:

**1. Utilizando `forEach`**

```js
const elements = document.querySelectorAll('div'); // selecciona todos los elementos div
elements.forEach(element => {
  console.log(element.textContent); // imprime el texto de cada elemento div
	}
)
```

**2. Utilizando `for...of`**

```js
const elements = document.querySelectorAll('div'); // selecciona todos los elementos div
for (const element of elements) {
  console.log(element.textContent); // imprime el texto de cada elemento div
}
```

**3. Utilizando `for` tradicional**

```js
const elements = document.querySelectorAll('div'); // selecciona todos los elementos div
for (let i = 0; i < elements.length; i++) {
  console.log(elements[i].textContent); // imprime el texto de cada elemento div
}
```

**4. Utilizando `NodeList.prototype.forEach()` (solo para NodeList)**

```js
document.querySelectorAll('div').forEach(element => {
  console.log(element.textContent); // imprime el texto de cada elemento div
});
```

Recuerda que `querySelectorAll` devuelve una NodeList, que es una colección de elementos del DOM. Los métodos `forEach` y `for...of` son compatibles con NodeList.

#### SessionStorage y LocalStorage

**¿Qué son SessionStorage y LocalStorage?**

SessionStorage y LocalStorage son dos tipos de almacenamiento web que permiten a los desarrolladores web almacenar datos en el lado del cliente, es decir, en el navegador del usuario. Estos datos se almacenan en forma de clave-valor y se pueden acceder y manipular utilizando JavaScript.

**Diferencias entre SessionStorage y LocalStorage**

La principal diferencia entre SessionStorage y LocalStorage es la duración de la vida de los datos almacenados:

- **SessionStorage**: Los datos almacenados en SessionStorage se eliminan cuando el usuario cierra la sesión actual (es decir, cuando cierra el navegador o la pestaña). Los datos se almacenan solo durante la sesión actual y no se conservan entre sesiones.
- **LocalStorage**: Los datos almacenados en LocalStorage se conservan incluso después de que el usuario cierra el navegador o la pestaña. Los datos se almacenan de forma permanente en el navegador del usuario, a menos que se eliminen explícitamente.

##### Métodos

**SessionStorage**

- **setItem(key, value)**: Almacena un valor en SessionStorage con una clave específica.
- **getItem(key)**: Recupera el valor almacenado en SessionStorage con una clave específica.
- **removeItem(key)**: Elimina el valor almacenado en SessionStorage con una clave específica.
- **clear()**: Elimina todos los valores almacenados en SessionStorage.

Ejemplo:

```js
// Almacenar un valor en SessionStorage
sessionStorage.setItem('nombre', 'Juan');

// Recuperar un valor de SessionStorage
console.log(sessionStorage.getItem('nombre')); // Output: Juan

// Eliminar un valor de SessionStorage
sessionStorage.removeItem('nombre');

// Eliminar todos los valores de SessionStorage
sessionStorage.clear();
```

**LocalStorage**

- **setItem(key, value)**: Almacena un valor en LocalStorage con una clave específica.
- **getItem(key)**: Recupera el valor almacenado en LocalStorage con una clave específica.
- **removeItem(key)**: Elimina el valor almacenado en LocalStorage con una clave específica.
- **clear()**: Elimina todos los valores almacenados en LocalStorage.

Ejemplo:

```js
// Almacenar un valor en LocalStorage
localStorage.setItem('apellido', 'Pérez');

// Recuperar un valor de LocalStorage
console.log(localStorage.getItem('apellido')); // Output: Pérez

// Eliminar un valor de LocalStorage
localStorage.removeItem('apellido');

// Eliminar todos los valores de LocalStorage
localStorage.clear();
```

**Ventajas y desventajas**

Ventajas:

- Permite almacenar datos en el lado del cliente, lo que reduce la carga en el servidor.
- Permite acceder a los datos almacenados en cualquier momento, sin necesidad de realizar una solicitud al servidor.
- Es una forma segura de almacenar datos, ya que los datos se almacenan en el navegador del usuario y no se envían al servidor.

Desventajas:

- los datos almacenados en SessionStorage y LocalStorage solo pueden guardar strings (no objetos)
- Los datos almacenados en SessionStorage y LocalStorage no son persistentes, es decir, se eliminan cuando el usuario cierra el navegador o la pestaña.
- Los datos almacenados en SessionStorage y LocalStorage no se pueden compartir entre diferentes sitios web o aplicaciones.
- Los datos almacenados en SessionStorage y LocalStorage pueden ser eliminados por el usuario o por el navegador.

En resumen, SessionStorage y LocalStorage son dos formas de almacenar datos en el lado del cliente, con SessionStorage siendo una forma temporal y LocalStorage siendo una forma permanente. Ambas formas tienen sus ventajas y desventajas, y se deben utilizar según las necesidades específicas de la aplicación.

##### Ejemplo: Selección de tema de la página

- Inicialmente:

![image-20240828082801243](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240828082801243.png)

````js
let theme = localStorage.getItem('theme')
console.log(theme)
if(!theme){
    theme = prompt('Seleccione un tema:\n-blanco\n-oscuro')
    /* Si quieren validan */
    localStorage.setItem('theme', theme)
}
````

En el code se guarda el tema de la pagina en el localStorage.

![image-20240826113651451](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240826113651451.png)

````js
<!--Html-->
<style>
    .mode-oscuro{
    	color: white;
        background-color:black;
    }
    .modo-claro{
        color: black;
        background-color: white;
    }
</style>
<body id="body">
    
<!--javaScript-->
const body = document.getElementById('body')
body.classList.add('mode-' + theme)// se llama a la lista de clases
const cambiarTheme = () => {
    theme = prompt('Seleccione un tema:\n-blanco\n-oscuro')
    localStorage.setItem('theme', theme)
    body.classList.add('mode-' + theme)
}
````

Esta parte del code permite solicitar tipo de tema. Una ves guardado en el localStorage podemos traer 

![image-20240828084129183](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240828084129183.png)

#### classList

La propiedad `classList` es una forma conveniente de trabajar con las clases CSS de un elemento en JavaScript. Aquí te presento algunos otros métodos y propiedades que se pueden aplicar:

**Métodos**

- `add()`: Agrega una o varias clases a la lista de clases del elemento.

```js
body.classList.add('mode-claro', 'otra-clase');
```

- `remove()`: Elimina una o varias clases de la lista de clases del elemento.

```js
body.classList.remove('mode-oscuro', 'otra-clase');
```

- `toggle()`: Alterna la presencia de una clase en la lista de clases del elemento.

```js
body.classList.toggle('mode-oscuro');
```

- `contains()`: Verifica si una clase está presente en la lista de clases del elemento.

```js
if (body.classList.contains('mode-oscuro')) {
  console.log('La clase mode-oscuro está presente');
}
```

- `replace()`: Reemplaza una clase por otra en la lista de clases del elemento.

```js
body.classList.replace('mode-oscuro', 'mode-claro');
```

**Propiedades**

- `length`: Devuelve el número de clases en la lista de clases del elemento.

```js
console.log(body.classList.length); // número de clases
```

- `item()`: Devuelve la clase en la posición especificada en la lista de clases del elemento.

```js
console.log(body.classList.item(0)); // primera clase
```

- `entries()`, `keys()`, `values()`: Devuelven iteradores para recorrer la lista de clases del elemento.

```js
for (const clase of body.classList.values()) {
  console.log(clase);
}
```

> Recuerda que `classList` es una propiedad de **solo lectura**, por lo que *no se puede asignar un nuevo valor directamente*. En su lugar, debes utilizar los métodos proporcionados para modificar la lista de clases. O sea, para modificar un classList hay que removerlo (eliminarlo).

#### Ejemplo

- Paso a Paso botón modo tema

````html
<body id="body">
    <button id="button" type="button">Cambiar Tema</button>
</body>
````

````js
/*SessionStorage & LocalStorage*/
// Tema de la pagina
let theme = localStorage.getItem('theme')
console.log(theme)
if(!theme){
    theme = prompt('Seleccione un tema:\n-blanco\n-oscuro')
    /* Si quieren validan */
    localStorage.setItem('theme', theme)
}

````

**1. `let theme = localStorage.getItem('theme')`**

- `localStorage` es un objeto que permite acceder al almacenamiento local del navegador.
- `getItem` es un método que devuelve el valor asociado a una clave específica en el almacenamiento local.
- `'theme'` es la clave que se utiliza para almacenar el tema de la página.
- `theme` es la variable que almacena el valor devuelto por `getItem`.

**2. `if(!theme){...}`**

- `!theme` es una condición que verifica si el valor de `theme` es `null` o `undefined`.
- Si la condición es verdadera, se ejecuta el código dentro del bloque `if`.

**3. `theme = prompt('Seleccione un tema:\n-blanco\n-oscuro')`**

- `prompt` es un método que muestra un cuadro de diálogo que solicita al usuario que ingrese un valor.
- El valor ingresado por el usuario se almacena en la variable `theme`.

**4. `localStorage.setItem('theme', theme)`**

- `setItem` es un método que almacena un valor en el almacenamiento local.
- `'theme'` es la clave que se utiliza para almacenar el valor.
- `theme` es el valor que se almacena.

````js
const body = document.getElementById('body')
body.classList.add('mode-' + theme)// se llama a la lista de clases
const button = document.getElementById('button')
button.addEventListener('click', cambiarTheme);
````

**5. `const body = document.getElementById('body')`**

- `document` es el objeto que representa el documento HTML.
- `getElementById` es un método que devuelve el elemento HTML con el ID especificado.
- `'body'` es el ID del elemento que se busca.
- `body` es la variable que almacena el elemento devuelto.

**6. `body.classList.add('mode-' + theme)`**

- `classList` es una propiedad que devuelve una lista de clases CSS que se han aplicado al elemento.
- `add` es un método que agrega una clase CSS a la lista de clases.
- `'mode-' + theme` es la clase CSS que se agrega.

![image-20240831173507835](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240831173507835.png)

> class= "mode-null" debido a que no se indico en el prompt el theme.
>
> class = "mode-oscuro" se indico modo oscuro en el prompt.

**7. `const button = document.getElementById('button')`**

- Se busca el elemento HTML con el ID `'button'` y se almacena en la variable `button`.

**8. `button.addEventListener('click', cambiarTheme);`**

- `button` es el elemento HTML que representa el botón "Cambiar Tema".
- `addEventListener` es un método que permite agregar un evento a un elemento HTML.
- `'click'` es el tipo de evento que se va a escuchar (en este caso, un clic en el botón).
- `cambiarTheme` es la función que se va a ejecutar cuando se produzca el evento (en este caso, cuando se haga clic en el botón).

````js
function cambiarTheme() {
    if (body.classList.contains('modo-claro')) {
        // Si la tiene, la removemos y agregamos la clase "mode-oscuro"
        body.classList.remove('modo-claro');
        body.classList.add('mode-oscuro');
        titulo.classList.add('mode-oscuro');
        caja.classList.add('mode-oscuro');
    } else {
        // Si no la tiene, removemos la clase "mode-oscuro" y agregamos la clase "modo-claro"
        body.classList.remove('mode-oscuro');
        body.classList.add('modo-claro');
        titulo.classList.remove('mode-oscuro');
        caja.classList.remove('mode-oscuro');
    }
}
````

**9. `function cambiarTheme() { ... }`**

- `CallBack`
- `cambiarTheme` es el nombre de la función que se va a ejecutar cuando se haga clic en el botón.

**10. `if (body.classList.contains('modo-claro')) { ... }`**

- `body` es el elemento HTML que representa el cuerpo de la página (en este caso, el elemento `<body>`).
- `classList` es una propiedad que devuelve una lista de clases CSS que se han aplicado al elemento.
- `contains` es un método que verifica si una clase específica está presente en la lista de clases.
- `'modo-claro'` es la clase CSS que se va a verificar.
- Si la clase `'modo-claro'` está presente, se ejecuta el código dentro del bloque `if`.

![image-20240831175444304](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240831175444304.png)

**11. `body.classList.remove('modo-claro');`**

- `remove` es un método que elimina una clase CSS de la lista de clases del elemento.
- `'modo-claro'` es la clase CSS que se va a eliminar.

**12. `body.classList.add('mode-oscuro');`**

- `add` es un método que agrega una clase CSS a la lista de clases del elemento.
- `'mode-oscuro'` es la clase CSS que se va a agregar.

**13. `titulo.classList.add('mode-oscuro');` y `caja.classList.add('mode-oscuro');`**

- Se agregan las mismas clases CSS a los elementos `titulo` y `caja`.

**14. `} else { ... }`**

- Si la clase `'modo-claro'` no está presente, se ejecuta el código dentro del bloque `else`.

**15. `body.classList.remove('mode-oscuro');` y `body.classList.add('modo-claro');`**

- Se eliminan y se agregan las clases CSS de manera similar a los pasos 11 y 12.

**16. `titulo.classList.remove('mode-oscuro');` y `caja.classList.remove('mode-oscuro');`**

- Se eliminan las clases CSS de los elementos `titulo` y `caja`.

En resumen, esta función cambia el tema de la página entre claro y oscuro, agregando o eliminando las clases CSS correspondientes a los elementos `body`, `titulo` y `caja`.

---

### Eventos

https://www.w3schools.com/tags/ref_eventattributes.asp

Los eventos en JavaScript HTML son "cosas" que suceden a los elementos HTML. Cuando se utiliza JavaScript en páginas HTML, JavaScript puede "reaccionar" a estos eventos. Estos eventos pueden ser desencadenados por diversas interacciones del usuario o por el propio navegador. Por ejemplo, cuando un usuario hace clic en un botón, se desencadena el evento `onclick`. A continuación, te presento algunos eventos HTML comunes:

#### Eventos HTML comunes

| Atributos   | Descripción                                         |
| ----------- | --------------------------------------------------- |
| onchange    | Un elemento HTML ha sido modificado                 |
| onclick     | El usuario hace clic en un elemento HTML            |
| onmouseover | El usuario mueve el ratón sobre un elemento HTML    |
| onmouseout  | El usuario mueve el ratón fuera de un elemento HTML |
| onkeydown   | El usuario presiona una tecla del teclado           |
| onload      | El navegador ha terminado de cargar la página       |
| onsubmit    | El usuario envía un formulario                      |
| onfocus     | Un elemento obtiene el foco                         |
| onblur      | Un elemento pierde el foco                          |

#### Asignar eventos utilizando HTML

Puedes asignar eventos a elementos HTML utilizando atributos de evento HTML. Por ejemplo, puedes agregar un atributo `onclick` a un elemento `<button>`:

```html
<button onclick="alert('Hola')">Haz clic en mí</button>
```

#### Asignar eventos utilizando JavaScript

También puedes asignar eventos a elementos HTML utilizando JavaScript. Por ejemplo, puedes utilizar el método `addEventListener` para agregar un oyente de eventos a un elemento `<button>`:

```js
let button = document.getElementById('myButton');
button.addEventListener('click', function() {
    alert('Hola');
});
```

#### Manejadores de eventos

Los manejadores de eventos son funciones que se ejecutan en respuesta a eventos específicos que ocurren en el navegador. Pueden estar adjuntos a elementos HTML utilizando atributos de evento como `onclick`, `onmouseover`, etc., o agregados dinámicamente utilizando el método `addEventListener` en JavaScript.

Aquí te muestro un ejemplo de un manejador de eventos JavaScript adjunto a un elemento de botón HTML utilizando el atributo `onclick`:

```
htmlEditRunCopy code1<button onclick="miFuncion()">Haz clic en mí</button>
2
3<script>
4    function miFuncion() {
5        alert("¡Botón pulsado! ");
6    }
7</script>
```

---

### API

[JSONPlaceholder - Free Fake REST API (typicode.com)](https://jsonplaceholder.typicode.com/)

Un JSON (JavaScript Object Notation) y un HTML (HyperText Markup Language) son dos tecnologías diferentes utilizadas en el desarrollo web.

**JSON** es un formato de intercambio de datos ligero y fácil de leer que se utiliza para representar datos estructurados. Se utiliza comúnmente para intercambiar datos entre servidores web, aplicaciones móviles y aplicaciones web. Un archivo JSON se compone de pares clave-valor, arrays y objetos, y se puede leer y escribir fácilmente en la mayoría de los lenguajes de programación.

Por ejemplo, un objeto JSON simple podría ser:

```json
{
  "nombre": "Juan",
  "edad": 30,
  "ciudad": "Madrid"
}
```

**HTML**, por otro lado, es un lenguaje de marcado utilizado para crear páginas web. Se utiliza para definir la estructura y el contenido de una página web, incluyendo texto, imágenes, enlaces, formularios, etc. El HTML se utiliza para crear la estructura básica de una página web, mientras que el CSS (Cascading Style Sheets) se utiliza para definir la presentación visual.

Por ejemplo, un ejemplo simple de código HTML podría ser:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Mi página web</title>
</head>
<body>
  <h1>Bienvenido a mi página web</h1>
  <p>Esta es una página web de ejemplo.</p>
</body>
</html>
```

En resumen, JSON se utiliza para intercambiar datos, mientras que HTML se utiliza para crear la estructura y el contenido de una página web.

---

### Métodos de Optimización

Para optimizar el rendimiento de páginas JavaScript, existen varios métodos que se pueden utilizar. Uno de ellos es minimizar el código JavaScript, lo que reduce la cantidad de bytes que se deben descargar y procesar. Otro método es utilizar directivas como `preload`, `prefetch` y `preconnect` para ayudar al navegador a optimizar la carga de recursos.

#### Uso de MutationObserver

Otro método es utilizar `MutationObserver` para detectar automáticamente cuándo los fragmentos de código son insertados en la página y resaltarlos. Esto se puede lograr mediante el siguiente código:

```
javascriptEditCopy code1let observer = new MutationObserver(mutations => {
2  for (let mutation of mutations) {
3    // examine nodos nuevos, ¿hay algo para resaltar?
4    for (let node of mutation.addedNodes) {
5      // seguimos elementos solamente, saltamos los otros nodos (es decir nodos de texto)
6      if (!(node instanceof HTMLElement)) continue;
7      // verificamos que el elemento insertado sea un fragmento de código
8      if (node.matches('pre[class*="language-"]')) {
9        Prism.highlightElement(node);
10      }
11      // ¿o tal vez haya un fragmento de código en su sub-árbol?
12      for (let elem of node.querySelectorAll('pre[class*="language-"]')) {
13        Prism.highlightElement(elem);
14      }
15    }
16  }
17});
18
19let demoElem = document.getElementById('highlight-demo');
20observer.observe(demoElem, { childList: true, subtree: true });
```

Este código crea un `MutationObserver` que observa el elemento con el id `highlight-demo` y resalta cualquier fragmento de código que aparezca en él.

#### Otros métodos de optimización

Otros métodos de optimización incluyen:

- Reducir el tamaño de los archivos JavaScript
- Utilizar mecanismos de compresión de recursos como Gzip o Brotli
- Utilizar Web workers para ejecutar tareas asíncronas
- Utilizar los atributos `defer` o `async` en los tag de script para permitir que el navegador continúe cargando la página mientras se carga el script

#### **Fragmentos**

Cuando me refiero a "fragmentos" en el contexto de optimización de páginas JavaScript, me refiero a pequeñas secciones de código JavaScript que se cargan dinámicamente en una página web. Estos fragmentos pueden ser:

1. **Código JavaScript inline**: pequeñas secciones de código JavaScript que se encuentran directamente en el HTML, generalmente dentro de un elemento `<script>`.
2. **Código JavaScript dinámico**: secciones de código JavaScript que se cargan dinámicamente en la página mediante técnicas como Ajax, JSONP o mediante la carga de módulos JavaScript.
3. **Fragmentos de código de bibliotecas**: pequeñas secciones de código JavaScript que se cargan desde bibliotecas externas, como jQuery, Lodash, o Prism (como en el ejemplo que te proporcioné).

Estos fragmentos de código pueden ser cargados en diferentes momentos durante la carga de la página, lo que puede afectar el rendimiento de la página. Algunos ejemplos de fragmentos de código que pueden ser cargados dinámicamente son:

- Un widget de comentarios que se carga después de que el usuario hace clic en un botón.
- Un gráfico que se carga después de que el usuario selecciona una opción en un menú desplegable.
- Un formulario que se carga después de que el usuario hace clic en un enlace.

Al optimizar la carga de estos fragmentos de código, podemos mejorar el rendimiento de la página y reducir el tiempo de carga.


----

### Referencias:

- [Eloquent JavaScript en Español (eloquent-javascript-es.vercel.app)](https://eloquent-javascript-es.vercel.app/)
- [Fundamentos de JavaScript - Aprende desarrollo web | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/JavaScript_basics)
- [JavaScript Tutorial (w3schools.com)](https://www.w3schools.com/js/DEFAULT.asp)
- [mouredev/hello-javascript: Curso para aprender el lenguaje de programación JavaScript desde cero y para principiantes. (github.com)](https://github.com/mouredev/hello-javascript)
- [Learn JavaScript  | web.dev](https://web.dev/learn/javascript)
- [The Modern JavaScript Tutorial](https://javascript.info/)

---

