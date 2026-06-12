# CHANGELOG

## [Sprint 1] - 2026-04-22

### Ejercicio 01
- Creación de la estructura de directorios del proyecto
- Creación de README.md
- Creación de CHANGELOG.md

### Ejercicio 02
- Descarga del dataset original y almacenamiento en urban_flow/data/raw
- Visualización de las primeras 5 filas
- Análisis de tipos de datos
- Conteo de valores nulos

### Ejercicio 03
- Normalización de fechas, horas, ubicaciones y patentes
- Eliminación de filas con valores relevantes vacíos
- Detección y eliminación de outliers
- Cálculo de exceso de velocidad real y con margen del 5%
- Filtrado de infracciones
- Guardado del dataset limpio en urban_flow/data/interim

### Ejercicio 04
- Definición de la clase FineAnalyzer
- Implementación de métodos de análisis (rankings, promedios, conteos)
- Creación del objeto e invocación de métodos en celdas separadas

### Ejercicio 05
- Creación del gráfico de ranking de las 10 patentes más reincidentes.
- Creación del gráfico de torta con el porcentaje de infracciones por hora.
- Creación del gráfico de barras horizontal con la cantidad de infracciones por mes.
- Creación del gráfico de líneas de los excesos de velocidad filtrados por la hora 00:00.
- Creación del gráfico de líneas de los excesos de velocidad filtrados por la fecha 1932-01-01.
### Ejercicio 06
- Cálculo del porcentaje de infracciones ocurridas en la fecha 1932-01-01.
- Cálculo del porcentaje de infracciones ocurridas en la hora 00:00.

## [Sprint 2] - 2026-05-17

### Ejercicio 01
- Descarga del dataset de imágenes y almacenamiento en urban_flow/data/raw/imgs
- Inicializacion y configuración de las herramientas de versionado
### Ejercicio 02
- Listar todas las imágenes disponibles (no mostrar/no imprimir). Se debe mostrar el nombre y su tamaño en KB.
- Construcción del diccionario group_images.
- Función para mostrar 8 imágenes de forma aleatoria.
### Ejercicio 03
- Conversión a escala de grises almacenada en 03_01_gray_scale.
- Suavizado Gaussiano almacenado en 03_02_blur.
- Detección de bordes con Canny almacenada en 03_03_canny.
### Ejercicio 04
- Extracción de patentes con easyocr sobre los grupos plates y completes.
- Matching contra speeding_fines.csv con umbral del 80%.
- Generación de speeding_fines_image.csv con columnas imagen, patente_imagen y ratio.
### Ejercicio 05
- Métricas del dataset final: multas sin imagen, con imagen, imágenes sin match, pendientes de pago y pendientes con imagen.
### Ejercicio 06
- Análisis y conclusiones sobre la relación entre imágenes y datos del dataset de multas.

## [Sprint 3] - 2026-06-12

### Ejercicio 01
- Inicialización y configuración de la herramienta de versionado en rama Sprint_3 desde Sprint_2.
- Verificación de acceso a todos los datasets generados.
- Actualización del README con Sprint 3.
