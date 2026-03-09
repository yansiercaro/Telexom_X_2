# Telexom_X_2

Challenge de Alura

Este proyecto aplica técnicas de Machine Learning para predecir la probabilidad de que un cliente cancele sus servicios en una empresa de telecomunicaciones. El objetivo es proporcionar al departamento de Marketing una herramienta accionable para reducir la tasa de rotación y mejorar la retención de ingresos.

# 🎯 Descripción del Problema

La pérdida de clientes (Churn) es uno de los mayores desafíos en la industria de telecomunicaciones. Retener a un cliente existente es considerablemente más económico que adquirir uno nuevo. Este proyecto busca identificar los factores de riesgo y predecir qué clientes tienen mayor probabilidad de irse.

# 🗂️ Dataset

El conjunto de datos incluye información sobre:

**Servicios**: Telefonía, múltiples líneas, internet, seguridad online, soporte técnico, streaming de TV y películas.

**Información del Cliente**: Antigüedad (meses), tipo de contrato, método de pago, facturación electrónica y cargos mensuales/totales.

**Target**: Fuga_Cliente (Variable binaria: Sí/No).

# 🛠️ Tecnologías Utilizadas
Lenguaje: Python 3.12

Librerías: * pandas & numpy (Manipulación de datos)

seaborn & matplotlib (Visualización)

scikit-learn (Machine Learning)

imblearn (SMOTE para balanceo de clases)

# 🚀 Pipeline del Proyecto. 
**Preparación y Limpieza**

Eliminación de identificadores irrelevantes (customerID).
Codificación de variables categóricas mediante One-Hot Encoding.
Tratamiento de valores nulos y filtrado de ruido (correlaciones $< 0.05$).

**Balanceo de Datos**
Dado que la mayoría de los clientes no cancelan, se utilizó SMOTE (Synthetic Minority Over-sampling Technique) para equilibrar las clases y evitar sesgos en el modelo.

**Modelado y Evaluación**
Se entrenaron y compararon múltiples modelos:

Regresión Logística: (Con normalización) Para análisis de coeficientes lineales.

Random Forest: (Sin normalización) Para capturar relaciones no lineales complejas.

SVM & KNN: Para análisis de fronteras de decisión y vecindad.

# 📈 Resultados y Modelos
El modelo final seleccionado fue Random Forest debido a su robustez y equilibrio en las métricas.

Matriz de Confusión: El modelo de Random Forest demostró una alta capacidad para minimizar los Falsos Negativos, asegurando que se identifiquen a la mayoría de los clientes en riesgo real de fuga.

# 💡 Conclusiones y Estrategia
El análisis de Importancia de Variables (Gini Importance) reveló que:

Tipo de contrato: Los contratos mes a mes son el mayor predictor de fuga.

Antigüedad: Los primeros 6 meses son críticos para la retención.

Cargos mensuales: Clientes con facturas elevadas sin servicios de soporte técnico tienden a retirarse más rápido.

**Estrategias Propuestas:**

Campañas de migración de contratos mensuales a anuales mediante incentivos.

Programas de bienvenida  para clientes nuevos (0-6 meses).

Revisión técnica y comercial del servicio de Fibra Óptica.

# 📂 Estructura del Repositorio
Telecom_X_2.ipynb: Cuaderno Jupyter con todo el procedimiento técnico.

datos_tratados.csv: Dataset procesado utilizado para el entrenamiento.

README.md: Documentación del proyecto.

# 🛠️ Soporte Técnico y Contacto

Si tienes alguna duda sobre la implementación, encuentras algún error en el código o deseas colaborar en una mejora del modelo, no dudes en ponerte en contacto:

Correo Electrónico:joseyansiercarovarona@gmail.com

