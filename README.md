# 📊 Quantitative Portfolio Analysis Engine

![Python](https://img.shields.io/badge/Python-3.11%2B-blue?logo=python&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Activo-brightgreen)

Motor de análisis cuantitativo desarrollado en Python para la auditoría de rendimiento histórico, medición de riesgos institucionales, modelado estocástico y visualización de carteras multiactivo.

## 🚀 Características Principales

* **Adquisición Dinámica:** Conexión en tiempo real con Yahoo Finance para la extracción de precios históricos y benchmarks (`^GSPC`, `^IXIC`).
* **Métricas Institucionales:** Cálculo automatizado de CAGR, Volatilidad Anualizada, Ratio de Sharpe, Max Drawdown y **Beta** (riesgo sistemático vs. el mercado).
* **Análisis de Correlación:** Matriz de correlación entre activos para evaluar el grado real de diversificación de la cartera.
* **Composición de Cartera:** Desglose de tenencias por activo y por sector económico, replicando el formato de un reporte institucional.
* **Análisis de Riesgo Avanzado:** Curvas submarinas (*drawdown curves*) duales y desglosadas por activo para medir el estrés histórico de la cartera.
* **Modelado Estocástico:** Simulación de Monte Carlo (1.000 trayectorias a 1 año) con bandas de confianza (Mediana y VaR al 5%).
* **Visualización de Datos:** Gráficos de alta fidelidad optimizados con `matplotlib` y `seaborn` replicando estándares de reportes financieros.

## 📈 Resultados de Ejemplo

<!-- TODO: reemplazar por capturas reales exportadas desde el notebook (guardarlas en una carpeta assets/ del repo) -->
<!-- Sugerencia: el scatter de riesgo vs. retorno con Beta, y la curva de drawdown dual son las más ilustrativas -->
| Métrica | Mi Cartera | S&P 500 | NASDAQ |
|---|---|---|---|
| CAGR | 29.42% | 19.24% | 25.99% |
| Volatilidad Anual | 22.79% | 16.10% | 21.62% |
| Sharpe Ratio | 1.09 | 0.92 | 0.99 |
| Max Drawdown | -19.81% | -18.90% | -24.32% |
| Beta (vs S&P 500) | 1.28 | 1.00 | 1.30 |

`![Riesgo vs. Retorno](assets/riesgo_retorno.png)`
`![Curva de Drawdown](assets/drawdown.png)`

## 🧠 Metodología

* **CAGR:** tasa de crecimiento anual compuesto, calculada a partir del retorno acumulado de la serie.
* **Sharpe Ratio:** `(CAGR - tasa libre de riesgo) / Volatilidad anualizada` — retorno obtenido por unidad de riesgo asumido.
* **Beta:** `Covarianza(cartera, mercado) / Varianza(mercado)` — sensibilidad de la cartera a los movimientos del S&P 500.
* **Max Drawdown:** la mayor caída porcentual desde un máximo histórico hasta el mínimo posterior.
* **Monte Carlo:** simulación de 1.000 trayectorias aleatorias basadas en la media y desviación estándar histórica de los retornos, para estimar un rango de resultados futuros (mediana y VaR al 5%).

## 🛠️ Stack Tecnológico

* **Lenguaje:** Python (3.11+)
* **Librerías:** `pandas`, `numpy`, `yfinance`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`
* **Entorno:** Jupyter Notebook / Anaconda

## 📂 Estructura del Proyecto

```text
portfolio-quantitative-engine/
│
├── portfolio_analysis.ipynb   # Notebook principal con el motor de análisis
├── requirements.txt           # Dependencias del proyecto
├── assets/                    # Capturas de los gráficos generados (para este README)
└── README.md                  # Documentación del proyecto
```

## ⚙️ Cómo Ejecutar el Proyecto

1. Clona este repositorio:
   ```bash
   git clone https://github.com/veracarlosjr/portfolio-quantitative-engine.git
   ```

2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

3. Abre la libreta en Jupyter Notebook:
   ```bash
   jupyter notebook portfolio_analysis.ipynb
   ```

## 🔧 Personalización

Para correr el análisis sobre tu propia cartera, solo tenés que editar el diccionario `portfolio_weights` al inicio del notebook con tus propios tickers y pesos, y ajustar `sector_map` si querés que el desglose por sector refleje tu composición real.

## 🗺️ Próximos Pasos

* Value at Risk (VaR) paramétrico e histórico, además del VaR por simulación ya incluido en Monte Carlo
* Optimización de cartera (frontera eficiente de Markowitz)
* Backtesting de estrategias de rebalanceo
* Beta rolling (ventanas móviles) para detectar cambios en la sensibilidad al mercado a lo largo del tiempo

## ⚠️ Disclaimer

Este proyecto tiene fines educativos y de demostración técnica. No constituye asesoramiento financiero ni una recomendación de inversión. Los datos de la cartera utilizados son reales pero el análisis no debe usarse como única base para decisiones de inversión.

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 👤 Autor

Desarrollado por **Carlos Vera**
[LinkedIn](TU_LINK_DE_LINKEDIN_ACA) · [GitHub](https://github.com/veracarlosjr)
