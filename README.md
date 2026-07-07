# ConnectaTel - Análisis de Comportamiento de Clientes

## 🎯 Objetivo del proyecto
Evaluar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica, a partir de datos registrados hasta el año 2024. El análisis busca construir un perfil estadístico de los clientes, detectar comportamientos atípicos y crear segmentos de clientes que permitan identificar patrones de consumo, diseñar estrategias de retención y sugerir mejoras en los planes ofrecidos.

## 📊 Datasets utilizados
- **plans.csv**: información de los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
- **users_latam.csv**: información de los clientes (edad, ciudad, fecha de registro, plan, churn).
- **usage.csv**: detalle del uso real de los servicios (llamadas y mensajes).

## 🔍 Etapas del análisis
1. **Carga y exploración**: revisión inicial de estructura, tipos de datos e inconsistencias en los tres datasets.
2. **Limpieza de datos**: corrección de valores sentinela (-999 en `age`), estandarización de nulos (`"?"` en `city`), y corrección de fechas imposibles en `reg_date`.
3. **Análisis de valores nulos**: verificación de si los nulos en `duration` y `length` son MAR (Missing At Random), confirmando su dependencia de la columna `type`.
4. **Agregación de datos**: construcción de una tabla resumen por usuario (`user_profile`) combinando cantidad de mensajes, llamadas y minutos totales.
5. **Estadística descriptiva**: resumen numérico y distribución porcentual del tipo de plan.
6. **Visualización de distribuciones**: histogramas de edad, mensajes, llamadas y minutos de llamada, segmentados por tipo de plan.
7. **Identificación de outliers**: detección de valores extremos mediante boxplots y el método IQR.
8. **Segmentación de clientes**: clasificación por nivel de uso (`grupo_uso`) y por edad (`grupo_edad`).
9. **Insight ejecutivo**: conclusiones y recomendaciones de negocio basadas en los hallazgos del análisis.

## ⚙️ Cómo ejecutar el notebook
1. Descarga el archivo `S7 -ConnectaTel Analisys Valeria Ramirez.ipynb` de este repositorio.
2. Ábrelo en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
3. Asegúrate de tener instaladas las librerías: `pandas`, `numpy`, `matplotlib`, `seaborn`.
4. Ejecuta las celdas en orden (`Runtime → Run all` en Colab, o `Kernel → Restart & Run All` en Jupyter).

## 🛠️ Herramientas utilizadas
- Python (pandas, numpy, matplotlib, seaborn)
- Jupyter Notebook / Google Colab

## 👤 Autora
Valeria Ramírez Acuña
