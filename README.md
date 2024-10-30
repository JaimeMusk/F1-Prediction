F1 Final Position Predictor
Proyecto desarrollado por Jaime Ortueta en el contexto de Data Science para predecir la posición final de un piloto en la temporada de Fórmula 1 2024. Este proyecto aplica técnicas avanzadas de Machine Learning, desde la definición del problema hasta el despliegue de la aplicación en Docker con Gradio, proporcionando una herramienta interactiva y predictiva en el mundo de la Fórmula 1.

Descripción del Proyecto
La idea central del proyecto fue construir un modelo capaz de predecir la posición final de un piloto en el campeonato basado en datos históricos de rendimiento. El modelo final, implementado con Random Forest Regressor, se seleccionó después de evaluar varias opciones de algoritmos y técnicas de optimización de hiperparámetros.

Estructura del Proyecto
Este repositorio está organizado de la siguiente manera:

notebooks/: Contiene los Jupyter Notebooks (.ipynb) utilizados para la exploración, pruebas y experimentos con diferentes modelos.
data/: Contiene los archivos de datos (CSV, parquet, sqlite, etc.) que fueron utilizados para el procesamiento y entrenamiento del modelo.
app/: Contiene los archivos necesarios para el despliegue de la aplicación.
new_app.py: Código principal de la aplicación utilizando Gradio para la interfaz.
Dockerfile: Archivo Docker para configurar el entorno de despliegue.
models/: Archivos de modelos entrenados y otros recursos de Machine Learning.
modelo_entrenado.pkl: Modelo final en formato pickle para su uso en la aplicación.
README.md: Documentación del proyecto con información detallada sobre los archivos y el propósito de cada uno.
Instalación
Para ejecutar este proyecto en tu máquina local, sigue estos pasos:

Clonar el repositorio:

bash
Copy code
git clone https://github.com/JaimeMusk/F1Prediction.git
cd F1Prediction
Construir la imagen de Docker (opcional, si deseas ejecutar en un contenedor):

bash
Copy code
docker build -t f1-predictor .
Ejecutar la aplicación: Para lanzar la aplicación localmente:

bash
Copy code
python3 app/new_app.py
O si prefieres ejecutarla en Docker:

bash
Copy code
docker run -p 7860:7860 f1-predictor
Uso de la Aplicación
La aplicación está diseñada para proporcionar predicciones basadas en el nombre del piloto seleccionado. Los datos de entrada, como puntos, posición promedio y cantidad de DNF (Did Not Finish), se utilizan para calcular una predicción de la posición final.

Interfaz de usuario: La aplicación está construida con Gradio, ofreciendo una interfaz fácil de usar para seleccionar un piloto y obtener una predicción inmediata.
Contribuciones
Las contribuciones son bienvenidas. Para contribuir:

Haz un fork del repositorio.
Crea una rama para tu funcionalidad (git checkout -b nueva-funcionalidad).
Haz commit de tus cambios (git commit -m 'Añadir nueva funcionalidad').
Haz push a la rama (git push origin nueva-funcionalidad).
Abre un Pull Request.
