
# API Precioil.es

La **API Precioil.es** proporciona datos actualizados sobre precios de combustibles y estaciones de servicio en varios países, incluyendo España, Portugal, Francia e Italia. Esta herramienta permite a los desarrolladores acceder a información en tiempo real.

## Tabla de Contenidos

- [Descripción](#descripción)
- [Límites de Uso](#límites-de-uso)
- [Endpoints](#endpoints)
  - [Estaciones de Servicio](#estaciones-de-servicio)
  - [Datos Geográficos](#datos-geográficos)
  - [Precios de Combustible](#precios-de-combustible)
- [Ejemplo de Uso](#ejemplo-de-uso)
- [Soporte y Contacto](#soporte-y-contacto)
- [Licencia](#licencia)

## Descripción

La API Precioil.es permite obtener datos detallados de estaciones de servicio, sus ubicaciones, y precios de combustibles en varios países. Estos datos se actualizan cada 30 minutos. Actualmente, la API está en fase beta, por lo que se están realizando mejoras y ajustes.

## Límites de Uso

Para garantizar un rendimiento óptimo para todos los usuarios, existen límites en la cantidad de solicitudes que pueden realizarse. Si necesitas un mayor volumen de consultas, se recomienda optimizar las solicitudes y, si es necesario, contactar para ajustes de límites específicos.

## Endpoints

A continuación se presentan los principales endpoints de la API. Cada uno incluye el método HTTP, la ruta y una breve descripción de su funcionalidad.

### Estaciones de Servicio

- **Obtener Estaciones Cercanas a una Estación Específica**
  ```
  GET /estaciones/cerca/{idEstacion}
  ```
  Devuelve estaciones cercanas a una estación específica en un radio definido alrededor del `idEstacion`.

- **Detalles de una Estación**
  ```
  GET /estaciones/detalles/{idEstacion}
  ```
  Obtiene detalles completos sobre una estación específica indicada por `idEstacion`.

- **Historial de Precios de una Estación**
  ```
  GET /estaciones/historico/{idEstacion}
  ```
  Devuelve el historial de precios para una estación en particular.

- **Estaciones en un Municipio**
  ```
  GET /estaciones/municipio/{idMunicipio}
  ```
  Lista todas las estaciones de servicio en un municipio específico indicado por `idMunicipio`.

- **Estaciones dentro de un Radio**
  ```
  GET /estaciones/radio
  ```
  Devuelve todas las estaciones de servicio dentro de un radio específico de un punto determinado.

### Datos Geográficos

- **Municipios de una Provincia**
  ```
  GET /municipios/provincia/{idProvincia}
  ```
  Lista todos los municipios dentro de una provincia específica indicada por `idProvincia`.

- **Listado de Provincias**
  ```
  GET /provincias
  ```
  Devuelve una lista de todas las provincias disponibles en la base de datos.

### Precios de Combustible

- **Precio Medio Diario de Combustible**
  ```
  GET /precioMedioDiario
  ```
  Obtiene el precio promedio diario de los combustibles.

- **Precios Medios por Provincia**
  ```
  GET /precios/medios/provincia/{idProvincia}
  ```
  Devuelve el precio medio de cada tipo de combustible en una provincia específica indicada por `idProvincia`.

## Ejemplo de Uso

Aquí se muestra cómo realizar una solicitud simple a la API.

### Usando `curl`

```bash
curl -X GET "https://api.precioil.es/estaciones/detalles/{idEstacion}" -H "accept: application/json"
```

### Usando JavaScript (Fetch API)

```javascript
fetch("https://api.precioil.es/estaciones/detalles/{idEstacion}")
  .then(response => response.json())
  .then(data => console.log(data));
```

## Soporte y Contacto

Para preguntas, sugerencias  puedes contactar en [contacto@api.precioil.es](mailto:contacto@api.precioil.es). 

## Licencia

Este proyecto se distribuye bajo la licencia [MIT](./LICENSE).

---


