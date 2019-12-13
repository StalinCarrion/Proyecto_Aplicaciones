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
| ------------- | ------------- |
| Actores:  | Conductor |
| Descripción: | El conductor podrá visualizar el tiempo que le tomará llegar a los parqueaderos. |
| Precondiciones: | El conductor debe activar la ubicación en su celular. |
| Poscondiciones: | El sistema muestra el tiempo calculado de la llegada al parqueadero. |
| Flujo básico:  |
|  1. El sistema mostrará un mapa en donde se muestre la posición del conductor y el parqueadero al que desea ir.
   2. El sistema calculará la distancia entre el conductor y el parqueadero.
   3. El sistema le mostrará al conductor en forma de mensaje el tiempo en minutos que tardará en llegar a ese parqueadero.
 |
