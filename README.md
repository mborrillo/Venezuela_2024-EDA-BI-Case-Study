# Venezuela_2024-EDA-BI-Case-Study

Análisis completo de las elecciones presidenciales de Venezuela 2024, desde la carga bruta de datos hasta un dashboard interactivo en Looker Studio.

## 🎯 Objetivo

Demostrar el flujo completo de un proyecto BI:
- **Extracción**: Datos públicos de macedoniadelnorte.com
- **Transformación**: Limpieza, validación y cálculo de KPIs en Python
- **Visualización**: Dashboard interactivo en Looker Studio

## 📊 Datos

- **Fuente**: https://static.resultadosconvzla.com/RESULTADOS_2024_CSV_V2.csv
- **Registros**: ~1.2M filas (votos desagregados)
- **Cobertura**: 24 estados, 267 municipios, 13k+ centros de votación
- **Actualización**: Descarga automática en cada ejecución del notebook

## 🔄 Flujo del Proyecto
<img width="295" height="317" alt="image" src="https://github.com/user-attachments/assets/d14ecf6f-9f7a-48f1-8802-8a083f375cc9" />

## 🛠️ Instalación

```bash
# Clonar repo
git clone <tu-repo>
cd venezuela-electoral-2024-eda-to-bi

# Crear entorno virtual
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate

# Instalar dependencias
pip install -r requirements.txt

# Abrir Jupyter
jupyter lab notebooks/

📓 Notebook - 2 Secciones
SECCIÓN 1: ETL (Extraction, Transform, Load)
Descarga automática del CSV

Inspección inicial (shape, tipos, nulos)

Limpieza y transformación

Cálculo de KPIs (votos, porcentajes, agregaciones)

Exportación a CSV limpio

SECCIÓN 2: EDA + Análisis
Estadísticas descriptivas

Top municipios por candidato

Distribución geográfica

Conclusiones y hallazgos

📈 KPIs Calculados
{
  "votos_totales": 10887259,
  "votos_validos": 10887259,
  "votos_nulos": 1214,
  "candidatos": {
    "edmundo_gonzalez": {
      "votos": 7303482,
      "porcentaje": 67.08
    },
    "nicolas_maduro": {
      "votos": 3316135,
      "porcentaje": 30.46
    },
    "otros": {
      "votos": 267642,
      "porcentaje": 2.46
    }
  },
  "por_estado": [...],
  "por_municipio": [...]
}


