# DATE JavaScript



la clase `Date`en JavaScript se utiliza par atrabajar con fechas y horas en aplicaciones web y se utiliza comúnmente para realizar operaciones de manejo de tiempo.

#### Creación de objetos Date

Podemos crear un objeto `Date`de las siguientes maneras:

```javascript
// De esta forma creamos un objeto Date con la fecha y hora actuales
const fechaActual = new Date();

//De esta forma creamos un objeto Date con una fecha especifica
const fechaEspecifica = new Date('2024-02-13');

//De esta forma creamos un objeto Date con una fecha y hora especificas
const fechaHoraEspecifica = new Date(2024,1,13,12,30,0);

```

#### Métodos de la clase Date

Algunos de los métodos más comunes de la clase `Date` son:

##### Métodos para obtener diferentes partes de la fecha y hora

- `getFullYear()`: Devuelve el año

  ```javascript
  const año = fechaActual.getFullYear();
  ```

- `getMonth()`: Devuelve el mes (0-11)

  ```javascript
  // Los meses van de 0 a 11
  const mes = fechaActual.getMonth(); 
  ```

- `getDate()`: Devuelve el día del mes (1-31)

  ```javascript
  const dia = fechaActual.getDate();
  ```

- `getDay()`: Devuelve el día de la semana (0-6)

  ```javascript
  // Los días de la semana van de 0 (domingo) a 6 (sábado)
  const diaSemana = fechaActual.getDay(); 
  ```

- `getHours()`: Devuelve la hora (0-23)

  ```javascript
  const hora = fechaActual.getHours();
  ```

- `getMinutes()`: Devuelve los minutos (0-59)

  ```javascript
  const minutos = fechaActual.getMinutes();
  ```

- `getSeconds()`: Devuelve los segundos (0-59)

  ```javascript
  const segundos = fechaActual.getSeconds();
  ```

- `getMilliseconds()`: Devuelve los milisegundos (0-999)

  ```javascript
  const milisegundos = fechaActual.getMilliseconds();
  ```

- `getTime()`: Devuelve el número de mili-segundos desde el 1 de enero de 1970 (Epoch time)

  ```javascript
  const tiempoEpoch = fechaActual.getTime();
  ```

  

  ##### Métodos para convertir la fecha a diferentes formatos de cadena

- `toString()`: Devuelve la fecha como una cadena legible para humanos

  ```javascript
  const cadenaFecha = fechaActual.toString();
  ```

- `toDateString()`: Devuelve la parte de la fecha como una cadena

  ```javascript
  const cadenaFechaSimple = fechaActual.toDateString();
  ```

- `toTimeString()`: Devuelve la parte del tiempo como una cadena.

  ```javascript
  const cadenaHoraSimple = fechaActual.toTimeString();
  ```

- `toLocaleString()`: Devuelve la fecha y la hora como una cadena en la configuración regional local

  ```javascript
  const cadenaLocal = fechaActual.toLocaleString();
  ```

- `toLocaleDateString()`: Devuelve la parte de la fecha como una cadena en la configuración regional local

  ```javascript
  const cadenaFechaLocal = fechaActual.toLocaleDateString();
  ```

- `toLocaleTimeString()`: Devuelve la parte del tiempo como una cadena en la configuración regional local

  ```javascript
  const cadenaHoraLocal = fechaActual.toLocaleTimeString();
  ```

##### Métodos modifican el objeto `Date` existente y devuelven el valor actualizado de la fecha

1. setFullYear(year[, month[, day]]):

   - Establece el año de la fecha.

   - `year`: Valor numérico que representa el año.

   - `month` (opcional): Valor numérico que representa el mes (0-11).

   - `day` (opcional): Valor numérico que representa el día del mes (1-31).

```javascript
javascriptCopy codeconst fecha = new Date();
fecha.setFullYear(2025); // Establecer el año 2025
```

2. setMonth(month[, day]):

   - Establece el mes de la fecha.

   - `month`: Valor numérico que representa el mes (0-11).

   - `day` (opcional): Valor numérico que representa el día del mes (1-31).

```javascript
javascriptCopy codeconst fecha = new Date();
fecha.setMonth(5); // Establecer junio (mes 5)
```

3. setDate(day):

   - Establece el día del mes de la fecha.

   - `day`: Valor numérico que representa el día del mes (1-31).

```javascript
javascriptCopy codeconst fecha = new Date();
fecha.setDate(15); // Establecer el día 15 del mes
```

4. setHours(hours[, min[, sec[, ms]]]):

   - Establece la hora de la fecha.

   - `hours`: Valor numérico que representa la hora (0-23).

   - `min` (opcional): Valor numérico que representa los minutos (0-59).

   - `sec` (opcional): Valor numérico que representa los segundos (0-59).

   - `ms` (opcional): Valor numérico que representa los milisegundos (0-999).

```javascript
javascriptCopy codeconst fecha = new Date();
fecha.setHours(12, 30); // Establecer 12:30
```

5. setMinutes(min[, sec[, ms]]):

   - Establece los minutos de la fecha.

   - `min`: Valor numérico que representa los minutos (0-59).

   - `sec` (opcional): Valor numérico que representa los segundos (0-59).

   - `ms` (opcional): Valor numérico que representa los milisegundos (0-999).

```javascript
javascriptCopy codeconst fecha = new Date();
fecha.setMinutes(45); // Establecer 45 minutos
```

6. setSeconds(sec[, ms]):

   - Establece los segundos de la fecha.

   - `sec`: Valor numérico que representa los segundos (0-59).

   - `ms` (opcional): Valor numérico que representa los milisegundos (0-999).

```javascript
javascriptCopy codeconst fecha = new Date();
fecha.setSeconds(30); // Establecer 30 segundos
```

7. setMilliseconds(ms):

   - Establece los milisegundos de la fecha.

   - `ms`: Valor numérico que representa los milisegundos (0-999).

```javascript
javascriptCopy codeconst fecha = new Date();
fecha.setMilliseconds(500); // Establecer 500 milisegundos
```



**OPERACIONES CON FECHAS Y EJEMPLOS**

1. Sumar o restar días a una fecha:

```javascript
const fechaActual = new Date();

fechaActual.setDate(fechaActual.getDate() + 5);

console.log('Fecha después de sumar 5 días:', fechaActual);
```

2. Comparar dos fechas:

```javascript
const fecha1 = new Date('2024-02-13');
const fecha2 = new Date('2024-02-15');

if (fecha1 > fecha2) {
    console.log('La fecha 1 es posterior a la fecha 2');
} else if (fecha1 < fecha2) {
    console.log('La fecha 1 es anterior a la fecha 2');
} else {
    console.log('Ambas fechas son iguales');
}
```

3. Calcular la diferencia entre dos fechas:

```javascript
const fechaInicio = new Date('2024-02-13');
const fechaFin = new Date('2024-02-20');

// Restar las fechas y convertir el resultado a días
const diferenciaEnTiempo = fechaFin.getTime() - fechaInicio.getTime();
const diferenciaEnDias = diferenciaEnTiempo / (1000 * 3600 * 24);

console.log('Diferencia en días:', diferenciaEnDias);
```

4. Obtener el día de la semana de una fecha:

```javascript
const fecha = new Date('2024-02-13');
const diasSemana = ['Domingo', 'Lunes', 'Martes', 'Miércoles', 'Jueves', 'Viernes', 'Sábado'];
const diaSemana = diasSemana[fecha.getDay()];

console.log('Día de la semana:', diaSemana);
```

5. Calcular la edad a partir de la fecha de nacimiento:

```javascript
const fechaNacimiento = new Date('1999-11-28');
const fechaActual = new Date();

let edad = fechaActual.getFullYear() - fechaNacimiento.getFullYear();
if (fechaActual.getMonth() < fechaNacimiento.getMonth() || 
    (fechaActual.getMonth() === fechaNacimiento.getMonth() && fechaActual.getDate() < fechaNacimiento.getDate())) {
    edad--;
}

console.log('Edad:', edad);
```
