# Heart Disease Risk Prediction using Logistic Regression

## Resumen del Proyecto

Este proyecto implementa desde cero un modelo de regresión logística para predecir el riesgo de enfermedad cardíaca a partir de variables clínicas. El objetivo es desarrollar una solución reproducible, defendible y completamente manual, cumpliendo con las restricciones académicas y técnicas del curso. El flujo incluye análisis exploratorio, preprocesamiento, entrenamiento, evaluación, regularización, exportación y simulación de despliegue tipo SageMaker.

## Descripción del Dataset

- **Fuente:** Kaggle (Heart Disease Prediction)
- **Registros:** ~300 pacientes
- **Variables principales:** Edad, Sexo, Tipo de dolor torácico, Presión arterial, Colesterol, Frecuencia cardíaca máxima, Depresión ST, Número de vasos fluro, Diagnóstico (Presence/Absence)
- **Distribución de clases:** Balance moderado entre presencia y ausencia de enfermedad cardíaca

## Metodología

1. **EDA:** Estadísticas descriptivas, histogramas, boxplots, correlaciones y análisis crítico.
2. **Preprocesamiento:** Manejo de valores faltantes, normalización manual (z-score), binarización del target, selección de variables y división estratificada 70/30 sin sklearn.
3. **Implementación manual:** Todas las funciones clave (sigmoid, costo, gradiente, descenso de gradiente, predicción) están programadas desde cero usando numpy.
4. **Regularización L2:** Modificación matemática y comparación de diferentes valores de lambda, análisis de norma de pesos y selección óptima.
5. **Evaluación:** Cálculo manual de accuracy, precision, recall, F1 y matriz de confusión. Visualización de fronteras de decisión para ≥3 pares de variables.
6. **Exportación:** Guardado y carga de pesos y sesgo en archivos .npy, ejemplo funcional de predicción.
7. **Simulación SageMaker:** Endpoint local que recibe JSON, normaliza y devuelve probabilidad. Explicación de migración real a AWS.

## Resultados

- **Métricas principales:** Accuracy, precision, recall y F1-score calculados manualmente en train y test.
- **Visualización:** Fronteras de decisión claras y bien rotuladas, matriz de confusión, análisis gráfico de regularización.
- **Impacto:** El modelo es interpretable, reproducible y adecuado para aplicaciones clínicas básicas.

## Despliegue

- **Exportación:** Pesos y sesgo guardados en .npy, ejemplo de carga y predicción incluido.
- **Simulación SageMaker:** Endpoint funcional con entrada JSON y salida probabilística. Código portable a AWS.
- **Ejemplo de inferencia:** Se incluye en el notebook y en el script de inferencia.

## Evidencias

- Outputs y gráficos generados en el notebook.
- Ejemplo de predicción y exportación funcional.
- Referencia a imágenes y visualizaciones en el notebook.

## Reproducibilidad

- **Instalación:**
  - Ejecutar `%pip install numpy pandas matplotlib seaborn`
- **Ejecución:**
  - Abrir y ejecutar secuencialmente el notebook `heart_disease_lr_analysis.ipynb`
- **Requisitos:**
  - Python 3.8+, Jupyter Notebook/Lab o VS Code
  - Dataset `Heart_Disease_Prediction.csv` en la misma carpeta

## Conclusiones

- El modelo cumple con todas las restricciones y objetivos académicos.
- Es defendible ante jurado y reproducible en cualquier entorno compatible.
- Limitaciones: linealidad, tamaño de dataset, falta de validación cruzada.
- Trabajo futuro: modelos no lineales, validación cruzada, explicabilidad y despliegue real.
- Aplicaciones: soporte clínico, priorización de pacientes, integración en sistemas hospitalarios.

## Autor

- **Estudiante:** David Eduardo Salamanca Aguilar
- **Profesor:** Luis Daniel Benavides Navarro
- **Universidad:** Escuela Colombiana de Ingeniería Julio Garavito
