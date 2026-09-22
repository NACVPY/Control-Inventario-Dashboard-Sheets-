# 📦 Sistema de Control de Inventario y Cuadro de Mando de Ventas

## 📌 Descripción del Proyecto
Este proyecto consiste en el desarrollo de un **sistema integral de gestión de inventario y análisis de ventas** diseñado en Google Sheets para una pequeña/mediana empresa de comercio electrónico. 

El sistema soluciona dos problemas operativos clave:
1. **Control de Stock en Tiempo Real:** Automatización de alertas de reabastecimiento para evitar roturas de stock.
2. **Análisis de Rendimiento Comercial:** Visualización centralizada de KPIs globales e ingresos consolidados por categoría de producto.

---

## 🛠️ Funcionalidades y Técnicas Utilizadas

- **Consolidación y Cruce de Datos:** Uso de la función `BUSCARV` (`VLOOKUP`) para conectar tablas relacionales (`01_Productos` y `02_Ventas`) e importar dinámicamente categorías y precios unitarios.
- **Alertas Operativas Automatizadas:** Implementación de funciones lógicas `=SI()` (`IF`) para la detección de stock crítico (límite $\le 25$ unidades) complementado con **Formato Condicional** visual.
- **Cálculo de Agregación:** Uso de `=SUMAR.SI()` (`SUMIF`) y `=SUMA()` (`SUM`) para el rastreo del total de unidades vendidas e ingresos brutos por transacción.
- **Análisis Multidimensional:** Creación de una **Tabla Dinámica** centralizada en el Dashboard para evaluar el volumen de ventas e ingresos por categoría de producto.
- **Visualización de Datos:** Cuadro de mando (`03_Dashboard`) interactivo con KPIs ejecutivos y un gráfico analítico de columnas.

---

## 📂 Estructura del Libro de Trabajo

El proyecto está estructurado en tres pestañas interconectadas:

1. **`01_Productos` (Catálogo Master):** Contiene el catálogo de productos, precios, costos, stock inicial, stock actual calculado y el estado de alerta de reabastecimiento.
2. **`02_Ventas` (Registro Transaccional):** Histórico de transacciones de venta enriquecido dinámicamente con categorías e ingresos calculados.
3. **`03_Dashboard` (Cuadro de Mando):** Resumen ejecutivo con indicadores clave (Total Productos, Alertas Activas, Total Unidades) y gráfico de ventas por categoría.

---

## 📊 Principales Hallazgos (Insights)

- **Alertas de Stock:** Se identificó que el producto **Escritorio Madera (PROD-005)** requiere reabastecimiento inmediato al contar con únicamente 13 unidades disponibles.
- **Categoría Líder:** La categoría **Mobiliario** generó la mayor parte de los ingresos brutos debido al alto valor unitario de sus productos.
- **Efectividad Operativa:** La automatización reduce los tiempos de revisión manual de stock y elimina el riesgo de error humano en la actualización de precios e ingresos.

---

## 🚀 Cómo Utilizar este Repositorio

1. Descarga el archivo `.xlsx` o `.csv` adjunto en este repositorio.
2. Impórtalo en **Google Sheets** o **Microsoft Excel**.
3. Navega a la pestaña `03_Dashboard` para consultar el cuadro de mando general.
