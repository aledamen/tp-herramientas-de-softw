## Conclusión del dataset

Cuando me puse a trabajar con este dataset, me encontré con varios datos que vienen desprolijos. Había fechas en distintos formatos, horas que no tenían sentido, valores faltantes, ubicaciones escritas de mil maneras distintas y algunos registros que directamente no cerraban por ningún lado. 

Como lo indicaba el primer sprint le dedique tiempo a limpiar, ordenar y normalizar todo.

Una vez hecha la limpieza, se empezaron a ver cosas interesantes. Por ejemplo, algunas patentes aparecían varias veces, lo que deja entrever que hay vehículos que reinciden bastante. También llamó la atención que ciertas franjas horarias como las 00:00 concentran una cantidad significativa de infracciones (teniendo en cuenta tambien de que es nuestra hora por default), algo que probablemente tenga que ver con cómo cambia el tránsito durante la noche.

Si mirás los datos a nivel mensual, también aparecen diferencias, lo que sugiere que la dinámica del tránsito no es la misma a lo largo del año.

En definitiva, el dataset muestra que el control de velocidad refleja comportamientos bastante variados, pero también deja algo claro: si los datos no están bien trabajados desde el principio, cualquier análisis puede quedar medio flojo.

Viniendo del mundo del desarrollo y no tanto del análisis de datos, seguramente haya cosas que se podrían mejorar, errores que se me hayan pasado o formas más óptimas de encarar algunas partes del proceso. Aun así, me sirvió para salir un poco del enfoque más tradicional de código y meterme en este tipo de trabajo.

También fue útil para ver de primera mano todo el “ruido” que traen los datos reales y cómo eso impacta directamente en lo que después uno interpreta.
## Conclusiones del Sprint 2

Al relacionar las imágenes con los datos de multas observamos:

1. Cobertura parcial: no todas las multas tienen evidencia visual asociada, lo que limita la validación automática del sistema.

2. Errores del OCR: el reconocimiento de patentes no es perfecto. El umbral del 80% permite absorber errores típicos como la confusión entre caracteres similares (I/1, O/0, B/8).

3. Heterogeneidad visual: las imágenes varían en resolución, iluminación y ángulo, lo que impacta la precisión del OCR.

4. Dependencia del Sprint 1: la calidad del matching depende de la normalización previa de patentes realizada en el Sprint 1.

5. Limitación del enfoque base: las imágenes del grupo completes requieren localización previa de la patente antes del OCR, complejidad no abordada en esta aproximación base.

## Conclusión del Sprint 3

Este sprint fue el más exigente de los tres.

Migrar de CSV a una base de datos relacional obliga a pensar el
dominio de otra manera: qué es una entidad, qué es una relación,
qué conviene normalizar. Diseñar el modelo lógico con dataclasses
antes que el ORM ayudó a no mezclar esas dos preguntas, aunque
al principio no estaba claro por qué había que separarlas.

DVC resolvió algo que venía siendo incómodo: tener imágenes en
git no escala. La separación entre lo que git trackea y lo que
DVC maneja tiene sentido una vez que lo vivís en la práctica.

La integración con ChromaDB y OpenCLIP fue la parte más nueva.
Buscar imágenes por similitud semántica en lugar de por nombre
de archivo es un enfoque distinto al que estaba acostumbrado.
Entender que una imagen se puede representar como un vector y
operar sobre eso llevó un tiempo, pero el resultado es útil.

En general, los tres sprints construyeron algo que en el sprint 1
era solo un CSV. Terminó siendo un sistema con capas y herramientas
distintas para cada tipo de dato. 
