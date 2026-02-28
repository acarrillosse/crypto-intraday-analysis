# Análisis intrasesión de criptomonedas (Top 50 CoinMarketCap)

## 📌 Descripción del proyecto

Este proyecto analiza el comportamiento intrasesión de las 50 principales criptomonedas por capitalización de mercado utilizando datos de alta frecuencia extraídos desde la API de CoinMarketCap. A partir de observaciones tomadas cada 15 minutos durante una ventana temporal limitada, se construyen métricas financieras clave y se aplica un análisis exploratorio y no supervisado para identificar patrones de comportamiento a corto plazo.

El objetivo principal es demostrar cómo, incluso con una ventana temporal reducida, es posible extraer información relevante sobre retornos, volatilidad y actividad de mercado mediante técnicas de ingeniería de variables y clustering.

---

## 📊 Fuente de datos

Los datos se obtienen directamente desde la API oficial de CoinMarketCap a través del endpoint:

- `cryptocurrency/listings/latest`

Características del dataset:
- 50 criptomonedas (Top 50 por capitalización)
- Observaciones cada 15 minutos
- Ventana aproximada de 3 horas
- Datos en USD
- Almacenamiento incremental en CSV

---

## 🗂️ Estructura del repositorio

├── data_collection.ipynb
├── CoinMarket_website_project.ipynb
├── coinmarket_data.csv
└── README.md


### 📁 `data_collection.ipynb`
Notebook encargado de la extracción periódica de datos desde la API de CoinMarketCap. Implementa:
- Conexión autenticada a la API
- Descarga de datos del Top 50
- Normalización del JSON
- Almacenamiento incremental en CSV con timestamp

### 📁 `CoinMarket_website_project.ipynb`
Notebook principal de análisis, que incluye:
- Limpieza y preparación de datos
- Conversión de variables
- Construcción de métricas financieras intrasesión
- Ingeniería de variables
- Visualización multivariante
- Escalado y clustering no supervisado (K-Means)

### 📁 `coinmarket_data.csv`
Dataset final generado a partir de la recolección periódica de datos desde la API.

---

## 🔍 Principales conclusiones

- Los retornos intrasesión presentan una distribución centrada en cero con colas pesadas, típica de activos financieros de alta frecuencia.
- Existe una fuerte heterogeneidad en el comportamiento intrasesión incluso dentro del Top 50.
- La combinación de retorno, volatilidad e intensidad de volumen permite identificar perfiles de criptomonedas con comportamientos claramente diferenciados.
- El clustering no supervisado resulta útil para segmentar activos según su dinámica de corto plazo.

---

## 🛠️ Tecnologías utilizadas

- Python
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- CoinMarketCap API

---

## 👤 Autor

Proyecto desarrollado como ejercicio de análisis de datos financieros y series temporales intrasesión.
