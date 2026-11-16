# Estado del catálogo de vehículos

## Alcance de esta carga inicial

- 100 identificadores originales preservados: VEH-001 a VEH-100.
- Inventario de trabajo, no aprobación documental final.
- No se elimina ni sustituye ningún ID.
- Los campos sin evidencia documental incorporada se mantienen como `null` o pendientes.
- Las puntuaciones originales se consignan únicamente cuando fueron recuperadas de forma suficientemente clara en el trabajo previo. Los valores no recuperados quedan como `null`.
- Las relaciones entre IDs indican parentesco de personaje, continuidad, familia de diseño o adaptación; no implican duplicación ni eliminación.

## Estados

- `partial`: existe información de trabajo, pero falta consolidar fuentes específicas y validar cada campo.
- `pending`: identificación, puntuación original o datos esenciales pendientes de recuperación/verificación.
- La naturaleza, fabricante, modelo, fechas y fuentes se completarán tras revisión documental.

## Pendientes prioritarios

1. Recuperar y resolver el referente original de VEH-073 sin sustituirlo.
2. Consolidar fuentes específicas por ficha y campo.
3. Distinguir año de primera aparición, año del modelo real y año de fabricación de la unidad usada en rodaje.
4. Revisar naturaleza: real, modificado, réplica, ficticio, animado/digital o híbrido.
5. Recalibrar iconicidad con una justificación homogénea, sin alterar las puntuaciones originales históricas.
6. Completar las relaciones justificadas entre vehículos y auditar que no se confundan con duplicados.
7. Realizar validación final del JSON, fuentes y 100 IDs.

## Estructura de datos

El archivo `data/vehicles/vehicles_master.json` es el inventario maestro inicial. Las correcciones aceptadas y discrepancias se registran en `docs/VEHICLE_CORRECTIONS_LOG.md`.

## Regla de publicación

Ninguna ficha se considerará documentalmente cerrada por el mero hecho de estar incluida en el JSON. Solo se marcará como confirmada cuando sus afirmaciones esenciales estén respaldadas por fuentes específicas y trazables.


## Avance documental — bloque VEH-001 a VEH-025

**Investigación inicial incorporada al JSON:** las 25 fichas recibieron datos de producción, año de primera aparición, modelo/fabricante cuando la evidencia lo permite, naturaleza, identidad ficticia, personajes asociados, notas de incertidumbre y referencias web específicas.

- 24 fichas: estado `partial` (hay evidencia útil, pero falta completar o triangular algunos campos).
- 1 ficha: estado `pending` (VEH-023, falta confirmar la base mecánica del Dragon car).
- Ninguna ficha de este bloque se declara `confirmed`.
- VEH-073 permanece fuera de este bloque y conserva su pendiente de identificación.

### Incidencias que requieren atención

- VEH-002: discrepancia entre fuentes sobre si los chasis base eran Impala 1967 o 1968; no se asignó año de modelo.
- VEH-003: DB5 prototipo; confirmar año exacto de fabricación de la unidad de rodaje.
- VEH-010: Herbie fue representado por varias unidades; no existe un único año de modelo aplicable a todo el personaje.
- VEH-013: el Tumbler fue una construcción de producción; las fuentes difieren en el recuento de vehículos funcionales frente al total de unidades/maquetas.
- VEH-014: identificación de la flota Explorer apoyada por archivo especializado; falta fuente primaria/institucional.
- VEH-018 y VEH-019: varias unidades de vehículos reales fueron utilizadas para distintas tomas; no imponer un único año de modelo.
- VEH-020: separar la moto original de rodaje de las motos promocionales y réplicas posteriores.
- VEH-021: varias construcciones físicas representaron el coche ficticio.
- VEH-022: una sola unidad física construida, aunque la película representa dos.
- VEH-023: no confirmar la base Volkswagen ni otro chasis sin documentación técnica sólida.
- VEH-025: diseño ficticio, con modelos y construcciones físicas de efectos; no es un automóvil de producción.

### Fuentes y método

Las fuentes institucionales/museísticas, archivos de producción, registros históricos, entrevistas directas y publicaciones especializadas se registran por ficha. La calidad de las fuentes no es uniforme; por eso las fichas permanecen parciales cuando la fuente solo acredita una parte de la identidad. Los enlaces son referencias de trabajo y deberán revisarse de nuevo en el control documental final.


## Segunda pasada de control documental — VEH-001 a VEH-025

Se realizó una segunda revisión de fuentes y discrepancias y se actualizó el JSON maestro. Se añadieron o sustituyeron referencias débiles por registros de museo, fuentes oficiales de franquicia/fabricante, asociaciones profesionales, archivos institucionales, documentos judiciales y entrevistas directas. El bloque contiene ahora 45 referencias distribuidas entre sus 25 fichas.

### Ajustes concretos de esta pasada

- VEH-001: añadido el Petersen Automotive Museum; el ejemplar de colección es un DMC-12 de 1981 y la conversión de Universal Studios. Ese año no se generaliza a todas las unidades de la trilogía.
- VEH-002: se mantiene la discrepancia de año entre el Impala donante citado por Petersen (1967) y el año de chasis referido en el reportaje contemporáneo. Se evita tratar año del donante y año de chasis como si fueran el mismo dato.
- VEH-003: añadido el archivo especializado Aston Martins.com; se distingue el prototipo DP216/1 (coche de efectos) del DB5 de producción DB5/1486/R usado para conducción.
- VEH-004: corregida la descripción para reflejar dos Cadillac 1959: unidad negra prestada y unidad hero roja/blanca.
- VEH-005: corregido el enlace de la ficha técnica del Falcon XB GT; la URL anterior apuntaba a otro fascículo.
- VEH-006: reforzada la identificación de Eleanor mediante sentencia de apelación de California; el Mustang 1967 personalizado no era un Shelby GT500 original.
- VEH-008: eliminada la duplicación de la misma referencia Toyota.
- VEH-009: reforzado con el National Historic Vehicle Register y cronología de Ford; identificados los dos VIN y sus funciones.
- VEH-010: se explicita que Herbie es un personaje representado por varias unidades y que no debe asignársele un año único.
- VEH-011: reforzado con Petersen; el museo documenta 24 Fury adquiridos y una unidad stunt concreta.
- VEH-012: reforzada la identificación del trío Mini con sus matrículas, usando el archivo especializado del set.
- VEH-013: resuelta la aparente discrepancia: Los Angeles Times habla de ocho vehículos producidos en total; ASC detalla cinco Tumbler funcionales. Se conservan ambos alcances.
- VEH-014: se mantiene parcial porque la identificación 1992 XLT y la excepción XL se apoyan en un archivo de aficionados, no en documento de producción.
- VEH-016: reforzado con entrevista directa a John Landis: Dodge Monaco 1974 y adquisición de 12–13 unidades.
- VEH-017: reforzado con Wizarding World y British Motor Museum: Anglia 105E de 1962 y 16 unidades adaptadas.
- VEH-018: documentada la flota de 16 GM New Look y vehículos adicionales; se distingue el autobús central de otros usados en explosiones/efectos.
- VEH-019: fuente primaria de los directores en DGA confirma cinco VW Bus de finales de los setenta.
- VEH-020: se retira FLH como designación confirmada. El museo documenta una chopper artesanal creada por Ben Hardy y Cliff Vaughs, pero no confirma que la motocicleta completa fuera un modelo FLH de fábrica.
- VEH-021: National Motor Museum confirma seis Chitty originales construidos por Alan Mann Racing.
- VEH-022: AFI confirma el Land Master de doce ruedas, motor Ford industrial 391 y una sola unidad fabricada aunque la película represente dos.
- VEH-025: reforzado con MoPOP y ACMI; se distinguen el diseño de Syd Mead, la construcción de Gene Winfield, los modelos y las tres unidades a tamaño real.

### Estado tras segunda pasada

- 24 fichas permanecen `partial`.
- VEH-023 permanece `pending` por falta de identificación fiable de su base mecánica.
- No se ha cambiado ninguna ficha a `confirmed`.
- VEH-002, VEH-014 y VEH-020 conservan incertidumbres concretas; las fuentes ahora permiten describirlas con mayor precisión, pero no cerrar todos los campos.

**Decisión:** no iniciar VEH-026–VEH-050 todavía. Primero hay que resolver o documentar formalmente las incertidumbres restantes y auditar los campos individuales de las 25 fichas. La existencia de referencias en el JSON no equivale a que todas las afirmaciones estén probadas.
