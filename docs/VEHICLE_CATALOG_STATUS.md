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
