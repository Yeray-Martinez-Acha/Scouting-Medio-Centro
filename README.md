# ⚽ Scouting de Mediocentros | Sustituto de Toni Kroos

## 🎯 Objetivo del proyecto

Este proyecto tiene como objetivo identificar mediocentros con un perfil similar al de Toni Kroos mediante técnicas de análisis de datos.

Se simula el trabajo de un departamento de scouting, buscando un jugador que pueda asumir el rol de organizador del juego tras la retirada del futbolista alemán.

El objetivo es:
- Detectar perfiles similares a Kroos
- Reducir el número de candidatos
- Apoyar la toma de decisiones en fichajes

---

## 📊 Datos

El análisis se basa en datos de jugadores de las Top 5 ligas europeas (2024/2025), incluyendo métricas relacionadas con:

- Creación de juego (Ast, xAG)
- Progresión (PrgP, PrgC, PrgR)
- Contribución ofensiva

El dataset incluye todos los jugadores, pero el análisis se centra en mediocampistas.

---

## ⚙️ Metodología

El pipeline se estructura en varias fases:

### 1. Selección de variables

Se seleccionan métricas alineadas con el rol de mediocentro organizador:

- Ast, xAG  
- PrgP (pases progresivos)  
- PrgC (conducciones progresivas)  
- Ast_90, xAG_90  

👉 Estas variables capturan creación y progresión del juego :contentReference[oaicite:0]{index=0}

---

### 2. Análisis exploratorio (EDA)

- Histogramas → detección de sesgo en variables ofensivas
- Boxplots → comparación por posición

Resultados clave:
- Los mediocampistas destacan en creación y progresión
- Alta dispersión → existencia de distintos perfiles :contentReference[oaicite:1]{index=1}

---

### 3. Análisis de correlaciones

- Correlaciones positivas moderadas entre variables
- No existe redundancia total → cada variable aporta información distinta :contentReference[oaicite:2]{index=2}

---

### 4. Filtrado de jugadores

Criterios:
- Edad < media (~24 años)
- Minutos > mediana (~1013)
- Partidos > mediana (~11.3)

👉 Se busca un perfil joven con impacto inmediato :contentReference[oaicite:3]{index=3}

---

### 5. Modelo de similitud (Distancia Euclidiana)

Se calcula la distancia entre jugadores en un espacio multidimensional de variables.

Cada jugador se representa como un vector de características y se compara con el perfil de Toni Kroos.

👉 Cuanto menor la distancia → mayor similitud

Resultados destacados:
- Angelo Stiller (perfil más cercano)
- Enzo Fernández
- João Neves
- Pedri :contentReference[oaicite:4]{index=4}

---

### 6. PCA (Análisis de Componentes Principales)

- Reducción de dimensionalidad
- Visualización de jugadores en espacio 2D

Resultados:
- Los jugadores más similares se agrupan cerca de Kroos
- Validación visual del modelo :contentReference[oaicite:5]{index=5}

---

### 7. Radar charts

- Comparación directa de perfiles
- Identificación de similitudes y diferencias en variables clave

---

## 🧠 Resultados clave

El análisis identifica distintos perfiles:

- 🔵 Perfil organizador puro (similar a Kroos)
- 🟡 Perfil dinámico (más conducción y verticalidad)
- 🔴 Perfil ofensivo (menos estructural)

👉 Angelo Stiller emerge como el perfil más similar

---

## ⚠️ Limitaciones

- Dataset centrado en métricas ofensivas
- No incluye:
  - Variables defensivas
  - Posicionamiento
  - Contexto táctico

👉 El modelo captura similitud ofensiva, no el perfil completo del jugador :contentReference[oaicite:6]{index=6}

---

## 📁 Estructura del proyecto

scouting-mediocentros/
│
├── analisisScoutingMediocentro.ipynb
├── dataset.csv
├── ranking_mediocentros.csv
└── README.md

---

## ▶️ Reproducibilidad

1. Instalar dependencias:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn

analisisScoutingMediocentro.ipynb

## 👤 Author

Yeray Martínez  
Master in Big Data & Artificial Intelligence
