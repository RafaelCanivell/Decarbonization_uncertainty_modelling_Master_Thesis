# Decarbonization Trajectory Modeling under Contextual and Medical-Operational Uncertainty

> **Master's Thesis — Universidad Nacional de Educacion a Distancia · December 2025**  
> *Author: Rafael Canivell ·

---

## English

### Overview

This repository contains the code, data pipelines, and analytical notebooks developed for the Master's Thesis (TFM):

> **"Modeling Decarbonization Trajectories under Contextual and Medical-Operational Uncertainty"**

The work develops an analytical and predictive framework to model decarbonization trajectories in **medical-humanitarian projects**, incorporating operational and contextual uncertainty to support strategic decision-making toward the institutional goal of **reducing carbon emissions by 50% by 2030**.

---

### Objectives

#### Objective 1 — Historical Carbon Footprint Analysis
> *Where are we and how did we get here?*

Characterizes the historical trajectory of environmental and operational performance, analyzing:
- Evolution of the operational volume index (z-score normalization, PCA, Factor Analysis)
- Cost of decarbonization (linear regression: expenditure per operational unit vs. emission intensity)
- Temporal decomposition of emissions (STL: Seasonal-Trend decomposition using Loess)
- Correlation between operational volume and CO₂ emissions
- Identification of highest-emitting categories and cluster analysis

#### Objective 2 — Drivers of Decarbonization Success
> *What explains whether a project succeeds in reducing emissions?*

Identifies the factors that explain environmental success using three complementary lenses:
- **Composite environmental score** + logistic regression (probability of success)
- **Clustering + H2O AutoML** (GBM, XGBoost, Random Forests) with SHAP explainability
- **Causal inference** (T-Learner with XGBoost) to distinguish causation from correlation between medical activity and emissions

#### Objective 3 — Impact Evaluation of Decarbonization Strategies
> *How effective are Green Initiatives and non-registered strategies?*

Evaluates the impact of decarbonization strategies from two angles:
- **Green Initiatives (GI) evaluation** (2023–2024): counterfactual modeling with H2O AutoML + causal estimation with T-Learner (CATE, ATE, tCO₂/€ efficiency)
- **Latent proxy variable** for unregistered decarbonization strategies: autoencoder-based anomaly detection + K-Means clustering + T-Learner causal estimation

---

### Methodology Summary

| Technique | Purpose |
|---|---|
| Z-score normalization + PCA + FA | Operational volume index construction |
| STL decomposition | Temporal emission pattern analysis |
| Linear regression | Decarbonization cost proxy |
| Logistic regression | Probability of environmental success |
| H2O AutoML (GBM, XGBoost, RF) | Feature importance & predictive modeling |
| SHAP values | Local & global explainability |
| T-Learner (CausalML + XGBoost) | CATE / ATE estimation |
| Autoencoder + K-Means | Latent proxy for unregistered strategies |

---

### Scope & Limitations

- Analysis is constrained by **data availability** — absence of georeferenced historical data prevented integration of environmental covariates.
- Scope is limited to **country and project coordination levels**, the most directly linked to medical-humanitarian activities.
- Annual data on expenditure and medical activities are transformed to **daily averages**; full-time equivalent (FTE) staffing is held constant within each year.

---

### Citation

If you use this work, please cite:

```
Rafael Canivell (2025). Modeling Decarbonization Trajectories under Contextual 
and Medical-Operational Uncertainty. Master's Thesis, [UNED].
```

---

# Modelización de Trayectorias de Descarbonización bajo Incertidumbre Contextual y Médico-Operacional

> **Trabajo de Fin de Máster (TFM) — Universidad Espanola de Eduacion a Distancia-UNED · Diciembre 2025**  
> *Autor: Rafael Canivell*

---

## Español

### Descripción general

Este repositorio contiene el código, los pipelines de datos y los notebooks analíticos desarrollados para el Trabajo de Fin de Máster (TFM):

> **"Modelización de Trayectorias de Descarbonización bajo Incertidumbre Contextual y Médico-Operacional"**

El trabajo desarrolla un marco analítico y predictivo para modelar las trayectorias de descarbonización en **proyectos médico-humanitarios**, incorporando la incertidumbre operacional y contextual para orientar la toma de decisiones estratégicas hacia la meta institucional de **reducir un 50% las emisiones de carbono para 2030**.

---

### Objetivos

#### Objetivo 1 — Análisis histórico de la huella de carbono
> *¿Dónde estamos y cómo hemos llegado hasta aquí?*

Caracteriza la trayectoria histórica del desempeño ambiental y operativo, analizando:
- Evolución del índice de volumen operacional (normalización z-score, PCA, Análisis Factorial)
- Coste de la descarbonización (regresión lineal: gasto por unidad operacional vs. intensidad de emisiones)
- Descomposición temporal de emisiones (STL: Seasonal-Trend decomposition using Loess)
- Correlación entre volumen operacional y emisiones de CO₂
- Identificación de categorías más emisoras y análisis de clusters

#### Objetivo 2 — Causas de éxito en la descarbonización
> *¿Qué explica si un proyecto tiene éxito en reducir emisiones?*

Identifica los factores que explican el éxito ambiental mediante tres perspectivas complementarias:
- **Score ambiental compuesto** + regresión logística (probabilidad de éxito)
- **Clustering + H2O AutoML** (GBM, XGBoost, Random Forests) con explicabilidad SHAP
- **Inferencia causal** (T-Learner con XGBoost) para distinguir causalidad de correlación entre actividad médica y emisiones

#### Objetivo 3 — Evaluación del impacto de estrategias de descarbonización
> *¿Qué tan efectivas son las Green Initiatives y las estrategias no registradas?*

Evalúa el impacto de las estrategias de descarbonización desde dos ángulos:
- **Evaluación de Green Initiatives (GI)** (2023–2024): modelado contrafactual con H2O AutoML + estimación causal con T-Learner (CATE, ATE, eficiencia tCO₂/€)
- **Variable latente proxy** para estrategias de descarbonización no registradas: detección de anomalías con autoencoder + clustering K-Means + estimación causal T-Learner

---

### Resumen metodológico

| Técnica | Propósito |
|---|---|
| Normalización z-score + PCA + AF | Construcción del índice de volumen operacional |
| Descomposición STL | Análisis de patrones temporales de emisiones |
| Regresión lineal | Proxy del coste de descarbonización |
| Regresión logística | Probabilidad de éxito ambiental |
| H2O AutoML (GBM, XGBoost, RF) | Importancia de variables y modelado predictivo |
| Valores SHAP | Explicabilidad local y global |
| T-Learner (CausalML + XGBoost) | Estimación de CATE / ATE |
| Autoencoder + K-Means | Variable proxy latente para estrategias no registradas |

---

### Alcance y limitaciones

- El análisis está condicionado por la **disponibilidad de datos** — la ausencia de información georreferenciada histórica impidió integrar covariables ambientales en los modelos.
- El estudio se centra en los **niveles de coordinación de país y proyecto**, los más directamente vinculados a las actividades médico-humanitarias.
- Los datos anuales de gasto y actividades médicas se transforman en **valores diarios promedio**; los datos de equivalente a tiempo completo (ETC) se mantienen constantes a lo largo de cada año.

---

### Cita

Si utilizas este trabajo, por favor cítalo de la siguiente manera:

```
Rafael Canivell (2025). Modelización de Trayectorias de Descarbonización 
bajo Incertidumbre Contextual y Médico-Operacional. 
Trabajo de Fin de Máster, UNED.
```
