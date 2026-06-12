# Urban Flow

## Sprint 1

### Objetivo
Analizar y depurar los datos del sistema heredado de radares urbanos
de la localidad de Vaalserberg para obtener información relevante
sobre infracciones por exceso de velocidad.

### Introducción y contexto
La localidad de Vaalserberg (Bélgica), ubicada en zona fronteriza con
Países Bajos y Alemania, cuenta con un sistema de radares cuyos datos
históricos presentan errores de formato y valores faltantes. El objetivo
de este sprint es limpiar y normalizar dichos registros para integrarlos
sin inconsistencias al nuevo sistema.

## Sprint 2

### Objetivo
El objetivo principal de este proyecto es aplicar los conocimientos adquiridos en el tratamiento de imágenes y en la programación limpia y clara.

### Introducción y contexto del nuevo problema
Los radares urbanos generan registros administrativos de multas de forma automática y las cámaras asociadas registran la evidencia visual que acompaña y valida la infracción. Sin embargo, se plantean los siguientes puntos a considerar:
- No todas las multas tienen una imagen asociada.
- No todas las imágenes corresponden a una infracción.
- Puede haber errores de detección.

El objetivo actual es desarrollar un sistema que determine qué multas tienen evidencia visual válida.

Para esto vamos a necesitar los siguientes datasets:
- Dataset procesado en el Sprint 1.

## Sprint 3

### Objetivo
Profesionalizar la solución incorporando persistencia en base de datos relacional, uso de ORM mediante SQLAlchemy, control de versiones de datos y preparación para búsquedas avanzadas.

### Introducción y contexto
El sistema creció en volumen y complejidad. Se migran los datos procesados a una base de datos estructurada y se incorpora una base de datos vectorial para búsqueda por imagen.
