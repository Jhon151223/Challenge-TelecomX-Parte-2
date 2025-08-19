# Challenge-TelecomX-Parte-2

Análisis Predictivo de Churn – Telecom X
Descripción del proyecto

Este proyecto tiene como objetivo predecir la cancelación de servicios (churn) de los clientes de Telecom X y proporcionar insights estratégicos para reducir la tasa de abandono.
Se emplearon técnicas de preprocesamiento de datos, análisis exploratorio y modelado predictivo usando Python y librerías de Machine Learning.

Estructura del proyecto

notebook/: Contiene el Jupyter Notebook con todo el flujo de análisis.

data/: Dataset original (telco_churn.csv).

README.md: Este archivo.

1️⃣ Limpieza y Preprocesamiento de Datos

Se eliminaron columnas irrelevantes para la predicción, como identificadores únicos (customerID).

Se transformaron las variables categóricas a formato numérico mediante one-hot encoding.

Se manejaron valores faltantes reemplazándolos por valores por defecto (No) o 0.

Se balancearon las clases usando SMOTE para evitar sesgo hacia la clase mayoritaria.

2️⃣ Análisis Exploratorio de Datos

Se exploraron las distribuciones de variables numéricas y categóricas frente al churn.

Se construyeron boxplots y scatterplots para visualizar patrones de cancelación según:

Tiempo de contrato (customer_tenure)

Gasto mensual y total (account_Charges.Monthly, account_Charges.Total)

Se observó un desbalance moderado entre clientes activos y cancelados.

3️⃣ Modelado Predictivo

Se entrenaron dos modelos principales:

Random Forest Classifier

No requiere normalización.

Mostró mayor exactitud y robustez frente a los datos balanceados.

Permite analizar la importancia de las variables directamente.

Regresión Logística

Requiere normalización de las variables.

Facilita la interpretación de los coeficientes y la influencia de cada variable en la probabilidad de churn.

4️⃣ Evaluación de Modelos

Se evaluó el desempeño de cada modelo usando las siguientes métricas:

Métrica	Random Forest	Regresión Logística
Exactitud	0.73	0.70
Precisión	0.72	0.68
Recall	0.71	0.66
F1-Score	0.71	0.67

Conclusión: Random Forest presentó mejor rendimiento y estabilidad.

Se observó que las variables más relevantes para predecir churn fueron: tiempo de contrato, tipo de contrato, gasto total y mensual, y servicios adicionales contratados.

5️⃣ Conclusiones y Recomendaciones

Factores clave que influyen en la cancelación:

Menor tiempo de permanencia en la empresa.

Contratos mensuales frente a contratos largos.

Servicios adicionales insuficientes (seguridad, soporte técnico, streaming).

Facturación y métodos de pago específicos.

Estrategias de retención:

Incentivos para clientes nuevos o de corta permanencia.

Mejorar y promocionar servicios adicionales.

Optimizar la experiencia de facturación y método de pago.

Implementar alertas tempranas de churn usando el modelo predictivo.

6️⃣ Tecnologías y Librerías

Python 3.11

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn (Random Forest, Regresión Logística, SMOTE)

7️⃣ Resultados

El proyecto permite:

Identificar clientes con mayor riesgo de cancelar.

Ofrecer estrategias personalizadas de retención.

Aumentar la capacidad de la empresa para anticiparse a la cancelación y reducir churn.
