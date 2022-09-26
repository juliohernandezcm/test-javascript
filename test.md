# Test de JavaScript

¡Es hora de poner a prueba cuánto sabes sobre JavaScript!

Esta lectura es una prueba de JavaScript. A diferencia de un examen, nadie te obligará a nada. **Puedes hacer trampa y saltar a la siguiente clase**, ese es el camino fácil. Pero tengo mucha fe en ti, confío en que seguirás mis consejos y no avanzarás a la siguiente clase hasta superar esta prueba.

## Instrucciones para tomar esta prueba

-  Evalúa muy críticamente tu conocimiento.
-  Si logras resolver la prueba, no importa cuánto te cueste, puedo asegurarte que tienes todo para continuar a las siguientes clases y tomar el resto del curso.
-  Si no lo logras, no te preocupes, absolutamente nadie puede juzgarte, solo tú. Vuelve al [Curso Básico de JavaScript](https://platzi.com/cursos/basico-javascript/), anota los temas clave donde puedes mejorar, ubica las clases donde puedes aprenderlos y estudia vigorosamente.
-  Es completamente válido hacer búsquedas en Google, cursos y tutoriales de Platzi, incluso usar tu cuaderno de notas sin importar si es físico o virtual.

Recuerda que **el éxito no se mide por cuánto tiempo te toma aprender**, esa métrica es relativamente inútil. Mejor concéntrate en completar los cursos de tu ruta de aprendizaje profesional y desarrollar los proyectos que realmente demuestran que dominas cada tecnología.

¡Mucha suerte!

## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

-  ¿Qué es una variable y para qué sirve?

Cajitas (Espacios en memoria) donde podemos guardar información dependiendo
de los tipos y estructuras de datos que soporte nuestros lenguajes.

-  ¿Cuál es la diferencia entre declarar e inicializar una variable?

Declarar es cuando le decimos a JavaScript que vamos a crear una variable con el nombre como tal,
Mientras que inicializar (o reinicializar) es asignarle un valor a esa variable.

-  ¿Cuál es la diferencia entre sumar números y concatenar strings?

Cuando sumamos numeros estamos realizando la operación matematicas de adición,
mientras que concatenar strings es unir un string con otro.

-  ¿Cuál operador me permite sumar o concatenar?

El operador que nos permite sumar o concatenar es el +. Este operador nos permite sumar números cuando lo usamos con números.
Pero cuando lo utilizamos con strings nos permite unir (concatenar) dichos strings.

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

-  Nombre -> string
-  Apellido -> string
-  Nombre de usuario en Platzi -> string
-  Edad -> number
-  Correo electrónico -> string
-  Mayor de edad -> boolean
-  Dinero ahorrado -> number
-  Deudas -> number

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```js
let name = 'Julio';
let lastname = 'Hernandez';
let username = 'Julius';
let edad = 35;
let email = 'julio@gmail.com';
let isAdult = true;
let saveMoney = 1000;
let debs = 100;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

-  Nombre completo (nombre y apellido)

```js
let fullname = `${name} ${lastname}`;
console.log(fullname);
```

-  Dinero real (dinero ahorrado menos deudas)

```js
let realMoney = saveMoney - debs;
console.log(realMoney);
```

## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

-  ¿Qué es una función?

Las funciones nos permiten encapsular (guardar) bloques de codigos para reutilizarlos y ejecutarlos en el futuro

-  ¿Cuándo me sirve usar una función en mi código?

Nos sirve cuando tenemos variables o bloques de código muy parecidos (con cambios que podrían ser parámetros y argumentos) que podemos encapsular para reutilizar mas de una vez en el futuro.

También nos sirve para ordenar y mejorar la legibilidad de nuestro código.

-  ¿Cuál es la diferencia entre parámetros y argumentos de una función?

Las funciones reciben parametros cuando las creamos, y les enviamos argumentos cuando las ejecutamos.

### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js
const name = 'Juan David';
const lastname = 'Castro Gallego';
const completeName = name + lastname;
const nickname = 'juandc';

console.log(
	'Mi nombre es ' +
		completeName +
		', pero prefiero que me digas ' +
		nickname +
		'.'
);
```

```js
function fullName(name, lastname) {
	return name + ' ' + lastname;
}

function saludo(name, lastname, nickname) {
	const completeName = fullName(name, lastname);

	console.log(
		`Mi nombre es: ${completeName}, pero prefiero que me digas: ${nickname}`
	);
}

saludo('julio', 'hernandez', 'julius');
```

## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

-  ¿Qué es un condicional?

Son la forma en que ejecutamos un bloque de código u otro dependiendo de alguna condición o validaciín.

-  ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?

IF (else y else if), switch
El condicional if (Con else y else if) nos permite hacer validaciones completamente distintas (si aspí queremos) en cada validación o condicional. En cambio, en el switch todos los cases se comparan con la misma variable o condición que definimos en el switch.

-  ¿Puedo combinar funciones y condicionales?

Si. Las funciones pueden encapsular cualquier bloque de código, incluyendo condicionales.

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```js
const tipoDeSuscripcion = 'Basic';

switch (tipoDeSuscripcion) {
	case 'Free':
		console.log('Solo puedes tomar los cursos gratis');
		break;
	case 'Basic':
		console.log(
			'Puedes tomar casi todos los cursos de Platzi durante un mes'
		);
		break;
	case 'Expert':
		console.log(
			'Puedes tomar casi todos los cursos de Platzi durante un año'
		);
		break;
	case 'ExpertPlus':
		console.log(
			'Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año'
		);
		break;
}
```

```js
if (tipoDeSuscripcion == 'Free') {
	console.log('Solo puedes tomar los cursos gratis');
} else if (tipoDeSuscripcion === 'Basic') {
	console.log('Puedes tomar casi todos los cursos de Platzi durante un mes');
} else if (tipoDeSuscripcion === 'Expert') {
	console.log('Puedes tomar casi todos los cursos de Platzi durante un año');
} else if (tipoDeSuscripcion == 'ExpertDuo') {
	console.log(
		'Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año'
	);
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays, objetos y un solo condicional. 😏

```js
const tiposDeSuscripciones = {
	free: 'Solo puedes tomar los cursos gratis',
	basic: 'Puedes tomar casi todos los cursos de Platzi durante un mes',
	expert: 'Puedes tomar casi todos los cursos de Platzi durante un año',
	expertduo:
		'Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año',
};

function conseguirTipoSuscripcion(suscripcion) {
	if (tiposDeSuscripciones[suscripcion]) {
		console.log(tiposDeSuscripciones[suscripcion]);
		return;
	}
	console.warn('Ese tipo de suscripcion no existe');
}

conseguirTipoSuscripcion('expertduo');
```

## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

-  ¿Qué es un ciclo?

Un ciclo es la forma de ejecutar un bloque de código mientras una condición sea verdadera o se cumpla.

-  ¿Qué tipos de ciclos existen en JavaScript?

while, do while y for.

-  ¿Qué es un ciclo infinito y por qué es un problema?

Es cuando la validaciíon de nuestros condicionales nunca se cumple y termina colgando la aplicación (ej. cuando el navegador ya no puede más de tanta ejecución de ese bloque de código.)

-  ¿Puedo mezclar ciclos y condicionales?

Sí, aunque los ciclos son una especie de condicionales, nada nos impide agregar más condicionales dentro del ciclo.

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```js
for (let i = 0; i < 5; i++) {
	console.log('El valor de i es: ' + i);
}

for (let i = 10; i >= 2; i--) {
	console.log('El valor de i es: ' + i);
}
```

```js
let i = 0;

while (i < 5) {
	console.log('El valor de i es: ' + i);
	i++;
}

let i = 10;

while (i > 1) {
	console.log('El valor de i es: ' + i);
	i--;
}
```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```js
let respuesta;

while (respuesta != '4') {
	let pregunta = prompt('¿Cuánto es 2 + 2?');
	respuesta = pregunta;
}
```

## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

-  ¿Qué es un array?

Es una lista de elementos.

```js
const array = [1, 'jajaja', true, false];
```

-  ¿Qué es un objeto?

Es una lista de elementos PERO cada elemento tiene un nombre clave.

```js
const obj = {
	nombre: 'fulanito',
	edad: 3,
	comidasFavoritas: ['Pollo frito', 'Pizza'],
};
```

-  ¿Cuándo es mejor usar objetos o arrays?

Arrays cuando lo que aremos en un elemento es lo mismo que en todo lo demás (la regla se puede incumplir). Mientras que un objeto cuando los nombres de cada elemento son importantes para nuestro algoritmo.

-  ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

Si. los arrays pueden guardar objetos. Y los objetos pueden guardar arrays entre sus propiedades.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```js
function imprimirPrimerElementoArray(arr) {
	console.log(arr[0]);
}
```

### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```js
/* Forma echa en la clase */
function imprimirElementoPorElemento(arr) {
	for (let i = 0; i < arr.length; i++) {
		console.log(arr[i]);
	}
}
```

```js
/* Forma echa por mi con un metodo de array */
function imprimirElementoPorElemento(arr) {
	arr.forEach((element) => {
		console.log(element);
	});
}
```

### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```js
function imprimeElementoPorElementoObjeto(obj) {
	const arr = Object.values(obj);
	arr.forEach((element) => {
		console.log(element);
	});
}
```

## ¿Cómo te fue? 🏆

**¡Felicidades por completar la prueba de JavaScript!** Confío en que hayas completado cada paso y hayas pausado para repasar los temas de los ejercicios que se te complicaron.

Ahora sí, continúa a la siguiente clase, pero recuerda que **ya no puedes abandonar el curso**, debes completarlo hasta el final. No importa cuánto tiempo te tome. **Yo sé que tú puedes. Y tú deberías de saberlo también.**

¡Te espero en la siguiente clase para comenzar!
