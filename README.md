# 📊 Análisis Exploratorio y Segmentación de Clientes - ConnectaTel

## 📌 Descripción del proyecto

Como analista de datos, el objetivo de este proyecto es evaluar el comportamiento de los clientes de **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica.

El análisis se realiza utilizando información registrada **hasta el año 2024**, con el propósito de comprender el comportamiento de los clientes, detectar oportunidades de mejora en los planes comerciales y generar recomendaciones basadas en datos para apoyar la toma de decisiones del negocio.

Durante el proyecto se desarrolla un proceso completo de **Análisis Exploratorio de Datos (EDA)**, limpieza de datos, detección de valores atípicos y segmentación de clientes según su comportamiento de uso y características demográficas.

---

# 🎯 Objetivos

El proyecto tiene como finalidad:

- Explorar y comprender la calidad de los datos.
- Detectar y corregir valores faltantes, sentinels y registros inválidos.
- Analizar el comportamiento de consumo de los clientes.
- Construir un perfil estadístico de los usuarios.
- Detectar patrones de uso y valores atípicos (outliers).
- Segmentar clientes según su nivel de uso y grupo de edad.
- Generar recomendaciones estratégicas para mejorar la oferta de planes y fortalecer las estrategias de retención.

---

# 📂 Datasets utilizados

Se trabajó con tres conjuntos de datos.

## 📁 plans.csv

Contiene la información de los planes comerciales actuales.

Incluye variables como:

- Precio mensual
- Minutos incluidos
- GB incluidos
- Costo por consumo adicional

---

## 📁 users.csv

Contiene la información de los clientes.

Variables principales:

- user_id
- first_name
- last_name
- age
- city
- reg_date
- plan
- churn_date

---

## 📁 usage.csv

Contiene el detalle del uso real de los servicios de telecomunicaciones.

Variables principales:

- id
- user_id
- type (call o text)
- date
- duration
- length

---

# 🔎 Etapas del análisis

El proyecto se desarrolló siguiendo las principales etapas de un proceso de análisis de datos.

## 1. Exploración inicial

- Revisión de estructura de los datasets.
- Validación de tipos de datos.
- Identificación de valores nulos.
- Revisión de estadísticas descriptivas.
- Exploración de variables categóricas.

---

## 2. Limpieza de datos

Se realizaron las siguientes acciones:

- Corrección del valor sentinel **-999** en la variable edad.
- Conversión del valor **"?"** en ciudad a valores nulos.
- Conversión de columnas de fecha al formato datetime.
- Identificación de fechas futuras (2026) y marcadas como valores nulos.
- Validación del patrón **MAR (Missing At Random)** para las variables duración de llamadas y longitud de mensajes.

---

## 3. Construcción del perfil de usuario

Se generaron métricas agregadas por cliente:

- Cantidad total de mensajes.
- Cantidad total de llamadas.
- Total de minutos consumidos en llamadas.

Posteriormente estas métricas fueron integradas con la información demográfica de cada usuario.

---

## 4. Análisis Exploratorio (EDA)

Se analizaron:

- Distribución de edades.
- Distribución del consumo.
- Variables categóricas.
- Valores faltantes.
- Valores inválidos.
- Valores atípicos mediante Boxplots e IQR.

---

## 5. Segmentación de clientes

Se construyeron dos tipos de segmentación.

### Segmentación por uso

- Bajo uso
- Uso medio
- Alto uso

### Segmentación por edad

- Joven
- Adulto
- Adulto Mayor

---

## 6. Visualización de datos

Se generaron diferentes visualizaciones para apoyar el análisis:

- Histogramas
- Boxplots
- Countplots

Estas visualizaciones permitieron comprender el comportamiento de las variables principales y detectar patrones de consumo.

---

## 7. Insights ejecutivos

Finalmente se elaboró un análisis orientado al negocio, incluyendo:

- Problemas de calidad de datos.
- Perfil de los clientes.
- Segmentos identificados.
- Patrones de consumo.
- Recomendaciones para nuevos planes.
- Estrategias de retención.

---

# 📈 Principales hallazgos

- Se detectaron valores sentinels y fechas fuera del periodo de análisis que fueron corregidos.
- Los valores nulos en **duration** y **length** corresponden a un patrón MAR y no representan errores.
- La mayor parte de los clientes presenta un consumo moderado de llamadas y mensajes.
- Existe un segmento reducido de usuarios con consumo intensivo que representa una oportunidad comercial para ConnectaTel.
- La edad no mostró una relación clara con el tipo de plan contratado.
- Los outliers identificados corresponden a comportamientos reales de clientes y fueron conservados para no perder información valiosa.

---

# 💡 Recomendaciones

Con base en el análisis realizado se recomienda:

- Implementar estrategias de segmentación basadas en el comportamiento de consumo.
- Diseñar planes diferenciados para clientes de alto consumo.
- Fortalecer campañas de migración hacia planes Premium.
- Mejorar los procesos de captura y validación de datos para reducir sentinels y registros inválidos.
- Monitorear continuamente los segmentos de alto valor para incrementar la retención y rentabilidad.

---

# ▶️ Cómo ejecutar el proyecto

## Opción 1. Google Colab

1. Abrir el notebook (`.ipynb`) en Google Colab.
2. Cargar los archivos:
   - `plans.csv`
   - `users.csv`
   - `usage.csv`
3. Ejecutar todas las celdas en orden mediante:

```
Entorno de ejecución → Ejecutar todo
```

---

## Opción 2. Jupyter Notebook

Clonar el repositorio:

```bash
git clone (https://github.com/Susana-Ramirez-Severiano/telecom-analysis.git)
```

Entrar al proyecto:

```bash
cd telecom-analysis
```

Instalar dependencias:

```bash
pip install pandas numpy matplotlib seaborn
```

## Estructura del proyecto

```text
telecom-analysis/
│
├── README.md
└── notebooks/
    └── telecom_analysis.ipynb
```

Abrir el notebook:

```bash
jupyter notebook
```

---

# 🔄 Guía de reproducción

Para reproducir el análisis:

1. Clonar o descargar este repositorio.
2. Colocar los tres archivos CSV dentro del proyecto.
3. Abrir el notebook en Google Colab o Jupyter Notebook.
4. Ejecutar todas las celdas en el orden establecido.
5. Revisar los resultados, visualizaciones e insights generados.

---

# 🛠️ Tecnologías utilizadas

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab
- Jupyter Notebook

---

# 👩‍💻 Autora

**Susana Ramírez Severiano**

Proyecto desarrollado como parte del proceso de formación en **Análisis de Datos con Python**, aplicando técnicas de limpieza de datos, análisis exploratorio (EDA), visualización, detección de outliers y segmentación de clientes para generar recomendaciones estratégicas orientadas al negocio.
