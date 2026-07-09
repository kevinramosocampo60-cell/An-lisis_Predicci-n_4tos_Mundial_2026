# ⚽ Predicción Bayesiana de los Semifinalistas del Mundial FIFA 2026
### Modelo Jerárquico Dixon-Coles con PyMC

Este proyecto implementa un **modelo bayesiano jerárquico basado en Dixon-Coles** utilizando **PyMC** para estimar las fortalezas ofensivas y defensivas de las selecciones clasificadas a las fases finales del Mundial FIFA 2026. A partir de estas estimaciones se realizan simulaciones Monte Carlo para predecir las probabilidades de clasificación hacia las semifinales.

---

## 📌 Descripción

El notebook desarrolla un flujo completo de modelado probabilístico que combina información histórica de resultados internacionales con variables externas como:

- Ranking FIFA.
- Valor de mercado de las selecciones.
- Historial de goles.
- Ventaja de localía.
- Modelo de goles basado en distribuciones de Poisson.

A diferencia de un modelo determinista, este enfoque incorpora la incertidumbre mediante inferencia bayesiana, permitiendo obtener distribuciones posteriores de las habilidades de cada equipo y estimar probabilidades reales de clasificación.

---

## 🚀 Características

- Implementación completa del modelo Dixon-Coles.
- Modelo jerárquico construido con PyMC.
- Priors informativos utilizando Ranking FIFA y valor de mercado.
- Inferencia Bayesiana mediante NUTS (No-U-Turn Sampler).
- Simulación Monte Carlo de los cruces eliminatorios.
- Visualización y análisis de distribuciones posteriores.
- Código completamente documentado paso a paso.

---

## 📂 Estructura del Notebook

1. Instalación de dependencias.
2. Configuración del entorno.
3. Carga de datasets.
4. Identificación automática de columnas.
5. Indexación de equipos.
6. Construcción de priors informativos.
7. Definición del modelo jerárquico Dixon-Coles.
8. Muestreo de la distribución posterior.
9. Simulación probabilística de partidos.
10. Predicción de semifinalistas mediante Monte Carlo.

---

## 📊 Modelo Estadístico

El modelo asume que los goles anotados por cada selección siguen una distribución de Poisson:

\[
G_{local}\sim Poisson(\lambda_{local})
\]

\[
G_{visita}\sim Poisson(\lambda_{visita})
\]

donde las intensidades dependen de:

- Fortaleza ofensiva.
- Fortaleza defensiva.
- Ventaja de localía.
- Priors informativos derivados del Ranking FIFA.
- Priors informativos derivados del valor de mercado.

Las distribuciones posteriores son obtenidas mediante **MCMC** utilizando el algoritmo **NUTS**.

---

## 📈 Resultados

El modelo permite estimar:

- Fortaleza ofensiva de cada selección.
- Fortaleza defensiva de cada selección.
- Distribuciones posteriores de los parámetros.
- Probabilidades de victoria.
- Probabilidades de clasificación.
- Probabilidades de alcanzar las semifinales.
- Simulaciones de múltiples escenarios posibles.

---

## 🛠️ Tecnologías utilizadas

- Python
- PyMC
- ArviZ
- NumPy
- Pandas
- SciPy
- Matplotlib
- Scikit-Learn
- PyTensor

---

## 📁 Datos utilizados

El proyecto utiliza tres fuentes principales de información:

- Historial de partidos internacionales.
- Ranking FIFA.
- Valor de mercado de las selecciones nacionales.

Estos datos son empleados para construir priors informativos que mejoran la estabilidad del modelo.

---

## ▶️ Ejecución

1. Clonar el repositorio.

```bash
git clone https://github.com/usuario/repositorio.git
```

2. Instalar las dependencias.

```bash
pip install pymc arviz pytensor scikit-learn pandas numpy matplotlib scipy
```

3. Configurar la ruta donde se encuentran los archivos CSV.

4. Ejecutar el notebook desde Jupyter Notebook o Google Colab.

---

## 📚 Aplicaciones

Este proyecto puede adaptarse para:

- Predicción de torneos internacionales.
- Análisis deportivo.
- Modelado Bayesiano.
- Ciencia de Datos.
- Aprendizaje Estadístico.
- Simulación Monte Carlo.
- Investigación en analítica deportiva.

---

## 📖 Referencias

- Dixon, M. J., & Coles, S. G. (1997). *Modelling Association Football Scores and Inefficiencies in the Football Betting Market.*
- PyMC Documentation.
- ArviZ Documentation.

---

## 👨‍💻 Autor

**Kevin Ramos Ocampo**

Proyecto desarrollado con fines académicos para el estudio de modelos bayesianos aplicados a la predicción deportiva mediante inferencia probabilística y simulación Monte Carlo.
