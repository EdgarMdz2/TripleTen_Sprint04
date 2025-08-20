# 🛒 Análisis de Pedidos en Instacart

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)

**Instacart** es una plataforma de entregas de comestibles donde los clientes pueden registrar un pedido y recibirlo a domicilio, de manera similar a Uber Eats o Door Dash.

El presente análisis se centra en el estudio de patrones de consumo y comportamiento de usuarios, con el fin de extraer información útil que pueda orientar estrategias de negocio y mejorar la experiencia de compra.

El proyecto se estructura en tres fases principales:

1. Acceso y preparación de los datos  
2. Preprocesamiento y limpieza  
3. Análisis exploratorio y hallazgos clave  

---

## 📂 Conjunto de datos

El dataset incluye cinco tablas principales, que en conjunto permiten un análisis integral:

- `instacart_orders.csv` → Información sobre cada pedido (usuario, fecha, frecuencia).  
- `products.csv` → Catálogo de productos disponibles en la plataforma.  
- `order_products.csv` → Relación de artículos dentro de cada pedido.  
- `aisles.csv` → Identificación de pasillos.  
- `departments.csv` → Identificación de departamentos.  

Cada archivo fue convertido en un **DataFrame** y sometido a una revisión inicial para identificar inconsistencias.

---

## 🔎 Paso 1. Descripción y exploración inicial

Se revisó la estructura de los datos, aplicando métodos como `info()` y `head()` para obtener una primera impresión.  
Durante esta fase se identificaron necesidades de limpieza, como:

- Valores nulos en **days_since_prior_order** (`instacart_orders`).  
- Datos ausentes en **product_name** (`products`).  
- Ajustes en tipos de datos numéricos, como en **add_to_cart_order** `order_products`).  

---

## 🛠️ Paso 2. Preprocesamiento de datos

El preprocesamiento incluyó:

- Corrección de tipos de datos (IDs y secuencias).  
- Tratamiento de valores ausentes → imputación o eliminación según contexto.  
- Eliminación de duplicados explícitos e implícitos.  

Este proceso aseguró que los **DataFrames** estuvieran listos para un análisis confiable.

---

## 🧠 Paso 3. Análisis de los datos

El análisis se desarrolló en tres etapas:

### 📊 Etapa A: Exploración básica

- Validación de la consistencia en horas y días de pedidos.  
- Distribución de compras por hora del día y día de la semana.  
- Análisis del tiempo de espera entre pedidos.  

### 📊 Etapa B: Comportamiento de clientes

- Comparación de distribuciones entre distintos días (ej. miércoles vs sábados).  
- Distribución del número de pedidos por cliente.  
- Identificación de los **20 productos más pedidos**.  

### 📊 Etapa C: Patrones de compra

- Distribución del número de artículos por pedido.  
- Identificación de los **20 productos más reordenados**.  
- Cálculo de la **tasa de repetición por producto y por cliente**.  
- Detección de los artículos más frecuentes como *“primer producto en carrito”*.  

---

## 📝 Conclusiones

El análisis permitió identificar **insights clave**:

- Productos más populares dentro de la plataforma.  
- Momentos de mayor actividad (horarios y días específicos).  
- Clientes leales con alta frecuencia de reordenamiento.  
- Tendencias en el tamaño de los pedidos.  
- Productos con mayor recurrencia en reordenes.  

Estos hallazgos representan información valiosa para:

✅ Optimizar estrategias de marketing.  
✅ Diseñar promociones dirigidas a los clientes más leales.  
✅ Ajustar inventarios según la demanda real.  
✅ Mejorar la experiencia del usuario dentro de la app.  

---

Este proyecto demuestra cómo el análisis de datos puede revelar patrones de consumo que ayudan a tomar decisiones estratégicas en plataformas de **e-commerce y delivery**.
