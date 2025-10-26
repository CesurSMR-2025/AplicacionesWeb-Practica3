# Aplicaciones Web - Práctica 3: Introduccion a JavaScript
## Introducción
JavaScript es el lenguaje de programación que se utiliza en las páginas web para hacerlas interactivas. Es el único lenguaje que los navegadores web entienden de forma nativa, por lo que es una herramienta clave para el desarrollo web. En esta práctica, aprenderemos los conceptos básicos de JavaScript y más adelante veremos cómo integrarlo en nuestras páginas web. 

## JavaScript

Algunas de las características más importantes de JavaScript son:
- **Lenguaje interpretado**: JavaScript no necesita ser compilado antes de ejecutarse. Se interpreta línea por línea en tiempo de ejecución (i.e. cuando se ejecuta).
- **Tipado dinámico**: No es necesario declarar (i.e. especificar) el tipo de dato de una variable al momento de su creación. El tipo se determina automáticamente en tiempo de ejecución.
- **Integración con HTML y CSS**: JavaScript se integra fácilmente con HTML y CSS, lo que permite manipular el contenido y el estilo de las páginas web de manera dinámica.
- **Multiplataforma**: JavaScript se puede ejecutar en diferentes entornos, como navegadores web, servidores (con Node.js) y aplicaciones móviles (con frameworks como React Native).
- **Amplia comunidad y ecosistema**: JavaScript cuenta con una gran comunidad de desarrolladores y una amplia variedad de bibliotecas y frameworks (como React, Angular y Vue.js) que facilitan el desarrollo de aplicaciones web complejas.
- **Soporte en todos los navegadores modernos**: Todos los navegadores web modernos (como Chrome, Firefox, Safari y Edge) soportan JavaScript, lo que garantiza que las aplicaciones web desarrolladas con este lenguaje funcionen en una amplia variedad de dispositivos y plataformas.
- **Sintaxis similar a otros lenguajes**: La sintaxis de JavaScript comparte similitudes con otros lenguajes de programación populares, como C, Java y Python, lo que facilita el aprendizaje para aquellos que ya tienen experiencia en programación.

## Node.js
JavaScript fue creado para ejecutarse en el navegador, pero con la llegada de Node.js, también se puede ejecutar en el servidor. Node.js o **Node** es un entorno de ejecución de JavaScript que permite ejecutar código JavaScript en el servidor, es decir, fuera del navegador. Esto posibilita el desarrollo de aplicaciones web completas utilizando JavaScript tanto en el cliente (navegador) como en el servidor.

Para ejecutar código JavaScript en Node.js, es necesario tener instalado Node.js en el sistema. Una vez instalado, se puede ejecutar un archivo JavaScript desde la línea de comandos utilizando el comando `node` seguido del nombre del archivo.

```bash
node archivo.js
```

Node.js también incluye un conjunto de módulos integrados que proporcionan funcionalidades adicionales, como la manipulación de archivos, la creación de servidores web y la gestión de bases de datos. Además, Node.js cuenta con un gestor de paquetes llamado **npm** (Node Package Manager) que permite instalar y gestionar bibliotecas y frameworks de terceros.

## Variables y tipos de datos
### Tipos
En JavaScript, al igual que en otros lenguajes de programación, las variables son contenedores que almacenan datos. JavaScript es un lenguaje de tipado dinámico, lo que significa que no es necesario declarar el tipo de dato de una variable al momento de su creación. Los tipos de datos más comunes en JavaScript son:

- Números (Number): representan valores numéricos, tanto enteros como decimales.
- Cadenas de texto (String): representan secuencias de caracteres, como palabras o frases
- Booleanos (Boolean): representan valores de verdad, es decir, `true` o `false`.
- Nulos (Null): representan la ausencia intencional de cualquier valor.
- Indefinidos (Undefined): representan variables que han sido declaradas pero no inicializadas.

```js
let nulo = null; // nulo es una variable de tipo Null
let indefinido; // indefinido es una variable de tipo Undefined
let numero = 42; // numero es una variable de tipo Number
let cadena = "Hola, mundo!"; // cadena es una variable de tipo String
let booleano = true; // booleano es una variable de tipo Boolean
```

Podemos inspeccionar el tipo de una variable utilizando el operador `typeof`.

```js
console.log(typeof numero); // Imprime "number"
console.log(typeof cadena); // Imprime "string"
console.log(typeof booleano); // Imprime "boolean"
console.log(typeof nulo); // Imprime "object" (no preocuparse por entender esto ahora)
console.log(typeof indefinido); // Imprime "undefined"
```

### Declaración de variables

Las variables en JavaScript se pueden declarar utilizando las palabras clave `var`, `let` o `const`. La diferencia principal entre ellas es donde serán válidas (scope) y la mutabilidad (si se puede cambiar su valor o no).

- `let`:  La variable es válida solo en el bloque en el que se declara. Su valor puede ser reasignado.
- `const`: La variable es válida solo en el bloque en el que se declara. Su valor no puede ser reasignado una vez que se ha establecido.
- `var`: Se desaconseja su uso.

```js
let edad = 25; // Declaración de una variable con let
edad = 26; // Reasignación de la variable edad
const pi = 3.14; // Declaración de una variable con const
// pi = 3.1416; // Esto generaría un error, ya que pi
// es una constante y no puede ser reasignada
```

### Conversión de tipos
JavaScript realiza conversiones de tipos de manera automática en ciertas situaciones. Por ejemplo, al utilizar el operador `+` con una cadena y un número, el número se convierte automáticamente a cadena y se concatenan.

```js
let resultado = "El número es: " + 42; // resultado es "El número
// es: 42"
```

**Hay que tener cuidado con las conversiones automáticas, ya que pueden llevar a resultados inesperados.**

También es posible convertir tipos de datos de forma explícita utilizando funciones como `String()`, `Number()` y `Boolean()`.

```js
let numeroComoCadena = String(42); // Convierte el número 42 a una cadena
let cadenaComoNumero = Number("42"); // Convierte la cadena "42" a un número
let booleanoComoNumero = Number(true); // Convierte el booleano true a 1
let numeroComoBooleano = Boolean(1); // Convierte el número 1 a true
```


## Operadores y expresiones
Los operadores son símbolos que realizan operaciones sobre uno o más operandos (valores o variables). Algunos de los operadores más comunes en JavaScript son:
- Aritméticos: `+`, `-`, `*`, `/`, `%` (suma, resta, multiplicación, división, módulo)
- De asignación: `=`, `+=`, `-=`, `*=`, `/=`
- De comparación: `==`, `===`, `!=`, `!==`, `<`, `>`, `<=`, `>=`
- Lógicos: `&&`, `||`, `!` (AND, OR, NOT)
- De concatenación: `+` (para unir cadenas de texto)
- Unarios: `++`, `--` (incremento y decremento)
- Tipo: `typeof` (para obtener el tipo de una variable)
- Exponentiation: `**` (para elevar un número a una potencia)

```js
let a = 10;
let b = 5;
let c = a * 32 * b; // c es 1600
```

```js
let nombre = "Juan";
let saludo = "Hola, " + nombre + "!"; // saludo es "Hola, Juan!"
```

```js
let esMayor = a > b; // esMayor es true
```

## Comentarios
Los comentarios son líneas de texto que se incluyen en el código para explicar su funcionamiento o para dejar notas para otros desarrolladores. En JavaScript, los comentarios se pueden hacer de dos maneras:

1. Comentarios de una sola línea: Se utilizan dos barras inclinadas `//` al inicio de la línea.
2. Comentarios de varias líneas: Se encierran entre `/*` y `*/`.

```js
// Este es un comentario de una sola línea

/*
Este es un comentario
de varias líneas
*/
```

Son **muy importantes** para mantener el código legible y comprensible, especialmente en proyectos grandes o cuando se trabaja en equipo.

## Estructuras de control
### Condicionales
Las estructuras condicionales permiten ejecutar diferentes bloques de código según si una condición es verdadera o falsa. En JavaScript, las estructuras condicionales más comunes son `if`, `else if`, `else`.

El bloque de código dentro de una estructura condicional se ejecuta solo si la condición evaluada es verdadera. Si la condición es falsa, se puede utilizar una instrucción `else` para ejecutar un bloque de código alternativo.

```js
let a = 10;
let b = 5;
if (a > b) {
    console.log("a es mayor que b");
} else if (a < b) {
    console.log("a es menor que b");
} else {
    console.log("a es igual a b");
}
```

Básicamente, una estructura condicional está formada por una instrucción `if`, 0 o más instrucciones `else if` y 0 o 1 instrucción `else`. La instrucción `if` es obligatoria, mientras que las instrucciones `else if` y `else` son opcionales.

```js
if (condición1) {
    // Bloque de código que se ejecuta si condición1 es verdadera
} else if (condición2) {
    // Bloque de código que se ejecuta si condición2 es verdadera
} else if (condición3) {
    // Bloque de código que se ejecuta si condición3 es verdadera
} else {
    // Bloque de código que se ejecuta si ninguna de las condiciones anteriores es verdadera
}
```

Las condiciones se evalúan en orden, de arriba hacia abajo. La primera condición que se evalúa como verdadera ejecuta su bloque de código asociado y el resto de condiciones se ignoran. Si ninguna condición es verdadera y existe una instrucción `else`, se ejecuta su bloque de código asociado.

### Bucles
Los bucles permiten ejecutar un bloque de código repetidamente mientras una condición sea verdadera. Los bucles más comunes son `while` y `for`.

El bucle `while` evalúa la condición antes de cada iteración, y si es verdadera, ejecuta el bloque de código. Si la condición es falsa, el bucle se detiene y se continúa la ejecución fuera del bucle. Mientras la condición sea verdadera, el bloque de código se ejecutará otra vez.

```js
// Bucle while
let j = 0;
while (j < 5) {
    console.log("Iteración " + j);
    j++; // Esto es equivalente a j = j + 1
}
```

El bucle `for` es un bucle que se utiliza cuando se conoce de antemano el número de iteraciones que se van a realizar. Está compuesto por tres partes: la inicialización, la condición y la actualización. La **inicialización** se ejecuta una sola vez al principio del bucle, la **condición** se evalúa antes de cada iteración y la **actualización** se ejecuta al final de cada iteración.

```js
// Bucle for
for (let i = 0; i < 5; i++) {
    console.log("Iteración " + i);
}
```

Es posible interrumpir la ejecución de un bucle utilizando la instrucción `break`. Cuando se encuentra una instrucción `break` dentro de un bucle, la ejecución del bucle se detiene inmediatamente y se continúa con la siguiente instrucción después del bucle.

```js
// Ejemplo de uso de break en un bucle
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break; // Interrumpe el bucle cuando i es igual a 5
    }
    console.log("Iteración " + i);
}
```

También es posible saltar a la siguiente iteración de un bucle utilizando la instrucción `continue`. Cuando se encuentra una instrucción `continue` dentro de un bucle, la ejecución del bloque de código actual se detiene y se pasa a la siguiente iteración del bucle.

```js
// Ejemplo de uso de continue en un bucle
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        continue; // Salta a la siguiente iteración cuando i es igual a 5
    }
    console.log("Iteración " + i);
}
```

Es posible utilizar el bucle `while` para todos los casos en los que se necesite un bucle, pero el bucle `for` en algunos casos puede resultar más conveniente y legible.

## Funciones
Las funciones son bloques de código reutilizables que realizan una tarea específica. En JavaScript, las funciones se definen utilizando la palabra clave `function`, seguida del nombre de la función, paréntesis y llaves.

```js
function saludar(nombre) {
    console.log("Hola, " + nombre + "!");
}
```

Para llamar a una función, simplemente se escribe su nombre seguido de paréntesis, y si la función tiene parámetros, se pasan los argumentos correspondientes dentro de los paréntesis.

```js
saludar("Juan"); // Llama a la función saludar con el argumento "Juan"
```

Las funciones pueden devolver un valor utilizando la palabra clave `return`. Cuando se ejecuta una instrucción `return`, la función termina y devuelve el valor especificado.

```js
function sumar(a, b) {
    return a + b; // Devuelve la suma de a y b
}
let resultado = sumar(3, 5); // Llama a la función sumar y almacena el resultado en la variable resultado
console.log(resultado); // Imprime 8
```

## Arrays
Los arrays son estructuras de datos que permiten almacenar múltiples valores en una sola variable. En JavaScript, los arrays se definen utilizando corchetes `[]`, y los elementos se separan por comas.

Para acceder a un elemento específico de un array, se utiliza su índice (posición), que comienza en 0.

```js
let frutas = ["manzana", "banana", "naranja"];
console.log(frutas[0]); // "manzana"
```

Tambien es posible posible declarar arrays vacíos y luego agregar elementos.

```js
let numeros = [];
numeros.push(1);
numeros.push(2);
numeros.push(3);
console.log(numeros); // [1, 2, 3]
```

O declarar arrays con un tamaño fijo.

```js
let dias = new Array(7);
dias[0] = "Lunes";
dias[1] = "Martes";
dias[2] = "Miércoles";
dias[3] = "Jueves";
dias[4] = "Viernes";
dias[5] = "Sábado";
dias[6] = "Domingo";
console.log(dias);
```

Tambien es posible recorrer los elementos de un array utilizando un bucle `for`. Con 

```js
for (let i = 0; i < frutas.length; i++) {
    console.log(frutas[i]);
}
```

O con un bucle `for...in`, que itera sobre los indices del array, guardando en cada iteración un elemento del array en una variable.

```js
for (let i in frutas) {
    console.log(frutas[i]);
}
```

O con un bucle `for...of`, que itera directamente sobre los elementos del array.

```js
for (let fruta of frutas) {
    console.log(fruta);
}
```

## Objetos
Podemos pensar en los objetos como colecciones de pares clave-valor. Cada clave (también llamada propiedad) es un nombre que identifica un valor asociado. Los valores pueden ser de cualquier tipo de dato, incluyendo otros objetos o funciones.

```js
let persona = {
    nombre: "Juan",
    edad: 30,
    esEstudiante: false,
    saludar: function() {
        console.log("Hola, mi nombre es " + this.nombre);
    }
};
```
Para acceder a las propiedades de un objeto, se utiliza la notación de punto o la notación de corchetes.

```js
console.log(persona.nombre); // "Juan"  
console.log(persona["edad"]); // 30
```

Para llamar a un método (función) de un objeto, se utiliza la notación de punto seguida de paréntesis.

```js
persona.saludar(); // Llama al método saludar del objeto persona
```

## Lectura de argumentos
En node.js podemos leer los argumentos de la línea de comandos utilizando el objeto `process.argv`, que es un array que contiene los argumentos pasados al script.

```js
// Imprime todos los argumentos
console.log(process.argv);

// Accede a un argumento específico
let nombre = process.argv[2];
console.log("Hola, " + nombre + "!");
```

En la primera posición (índice 0) se encuentra la ruta del ejecutable de Node.js, en la segunda posición (índice 1) se encuentra la ruta del script que se está ejecutando, y a partir de la tercera posición (índice 2) se encuentran los argumentos pasados al script.

## Clases
Las clases son plantillas para crear objetos con propiedades y métodos predefinidos. En JavaScript, se pueden definir clases utilizando la palabra clave `class`.

```js
class Persona {
    constructor(nombre, edad) {
        this.nombre = nombre;
        this.edad = edad;
    }

    saludar() {
        console.log("Hola, mi nombre es " + this.nombre);
    }
}
```

Para crear un objeto de una clase, se utiliza la palabra clave `new` seguida del nombre de la clase y paréntesis con los argumentos necesarios para el constructor.

```js
let juan = new Persona("Juan", 30);
juan.saludar(); // Llama al método saludar del objeto juan
```
