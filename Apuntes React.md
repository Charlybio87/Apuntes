Apuntes.

## \<React>

### Recursos

[React](https://react.dev/)

[Node.js — Run JavaScript Everywhere (nodejs.org)](https://nodejs.org/en)

[Vite | Herramienta frontend de próxima generación (vitejs.dev)](https://es.vitejs.dev/)

[npm | Home (npmjs.com)](https://www.npmjs.com/)

### React

**React: Una Biblioteca de JavaScript para Construir Interfac1es de Usuario**

React es una biblioteca de JavaScript de código abierto desarrollada por Facebook (ahora Meta) que permite a los desarrolladores crear interfaces de usuario (UI) interactivas y dinámicas para aplicaciones web. Fue lanzada por primera vez en 2013 y desde entonces ha ganado popularidad rápidamente en la comunidad de desarrollo web.

**Características clave de React**

1. **Componentes**: En React, se utiliza un enfoque basado en componentes para construir interfaces de usuario. Los componentes son bloques de construcción reutilizables que representan partes de la interfaz de usuario.
2. **Virtual DOM**: React utiliza un concepto llamado Virtual DOM (Documento de Objetos Virtuales), que es una representación en memoria de la interfaz de usuario real. Cuando se produce un cambio en el estado de la aplicación, React actualiza el Virtual DOM y luego aplica los cambios necesarios al DOM real, lo que mejora el rendimiento.
3. **Declarative Programming**: En React, se utiliza un enfoque de programación declarativa, lo que significa que se describe lo que se quiere mostrar en la pantalla y no cómo se debe hacer.
4. **Estado y Props**: Los componentes en React tienen un estado (state) y props (propiedades). El estado se utiliza para almacenar datos que cambian con el tiempo, mientras que las props se utilizan para pasar datos de un componente padre a un componente hijo.

**Ventajas de React**

1. **Rendimiento**: React es rápido y eficiente, gracias a su uso del Virtual DOM.
2. **Reutilización de código**: Los componentes de React son reutilizables, lo que facilita la construcción de interfaces de usuario complejas.
3. **Fácil de aprender**: React tiene una curva de aprendizaje relativamente baja, especialmente para desarrolladores con experiencia en JavaScript.

**Uso común de React**

React se utiliza comúnmente para construir aplicaciones web complejas, como:

1. **Aplicaciones de una sola página** (SPA): React es ideal para construir aplicaciones que se cargan en una sola página, como aplicaciones de redes sociales o herramientas de productividad.
2. **Componentes de interfaz de usuario**: React se utiliza para construir componentes de interfaz de usuario personalizados, como botones, formularios y tablas.
3. **Aplicaciones móviles**: React se puede utilizar para construir aplicaciones móviles utilizando frameworks como React Native.

#### **Términos**

**Paradigma Declarativo**

ReactJS se basa en un paradigma declarativo, lo que significa que, en lugar de describir cómo se debe realizar algo, se describe lo que se quiere lograr. En otras palabras, en lugar de escribir código que explique paso a paso cómo se debe renderizar una interfaz de usuario, se describe la interfaz de usuario deseada y ReactJS se encarga de hacer que suceda.

**Componentes**

En ReactJS, los componentes son bloques de construcción fundamentales. Un componente es una pieza de código que representa una parte de la interfaz de usuario, como un botón, un formulario o una lista. Los componentes pueden contener otros componentes, lo que permite crear interfaces de usuario complejas a partir de componentes más pequeños y reutilizables.

**Funcionamiento de Estados**

En ReactJS, los estados (state) se refieren a los datos que cambian en una aplicación. Los estados se almacenan en componentes y se actualizan cuando el usuario interactúa con la aplicación. Cuando el estado de un componente cambia, ReactJS vuelve a renderizar el componente con los nuevos datos.

**Frontend Web**

ReactJS se utiliza principalmente para desarrollar aplicaciones web frontend, es decir, la parte de la aplicación que se ejecuta en el lado del cliente (navegador web). ReactJS se encarga de renderizar la interfaz de usuario y manejar los eventos del usuario, como clicks y entradas de texto.

**Backend con Node**

Aunque ReactJS se utiliza principalmente para frontend, también se puede utilizar con Node.js para crear aplicaciones web full-stack. En este caso, ReactJS se utiliza para renderizar la interfaz de usuario en el lado del cliente, mientras que Node.js se utiliza para crear la lógica de negocio y la API en el lado del servidor.

**Lenguaje JavaScript**

ReactJS se basa en JavaScript, por lo que es necesario tener conocimientos básicos de JavaScript para utilizar ReactJS. Sin embargo, ReactJS introduce conceptos y características adicionales, como JSX (una extensión de JavaScript que permite escribir HTML en JavaScript) y hooks (funciones que permiten acceder a los estados y ciclos de vida de los componentes).

### Node

Node.js es un entorno de ejecución de JavaScript del lado del servidor, que permite a los desarrolladores crear aplicaciones web escalables y de alta performance. Fue creado por Ryan Dahl en 2009 y desde entonces ha ganado popularidad rápidamente en la comunidad de desarrollo web.

**Características clave de Node.js:**

- **JavaScript del lado del servidor**: Node.js permite ejecutar código JavaScript en el servidor, lo que significa que los desarrolladores pueden utilizar el mismo lenguaje para crear la lógica del lado del cliente y del lado del servidor.
- **Asíncrono y no bloqueante**: Node.js utiliza un modelo de programación asíncrono y no bloqueante, lo que significa que el servidor no se bloquea esperando a que se completen las operaciones I/O. Esto permite manejar múltiples solicitudes concurrentes de manera eficiente.
- **Event-driven**: Node.js utiliza un modelo de programación basado en eventos, lo que significa que el código se ejecuta en respuesta a eventos, como solicitudes HTTP o lecturas de archivos.
- **Modularidad**: Node.js tiene una arquitectura modular, lo que significa que los desarrolladores pueden crear módulos reutilizables y fácilmente mantenibles.

**Ventajas de Node.js:**

- **Rendimiento**: Node.js es rápido y escalable, lo que lo hace ideal para aplicaciones web que requieren un alto rendimiento.
- **Flexibilidad**: Node.js permite a los desarrolladores crear aplicaciones web personalizadas y escalables.
- **Comunidad activa**: Node.js tiene una comunidad activa y en constante crecimiento, lo que significa que hay muchos recursos disponibles para los desarrolladores.

**Relación con HTML:**

Node.js se utiliza comúnmente para crear aplicaciones web que interactúan con HTML, CSS y JavaScript del lado del cliente. Node.js se encarga de manejar las solicitudes HTTP y de generar la respuesta HTML, mientras que el HTML se utiliza para definir la estructura y el contenido de la página web.

### Vite

Vite es una herramienta de construcción y desarrollo de aplicaciones web modernas.

**¿Qué es Vite?**

Vite es una herramienta de compilación moderna y rápida diseñada para proyectos de JavaScript y TypeScript. Su objetivo es proporcionar una experiencia de desarrollo más rápida y liviana para aplicaciones web modernas. Se enfoca en la compilación de código frontend y ofrece características como recarga en caliente , compilación de módulos y soporte para plugins. En el contexto de React y Node.js, Vite se puede utilizar como una alternativa a Create React App (CRA) para crear aplicaciones React rápidas y escalables.

**Características de Vite**

- **Velocidad**: Vite es muy rápido, gracias a su arquitectura basada en módulos ES y su capacidad para aprovechar el caché del navegador.
- **Soporte para módulos ES**: Vite admite módulos ES de forma nativa, lo que significa que no necesitas transpilar tu código para que funcione en navegadores antiguos.
- **Compatibilidad con librerías y frameworks**: Vite es compatible con una amplia variedad de librerías y frameworks, incluyendo Vue.js, React, Angular y más.
- **Soporte para TypeScript**: Vite admite TypeScript de forma nativa, lo que te permite escribir código TypeScript sin necesidad de configuraciones adicionales.

**Vite vs Create React App**

Vite y Create React App (CRA) son dos herramientas populares para crear aplicaciones React. Sin embargo, tienen enfoques diferentes. CRA es una herramienta más completa que proporciona una configuración predeterminada para aplicaciones React, incluyendo un servidor de desarrollo, un compilador de código y una configuración de producción. Por otro lado, Vite es una herramienta más liviana que se centra en la compilación y el servidor de desarrollo, dejando la configuración de producción y otros aspectos a la elección del desarrollador.

**Vite y Node.js**

Vite se puede utilizar con Node.js para crear aplicaciones server-side rendering (SSR) y aplicaciones que requieren una mayor integración con el servidor. En este caso, Vite se utiliza como una herramienta de compilación y servidor de desarrollo, mientras que Node.js se utiliza como el entorno de ejecución del servidor.

En cuanto a Node.js, Vite se ejecuta en él. Node.js es el entorno de ejecución de JavaScript en el lado del servidor, y Vite utiliza su capacidad para ejecutar código JavaScript en el lado del servidor. De esta manera, Vite puede compilar y servir tus aplicaciones web de manera más rápida y eficiente.

**Ventajas de utilizar Vite con React y Node.js**

- Mayor velocidad de desarrollo gracias a la recarga en caliente y la compilación de módulos
- Mejora la experiencia del usuario final con una carga más rápida de la aplicación
- Permite una integración más sencilla y rápida con React gracias al plugin oficial
- Puede ser utilizado con Node.js para ejecutar código JavaScript en el lado del servidor

**Ejemplo de configuración de Vite con React**

```jsx
import { defineConfig } from 'vite';
import reactRefresh from '@vitejs/plugin-react-refresh';

export default defineConfig({
  plugins: [reactRefresh()],
});
```

Este ejemplo muestra cómo configurar Vite para utilizar el plugin de React Refresh, que permite la recarga en caliente de la aplicación React.

**Características de Vite**

- Compilación rápida y liviana
- Soporte para JavaScript y TypeScript
- Servidor de desarrollo rápido y con Hot Module Replacement (HMR)
- Soporte para plugins y configuración personalizada
- Producción de archivos estáticos optimizados

**Ejemplo de uso de Vite con React**

Para crear una aplicación React con Vite, puedes seguir los siguientes pasos:

1. Instala Vite mediante npm o yarn: `npm install vite` o `yarn add vite`
2. Crea un nuevo proyecto React con Vite: `npx vite init my-react-app`
3. Inicia el servidor de desarrollo: `cd my-react-app && npm run dev`
4. Abre la aplicación en el navegador: `http://localhost:3000`

**Código de ejemplo**

```jsx
// my-react-app/src/App.js
import React from 'react';

function App() {
  return <div>Hello World!</div>;
}
export default App;
// my-react-app/vite.config.js
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
});
```

**Conclusión**

Vite es una herramienta poderosa para desarrollar aplicaciones web modernas. Su velocidad, soporte para módulos ES y compatibilidad con librerías y frameworks la convierten en una excelente opción para cualquier proyecto web. 

### NPM

NPM (Node Package Manager) es el gestor de paquetes predeterminado para Node.js. En el contexto de desarrollo web con React, Vite y Node.js, NPM se utiliza para instalar y administrar dependencias de proyectos.

En otras palabras, NPM te permite:

1. **Instalar paquetes**: Descargar e instalar bibliotecas y herramientas de terceros necesarias para tu proyecto, como React, Vite, Webpack, Babel, etc.
2. **Administrar dependencias**: Gestionar las versiones de las dependencias y asegurarte de que estén actualizadas.
3. **Crear y publicar paquetes**: Crear tus propios paquetes y compartirlos con la comunidad.

En un proyecto React con Vite y Node.js, NPM se utiliza para instalar las dependencias necesarias, como React, Vite, y otras bibliotecas. Por ejemplo, para instalar React, ejecutarías el comando `npm install react` en la terminal.

Además, NPM también se utiliza para ejecutar scripts de inicio, como `npm start` o `npm run dev`, que inician el servidor de desarrollo de Vite.

En resumen, NPM es una herramienta esencial en el desarrollo web con Node.js, React y Vite, ya que te permite administrar y instalar dependencias de manera sencilla y eficiente.

**¿Qué es node_modules?**

La carpeta `node_modules` es una carpeta especial en proyectos de Node.js que almacena todas las dependencias del proyecto. Cuando ejecutas `npm install`, npm (el administrador de paquetes de Node.js) descarga e instala las dependencias especificadas en el archivo `package.json` en esta carpeta.

**¿Qué es json?**

JSON (JavaScript Object Notation) es un formato de intercambio de datos ligero y fácil de leer, que se utiliza para almacenar y transmitir datos entre aplicaciones. Es un formato de texto plano que se utiliza para representar objetos y arrays de datos.

En el contexto de Node.js, los archivos `package.json` utilizan el formato JSON para almacenar información sobre el proyecto, como su nombre, versión, dependencias y scripts.

Instalar solo la carpeta `node_modules` y dejar intactas las demás carpetas en tu proyecto de JavaScript con React.

Para lograr esto, puedes utilizar el comando `npm install` con la opción `--only=production` o `--only=dev` dependiendo de tus necesidades.

Aquí te explico las opciones:

- `--only=production`: Instala solo las dependencias de producción, es decir, las que se encuentran en la sección `dependencies` del archivo `package.json`. Esto no instalará las dependencias de desarrollo que se encuentran en la sección `devDependencies`.
- `--only=dev`: Instala solo las dependencias de desarrollo, es decir, las que se encuentran en la sección `devDependencies` del archivo `package.json`. Esto no instalará las dependencias de producción que se encuentran en la sección `dependencies`.

Si deseas instalar solo la carpeta `node_modules` y dejar intactas las demás carpetas, puedes utilizar el comando:

```bash
bash
npm install --only=production
```

Esto instalará solo las dependencias de producción y no afectará a las demás carpetas.

Si deseas instalar las dependencias de desarrollo también, puedes utilizar el comando:

```bash
bash
npm install --only=dev
```

Recuerda que si deseas instalar todas las dependencias (producción y desarrollo), puedes simplemente utilizar el comando:

```bash
bash
npm install
```

### NPX

Permite ejecutar los paquetes y luego eliminarlos una ves que se hayan ejecutado. Sin la necesidad de instalarlos localmente.

**npx create-react-app**

`npx create-react-app` es una herramienta oficial de React que te permite crear una aplicación de React desde cero con una configuración predeterminada. Cuando ejecutas `npx create-react-app my-app`, se crea un proyecto de React con la siguiente estructura de carpetas y archivos:

```
markdownEditCopy code1my-app/
2  README.md
3  node_modules/
4  package.json
5  .gitignore
6  public/
7    favicon.ico
8    index.html
9  src/
10    App.css
11    App.js
12    App.test.js
13    index.css
14    index.js
15    logo.svg
16    serviceWorker.js
```

La herramienta `create-react-app` se encarga de configurar todo lo necesario para que tu aplicación de React funcione correctamente, incluyendo:

- Webpack como compilador de código
- Babel como transpilador de código
- ESLint como linter de código
- Jest como framework de pruebas

**Vite**

Vite es una herramienta de desarrollo de aplicaciones web que se enfoca en la velocidad y la eficiencia. Permite crear aplicaciones de React (y otros frameworks) con una configuración mínima y sin la necesidad de configurar Webpack o otros compiladores de código.

Cuando ejecutas `npx vite` en un proyecto de React, Vite se encarga de:

- Compilar el código de tu aplicación en tiempo real
- Servir la aplicación en un servidor de desarrollo rápido
- Proporcionar una experiencia de desarrollo más rápida y fluida

La principal diferencia entre `npx create-react-app` y Vite es que Vite no crea un proyecto de React desde cero, sino que se enfoca en la compilación y el desarrollo de la aplicación. Por lo tanto, debes crear la estructura de carpetas y archivos manualmente o utilizar una plantilla de proyecto existente.

**Ventajas de Vite**

- Mayor velocidad de desarrollo gracias a la compilación en tiempo real
- Menos configuración necesaria para empezar a desarrollar
- Soporte para plugins y extensiones para personalizar la experiencia de desarrollo

**Desventajas de Vite**

- No crea un proyecto de React desde cero, por lo que debes crear la estructura de carpetas y archivos manualmente
- No incluye herramientas de pruebas y linter como Jest y ESLint

En resumen, si deseas crear una aplicación de React con una configuración predeterminada y herramientas de pruebas y linter integradas, `npx create-react-app` es la mejor opción. Sin embargo, si prefieres una experiencia de desarrollo más rápida y flexible, Vite es una excelente alternativa.

### s/Framework

En el contexto de JavaScript y React, "Vanilla" se refiere a JavaScript puro, sin frameworks o bibliotecas adicionales como React. En otras palabras, Vanilla JavaScript es el lenguaje de programación JavaScript sin ninguna capa adicional. [1]

**¿Qué es Vanilla JS?**

Vanilla JS es un JavaScript plano que no tiene adicionales de bibliotecas. Se utiliza sin objetos o funciones incorporadas. La mejor parte sobre el framework es que no necesitas descargar ninguna biblioteca adicional para que el objeto funcione. En resumen, es algo ordinario o estándar sin características adicionales. Sin embargo, el JavaScript plano hace que sea más liviano, y puedes crear cualquier aplicación web con él. [1]

**Ventajas de Vanilla JS**

- Es ideal para desarrolladores que no tienen conocimientos de codificación.
- No involucra estructuras de codificación complejas, por lo que es más fácil de usar que React.
- Los desarrolladores pueden crear códigos de alta calidad mientras desarrollan nuevas aplicaciones web.
- Puede adoptar nuevas bibliotecas y frameworks que aumentan la velocidad de desarrollo de la aplicación.
- Vanilla permanecerá para siempre, ya que permanece más tiempo que otros frameworks. Sin embargo, las bibliotecas y frameworks pueden reemplazarse en Vanilla JS.

#### Ejemplo:

````html
<button data-id="123">Me gusta</button>
<button data-id="123">Me gusta</button>
<button data-id="123">Me gusta</button>

<style>
	button {
        background: #09f;
        color: #fff;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
    	cursor: pointer;
	}
	body {
		background: #222;
	}
</style>
````

````js
// Vanilla JavaScript
// recupera el boton
const button = document.querySelectorAll('button')

buttons.forEach(button=>{
    // al hacer click en el boton, tenemos que ejecutar una funcion
    button.addEventListener('click',finction(){
        // recuperar la id del atributo del html
        const id = button.getAttribute('data-id')
        // llamar a un servicio para actualizar si me gusta
        // togglelike(id)
        if (button.classList.contains('liked')){
            button.classList.removed('liked')
            button.innerText = 'Me gusta'
        }else{
            button.classList.add('liked')
            button.innerText = 'Quitar me gusta'
        }
	)}
})
````

Este tipo de forma de hacer el código se conoce como **IMPERATIVO**. Porque básicamente le estamos señalando paso a paso lo que debe ir haciendo para este caso. *Es poco escalable.*

A diferencia de React que la forma de hacer el código es **DECLARATIVO**, donde esencialmente iremos describiendo lo que deseamos del código.

### Framework

- Mejora rendimiento y facilidad de uso.
- Permite la estandarización del desarrollo.

### Abrir React c/Vite

#### Pasos:

1. introducir carpeta al visual.
2. abrir terminal, y en consola introducir: **`npm create vite@latest`** de esta manera se ejecutara en el directorio en donde se encuentra.
3. introducir nombre de proyecto.
4. introducir nombre de package.
5. Selección de Framework: **`React`**
6. Selección de variante: **`JavaScript`** 
7. se descargara la estructura (plantilla) de una aplicacion con react.
8. debemos situarnos en la carpeta creada: **`>cd projectMiduDev`**
9. ubicado en la carpeta **`>\projectMiduDev>npm i`**. Se instala carpeta de proyectos **`node_module `**
10. para ejecutar scripts dev: **`npm run dev`**. 
11. Indicamos el Local:  **`http://localhost:5173/`**

### Dependencias y devDependencias



---

# Primer Paso - MoureDev

1. introducir carpeta al visual.
2. abrir terminal, y en consola introducir: `npx create-react-app .` de esta manera se ejecutara en el directorio en donde se encuentra.
3. se descargara la estructura de una aplicacion con react.
4. para ejecutar: `npm star`. En el localhost:3000 correra la aplicación con react.

### Elementos de la estrcutra

- **`Readme.md`** contiene un tutorial por defecto.
- **`package.json`** contendrá todas las dependencias que usar el proyecto.
- **`node_modules`** contiene una referencia de todas las librerías.
- directorio **`public`** contendrá elementos tipos de la web
- directorio **`src`** sitio de desarrollo, donde se encontrará los ficheros js, ccs y de test.

### Código de la App

En el **`index.js`** se hace referencia a un elemento root. El cual se encuentra en el div del html. Prácticamente se construye sobre el div todo con code JavaScript. 

````js
<!--Javascript-->
const root = ReactDOM.createRoot(document.getElementById('root'));
````

````html
<!--Html-->
<body>
    <div id="root"></div>
</body>
````

Dentro del code **`index.js`** se puede observar que se hacer referencia a otro fichero **`App.js`**.
```` jsx
<!--Javascript-->
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
````

En este fichero es donde se dibuja todos los elementos de nuestra web.

````jsx
<!--Javascript-->
function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
````

<img src="C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240903073755024.png" alt="image-20240903073755024" style="zoom:50%;" />

Al editar dentro del code este al recargarse se visulizará en el navegador de forma inmediata por el mecanísmo **Life reload** sin la necesidad de parar y volver arrancar el proceso.

Como se puede observa en el code la estructura tiene una sintáxis parecida a html, el cúal no lo es, sino es JSX. [Escribir marcado con JSX – React](https://es.react.dev/learn/writing-markup-with-jsx)

> *JSX* es una extensión de sintaxis para JavaScript que permite escribir marcado similar a HTML dentro de una archivo JavaScript. Aunque hay otras formas de escribir componentes, la mayoría de los desarrolladores de React prefieren la concisión de JSX, y la mayoría de las bases de código lo usan.

### Componentes

1. Crear un fichero **`component.jsx`**
2. Escribir en la área de trabajo: **`rfc`**. Se generará una estrcutura por defecto de un componente.   

````jsx
<!-- Component.jsx -->
import React from 'react'

export default function Component() {
  return (
    <div>Mi Componente</div>
  )
}
````

3. Para que se ejecute el componente debe ser llamado: 
   - Importado
   - llamarlo dentro del div

````jsx
<!-- App.js -->
import Component from './Component'; // importado 
function App() {
  return (
	<div className="App">
        ...
        <Component />				// llamado
    	...
  	</div>
  );
}
````

### Estados

También React se orienta a estados. Tiene la capacidad de dectectar que componentes se van a repintar en nuestra web. Pero para ello se deben utilizar estados.

Importar **`useState`** en el fichero Component.jsx

````jsx
import React,{useState} from 'react'
````

exporta **`default function Component(){...}`**

````jsx
export default function Component() {
    // propiedad: llamada text y asociada al cambio de estado setText
    const [text, setText] = useState()
    const [update, setUpDate] = useState()

    // recibe el valor del input y se asigna a la propiedad text
    const textOnChange = (event) => {
        setText(event.target.value)
    }
    // no recibe un evento en si
    const buttonOnClick = () => {
        setUpDate(text)
    }

    return (
    <div>
        <input type="text" value={text} onChange={textOnChange} />
        <button onClick={buttonOnClick}>Actualizar</button>
        <p>Texto input: {text}</p>
        <p>Texto actualizado: {update}</p>
    </div>
  
````

> Este ejemplo lo que realíza es la escritura de un text a través de un input, el cúal se visualizará en un parrafo posterior. Pero al presionar el botón actualizar automáticamente se visualizará en el segundo párrafo el text (interpolación, lo almacendo en la propiedad updated ), por medio de un evento onClick.

### Despliegue

- Gratuitas:
  - [GitHub Pages | Websites for you and your projects, hosted directly from your GitHub repository. Just edit, push, and your changes are live.](https://pages.github.com/)
  - [Vercel: Build and deploy the best web experiences with the Frontend Cloud](https://vercel.com/)
  - [Scale & Ship Faster with a Composable Web Architecture | Netlify](https://www.netlify.com/)
  - [Firebase | Google's Mobile and Web App Development Platform](https://firebase.google.com/?hl=es-419)

Todas permiten despleguar y probar tu proyecto en producción y no en un entorno local.

### Nota

JSX y React son independientes. A menudo se usan en conjunto, pero se *pueden* [usar de forma separada](https://es.reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html#whats-a-jsx-transform). JSX es una extensión de sintaxis, mientras React es una biblioteca de JavaScript.

---

# Aprendiendo React Sitio Oficial

[Inicio rápido – React](https://es.react.dev/learn) 

## Crear y anidar componentes 

Las aplicaciones de React están hechas a partir de *componentes*. Un componente es una pieza de UI (siglas en inglés de interfaz de usuario) que tiene su propia lógica y apariencia. Un componente puede ser tan pequeño como un botón, o tan grande como toda una página.

Los componentes de React son funciones de JavaScript que devuelven *markup* (marcado):

````jsx
import React from 'react'

export default function MyButton() {
  return (
    <button>Soy un botón</button>
  );
}
````

Ahora que has declarado `MyButton`, puedes anidarlo en otro componente:

```jsx
import React, { useState } from "react"
import MyButton from "./Funciones/MyButton"

export default function App() {
  return (
    <div>
      <h1>Bienvenido a mi aplicación</h1>
      <MyButton />
    </div>
  );
}
```

>Nota que `<MyButton />` empieza con mayúscula. Así es como sabes que es un componente de React. Los nombres de los componentes de React siempre deben comenzar con mayúscula, mientras las etiquetas HTML deben estar minúsculas.

Las palabras clave `export default` especifican el componente principal en el archivo. Si no estás familiarizado con alguna parte de la sintaxis de JavaScript, [MDN](https://developer.mozilla.org/es/docs/web/javascript/reference/statements/export) y [javascript.info](https://javascript.info/import-export) tienen magníficas referencias.

💡 [export - JavaScript | MDN (mozilla.org)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/export) | [Export and Import (javascript.info)](https://es.javascript.info/import-export)

## Escribir marcado con JSX 

La sintaxis de marcado que viste arriba se llama *JSX*. Es totalmente opcional, pero la mayoría de los proyectos de React usan JSX por la comodidad que ofrece. Todas las [herramientas que recomendamos para el desarrollo local](https://es.react.dev/learn/installation) son compatibles con JSX sin ningún tipo de configuración.

JSX es más estricto que HTML. Tienes que cerrar etiquetas como `<br />`. Tu componente tampoco puede devolver múltiples etiquetas de JSX. Debes envolverlas en un padre compartido, como `<div>...</div>` o en un envoltorio vacío `<>...</>`:

```jsx
import React from 'react'

function AboutPage() {
  return(
    <>
      <h1>Acerca de</h1>
      <p>Hola.<br />¿Cómo vas?</p>
    </>
  )  
}

export {AboutPage}
```

Si tienes mucho HTML que convertir a JSX, puedes utilizar un [convertidor en línea](https://transform.tools/html-to-jsx).

## Añadir estilos 

En React, especificas una clase de CSS con `className`. Funciona de la misma forma que el atributo [`class`](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/class) de HTML:

```jsx
/*import './style/app.css'*/
<img className="avatar" src="./public/vite.svg"/>
```

Luego escribes las reglas CSS para esa clase en un archivo CSS aparte:

```css
/* In your CSS */
.avatar {
  border-radius: 50%;
}
```

React no prescribe como debes añadir tus archivos CSS. En el caso más simple, añades una etiqueta [``](https://developer.mozilla.org/es/docs/Web/HTML/Element/link) a tu HTML. Si utilizas una herramienta de construcción o un framework, consulta su documentación para saber como añadir un archivo CSS a tu proyecto.

## Mostrar datos 

JSX te permite poner marcado dentro de JavaScript. Las llaves te permiten «escapar de nuevo» hacia JavaScript de forma tal que puedas incrustar una variable de tu código y mostrársela al usuario. Por ejemplo, esto mostrará `user.name`:

```jsx
return (
  <h1>
    {user.name}
  </h1>
);
```

También puedes «escaparte hacia JavaScript» en los atributos JSX, pero tienes que utilizar llaves *en lugar de* comillas. Por ejemplo, `className="avatar"` pasa la cadena `"avatar"` como la clase CSS, pero `src={user.imageUrl}` lee el valor de la variable de JavaScript `user.imageUrl` y luego pasa el valor como el atributo `src`:

```jsx
return (
  <img
    className="avatar"
    src={user.imageUrl}
  />
);
```

Puedes también poner expresiones más complejas dentro de llaves, por ejemplo, [concatenación de cadenas](https://javascript.info/operators#string-concatenation-with-binary):

````jsx
const user = {
  name: 'Hedy Lamarr',
  imageUrl: 'https://i.imgur.com/yXOvdOSs.jpg',
  imageSize: 90,
};

export default function Profile() {
  return (
    <>
      <h1>{user.name}</h1>
      <img
        className="avatar"
        src={user.imageUrl}
        alt={'Foto de ' + user.name}
        style={{
          width: user.imageSize,
          height: user.imageSize
        }}
      />
    </>
  );
}
````

En el ejemplo de arriba, `style={{}}` no es una sintaxis especial, sino un objeto regular `{}` dentro de las llaves de JSX de `style={ }`. Puedes utilizar el atributo `style` cuando tus estilos dependen de variables de JavaScript.

## Renderizado condicional 

En React, no hay una sintaxis especial para escribir condicionales. En cambio, usarás las mismas técnicas que usas al escribir código regular de JavaScript. Por ejemplo, puedes usar una sentencia [`if`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/if...else) para incluir JSX condicionalmente:

```jsx
let content;
if (isLoggedIn) {
  content = <AdminPanel />;
} else {
  content = <LoginForm />;
}
return (
  <div>
    {content}
  </div>
);
```

Si prefieres un código más compacto, puedes utilizar el [operador `?` condicional](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Conditional_Operator). A diferencia de `if`, funciona dentro de JSX:

```jsx
<div>
  {isLoggedIn ? (<AdminPanel /> ) : (<LoginForm />)} 
</div>
// (true) : adminpanel || (flase) : loginForm
```

Cuando no necesites la rama `else`, puedes también usar la [sintaxis lógica `&&`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND#short-circuit_evaluation), más breve:

```jsx
<div>
  {isLoggedIn && <AdminPanel />}
</div>
```

Todos estos enfoques también funcionan para especificar atributos condicionalmente. Si no estás familiarizado con toda esta sintaxis de JavaScript, puedes comenzar por usar siempre `if...else`.

## Renderizado de listas 

Dependerás de funcionalidades de JavaScript como los [bucles `for`](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Statements/for) y la [función map() de los arreglos](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/map) para renderizar listas de componentes.

Por ejemplo, digamos que tienes un arreglo de productos:

```jsx
const products = [
  { title: 'Col', id: 1 },
  { title: 'Ajo', id: 2 },
  { title: 'Manzana', id: 3 },
];
```

Dentro de tu componente, utiliza la función `map()` para transformar el arreglo de productos en un arreglo de elementos `<li>`:

```jsx
const listItems = products.map(product =>
  <li key={product.id}>
    {product.title}
  </li>
);
return (
  <ul>{listItems}</ul>
);
```

> Nota que `<li>` tiene un atributo `key` (llave). Para cada elemento en una lista, debes pasar una cadena o un número que identifique ese elemento de forma única entre sus hermanos. Usualmente, una llave debe provenir de tus datos, como un ID de una base de datos. React dependerá de tus llaves para entender qué ha ocurrido si luego insertas, eliminas o reordenas los elementos.

````jsx
const products = [
  { title: 'Col', isFruit: false, id: 1 },
  { title: 'Ajo', isFruit: false, id: 2 },
  { title: 'Manzana', isFruit: true, id: 3 },
];

export default function ShoppingList() {
  const listItems = products.map(product =>
    <li
      key={product.id}
      style={{
        color: product.isFruit ? 'magenta' : 'darkgreen'
      }}
    >
      {product.title}
    </li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

````

## Responder a eventos 

Puedes responder a eventos declarando funciones *controladoras de eventos* dentro de tus componentes:

```jsx
function MyButton() {
  function handleClick() {
    alert('¡Me hiciste clic!');
  }
  return (
    <button onClick={handleClick}>
      Hazme clic
    </button>
  );
}
```

> ¡Nota que `onClick={handleClick}` no tiene paréntesis al final! No *llames* a la función controladora de evento: solamente necesitas *pasarla hacia abajo*. React llamará a tu controlador de evento cuando el usuario haga clic en el botón.

## Actualizar la pantalla 

A menudo, querrás que tu componente «recuerde» alguna información y la muestre. Por ejemplo, quizá quieras contar el número de veces que hiciste clic en un botón. Para lograrlo, añade *estado* a tu componente.

Primero, importa [`useState`](https://es.react.dev/reference/react/useState) de React:

```jsx
import { useState } from 'react';
```

Ahora puedes declarar una *variable de estado* dentro de tu componente:

```jsx
function MyButton() {
  const [count, setCount] = useState(0); //Inicia en 0
  // ...
```

Obtendrás dos cosas de `useState`: el estado actual (`count`), y la función que te permite actualizarlo (`setCount`). Puedes nombrarlos de cualquier forma, pero la convención es llamarlos algo como `[something, setSomething]`.

La primera vez que se muestra el botón, `count` será `0` porque  pasaste `0` a `useState()`. Cuando quieras cambiar el estado llama a `setCount()` y pásale el nuevo valor. Al hacer clic en este botón se incrementará el contador:

```jsx
function MyButton() {
  const [count, setCount] = useState(0);
  function handleClick() {
    setCount(count + 1);
  }
  return (
    <button onClick={handleClick}>
      Hiciste clic {count} veces
    </button>
  );
}
```

React llamará de nuevo a la función del componente. Esta vez, `count` será `1`. Luego será `2`. Y así sucesivamente.

Si renderizas el mismo componente varias veces, cada uno obtendrá su propio estado. Intenta hacer clic independientemente en cada botón:

````jsx
import { useState } from 'react';

export default function MyApp() {
  return (
    <div>
      <h1>Contadores que se actualizan separadamente</h1>
      <MyButton />
      <MyButton />
    </div>
  );
}

function MyButton() {
  const [count, setCount] = useState(0);
  function handleClick() {
    setCount(count + 1);
  }
  return (
    <button onClick={handleClick}>
      Hiciste clic {count} veces
    </button>
  );
}

````

> Nota que cada botón «recuerda» su propio estado `count` y que no afecta a otros botones.

## El uso de los Hooks 

Las funciones que comienzan con `use` se llaman *Hooks*. `useState` es un Hook nativo dentro de React. Puedes encontrar otros Hooks nativos en la [referencia de la API de React](https://es.react.dev/reference/react). También puedes escribir tus propios Hooks mediante la combinación de otros existentes.

Los Hooks son más restrictivos que las funciones regulares. Solo puedes llamar a los Hooks *en el primer nivel* de tus componentes (u otros Hooks). Si quisieras utilizar `useState` en una condicional o en un bucle, extrae un nuevo componente y ponlo ahí.

## Compartir datos entre componentes 

En el ejemplo anterior, cada `MyButton` tenía su propio `count` independiente, y cuando hiciste clic en cada botón, solo el `count` del botón en hiciste clic cambiaba:

![image-20240910203715896](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240910203715896.png)

Sin embargo, a menudo necesitas que los componentes *compartan datos y se actualicen siempre en conjunto*.

Para hacer que ambos componentes `MyButton` muestren el mismo `count` y se actualicen juntos, necesitas mover el estado de los botones individuales «hacia arriba» al componente más cercano que los contiene a todos.

En este ejemplo, es `MyApp`:

![image-20240910204000599](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240910204000599.png)

Ahora cuando haces clic en cualquiera de los botones, `count` en `MyApp` cambiará, lo que causará que cambien ambos counts en `MyButton`. Aquí está como puedes expresarlo con código.

Primero, *mueve el estado hacia arriba* desde `MyButton` hacia `MyApp`:

```jsx
export default function MyApp() {
  const [count, setCount] = useState(0);
  function handleClick() {
    setCount(count + 1);
  }
  return (
    <div>
      <h1>Contadores que se actualizan separadamente</h1>
      <MyButton />
      <MyButton />
    </div>
  );
}
function MyButton() {
  // ... estamos moviendo el código de aquí ...
}
```

Luego, *pasa el estado hacia abajo* desde `MyApp` hacia cada `MyButton`, junto con la función compartida para controlar el evento de clic. Puedes pasar la información a `MyButton` usando las llaves de JSX, de la misma forma como lo hiciste anteriormente con las etiquetas nativas `<img>`:

```jsx
export default function MyApp() {
  const [count, setCount] = useState(0);
  function handleClick() {
    setCount(count + 1);
  }
  return (
    <div>
      <h1>Contadores que se actualizan juntos</h1>
      <MyButton count={count} onClick={handleClick} />
      <MyButton count={count} onClick={handleClick} />
    </div>
  );
}
```

La información que pasas hacia abajo se llaman *props*. Ahora el componente `MyApp` contiene el estado `count` y el controlador de evento `handleClick`, y *pasa ambos hacia abajo como props* a cada uno de los botones.

Finalmente, cambia `MyButton` para que *lea* las props que le pasaste desde el componente padre:

```jsx
function MyButton({ count, onClick }) {
  return (
    <button onClick={onClick}>
      Hiciste clic {count} veces
    </button>
  );
}
```

Cuando haces clic en el botón, el controlador `onClick` se dispara. A la prop `onClick` de cada botón se le asignó la función `handleClick` dentro de `MyApp`, de forma que el código dentro de ella se ejecuta. Ese código llama a `setCount(count + 1)`, que incremente la variable de estado `count`. El nuevo valor de `count` se pasa como prop a cada botón, y así todos muestran el nuevo valor.

Esto se llama «levantar el estado». Al mover el estado hacia arriba, lo compartimos entre componentes.

````jsx
import { useState } from 'react';

export default function MyApp() {
  const [count, setCount] = useState(0);
  function handleClick() {
    setCount(count + 1);
  }
  return (
    <div>
      <h1>Contadores que se actualizan juntos</h1>
      <MyButton count={count} onClick={handleClick} />
      <MyButton count={count} onClick={handleClick} />
    </div>
  );
}

function MyButton({ count, onClick }) {
  return (
    <button onClick={onClick}>
      Hiciste clic {count} veces
    </button>
  );
}
````

## Próximos pasos

Prueba el [Tutorial](https://es.react.dev/learn/tutorial-tic-tac-toe) para ponerlos en práctica y construir tu primera miniaplicación de React.

----

# Aprendiendo React con MiduDev

Entorno de: [codi.link | HTML, CSS, JavaScript Live Editor Playground](https://codi.link/||)

### Pasos Ejecución Proyectos:

Crear un mono repositorio multipaquete (en el mismo repositorio tendremos muchos proyectos)

- Open git Bash
- inicializa nuestro proyecto: ` npm init -y`
- observar: `ls`
- crear una carpeta: `mkdir projects`
- ingresar a la carpeta projects: `cd projects`
- creamos: `npm create vite@latest`
- nombre de proyecto:
- selección de framework: javaScript + swc
- ingresar a la carpeta del proyecto creado.
- realizo: `npm i`
- iniciar: `npm run dev`

````jsx
// fichero main.jsx 

import { StrictMode } from 'react' // importamos a modo estricto desde react (node_modules)
import { createRoot } from 'react-dom/client' // idem para el react-dom/client
import App from './App.jsx' // importamos un componente app
import './index.css' // importamos los estilos

const root = createRoot(document.getElementById('root'))
// document.getElementById('root') => elemento del html. Donde se creara la aplicación (renderizar la aplicación)
root.render(
  <StrictMode>
    <App />
  </StrictMode>,
)
````

## Proyectos

https://github.com/midudev/aprendiendo-react

### hola mundo

````jsx
// main.jsx

import { StrictMode } from 'react'
import { createRoot } from 'react-dom/client'

const root = createRoot(document.getElementById('root'))
root.render(<button>Hola button</button>)
````

> Un solo elemento se puede pasar.

````jsx
// Componente Button
const Button = ({text}) => {
  return(
  {/* Forma de hacer un comentario dentro de return()*/}
    <button>
      <svg>...</svg>
      {text}
    </button>
  )
}
root.render(
  <React.Fragment>
    <Button text="Button 1" />
    <Button text="Button 2" />
    <Button text="Button 3" />
  </React.Fragment>
)
````

Los nombres de los componentes deben ser PascalCase.

### card twiter

````jsx
// App.jsx
export function App() {
    return (
        <div>
            <h1>Twiter Card</h1>
        </div>
    )
}
// main.jsx
import { App } from './App.jsx'
...
root.render(
  <App />
)
````

> De esta manera se puede observar como se permite renderizar el componente del fichero App.jsx

Para implementar style no debe ser como string o cadena de texto, sino un objeto.

````jsx

<article style = "display: flex"> ❌ 
<article style = {{ display: 'flex', color:...}} 👌
````

creamos un fichero de estilos

````jsx
// index.jsx
body {
    margin: 0;
    background: #222;
    font-family: system-ui;
    display: grid;
    place-content: center;
    min-height: 100vh;
}
// importamos main.jsx
import './index.css'
// App.jsx
export function App() {
    return (
        <article style = {{ display: 'flex',alignItems:'center' ,color:'#fff'}}>
           ...
    )
}
````

> Está no es la mejor forma de darle estilo.

Para mejorar se crea un fichero App.css con todos los estilos en los elementos de las card. Se debe importar a nivel de componente. 

````jsx
// App.jsx
import './App.css'
````

Para que sea escalable de puede usar clases, en React **`className =''`**.

````jsx
 // App.jsx
export function App() {
    return (
	<article className ='tw-followCard'>
    <header className ='tw-followCard-header'>
    <img className ='tw-followCard-avatar'...>
	...
    )
}
````

> Estas clases se reflejarían en el App.css. 

Por el momento este componentes no es reusable o reutilizable, una de las causas por estar anivel de App.jsx.

````jsx
// TwitterFollowCard.jsx
export function TwitterFollowCard () {
    return (
        <article className ='tw-followCard'>
            ...
    )
}
````

>De todas maneras sigue sin ser de todo reutilizable.

La base de la **Reutilización de los componentes** en React son las propiedades (los parámetros), igual como las funciones para poder reutilizarlas se debe parametrizar. Los componentes para poder reutilizarlos se le debe pasar información que nos interese.

````jsx
// TwitterFollowCard.jsx
export function TwitterFollowCard ({userName, name, isFollowing}) {
    const imageSrc = `https://unavatar.io/${userName}`
    return (
        <article className ='tw-followCard'>
            <header className ='tw-followCard-header'>
                <img 
                className ='tw-followCard-avatar'
                src= {imageSrc}/>
                ...
    )
}
````

> En este caso se le proporciona parámetros (**props**) para que sea mas escalable y reutilizable.

```` jsx
// App.jsx
...
import { TwitterFollowCard } from './TwitterFollowCard.jsx'

export function App() {
    return (
    <TwitterFollowCard userName='midudev' name='Miguel angel Duran' />
    )
}
// alternativa para más...
return (
    <React.Fragment>
    <TwitterFollowCard userName='midudev' name='Miguel angel Duran' />
    <TwitterFollowCard userName='midudev' name='Miguel angel Duran' />
    </React.Fragment>
    )
// alternativa mas limpia
return (
    <>
    <TwitterFollowCard userName='midudev' name='Miguel angel Duran' />
    <TwitterFollowCard userName='midudev' name='Miguel angel Duran' />
    </>
    )

````

El crear el ui y que sea reutilizable permite realizar pequeños arreglos y este tenga afecte en los demás. El inconveniente radica que quizas por algun motivos esos arreglos puedan generar modificaciones que luego no seran necesario. El caso podría ser que en vez de tocar App.css (fichero de estilo) implementemos modificaciones en el index.css, o sea, más a nivel de aplicación. 

````jsx
// App.jsx
export function App() {
    return (
        <section  className="App">
        <TwitterFollowCard userName='midudev' name='Miguel angel Duran' /> 
    ...
        </section>
    )
}

// index.css
 .App {
    display: flex;
    flex-direction: column;
    gap: 16px
}           
````

> De esta manera las modificaciones se realizan a nivel del contenedor.

Para sumar mas funcionalidad también se pueden pasar funciones como CallBack a los componentes hijos como props:

````jsx
// App.jsx
export function App() {
    // Funcion de @
    const formatUserName = (userName) => `@${userName}`
    
    return (
        <section  className="App">
        <TwitterFollowCard formatUserName={formatUserName} isFollowing={true} userName='midudev' name='Miguel angel Duran' />
        </section>
    )
}
            
// TwitterFollowCard.jsx
	<div className='tw-followCard-info'>
        <strong>{name}</strong>
        <span className='tw-followCard-infoUserName'>{formatUserName(userName)}</span>
    </div>
````

Otra caracteristica más es que se puede pasar elementos como props:

````markdown
# App.jsx
// se crea un elemento envuelto con span
const formattedUserName = <span>@charlydev</span>
// se pasa como props (como un elemento)
formattedUserName={formattedUserName}

# TwitterFollowCard.jsx
<span className='tw-followCard-infoUserName'>
// se evalua el elemento y se renderiza
{formattedUserName}</span>
````

**Diferencia entre componente y elemento**

Un **componente** seria una factoria de elementos, es decir, es una funcion que te retorna o devuelve un elemento.

El **elemento** es lo que renderiza React.

Cuando se pasan las props estás deberían ser inmutables. (para buenas prácticas)

````jsx
// TwitterFollowCard.jsx
// Mala practica
export function TwitterFollowCard ({formatUserName,userName, name, isFollowing}) {
userName = `@${userName}` ❌
    return (
        ...
        <span className='tw-followCard-infoUserName'>{formatUserName(userName)}</span>
    	...
    )
}
// Alternativa
export function TwitterFollowCard ({formatUserName,userName, name, isFollowing}) {
const usuNombre = `@${userName}` 👍
    return (
        ...
        <span className='tw-followCard-infoUserName'>{formatUserName(usuNombre)}</span>
    	...
    )
}
````

> No es conveniente modificar o mutar la props. Esto genera que React no tenga la seguridad de la renderización.
>
> Es conveniente generar una constante con otro nombre, mejor si no se llama igual que la props.

Props especial: **`children`**, hace referencia a todo lo que envuelve.

````jsx
// App.jsx
// se envuelve el componente con el nombre
    <section className='App'>
        <TwitterFollowCard isFollowing={true} userName='midudev'>
        <strong>Miguel angel Duran</strong>
        </TwitterFollowCard> 
        <TwitterFollowCard isFollowing userName='_CarlosARibas'>
        Carlos A. Ribas
        </TwitterFollowCard>
    </section>
// TwitterFollowCard.jsx
export function TwitterFollowCard ({children,userName,...}) {
    return (
        {children}
        <span className='tw-followCard-infoUserName'>@{userName}</span>
    )
}
````

> En este caso, children esta renderizando una cadena de texto. O sea, la línea que envuelve "TwitterFollowCard" es lo que lleva children.

**resto operador** índica el pasaje de cada uno de las propiedades del objeto como si fuese una props para la componente twitterFollowCard: (mala practica)

````jsx
export function App() {
const charlydev = {isFollowing: true, userName: 'charlydev'}
return (
    <section className='App'>
        ...
        <!--{...charlydev} resto operator -->
        <TwitterFollowCard {...charlydev}>
        Carlos A Ribas
        </TwitterFollowCard>
    </section>
    )
)
}
````

> Desventajas: manda mucha info no necesaria, problema de optimización generando que se renderice o re renderice sin necesidad, y por último, lo complejo que es entender qué información es la que le llegá al componente. (Mejor ser mas declarativo)

El **Estado** se refiere a como se encuentra el componente y como esté afecta el entorno en donde se encuentra, pero al cambiarlo este genera otra situación en el entorno ocasionando otra visual en la interface del usuario. En definitiva, ***"la interfaz debe responder a los cambios que tenga el usuario"***.

**Estado del button:**

- Renderizado Condicional

````jsx
export function TwitterFollowCard ({children,formatUserName,userName, name, isFollowing}) {
    const text = isFollowing ? 'Siguiendo' : 'Sigue'
	const buttonClassName = isFollowing ? 'tw-followCard-button is-following' // (boton css + clase isfollowing) o (boton normal)
    : 'tw-followCard-button'
    return (
    ...
        <!-- responde a las ternarias -->
        <button className={buttonClassName}>{text}</button>
    )
````

> Las condiciones estableces cambios de estados en el botón. Esto es lo que permite que React sea Dinámico, donde vaya respondiendo a todos los cambios que vamos haciendo.

![image-20240905082847343](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240905082847343.png)

Lo que se pretende es que el propio componente decida cuando mostrar un estado o el otro. Ya no se recurre a las props sino al estado.

Para ello se requiere una utilidad: `{useState}` de react, generalmente conocidos como **hooks**. El useState sirve para poder guardar una variable que nos diga si estamos o no estamos siguiendo al usuario.

> Hooks:
>
> - permiten añadir cierta funcionalidad a los componentes de react 
> - permiten ejecutar código arbitrario cuando ocurre ciertas cosas en tus componentes 
> - mejorar rendimiento de componentes

````jsx
import { useState } from 'react';

export function TwitterFollowCard ({children,userName}) {
    const [isFollowing, setIsFollowing] = useState(false) // uso desestructuracion js
    <!-- Equivalente ⏫ -->
    const state = useState(false)
    const isFollowing = state[0]
    const setIsFollowing = state[1]
````

> En este caso se elimino la props isFollowing de los parámetro, ahora, se encuentra representado como estado.
>
> Lo que sucede al presionar el boton, el useState devuelve una array de 2 posiciones. La primer psoción es el isFollowing (valor del estado) y la segunda posición la forma actualizada.
>
> isFollowing: valor actual.
>
> setIsFollowing. forma de actualizar el estado.

````jsx
export function TwitterFollowCard ({children,userName}) {
    const [isFollowing, setIsFollowing] = useState(false) 
    const handleClick = () => { 
        setIsFollowing(!isFollowing)
    } // isFollowing=true -> isFollowing=false o visceversa
    return (
        <aside>
                <button className={buttonClassName} onClick ={handleClink}> <!--se pide que se ejecute una funcion-->
                    {text}
                </button>
        </aside>
    )
````

El arrow function ejecutará el setIsFollowing para que de la vuelta (como un interruptor) el isFollowing. De esta manera cuando el boton este en seguir al presionarlo pasara a siguiendo y visceversa, por detrás, pasa de un estado true a false (o false a true).

Lo que se puede observar es que el estado esta separado de cada componente, por lo que es un estado interno. Interno se refiere a que está a nivel de cada uno de los elementos que crea el componente, no esta compartido entre elementos.

![image-20240905094625376](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240905094625376.png)

*Cada vez que cambiamos el estado cambia, **React detecta el cambio de estado y lo refleja los cambios en la IU**.*

Otro concepto: **DomVirtual**.

Si se tuviera un code imperativo se le debería indicar al Dom cual es la parte que se debería cambiar. A diferencia del code declarativo y el que porque de React... es el DomVirtual.

Siguiendo con el ejemplo del boton seguir/siguiendo, es que al observarlo en las herramientas de desarrollo se ve que al presionar el boton solo se actualiza el cambio de estado, el texto y la clase, (en vez de renderizar todo el articulo). Esto con javascript vanilla y sin dependecias es muy complicado.

El funcionamiento de react es como si sacará una foto de todo el code que renderizo la primera vez... esto es lo que crea como un arbol de elementos. Hace un comparacion de esto con lo que quiere renderizar ahora y busca las diferencias. Una vez encontrado realiza las actualizaciones minimas para reflejar los cambios en la IU. Esto es el funcionamiento de React del concepto de re-Renderizado.  

Otra forma de  que se re-Renderice el componente es que se actualice el estado interno de un componente, react entiende que debe volver a renderizar devuelta el componente para así reflejar los cambios (pero solo las parte que han cambiado).

````markdown
<!-- Consola de la herramienta de desarrollo -->
$('.tw-followCard').innerHTML
'<header class="tw-followCard-header"><img class="tw-followCard-avatar" src="https://unavatar.io/midudev" alt="imagen avatar"><div class="tw-followCard-info"><strong>Miguel Ángel Duran</strong><span class="tw-followCard-infoUserName">@midudev</span></div></header><aside><button class="tw-followCard-button is-following">Siguiendo</button></aside>'
````

Otra forma de re-Renderizado del componente es cuando un componente padre (`App()`) se vuelve a renderizar y esto propaga los cambios hacia los componentes que estan abajo.

````jsx
export function App() {
    <!--se renderiza 👇-->
    const formatUserName = (userName) => `@${userName}`
     return (
     <section className='App'>
             <!--todos los componentes se vuelven a renderizar ⏬-->
            <TwitterFollowCard userName={name}>
            Miguel Ángel Duran
            </TwitterFollowCard> 
            <TwitterFollowCard  userName='_CarlosARibas'>
            Carlos A Ribas
            </TwitterFollowCard>
            <button onClick={ () => setName('otroNombre')
            }>Cambio nombre</button>
        </section>
    )
}
````

> Ejemplo deagregar un boton que cambie el nombre de usauario de uno de los componentes, y como actua el renderizado.

![image-20240905171859637](C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240905171859637.png)

Cuando se  ejecuta el  App() se vuelve a renderizar el componente aunque luego en HTML gracias a react observa que se intentara renderizar lo mismo no lleva esos cambios al DOM. O sea, hay propagacion de los cambio y el DOM permanece intacto.

Otra implementación en los botones es el de mantener los estados, es decir, si sigo a midudev deberia aparecer el estado siguiendo. De aquí viene lo de ***inicializar un estado con una props*** (en definitiva una props es un valor de js por lo que se prodría usar).

````jsx
// TwitterFollowCard.jsx
	...
export function TwitterFollowCard ({children,userName,initialIsFollowing}) {
    const [isFollowing, setIsFollowing] = useState(initialIsFollowing) // uso desestructuracion js
	...
}
// App.jsx
	...
export function App() {
    const [name, setName] = useState('midudev')
    return (
        <section className='App'>
            <TwitterFollowCard userName={'midudev'} initialIsFollowing = {true}>
            Miguel Ángel Duran
            </TwitterFollowCard> 
            ...
        </section>
    )
}
````

<img src="C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240906084644704.png" alt="image-20240906084644704" style="zoom:80%;" />

Como se sabe los componentes tiene un estado interno, en cuanto a la imagen se tiene 2 componentes que tiene 2 estados separado. 

Un error común (mala practica) que se sabe cometer es pensar que cuando se usa una Props de estado inicial se creé que genera algun tipo de conexión, y ello genera que se propague el estado del padre hacia el hijo, por lo cual esto no sucede.

como se verá... el app contiene el componente de TwitterFollowCard, ambos tienen un estado.

````jsx
// App.jsx
export function App() {
    // inicialización del estado como useState(false)
    const [isFollowing, setIsFollowing] = useState(false)
    ...
    // estado inicial
    ...
    <section className='App'>
        <TwitterFollowCard userName={'midudev'} initialIsFollowing = {isFollowing}>
                Miguel Ángel Duran
        </TwitterFollowCard>
    </section>
    
// TwitterFollowCard.jsx
	export function TwitterFollowCard ({children,userName,initialIsFollowing}) {
    const [isFollowing, setIsFollowing] = useState(initialIsFollowing)
    const text = isFollowing ? 'Siguiendo' : 'Seguir'
````

El estado del padre se lo va a pasar como props al hijo (App.jsx). En el hijo se ocupa la props para inicializar el estado del propio componente, pero luego internamente lo cambia.

Para que se entienda: 

<img src="C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240906095716703.png" alt="image-20240906095716703" style="zoom:50%;" />

se cambia el estado de la app (se presiona el boton), no se observan cambios del estado del hijo.

<img src="C:\Users\ribas\AppData\Roaming\Typora\typora-user-images\image-20240906095944016.png" alt="image-20240906095944016" style="zoom:75%;" />

pero al ver la consola se observan cambios... lo que sucede es que cuando se manda la props del padre al hijo, en el hijo se lo esta utilizando (como esta utilizando) como estado inicial. Aquí es donde se acentua el problema ya que el estado inicial solo se inicia una vez. En definitiva, *** al usar una props para inicializar un estado se inicializa una sola vez*** no se reinicializa cada vez que la props cambia.

En otro caso donde se tenga mas de un usuario o sea un array de usuarios (lista):

````jsx
const users = [
    {
        userName: 'midudev',
        name: 'Miguel Ángel Durán',
        isFollowing: true
    },
    {
        userName: 'pheralb',
        name: 'Pablo H.',
        isFollowing: false
    },
    {
        userName: 'PacoHdezs',
        name: 'Paco Hdez',
        isFollowing: true
    },
    {
        userName: '_CarlosARibas',
        name: 'Charly',
        isFollowing: false
    }
]
````

Ahora para renderizar usamos un mapeado:

````jsx
export function App() {
    return (
        <section className='App'>
            {
                // Info a obtener
                users.map(({ userName, name, isFollowing }) => (
                    // devuelve el componente que se renderiza para c/u de los user
                    <TwitterFollowCard
                        // pasamos
                        key={userName}
                        userName={userName}
                        initialIsFollowing={isFollowing}
                    >
                        {/* Children*/}
                        {name}
                    </TwitterFollowCard>
                ))
            }
        </section>
    )
}
````

> lo que devuelve el mapeo de usuarios es lo que se desea renderizar por ello esta encerrados enllaves ({ } son para evaluar) 
>
> Importantes en el uso de map. indicar la Key, ya que al utilizar el DomVirtual este debe sabar a que elemento nos referimos dentro del array y ello se lo realiza con el identificador unico (key). En el caso de twitter los nombres de usuarios son unicos para cada persona.

---

## 📹 Videos con las clases

- 01: [Introducción a React](https://www.youtube.com/watch?v=7iobxzd_2wY)
- 02: [React Hooks: useState y useEffect](https://www.youtube.com/watch?v=qkzcjwnueLA&feature=youtu.be)
- 03: [Prueba técnica con lo aprendido](https://www.youtube.com/watch?v=XYpadB4VadY&feature=youtu.be)
- 04: [Fetching de datos y Custom Hooks](https://youtu.be/x-LcbVw99o8)
- 05: [React Hooks: useRef, useMemo, useCallback](https://youtu.be/GOEiMwDJ3lc)
- 06: [React Hooks: useContext, useReducer, useId](https://www.youtube.com/watch?v=B9tDYAZZxcE)
- 07: [React Router + Lazy Loading](https://www.youtube.com/watch?v=K2NcGYajvY4)
- 08: [React + TypeScript (Día 01): props y state](https://www.youtube.com/watch?v=4lAYfsq-2TE)
- 09: [React + TypeScript + ChatGPT - Clon de Google Translate](https://www.youtube.com/watch?v=kZhabulNCUc)
- 10: [React Redux Toolkit + Rome Tools](https://www.youtube.com/watch?v=bEEjuwujbbU)
- 11: [Prueba técnica de React con TypeScript](https://www.youtube.com/watch?v=mNJOWXc83Y4)
- 12: [React Query + Paginación + Infinite Scroll](https://www.youtube.com/watch?v=WKfVjQUa6nE)
- 13: [JavaScript Quiz con Zustand + TypeScript desde cero](https://www.youtube.com/watch?v=p2wF2wRjcN0)
- 14: Hacker News con TypeScript + SWR - Pendiente de subir

## 100 Preguntas sobre React

> [midudev/preguntas-entrevista-react: Preguntas típicas sobre React para entrevistas de trabajo ⚛️ (github.com)](https://github.com/midudev/preguntas-entrevista-react)
