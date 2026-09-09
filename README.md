# 📊 Quantitative Portfolio Analysis Engine

Motor de análisis cuantitativo desarrollado en Python para la auditoría de rendimiento histórico, medición de riesgos institucionales, modelado estocástico y visualización de carteras multiactivo.

## 🚀 Características Principales
* **Adquisición Dinámica:** Conexión en tiempo real con Yahoo Finance para la extracción de precios históricos y benchmarks (`^GSPC`, `^IXIC`).
* **Métricas Institucionales:** Cálculo automatizado de CAGR, Volatilidad Anualizada, Ratio de Sharpe y Max Drawdown.
* **Análisis de Riesgo Avanzado:** Curvas submarinas (*drawdown curves*) duales y desglosadas por activo para medir el estrés histórico de la cartera.
* **Modelado Estocástico:** Simulación de Monte Carlo (1,000 trayectorias a 1 año) con bandas de confianza (Mediana y VaR al 5%).
* **Visualización de Datos:** Gráficos de alta fidelidad optimizados con `matplotlib` y `seaborn` replicando estándares de reportes financieros.

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
└── README.md                  # Documentación del proyecto
```
## ⚙️ Cómo Ejecutar el Proyecto
1. Clona este repositorio:
   ```bash
   git clone https://github.com/veracarlosjr/portafolio-quantitative-engine.git
   ```

2. Instalar dependencias:
    ```bash
pip install -r requirements.txt
    ```

3. Abre la libreta en Jupyter Notebook: 
    ```bash
    jupyter notebook portfolio_analysis.ipynb
    ```

    
Desarrollado por Carlos Vera