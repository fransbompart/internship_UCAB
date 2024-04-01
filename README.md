# 🤖 Prototipo para la Estimación de Tiempo en Proyectos de Desarrollo de Software

## 🧱 Estructura del Repositorio

El repositorio está organizado en varias ramas, cada una con un enfoque diferente:

- `effort-VS-time-with-cv`: Predicción de tiempo a partir del esfuerzo estimado, con validación cruzada (cv) aplicada durante el entrenamiento.
- `effort-VS-time`: Similar a la rama anterior, pero sin validación cruzada.
- `story-points-VS-time`: Predicción de tiempo a partir de un puntaje (story point) asignado a la tarea.
- `task-summary-VS-story-point`: Predicción del story point de cada tarea a partir de su descripción.

## 📁 Contenido de las Carpetas

Se describe a continuación la estructura de carpetas que se encuentra en todas las ramas, salvo por `effort-VS-time-with-cv` y `task-summary-VS-story-point` que tienen cierta variación.

- `datasets`: Contiene los archivos CSV que alimentan a los modelos inteligentes.
- `scripts`: Además del script a ejecutar, contiene las subcarpetas: 
  - `checkpoint-logs`: Se guarda el modelo de red neuronal con mejor configuracion de pesos, es decir, aquel con el mejor rendimiento durante el entrenamiento. Con este archivo y la estructura original de la red es posible su reutilización.
  - `logs`: Archivos de registro tanto para el entrenamiento como para la validación de las redes neuronales, con información sobre diferentes métricas y otros datos que se pueden visualizar en TensorBoard.
  - `outputs`: Salidas generadas por los modelos, desde el archivo de las predicciones, hasta graficas e históricos del entrenamiento, subdividiendose en dos carpetas para los modelos de red neuronal o para el de máquina vector soporte.

## 🛠️ Configuración del Ambiente y Ejecución de los Scripts

### 📍 Local

Se deben tener instaladas las siguientes dependencias:

**Ejemplo de instalación con pip:**

```bash
pip install tensorflow tensorflow-docs scikit-learn numpy matplotlib pandas seaborn ipython netron jupyter
```

*Recomendaciones:*

- Utilizar la version de Python 3.10 
- Crear un entorno virtual separado al ejecutar la rama task-summary-VS-story-point.

Ahora solo queda ejecutar el script!!

### 🌐 Google Colabs

Las predicciones realizadas en los scripts de cada rama se encuentras en los siguientes links, respectivamente:

- [Effort VS Time With Cross Validation](https://drive.google.com/drive/folders/19X_rnEb8TdPJuv0N_sSehg288dg3DAMt?usp=sharing)
- [Effort VS Time](https://drive.google.com/drive/folders/1Z8taga127X20pTZHVVso3ITMb10R5M0f?usp=sharing)
- [Story Points VS Time](https://drive.google.com/drive/folders/1Ppl3eTVuuAzpmHuF01eMztVb2RRIYLS9?usp=sharing)
- [Task Summary VS Story Points](https://drive.google.com/drive/folders/1MX-GuIW6LXinYrcD6cGdivK3Dt8FeUVG?usp=sharing)

Antes de ejecutar alguno es importante subir a la carpeta de archivos de Google Colabs el dataset correspondiente de la siguiente manera:

<div align=center">
  <img src="images\google_colabs_paso_1.png" width="200" />
  <img src="images\google_colabs_paso_2.png" width="200" />
  <img src="images\google_colabs_paso_3.png" width="200" /> 
</div>
<div align=center">
  <img src="images\google_colabs_paso_4.png" width="200" />
  <img src="images\google_colabs_paso_5.png" width="200" />
</div>

<div align=center">Replicar exactamente la carpeta en función de la ubicada en el drive</div>

## 📊 Reportes 

Evaluación de los modelos effort VS time

- [Multi-Layer Perceptron 1](https://app.powerbi.com/links/dz_jyXoizD?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)
- [Multi-Layer Perceptron 2](https://app.powerbi.com/links/CS6ecbGh-v?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)
- [Long-Short Term Memory](https://app.powerbi.com/links/bmGwUg0Jyu?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)
- [Support Vector Machine Regressor](https://app.powerbi.com/links/rjXsEAipse?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)

Evaluación de los modelos story points VS time

- [Multi-Layer Perceptron 1](https://app.powerbi.com/links/HbRokr34i5?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)
- [Multi-Layer Perceptron 2](https://app.powerbi.com/links/rE_HXh-ZRo?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)
- [Long-Short Term Memory](https://app.powerbi.com/links/0owvGJy-uE?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)

Evaluación del modelo task summary VS story point 

- [BERT](https://app.powerbi.com/links/RoLswGkbK0?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)

Preparación de ciertos datasets previo al entrenamiento de los modelos

- [Análisis del SiP Dataset](https://app.powerbi.com/links/GslWNkgMPl?ctid=29a18182-402d-4ca9-a51f-2a356c6efdb7&pbi_source=linkShare)

## 📝 Informe

Para comprender a mayor detalle el trabajo realizado se puede visualizar el [informe de la pasantía](https://docs.google.com/document/d/1HArcNjd5x_jXXRJAdH82Cfe7L1jQa6M1/edit?usp=sharing&ouid=105780322129878224469&rtpof=true&sd=true)
