
#### **docs/GUIA_BI.md**
```markdown
# Guía: Conectar a Looker Studio

## Paso 1: Preparar Datos

1. Ejecutar notebook (genera `electoral_data_clean.csv`)
2. Los datos están listos en `data/processed/`

## Paso 2: Subir a Google Sheets

1. Ir a https://sheets.google.com
2. Nuevo documento
3. File → Import → Upload → Seleccionar `electoral_data_clean.csv`
4. Looker Studio conectará automáticamente

## Paso 3: Crear Dashboard en Looker Studio

1. Ir a https://lookerstudio.google.com
2. "Crear" → "Informe"
3. Conectar fuente de datos (Google Sheets)
4. Seleccionar archivo subido
5. Insertar gráficos:
   - Tarjetas KPI (votos totales, participación)
   - Tabla (municipios ordenados)
   - Mapa geográfico (votos por estado)
   - Gráfico de barras (candidatos)

## Paso 4: Agregar Filtros Interactivos

- Filtro por Estado
- Filtro por Municipio
- Filtro por Rango de Fechas (si aplica)

## Alternativa: Metabase (Self-Hosted)

```bash
docker run -d -p 3000:3000 --name metabase metabase/metabase
