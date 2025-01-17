# Documentación Segundo Entregable - Análisis Exploratorio y Curación de Datos 2024

## Dataset Fuente
El trabajo usa el dataset de [Melbourne Housing Market](https://www.kaggle.com/datasets/anthonypino/melbourne-housing-market) con fuente de Kaggle

## Criterios de exclusión de ejemplos
1. No se han eliminado valores extremos, luego de comparar varias maneras de eliminarlos pero obteniendo una mejor sin removerlos.
2. Se descartaron las columnas `Date`: fecha del registro de la propiedad y `Address`: dirección de la propiedad.Por ser tener un tipado especial y tener mucha unicidad, respectivamente.  

## Características seleccionadas
### Características categóricas
1. `Suburb`: Suburbio de la propiedad, 314 valores posibles.
2. `Type`: tipo de propiedad, 3 valores posibles.
3. `Method`:Metodo de venta de la propiedad,  5  valores posibles.
4. `SellerG`: el agente Real Estate de la propiedad, 268 valores posibles.
5. `CouncilArea`: Consejo de gobierno para el área de la propiedad, 33 valores posibles.
6. `Regionname`: Región General (Oeste, Noroeste, Norte, Noroeste ... etc.) de la propiedad, 8 valores posibles.

Todas las características categóricas fueron codificadas con un
método OneHotEncoding.

### Características numéricas
1. `Rooms`: Cantidad de habitaciones
2. `Price`: Precio en dólares australianos.
3. `Distance`: Distancia al centro de la ciudad.
4. `Postcode`: Codigo Postal.
5. `Bedroom2`: Número de habitaciones escrapeadas de otra fuente.
6. `Bathroom`: Número de baños
7. `Car`: Capacidad del garage.
8. `Landsize`: Tamaño de tierra en metros
9. `Lattitude`: Latitud
10. `Longtitude`: Longitud
11. `Propertycount`: Número de propiedades que existen en el suburbio.

## Transformaciones:
1. Se cambio el tipo de la columna `Date` de `objeto` a `datetime`
2. Todas las características numéricas fueron escaladas.
3. Las columna `YearBuilt`,`BuildingArea` y `Car` fueron imputadas utilizando el método de KNN.

## Datos aumentados
1. Se agregan las 2 primeras columnas obtenidas a través del
método de PCA, aplicado sobre el conjunto de datos
totalmente procesado.
