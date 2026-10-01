# 🚦 Proyecto Siniestralidad Vial 2024

Análisis de los accidentes de tráfico con víctimas registrados durante 2024 en seis provincias españolas. El proyecto combina **Python, análisis estadístico y Power BI** para estudiar patrones temporales, territoriales y relacionados con las características de la vía y del accidente.

También se compara la siniestralidad entre provincias teniendo en cuenta su población, para no quedarse únicamente con los valores absolutos.

## 🗂️ Estructura del proyecto

```text
proyecto-siniestralidad-2024/
├── dashboard/
├── data/
│   ├── raw/
│   │   ├── dgt/
│   │   └── ine/
│   └── processed/
├── images/
├── notebooks/
├── reports/
├── README.md
└── .gitignore
```

## 🧩 Tecnologías y requisitos

- Python 3
- pandas
- matplotlib
- openpyxl
- scipy
- Jupyter Notebook / Visual Studio Code
- Power BI

## 📊 Datos utilizados

- **DGT:** accidentes con víctimas de 2024 y diccionario de códigos.
- **INE:** población de 2024 por provincia.
- **Provincias analizadas:** Barcelona, Madrid, Valencia/València, Málaga, Sevilla y Murcia.

## 🔎 Qué he trabajado en este proyecto

### 01 · Exploración de datos

Partimos de un dataset de **101.996 filas y 73 columnas**. Revisé duplicados, valores nulos, tipos de datos y códigos de provincia. Después seleccioné las seis provincias del análisis y uní los datos de accidentes de la DGT con la población del INE.

El dataset filtrado quedó en **51.762 accidentes**.

### 02 · Limpieza y transformación

Preparé las variables necesarias para el análisis y creé columnas descriptivas para facilitar su interpretación: meteorología, zona, tipo de accidente, tipo de vía, día de la semana, franja horaria y variables relacionadas con la gravedad.

El dataset limpio final tiene **51.762 filas y 88 columnas**.

### 03 · Análisis exploratorio

Analicé:

- Accidentes y víctimas.
- Fallecidos, heridos graves y heridos leves.
- Accidentes por provincia y tasas por 100.000 habitantes.
- Evolución mensual.
- Día de la semana y hora.
- Relación día × hora.
- Zona, tipo de vía y tipo de accidente.
- Frecuencia frente a gravedad.

### 04 · Análisis estadístico

Apliqué pruebas **Chi-cuadrado** y calculé la **V de Cramér** para estudiar la relación entre distintas variables y la gravedad del accidente.

Las asociaciones analizadas resultaron estadísticamente significativas, aunque en general fueron **débiles**. La relación más alta apareció entre **tipo de accidente y gravedad**.

### 05 · Dashboard en Power BI

El dashboard final está dividido en tres páginas:

- **Resumen:** principales KPIs y visión general de la siniestralidad.
- **Patrones:** análisis temporal y de las características de los accidentes.
- **Comparativa provincial:** accidentes, población, tasa por 100.000 habitantes y gravedad por provincia.

Incluye tarjetas KPI, gráficos interactivos, comparaciones provinciales, tablas y segmentadores para poder filtrar la información.

## 📈 Resultados y conclusiones

| Indicador | Resultado |
|---|---:|
| Accidentes | 51.762 |
| Víctimas | 67.768 |
| Fallecidos 24 h | 445 |
| Heridos graves 24 h | 3.763 |
| Accidentes graves | 7,35 % |
| Mes con más accidentes | Octubre · 4.788 |
| Mes con menos accidentes | Agosto · 3.463 |
| Día con más accidentes | Viernes · 8.398 |
| Día con menos accidentes | Domingo · 5.461 |
| Pico horario | 14:00 · 3.942 |
| Mayor combinación día/hora | Viernes 14:00 · 762 |

Barcelona registra el mayor número de accidentes (**17.945**) y también la mayor tasa entre las seis provincias analizadas (**305,31 por 100.000 habitantes**). Madrid es la segunda provincia en accidentes absolutos (**14.183**), pero presenta la tasa más baja (**202,35**).

Uno de los puntos que más me ha interesado del análisis es comprobar que **tener más accidentes no significa necesariamente tener mayor gravedad**. La madrugada registra menos accidentes, pero una proporción mayor de accidentes graves y mortales. También sábado y domingo presentan una gravedad relativa superior a varios días laborables.

El análisis estadístico confirma que existen relaciones entre las variables estudiadas y la gravedad, pero ninguna de ellas explica por sí sola el fenómeno con una asociación fuerte.

## ✅ Estado del proyecto

- Exploración inicial: **terminada**
- Limpieza y transformación: **terminada**
- EDA: **terminado**
- Análisis estadístico: **terminado**
- Dashboard Power BI: **terminado**
- Informe final: **terminado**

## 🤝 Mejoras futuras

Como posibles mejoras, ampliaría el análisis a más provincias y años para poder estudiar la evolución temporal y realizar comparaciones más completas.

También sería interesante incorporar nuevas variables externas que puedan ayudar a explicar mejor la gravedad de los accidentes.

## ✒️ Autor

**David Merín**  
GitHub: **damefer-code**
