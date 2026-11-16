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
