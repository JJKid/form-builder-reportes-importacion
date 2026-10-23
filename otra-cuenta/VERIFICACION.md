# Revisión de 37 encuestas de 10.90.0.24

La [tabla por encuesta](REPORTE.html) contiene la conversión del 8 de octubre de 2026. Se procesaron los datos de preguntas ya guardados con el adaptador y las bibliotecas actuales. Esta revisión no consultó los servidores remotos ni envió respuestas de participantes.

| Resultado | Encuestas |
| --- | ---: |
| Sin advertencias | 27 |
| Con advertencias, sin preguntas omitidas | 4 |
| Con preguntas omitidas | 1 |
| Vacía | 0 |
| Rechazada | 5 |
| **Total** | **37** |

Dos comprobaciones locales completas dieron las mismas categorías, advertencias y causas de rechazo por encuesta. Se comprobó la conversión, la aceptación de SurveyStructure y la creación de los controles Formly.

Los botones agrupados, las estrellas y el deslizador con carita conservan los códigos de respuesta. Las configuraciones `display_type` y `slider_rating` con valores admitidos ya no generan advertencias. Las pruebas de navegador comprobaron selección, borrado, obligatoriedad y controles deshabilitados; las del servidor comprobaron códigos y preguntas dependientes. Las estrellas se comprobaron con preguntas de prueba locales: no hay una configuración de estrellas en estas definiciones guardadas.

Las configuraciones de impresión, exportación para SPSS y gráficas de estadísticas se conservan en `source.originDetails`, sin generar advertencias de respuesta. Los temporizadores y el JavaScript del autor siguen sin ejecutarse; sus valores originales se conservan.

El [detalle JSON](encuestas.json) y las [preguntas originales incluidas en el HTML](REPORTE.html#preguntas-origen-171136) permiten revisar las causas. Aprobaron 616 pruebas del adaptador, incluidas las de Redis local desechable. Las dos pruebas que necesitan una instancia LimeSurvey accesible quedaron omitidas porque el servidor estaba caído; no se cuentan como aprobadas. También aprobaron las 195 de SurveyStructure, 96 del parser y 40 de diccionarios. Las pruebas de navegador aprobaron 71 casos en Ionic, 81 en Material y 81 en utils; las 494 pruebas del servidor aprobaron. La simplificación conserva las mismas líneas y ramas ejecutadas del adaptador y mantiene el catálogo completo en SurveyStructure. Estas pruebas no envían respuestas a producción ni recorren todas las pantallas de cada encuesta remota.
