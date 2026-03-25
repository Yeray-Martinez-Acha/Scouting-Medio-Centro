# 🍹 Análisis del Desempeño Comercial en el Sector de Bebidas

## 🎯 Objetivo

Este proyecto analiza un dataset de ventas del sector de bebidas con el objetivo de entender:

- La estructura del negocio (B2B vs B2C)
- El comportamiento de clientes y productos
- El impacto de la política de descuentos sobre ingresos y volumen
- La eficiencia comercial del modelo

---

## 📊 Dataset

El análisis se basa en un dataset transaccional con información sobre:

- Clientes (B2B y B2C)
- Productos y categorías
- Precios, descuentos y cantidades
- Regiones
- Fechas de pedido

---

## 🔍 Metodología

El proyecto sigue una estructura analítica completa:

### 1. Limpieza de datos
- Eliminación de valores nulos
- Verificación de coherencia (`Unit_Price * Quantity * (1 - Discount)`)
- Conversión de formatos

### 2. Análisis Exploratorio (EDA)
- Evolución temporal de ventas
- Distribución por categoría, producto y región
- Identificación de productos top

### 3. Análisis de clientes
- Comparativa B2B vs B2C
- Ticket medio y volumen de compra
- Principio de Pareto aplicado a clientes

### 4. Análisis de descuentos
- Frecuencia e intensidad del descuento
- Impacto económico (dinero dejado de ingresar)
- Comparativa por regiones

### 5. Relación descuento - ingresos
- Impacto en volumen de pedidos
- Impacto en ingreso medio y total
- Identificación de niveles óptimos de descuento

### 6. Análisis del mix de productos
- Evaluación del efecto composición
- Relación entre descuento y precio base
- Análisis por categorías y percentiles

---

## 📈 Principales insights

- 📌 El **77% de los ingresos proviene del canal B2B**, basado en pedidos de alto volumen :contentReference[oaicite:0]{index=0}  
- 📌 El **20% de los productos genera el 71,6% de la facturación** (concentración moderada) :contentReference[oaicite:1]{index=1}  
- 📌 La base de clientes está **relativamente diversificada** (20% → 46,5% ingresos) :contentReference[oaicite:2]{index=2}  
- 📌 El descuento:
  - Aumenta el tamaño del pedido  
  - NO maximiza ingresos en niveles altos  
  - Tiene su punto óptimo en torno al **10%** :contentReference[oaicite:3]{index=3}  

- 📌 Existe un **efecto de composición**:
  - Los mayores descuentos se aplican a productos más caros  
  - Esto distorsiona el análisis del ingreso por unidad  

---

## 🧠 Conclusión

El modelo de negocio está claramente orientado al volumen, con:

- Dependencia estructural del canal B2B  
- Política de descuentos centralizada  
- Segmentación implícita del catálogo según valor  

El descuento no actúa solo como incentivo, sino como parte del diseño estratégico del negocio.

---

## 🛠️ Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn


---

## ▶️ Reproducibilidad

1. Instalar dependencias:

```bash
pip install pandas numpy matplotlib seaborn 

## 📁 Estructura del proyecto
├── analisis_ventas_bebidas.ipynb
├── dataset.csv
├── Informe Venta Bebidas.pdf
└── README.md

## 👤 Author

Yeray Martínez  
Master in Big Data & Artificial Intelligence
