
#### **docs/METODOLOGIA.md**

## Fase 1: Definición

### Objetivo Inicial
Crear un análisis electoral desde cero que demuestre:
1. Capacidad de trabajar con datos públicos
2. Habilidad en ETL con Python
3. Experiencia en BI y visualización interactiva

### Datos Utilizados
- Fuente: macedoniadelnorte.com
- URL: https://static.resultadosconvzla.com/RESULTADOS_2024_CSV_V2.csv
- Contexto: Auditoría de elecciones presidenciales Venezuela 2024

## Fase 2: Exploración y Limpieza

### Estructura Original del CSV
COL_ID | NUM. CENTRO | NOMBRE_CENTRO | ESTADO | MUNICIPIO |
EDMUNDO_GONZALEZ | NICOLAS_MADURO | ... [más candidatos]

### Transformaciones Realizadas

#### 1. Normalización de datos
- Tipos de datos apropiados (int, float, string)
- Manejo de valores nulos
- Estandarización de strings (mayúsculas/minúsculas)

#### 2. Validaciones
- Suma de votos = total por centro
- Consistencia de agregaciones
- Detección de anomalías

#### 3. Nuevas columnas calculadas
- `votos_totales` = suma de todos los candidatos
- `porcentaje_candidato` = (votos / votos_totales) * 100
- `ranking_municipio` = orden por votos EG

## Fase 3: Agregaciones

### Niveles de Desagregación
1. **Centro de Votación** (nivel más granular)
2. **Municipio** (suma de centros)
3. **Estado** (suma de municipios)
4. **Nacional** (suma de estados)

### Cálculo de KPIs
- Participación electoral por región
- Diferencia EG vs NM
- Votos por habitante (si data disponible)

## Fase 4: Visualización

### Selección de Looker Studio
- Integración Google (data en Sheets)
- Filtros nativos interactivos
- Mapas geográficos
- No requiere servidor

### Alternativas Consideradas
- Metabase: ✅ Poderosa, ❌ Requiere servidor
- Streamlit: ✅ Fácil, ❌ Menos profesional
- Power BI: ✅ Completa, ❌ Propietaria

## Decisiones Clave

### ¿Por qué Python en lugar de herramientas BI nativas?
- Reproducibilidad
- Control total del proceso
- Educativo (aprende ETL real)
- Abierto y colaborable

### ¿Por qué Looker Studio (no Power BI)?
- Acceso público gratis
- Integración Google nativa
- No requiere costo de licencia

### ¿Por qué descargar automáticamente?
- Datos siempre frescos
- Reproducibilidad
- Fallback a local si hay errores

## Validaciones Aplicadas

1. **Integridad**: Votos por centro suman correctamente
2. **Consistencia**: Agregaciones son transitivas (centro→municipio→estado)
3. **Completitud**: Sin columnas críticas vacías
4. **Lógica**: Porcentajes entre 0-100

## Lecciones Aprendidas

[Será completado después de terminar el notebook]

---

**Próximas mejoras**:
- [ ] Análisis de series temporales (si hay datos históricos)
- [ ] Modelos predictivos
- [ ] API REST para consumir datos

