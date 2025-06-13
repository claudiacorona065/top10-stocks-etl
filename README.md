# top10-stocks-etl
# Top 10 US Stocks – ETL & Investment Analysis

Este proyecto implementa un flujo ETL completo con el objetivo de ayudar a un equipo de inversión a identificar las **10 mejores empresas estadounidenses** recientes con alto potencial de rentabilidad. Forma parte de una práctica universitaria para la asignatura *Fundamentos de Ciencia de Datos* (UAX).

## Objetivo del proyecto

- Recopilar y combinar datos de empresas estadounidenses desde varias fuentes web.
- Filtrar empresas fundadas **después de 1995** y con **más de 5000 empleados**.
- Aplicar dos criterios clave de ordenación: **capitalización de mercado** y **crecimiento relativo**.
- Construir un **top 10 de empresas** con alto potencial a largo y corto plazo.
- Almacenar los datos en una base de datos PostgreSQL y exportarlos en `.csv` y `.parquet`.

---

## Fuentes de datos

- 🌐 [Investing.com](https://www.investing.com/) – Para extraer datos financieros de miles de empresas.
- 🌐 [Google Finance](https://www.google.com/finance/) – Para completar columnas como empleados y año de fundación.

---

## Flujo ETL

1. **Extracción (E):**
   - Web scraping con Selenium.
   - Más de 6400 empresas extraídas desde Investing.
   - Segunda fuente: Google Finance (más lenta, 21 horas de scraping).

2. **Transformación (T):**
   - Limpieza de datos y combinación de datasets.
   - Filtros: empresas con >5000 empleados y fundadas >1995.
   - Cálculo de métricas, normalización y detección de outliers con IQR.

3. **Carga (L):**
   - Inserción en PostgreSQL para consultas SQL.
   - Backup en `.csv`.
   - Salida final en formato `.parquet`.

---

## Análisis y resultados

Se aplicaron múltiples técnicas de análisis de datos:

- **Estadística descriptiva** y dispersión de variables.
- **Análisis de correlación** entre precios, volumen y capitalización.
- **Criterios de ranking**:
  - **Capitalización de mercado (70%)** – estabilidad, bajo riesgo.
  - **Crecimiento relativo (30%)** – alto potencial a corto plazo.
- **Cálculo de rentabilidad acumulada**.
- **Comparativa Top 10 vs resto** (rendimientos, capitalización, empleados).
- **Visualizaciones KDE** para representar la diferencia de rendimiento.

---

##  Herramientas y tecnologías

- Python, Pandas, NumPy
- Selenium (scraping)
- PostgreSQL (base de datos)
- Jupyter Notebook (DataSpell)
- Parquet / CSV
- Matplotlib / Seaborn

---

## Conclusión

El ranking final logra **un equilibrio entre empresas grandes y seguras** y otras **con alto potencial de crecimiento**. Esto proporciona una estrategia de inversión más robusta, mitigando riesgos sin perder oportunidades de rentabilidad.

---

## Autoría

Proyecto desarrollado por **Claudia Corona Blanco**  
Universidad Alfonso X el Sabio (UAX) – 2025  
Asignatura: Fundamentos de Ciencia de Datos

---

