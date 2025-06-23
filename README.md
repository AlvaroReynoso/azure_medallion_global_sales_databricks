## 🛒 Modelo Medallón con Databricks: Ventas Globales de Supermercado
Este proyecto demuestra la aplicación del modelo medallón (Medallion Architecture) en Databricks, utilizando únicamente notebooks para gestionar y transformar datos de ventas globales de un supermercado a partir de archivos CSV. Se implementan tres capas: Bronce, Plata y Oro, cada una con su propósito claro dentro del flujo de procesamiento de datos.

### 🥉 Capa Bronce – Raw Layer
Objetivo: Ingestar los archivos CSV tal como vienen, sin transformaciones.

Acciones:

Lectura directa de los archivos *.csv desde el almacenamiento (ADLS).

Se registran los datos crudos en formato Delta Lake y como archivos .csv para trazabilidad y auditoría.

### 🥈 Capa Plata – Cleaned & Enriched Layer
Objetivo: Limpiar y transformar los datos para que sean usables.

Acciones:

Filtrado de registros nulos o inconsistentes.

Conversión de tipos de datos (ej. fechas, montos).

Normalización de campos (nombres de productos, categorías, etc.).

Enriquecimiento con campos derivados (ej. año, mes, día de la venta).

### 🥇 Capa Oro – Business Layer
Objetivo: Generar vistas finales para análisis de negocio con KPIs ,agregaciones y porcentajes


