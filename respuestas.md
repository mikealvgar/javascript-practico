
## Variables

- ¿Que es una variable y para qué sirve?
  Cajitas (espacios en memoria) donde podemos guardar información (dependiendo de los tipos y estructuras de datos que soporte nuestro lenguaje).

- ¿Cuál es la diferencia entre declarar e inicializar una varaible?
  Cuando declaramos en Javascript que vamos a crear un varaible con nombre tal. Mientras que inicializar es asignar un valor a la variable declarada.

- ¿Cuál es la diferencia entre sumar números y concatenar Strings?
- ¿Cuál operador me permite sumar o concatenar?
  El operar que nos permite sumar o concatenar es +. Cuando sumamos este operador nos permite sumar números cuando lo usamos con números. Pero cuando lo usamos con Strings, lo que hace es concatenar nuestros Strings.

- Determina el nombre y tipo de dato para almacenar en variables la siguiente información:
  - Nombre: String
  - Apellido: String
  - Nombre de usuario en Platzi: String
  - Edad: number
  - Correo electrónico: String
  - Mayor de edad: boolean
  - Dinero ahorrado: number
  - Deudas: number

- Traduce a código Javascrip las varabiles del ejemplo anterior y deja tu código en los comentarios.
 
  ```
  let nombre = 'Miguel';
  let apellido = 'Alvarez Garcia';
  let username = 'MikeDark';
  let mail = 'miguel@gmail.com';
  let esMayorDeEdad = true;
  let dineroAhorrado = 10000;
  let deudas = 100;
  ```

- Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior;

  - Nombre completo (nombre y apellido)
  - Dinero real (dinero ahorrado menos deudas)
  
  ````
  let nombreCompleto = nombre + apellido;
  let dineroReal = dineroAhorrado - deudas;
  ```

## Funciones

- ¿Qué es una función?
  Las funciones nos permiten encapsular (guardar) bloques de código para reutilizarlos y ejecutarlos en el futuro.

- ¿Cúando me sirve usar una función en mi código?
  Nos sirve cuando tenemos código repetido o muy parecidos, que podrian tener paramentros o argumentos que podriamos reutilizar encapsulando en una función.

  También nos sirve para mejorar la legibilidad de nuestro código.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?
  Las funciones reciben parámetros cuando las creamos. Y les enviamos argumentos cuando las ejecutamos.

  ### Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función.

  ```
  function(name, lastName, nickname){
    let fullName = nombreCompleto(name, lastName);
    let nickname = nickname;
    return 'Mi nombre es ' + fullName + ' ' + 'Pero prefiero que me digan ' + nickname;
  }
  ```

## Condicionales

- ¿Qué es un condicional?
  Son la forma en que ejecutamos un bloque de código u otro de pendiendo de alguna condición o validación.

- ¿Qué tipos de condicionales existen en Javascript y cuáles son sus diferencias?
  if(else y else if) y Switch

  El condiconal Switch nos da opciones o casos para preguntar si la condición se esta cumpliendo o no.
  El condicional If valida entre varias condiciones, a diferencia que Switch que siempre valida lo mismo.

```js
  function conseguirTipoSucripcion(suscripcion) {
    if(suscripcion == 'Free') {
        console.log("Solo puedes tomar los cursos gratis");
        return;
    }

    if(suscripcion == 'Basic') {
        console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
        return;
    }

    if(suscripcion == 'Expert') {
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
        return;
    }

    if(suscripcion == 'ExpertDuo') {
        console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
        return;
    }

    console.warn("Ese tipo de suscripción no existe");
  }
```

```js
  function conseguirTipoSucripcion(suscripcion) {
    if(tipoDeSuscripciones[suscripcion]) {
        console.log(tipoDeSuscripciones[suscripcion]);
        return;
    }
    
    console.warn("Ese tipo de suscripción no existe");
  }
```

  
  ## Ciclos

  - ¿Que es un ciclo?
  
  La forma de ejecutar un bloque de código hasta que se cumpla cierta condición.
  
  - ¿Que tipos de ciclos existen en JavaScript?
  While, do while y for.

  - ¿Que es un ciclo infinito y por que´es un problema?

  Es cuando la validacióon de nuestros condicionales nunca se cumple y termina toteando (dañando) la aplicación (e.j. cuando el navegador ya no puede más de tanta ejecución de ese bloque de código).

  - ¿Puedo mezclar ciclos y condicionales?

  Sí, aunque los ciclos son una especie de condicionales, nada nos impide agregar más condicionales dentro del ciclo.

  ### Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

  ```
  for (let i = 0; i < 5; i++){
    console.log("El valor de i es: " + i);
  }

  let i = 0;
  while (i < 5) {
    console.log("El valor de i es: " + i);
  }

  for (let i = 10; i >= 2; i--){
    console.log("El valor de i es: " + i);
  }

  let i = 10;
  while(i >= 2){
    console.log("El valor de i es: " + i);
    i--;
  }

### Escribe un código en Javascript que le pregunte a los usuarios cúanto es `2 + 2`, Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

```js
while (respuesta != '4') {
    let pregunta = prompt('Cúanto es 2 + 2')
    respuesta = pregunta;
}
```

## Listas

- ¿Qué es un array?

Es una lista de elementos.

```
const array = [1, 'jaja', true, false, {nombre: 'Mike'}];
```

- ¿Qué es un objeto?

Es una lista de elementos PERO cada elemento tiene un nombre clave.

```
const obj = {
  nombre: 'Fulanito',
  edad: 3,
  comidasFavoritas: ['Pollo', 'verduras', 'legunbres']
}
```

- ¿Cuándo es mejor usar objetos o arrays?

Arrays cunado lo que haremos en un elemento es lo mismo que en todos los demás (la regla se puede incumplir). Mientras que un objeto cuando los nombres de cada elemento son importantes para nuestro algoritmo.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

Sí, Los arrays pueden guardar objetos. Y los objetos pueden guardar arrays entre sus propiedades

### Crea una función que pueda recibir cualquier array como párametro e imprima su primer elemento.
```js
function imprimirPrimerElemento(arr){
    console.log(arr[0])
}
```
### Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```js
function imprimirElementoPorElemento(arr){
    for(var i = 0; i < arr.length; i++){
        console.log(arr[i])
    }
}
```

### Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```js
function imprimirElementoPorElemento(obj){
    var arr = Object.values(obj);
    for(var i = 0; i < arr.length; i++){
        console.log(arr[i])
    }
}
```