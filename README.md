# 📊 Telecom X - Predicción de Cancelación de Clientes (Churn)

Este proyecto corresponde a la **Parte 2 del Desafío Telecom X**, donde se construye un modelo predictivo para anticipar la cancelación de clientes (*churn*). A partir de los datos previamente limpiados y organizados en la Parte 1, se aplicaron técnicas de **preprocesamiento, análisis exploratorio, modelado y evaluación** de algoritmos de Machine Learning.

---

## 🎯 Objetivos
- Preparar los datos: limpieza, codificación de variables, eliminación de columnas irrelevantes y balanceo de clases.  
- Analizar la correlación y relación de variables clave con la cancelación.  
- Entrenar y evaluar al menos dos modelos predictivos distintos.  
- Interpretar la importancia de las variables más influyentes en la predicción de churn.  
- Proponer estrategias de retención basadas en los hallazgos.

---

## 🛠️ Tecnologías utilizadas
- **Python**  
- **Pandas & NumPy** → Manipulación de datos.  
- **Matplotlib & Seaborn** → Visualización.  
- **Scikit-Learn** → Modelado y métricas.  
- **Imbalanced-learn (SMOTE)** → Balanceo de clases.  

---

## 📂 Flujo de trabajo
1. **Carga de datos limpios** (archivo `datos_clientes_limpio.csv` de la Parte 1).  
2. **Preprocesamiento**:  
   - Eliminación de columnas irrelevantes como `customerID`.  
   - Codificación de variables categóricas (OneHotEncoder / get_dummies).  
   - Revisión del balance de clases y aplicación de SMOTE en caso necesario.  
3. **Análisis exploratorio**:  
   - Matriz de correlación entre variables numéricas.  
   - Relaciones dirigidas:  
     - Tipo de contrato × Cancelación.  
     - Total charges × Cancelación.  
4. **Modelado predictivo**:  
   - **Regresión Logística** (requiere normalización).  
   - **Random Forest** (no requiere normalización).  
   - División de los datos en entrenamiento y prueba (80/20).  
5. **Evaluación de los modelos**:  
   - Exactitud (Accuracy).  
   - Precisión.  
   - Recall.  
   - F1-score.  
   - Matriz de confusión.  
6. **Interpretación de variables**:  
   - Coeficientes en Regresión Logística.  
   - Importancia de variables en Random Forest.  

---

## 📊 Resultados principales
- **Mejor modelo:** Random Forest, con mayor balance entre *precision* y *recall*.  
- **Variables más influyentes en la cancelación:**  
  - Tipo de contrato (los clientes con contrato *month-to-month* son más propensos a cancelar).  
  - Método de pago (el uso de *electronic check* se asocia a mayor churn).  
  - Tenure (clientes con poco tiempo en la empresa tienen mayor riesgo).  
  - Monthly charges (cargos mensuales elevados aumentan la probabilidad de cancelación).  
  - Servicios adicionales como seguridad en línea y soporte técnico (su ausencia aumenta el churn).  

---

## 📝 Conclusiones y recomendaciones
El análisis muestra que la cancelación de clientes está principalmente influenciada por factores contractuales y de facturación.  
Se recomiendan las siguientes **estrategias de retención**:  
- Incentivar contratos a largo plazo mediante descuentos o beneficios.  
- Promover métodos de pago estables como débito automático o tarjeta de crédito.  
- Implementar programas de fidelización en los primeros meses de servicio.  
- Crear paquetes que incluyan servicios adicionales de valor (seguridad, soporte).  

---
