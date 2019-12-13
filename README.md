# Proyecto_Aplicaciones
_El proyecto trata de dar solución al problema de estacionamiento dentro de la ciudad de Loja. Para ello se ha desarrollado un sistema que le permita a los conductor poder estacionarse en un parqueadero privado desde su telefono movil, esta solucion tambien esta orientada al negocio de los parqueaderos, ya que los mismo podrán administrarlo dentro del sistema._

## Autores ✒️

* **Stalin Carrión** 
* **Anthony Ortiz** 

## Información 📖
Puedes encontrar mucho más de la descripción de este proyecto en este link [Información](https://drive.google.com/file/d/1TqT9R6WVpZi8IwziUe5A-vajkkacOscP/view?usp=sharing)

### Requerimientos 📋

_Se detallan los requerimientos encontrados en el problema_
### Elementos básicos
* Información del conductor
	* Si esta disponible el parqueo.
	* Informar la velocidad(minutos), la distancia de donde se encuentra hasta llegar al parqueaderos.
	* Calcular el índice de disponibilidad. o  informar el tiempo minutos) en los que se libera en general los parqueaderos.
	* No deben de registrarse para consultar.
	* Recolectar datos que no comprometan al conductor(el conductor dar permisos).
* Gestión de parqueadero
	* Solo privados.
	* Se tienen que registrar (compartir información privada (dirección, latitud, longitud) y número de parqueaderos que tiene).
	* Puede agregar servicios adicionales(copias, lavados,etc)podrá eliminarlos también.
	* Debe mostrar cuando el espacio esté ocupado o libre.
	* Podrá agregar o eliminar espacios de parqueo.
	* El sistema le mostrará los espacios que estén libres u ocupados.
	* El parqueadero será quien ponga el precio de los espacios,descuentos y promociones.
	* El valor a pagar dependerá del tiempo que esté el vehículo aparcado.
	* Permitir diferente tipos de cobro de forma dinámica.
* Gestión de cobro
	* Se podrá pagar en efectivo u otro tipo de cobro(tarjetas de crédito o debido,billetera móvil).
	* Tarjetas recargables (digitales).
	* Podrán reservar parqueos(solo con tarjeta y solo uno) solo socios.
	* Cuando se reserven los parqueos aparecerá en estado no disponible, si no llega en 10 minutos se vuelve en estado disponible.
	* Las tarjetas no estarán atadas a un conductor.
	* Solo habrá una única reserva y no podrá ser en diferentes parqueadores o diferentes espacios de parqueos.
	* Podrá estar la tarjeta en un estado de bloqueo por x razón.
	* Tarjetas con un valor superior a $0.25 estará en estado activo sino inactivo.
	* Solo las tarjetas activas podrán alquilar parqueos y reservas.
	* Si la tarjeta no tiene saldo. el vehículo no podrá abandonar el parqueo (el conductor debe recargar la tarjeta).
	* El conductor puede consultar el saldo.
	* Informar el tiempo de reserva según el saldo que tenga en la tarjeta. 
* Otras Características
	* No se mostrará información personal o del vehículo.
	* No se mostrará información de la recarga de las tarjetas de crédito.
	* Tendrá un historial o registro del uso de las tarjetas (cambios de estados, recargas, etc).
	* Crear tarjetas.
	* Los servicios adicionales se pueden cancelar con la tarjeta.
### Diagrama de casos de uso
![tt](https://user-images.githubusercontent.com/14815092/70767510-9d6c2480-1d2f-11ea-8cc0-c54d22558660.png)



### Especificacion de casos de uso
| Nombre: | Notificar tiempo de llegada al parqueadero |

|CASO: | 1 |
|-----------|-----------|
| Actores:  | Conductor |
| Descripción: | El conductor podrá visualizar el tiempo que le tomará llegar a los parqueaderos. |
| Precondiciones: | El conductor debe activar la ubicación en su celular. |
| Poscondiciones: | El sistema muestra el tiempo calculado de la llegada al parqueadero. |
| Flujo básico:  |
|  1. El sistema mostrará un mapa en donde se muestre la posición del conductor y el parqueadero al que desea ir.
   2. El sistema calculará la distancia entre el conductor y el parqueadero.
   3. El sistema le mostrará al conductor en forma de mensaje el tiempo en minutos que tardará en llegar a ese parqueadero. |

|CASO: | 2 |
|-----------|-----------|
| Nombre: | Información índice de disponibilidad del parqueadero |
| Actores:  | Conductor |
| Descripción: | El conductor podrá visualizar el índice de disponibilidad de los parqueaderos en horas. |
| Precondiciones: | El conductor debe haber activado la ubicación en su celular. |
| Poscondiciones: | El sistema muestra el cálculo. |
| Flujo básico:  |
|  1. El sistema mostrará los parqueaderos que estén disponibles.
   2.El conductor selecciona el parqueadero que quiera.
   3.El sistema le mostrará el índice en el que el parqueadero por lo general tiene espacios disponibles.|

|CASO: | 3 |
|-----------|-----------|
| Nombre: | Registrar parqueadero |
| Actores:  | Administrador |
| Descripción: | El administrador registra todos los datos necesarios para que el parqueadero pueda implementarse dentro del sistema. |
| Precondiciones: |  |
| Poscondiciones: | El nuevo parqueadero se almacenará en la base de datos. |
| Flujo básico:  |
|  1. El administrador ingresa a la opción de registrar parqueaderos y el sistema le despliega el formulario de registro de parqueaderos.
   2. El administrador ingresa todos los datos referentes al parqueadero(Nombre, latitud, longitud, dirección, descripción, teléfono, celular, número de espacios que tiene)
   3. El administrador presiona el botón de registrar y el sistema lo guarda en su base de datos.
   4. El sistema se actualiza automáticamente con el nuevo parqueadero ingresado. |

|CASO: | 4 |
|-----------|-----------|
| Nombre: | Gestionar espacios |
| Actores:  | Administrador |
| Descripción: | El administrador podrá crear o eliminar los espacios de cada parqueadero así como ingresar información adicional. |
| Precondiciones: | Debe existir algún parqueadero donde se encuentren los espacios. |
| Poscondiciones: | Todos los cambios referentes a los espacios se  almacenará en la base de datos. |
| Flujo básico:  |
|  1. El administrador ingresa a la opción de gestionar espacios y el sistema le despliega la lista de parqueaderos registrados.
   2. El administrador selecciona el parqueadero que desee y el sistema le muestra los datos del parqueadero incluyendo el número de espacios.
   3. El administrador elige la opción de crear un espacio o eliminarlo.
   4. El sistema guarda el cambio que ha hecho el administrador una vez que guardo los cambios. |

|CASO: | 5 |
|-----------|-----------|
| Nombre: | Implementar precios de espacios |
| Actores:  | Administrador |
| Descripción: | El administrador ingresa los precios de los espacios de cada parqueadero. |
| Precondiciones: | Debe estar registrador el parqueadero y al menos un espacio registrado. |
| Poscondiciones: | El precio se podrá modificar por el administrador. |
| Flujo básico:  |
|  1. El administrador selecciona el parqueadero y el sistema le muestra toda la información del mismo.
   2. El administrador selecciona el tipo de cobro que va a realizar(por horas o minutos), selecciona el valor que prefiera y le da a guardar.
   3. El sistema guarda el precio establecido. |

|CASO: | 6 |
|-----------|-----------|
| Nombre: | Gestionar ofertas |
| Actores:  | Administrador |
| Descripción: | El administrador podrá ingresar promociones y descuentos al parqueadero. |
| Precondiciones: | Tiene que el parqueadero estar registrado al sistema. |
| Poscondiciones: | Todas las ofertas no serán estáticas, y el administrador podrá cambiar cuando lo desee. |
| Flujo básico:  |
|  1. El administrador ingresa a la opción de gestionar ofertas y el sistema le despliega la lista de los parqueaderos registrados.
   2. El administrador selecciona el parqueadero y el sistema le muestra las opciones de ingresar promociones y/o descuentos.
   3. El administrador establece las promociones o descuentos y guarda las ofertas.
   4. El sistema se actualiza automáticamente con las nuevas ofertas para ese parqueadero. |

|CASO: | 7 |
|-----------|-----------|
| Nombre: | Gestionar servicios extras |
| Actores:  | Administrador |
| Descripción: | El administrador podrá ingresar servicios extras(copias, lavadero,etc) al parqueadero. |
| Precondiciones: | Todos los servicios extras tiene que estar asociados a un parqueadero. |
| Poscondiciones: | Los servicios extras formarán parte de las ofertas que pueda añadir el administrador. |
| Flujo básico:  |
|  1. El administrador ingresa a la opción de gestionar servicios extras y el sistema le despliega la lista de los parqueaderos registrados.
   2. El administrador selecciona el parqueadero y el sistema le muestra un campo donde ingresa los datos de los servicios extras(nombre, descripción, costo)..
   3. El sistema se actualiza automáticamente con las nuevos servicios para ese parqueadero. |

|CASO: | 8 |
|-----------|-----------|
| Nombre: | Visualizar disponibilidad de espacios |
| Actores:  | Administrador, Conductor, Socio |
| Descripción: | Todos los actores involucrados en el sistema pueden observar la disponibilidad de los espacios de los parqueaderos. |
| Precondiciones: | En el sistema tiene que estar registrado por lo menos un parqueadero. |
| Poscondiciones: | Los actores pueden visualizar los espacios y la disponibilidad del parqueadero que hayan elegido. |
| Flujo básico:  |
|  1. Los actores ingresan a la opción de visualizar los espacios.
   2. El sistema muestra una lista de los parqueaderos registrados.
   3. El socio selección un parqueadero.
   4. El sistema muestra la lista de los espacios del parqueadero. |

|CASO: | 9 |
|-----------|-----------|
| Nombre: | Reservar espacio |
| Actores:  | Socio |
| Descripción: | Los socios pueden reservar un único espacio de todos los parqueadero registrados. |
| Precondiciones: |  |
| Poscondiciones: | El socio tiene registrada una única reserva. |
| Flujo básico:  |
|  1. El sistema le muestra una lista de los parqueaderos.
   2. El socio elige un parqueadero a su elección.
   3. El sistema le muestra una lista de los espacios del parqueadero.
   4. El socio elige un espacio e ingresa la clave o el código de la tarjeta.
   5. El sistema guarda el registro de la reserva en un historial. |

|CASO: | 10 |
|-----------|-----------|
| Nombre: | Consultar saldo |
| Actores:  | Socio |
| Descripción: | Los socios pueden consultar el saldo que disponen en sus tarjetas. |
| Precondiciones: |  |
| Poscondiciones: | El sistema muestra el saldo del socio. |
| Flujo básico:  |
|  1. El socio realiza selecciona la consulta de su saldo.
   2. El socio ingresa la clave o identificador de su tarjeta y confirma la consulta.
   3. El sistema recolecta los datos de la tarjeta.
   4. El sistema muestra los datos del saldo al socio. |

|CASO: | 11 |
|-----------|-----------|
| Nombre: | Recargar tarjeta |
| Actores:  | Administrador |
| Descripción: | El administrador puede recargar el saldo de las tarjetas que disponen los socios. |
| Precondiciones: |  |
| Poscondiciones: | El sistema recarga el saldo de la tarjeta. |
| Flujo básico:  |
|  1. El administrador ingresa la clave y el saldo a recargar a la tarjeta.
   2. El administrador confirma la recarga.
   3. El sistema realiza la recarga a la tarjeta.
   4. El sistema registra la recarga en un historial. |

|CASO: | 12 |
|-----------|-----------|
| Nombre: | Cambiar estados |
| Actores:  | Administrador |
| Descripción: | El administrador puede cambiar el estado de la tarjeta para bloquear las actividades que puede realizar el socio y puede activarla para que el socio tenga nuevamente los permisos. |
| Precondiciones: |  |
| Poscondiciones: | El sistema cambia el saldo de la tarjeta. |
| Flujo básico:  |
|  1. El administrador ingresa los datos del socio.
   2. El administrador realiza la consulta de la tarjeta.
   3. El sistema retorna los datos de la tarjeta.
   4. El sistema muestra los datos de la tarjeta incluido el estado.
   5. El administrador elige bloquear o activar el estado de la tarjeta.
   6. El sistema realiza el cambio y guarda la actividad en un historial. |

|CASO: | 13 |
|-----------|-----------|
| Nombre: | Crear tarjetas |
| Actores:  | Administrador |
| Descripción: | El administrador puede crear las tarjetas de los socios para mantener un historial. |
| Precondiciones: |  |
| Poscondiciones: | El sistema tiene nuevas tarjetas registradas. |
| Flujo básico:  |
|  1. El administrador ingresa una cantidad de tarjeta.
   2. El sistema se crear las tarjetas con un identificador aleatorio.
   3. El sistema almacena la actividad en un historial. |

|CASO: | 14 |
|-----------|-----------|
| Nombre: | Gestionar tipo de pago |
| Actores:  | Administrador |
| Descripción: | El administrador puede elegir el tipo de pago que se realizará para la cancelación del parqueo. |
| Precondiciones: | El administrador debe estar en su interfaz correspondiente. |
| Poscondiciones: | El sistema recarga el saldo de la tarjeta. |
| Flujo básico:  |
|  1. El sistema carga la lista de sus espacios.
   2. El administrador selecciona el espacio.
   3. El sistema carga los datos que corresponde al parqueo.
   4. El administrador selecciona cancelar servicio .
   5. El sistema en lista las opciones para cancelar.
   6. El administrador elige la opción.
   7. El sistema muestra un formulario con respecto a la opción elegida.
   8. El administrador ingresa los datos y confirma el pago.
   9. El sistema registra la actividad en un historial. |