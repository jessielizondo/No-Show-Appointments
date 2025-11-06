# 🏥 No-Show Appointment Prediction
## 📊 Predicción de inasistencias a citas médicas con Machine Learning

Autora: Jessica Elizondo Treviño
Tecnologías: Python · Pandas · NumPy · Scikit-Learn · Matplotlib · Pipelines · ML Metrics

## 📌 1. Descripción del Proyecto

Las inasistencias a citas médicas (no-show appointments) representan un problema frecuente en centros de salud:
➡️ tiempo perdido
➡️ agendas saturadas
➡️ costos innecesarios
➡️ menor calidad del servicio

Este proyecto construye un modelo de Machine Learning para predecir si un paciente asistirá o no a su cita, optimizando la métrica F1 debido al desbalance entre clases.

El notebook realiza:

✅ limpieza de datos
✅ análisis exploratorio
✅ preprocesamiento con pipeline
✅ entrenamiento de múltiples modelos
✅ optimización de umbral
✅ evaluación final
✅ interpretación de variables

## 🎯 2. Objetivo del Proyecto

Desarrollar un modelo predictivo capaz de identificar pacientes con riesgo de no asistir a su cita médica para:

🔹 enviar recordatorios reforzados
🔹 hacer seguimiento telefónico
🔹 ajustar la programación de citas
🔹 optimizar la operación del centro de salud

## 🧩 3. Dataset Utilizado

El dataset contiene información sobre:

Fecha de agendado

Fecha de cita

Edad del paciente

Condiciones de salud

Recordatorio por SMS

Variable objetivo: no_show (1 = no asiste)

Además, se genera la variable derivada:

wait_days → diferencia entre cita y fecha de programación

## 🧹 4. Limpieza y Preprocesamiento

El notebook realiza:

✅ Conversión correcta de fechas
✅ Eliminación/corrección de edades inválidas
✅ Cálculo de wait_days
✅ Separación de variables numéricas y categóricas
✅ Imputación con SimpleImputer
✅ Escalado de numéricas con StandardScaler
✅ Codificación One-Hot de categóricas
✅ Creación de un ColumnTransformer
✅ Ensamblaje en un Pipeline profesional

## 🔎 5. Exploratory Data Analysis (EDA)

El EDA se realiza solo en los datos de entrenamiento para evitar fugas de información.

Incluye:

📊 Histogramas de edad
📊 Distribución de días de espera
📊 Tasa de no-show por SMS recibido
📊 Inspección básica del desbalance
📊 Relación preliminar de variables

## 🤖 6. Modelos Entrenados

Se evalúan varios modelos usando el mismo pipeline:

Modelo	Comentario
Logistic Regression	baseline interpretable
Random Forest	buen rendimiento con variables mixtas
Gradient Boosting	estable y poderoso

Se comparan con:

✅ ROC-AUC
✅ PR-AUC
✅ F1 Score
✅ Matriz de confusión

## 🎛 7. Optimización del Umbral

En lugar del umbral estándar 0.5, se utiliza la:

📈 Curva Precision–Recall

Para seleccionar el threshold que maximiza F1.
Esto es especialmente útil porque los no-show son una clase minoritaria.

## ✅ 8. Resultados Finales

El notebook calcula:

F1 Score optimizado

ROC-AUC

PR-AUC

Matriz de confusión

Reporte de clasificación

Importancia de características (si el modelo lo permite)

Generalmente, las variables más relevantes son:

⭐ wait_days
⭐ age
⭐ sms_received

## 📝 9. Conclusiones

El modelo predice no-shows con buena precisión usando algoritmos clásicos.

El ajuste del umbral mejora significativamente el desempeño.

La variable wait_days es clave en el comportamiento del paciente.

El pipeline garantiza reproducibilidad y elimina la fuga de datos.

Este tipo de sistema puede integrarse en clínicas y hospitales para mejorar la asistencia.

## 🚀 10. Líneas Futuras de Trabajo

🔹 Aplicar SMOTE para balanceo avanzado
🔹 Probar LightGBM y CatBoost
🔹 Calibrar probabilidades
🔹 Crear dashboard con Streamlit
🔹 Desplegar un servicio API para predicciones reales

🗂️ 11. Estructura del Repositorio
📁 no-show-prediction
│
├── no_show_project_enhanced.ipynb   # Notebook limpio y formateado
├── README.md                        # Este archivo 😄
└── data/                            # (opcional) dataset original

## ⚙️ 12. Cómo Ejecutarlo
1️⃣ Clona el repo:

git clone https://github.com/TU_USUARIO/no-show-prediction.git

2️⃣ Instala dependencias:

pip install pandas numpy scikit-learn matplotlib

3️⃣ Abre el notebook:

jupyter notebook no_show_appointments.ipynb



## 💬 12. Contacto

Jessica Elizondo Treviño
📧 jessicaelizondot@gmail.com

🔗 LinkedIn: https://www.linkedin.com/in/jessica-elizondo-t/
