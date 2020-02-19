# Messenger

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 9.0.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).



¿Qué tienen Angular, React y Vue en común?
Todos están orientados al desarrollo del frontend.

Todos están orientados al desarrollo de aplicaciones de tipo SPA (Single Page Application).

Una vez se aprenda uno ya cualquiera de los otros dos se hará fácil.

Pueden ser utilizadas para el desarrollo de aplicaciones mobiles.

Curva de Aprendizaje
Angular: Curva de aprendizaje más alta.

React: Es mucho más fácil de aprender que Angular.

Vue: Es aun más fácil debido a que sus librerías son muy parecidas.

Proyectos de gran escala
Angular: Tiene mucha más ventaja por la cantidad de componentes que tiene que pueden manejar y fue concebido para el desarrollo de aplicaciones de alta escala.
-React: react al igual que angular es usado para el desarrollo de aplicaciones grandes.
-Vue: No es tan robusto, sin embargo es recomendable usarlo para aplicaciones en despliegue legacy que ya tengan mucho desarrollo y requieren actualizarse a aplicaciones tipo SPA o hacer algún tipo de integración.

Herramientas de desarrollo
Angular: Typescript le da mucha ventaja por el uso de reglas de alto tipado, de igual forma vue y react pueden integrarse a TypeScript sin embargo no es obligatorio, esto de alguna forma obliga al desarrollador a tener un código mejor estructurado y limpio.

React: Tiene herramientas para el debug de codigo que son extensiones del navegador (Chrome y Firefox) React Developer Tools.

Mantenimiento de código
Angular: Es mucho más complejo en detección de bugs causados por sus mismos componentes.
-React y Vue: Son mucho más facil y flexible en la detección de errores.

Flexibilidad
Angular: por la cantidad de componentes que posee angular a veces se descargan una cantidad amplia de elementos que no necesariamente serán usados, esto lo hace poco flexible si se desea desarrollar aplicaciones pequeñas.

React y Vue: tienen pocas librerias y se adaptan a aplicaciones pequeñas y grandes.

Desarrollo mobile
Angular: Tiene framework de desarrollo híbrido como Ionic, que igualmente pueden integrarse a React y Vue en su ultima versión. La ventaja que tiene este framework basado en angular es que no genera aplicaciones nativas.

React: React usa react native y es un desarrollo no 100% nativo pero se acerca a dicho desarrollo y lo hace mucho más optimo.
-Vue: Usa NativeScript -. Vue permite la creación de aplicaciones nativas con NativeScript y Vue.

### Que hace esta app:
-app de mensajería instantánea, chat de persona a persona
-debe te
### Explorando el sistema de archivos
-A primera vista la estructura de los archivos del proyecto pudiera ser un tanto abrumadora ya que Angular necesita una gran cantidad de elementos y dependencias para proveernos del entorno adecuado para el desarrollo, pero al generar el entorno de producción, la mayoría de estas dependencias no estarán incluidas, por lo que la estructura final será mucho más sencilla.

Como parte de la estructura del proyecto econtramos el archivo /package.json/ y el directorio /npm_modules. Este directorio contiene un numero importante de sub-carpetas con los paquetes de todas las dependencias usadas por node para generar nuestra app y sus versiones específicas. Es muy recomendable instalar los paquetes del proyecto con la bandera npm install <nombre del paquete> --save-exact para evitar incompatibilidades con futuras versiones de los mismos paquetes.

La carpeta /src contienen los archivos con el código que vamos a editar. Los más importantes son: los css, el index.html que es donde corre toda la aplicación ya que, como vimos, Angular genera una SPA (aplicación de una sóla página).
También encontramos la carpeta /app donde están los archivos principales, que editaremos para crear nuestra aplicación, como es el caso de: app.component.css, app.component.html, app.component.spec.ts, app.component.ts y app.modules.ts.
Tenemos también la carpeta /assets, que con tiene todos los recursos estáticos usados por la aplicación
### Navegación básica entre componentes
Para implementar ruteo, que es la capacidad de navegar entre componentes (vistas) en Angular, es necesario importar Routes desde @angular/router en el componente base de nuestra app:

import { Routes } from '@angular/router';
Luego se deben declarar todas las rutas que vamos a usar en una constante de tipo Routes:

...
const appRoutes: Routes = [
  { path: '', component: HomeComponent },
  { path: 'home', component: HomeComponent },
  { path: 'login', component: LoginComponent }
];
...
Se incluyen todas las rutas definidas como elementos de un arreglo de objetos json de JS.
La propiedad path va a comparar el segmento coincidente en la url, mientras que component indica hacia cuál componente se va a navegar.

Para hacer funcionar las rutas en nuestra app, se debe importar el módulo RouterModule en la sección imports del app.component.ts ya que éste no se importa de manera automática.

Finalmente para implementar la navegación en nuestra app, es necesario indicar en el contenido de app.component.html una directiva <router-outlet></router-outlet> que se utilizará para inyectar eventualmente los componentes de toda la navegación que hemos definido. Todo lo que se coloque en el html, fuera de esta directiva, quedará fijado como contenido común en todas las vistas de nuestra navegación.

Es importante tener en cuenta que al usar enlaces o anclas ( <a> ... </a> ) de html, tendremos que sustituir el atributo href por routerLink, que es parte de RouterModule, para evitar la recarga completa de la página y la latencia, ya que esto iría en contra del concepto fundamental de lo que es una SPA (single page app).
### ¿Cómo usar tipos de datos con TypeScript?
TypeScript debe su nombre a los tipos de datos (types en inglés). JavaScript no es un lenguaje de programación tipado, por lo que es requerida en su sintaxis la definición de un tipo de dato al momento de instanciar las clases o variables en general. El uso de tipos explícitos en la programación permite a fin de cuentas un mejor aprovechamiento del recurso de memoria, entre muchos otros beneficios.

Los tipos básicos (built-in y definidos por el usuario) admitidos por TypeScript son: Boolean, Number, String, Array, Tuple, Enum, Void, Null y Undefined, y el tipo que es la base de todos los anteriores: Any, que básicamente representa cualquier cosa.

Los tipos de datos avanzados de Type
Script incluyen: Function, Object, Interface, Guard, Union, entre otros.
