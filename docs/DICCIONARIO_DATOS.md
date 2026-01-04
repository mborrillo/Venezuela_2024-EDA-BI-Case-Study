# Diccionario de Datos

## Estructura del CSV Procesado

| Columna | Tipo | Descripción | Ejemplo |
|---------|------|-------------|---------|
| `centro_id` | int | ID único del centro de votación | 40902025 |
| `centro_nombre` | str | Nombre del centro | LICEO NACIONAL... |
| `estado` | str | Estado donde está el centro | ZULIA |
| `municipio` | str | Municipio | MARACAIBO |
| `mesas` | int | Cantidad de mesas electorales | 3 |
| `edmundo_gonzalez` | int | Votos para EG | 789877 |
| `nicolas_maduro` | int | Votos para NM | 320000 |
| `[otros_candidatos]` | int | Votos candidato X | ... |
| `votos_validos` | int | Total votos válidos | 1105158 |
| `votos_nulos` | int | Votos nulos/blancos | 121 |
| `votos_totales` | int | votos_validos + votos_nulos | 1105279 |
| `eg_porcentaje` | float | (EG / votos_validos) * 100 | 71.43 |
| `nm_porcentaje` | float | (NM / votos_validos) * 100 | 28.95 |
| `diferencia_eg_nm` | int | EG - NM | 469877 |
| `nivel_agregacion` | str | "centro", "municipio", "estado" | centro |
