# 🤖 Prototipo para la Estimación de Tiempo en Proyectos de Desarrollo de Software

Este repositorio contiene un prototipo para la estimación de tiempo en proyectos de desarrollo de software.

## 🧱 Estructura del Repositorio

El repositorio está organizado en varias ramas, cada una con un enfoque diferente:

- `effort-VS-time-with-cv`: Predicción de tiempo a partir del esfuerzo estimado, con validación cruzada (cv) aplicada durante el entrenamiento.
- `effort-VS-time`: Similar a la rama anterior, pero sin validación cruzada.
- `story-points-VS-time`: Predicción de tiempo a partir de un puntaje (story point) asignado a la tarea.
- `task-summary-VS-story-point`: Predicción del story point de cada tarea a partir de su descripción.

## 📁 Contenido de las Carpetas

El repositorio contiene las siguientes carpetas:

- `datasets`: Contiene los archivos CSV que alimentan a los modelos inteligentes.
- `scripts`: 
  - `checkpoint-logs`: Se guarda el modelo de red neuronal con mejor configuracion de pesos, es decir, aquel con el mejor rendimiento durante el entrenamiento. Con este archivo y la estructura original de la red es posible su reutilización.
  - `logs`: Archivos de registro tanto para el entrenamiento como para la validación de las redes neuronales, con información sobre diferentes métricas y otros datos que se pueden visualizar en TensorBoard.
  - `outputs`: Salidas generadas por los modelos, desde el archivo de las predicciones, hasta graficas e históricos del entrenamiento, subdividiendose en dos carpetas para los modelos de red neuronal o para el de máquina vector soporte.

## 🛠️ Configuración del Ambiente y Ejecución de los Scripts

### Local

Se deben tener instaladas las siguientes dependencias:

**Ejemplo de instalación con pip:**

```bash
pip install tensorflow tensorflow-docs scikit-learn numpy matplotlib pandas seaborn ipython netron jupyter
```

**Recomendaciones**:

- Utilizar la version de Python 3.10 
- Crear un entorno virtual separado al ejecutar la rama `task-summary-VS-story-point`.

Ahora solo queda ejecutar el script!!

### Google Colabs

Las predicciones realizadas en los scripts de cada rama se encuentras en los siguientes links, respectivamente:

- [Effort VS Time With Cross Validation](https://drive.google.com/drive/folders/19X_rnEb8TdPJuv0N_sSehg288dg3DAMt?usp=drive_link)
- [Effort VS Time](https://drive.google.com/drive/folders/1Z8taga127X20pTZHVVso3ITMb10R5M0f?usp=drive_link)
- [Story Points VS Time](https://drive.google.com/drive/folders/1Ppl3eTVuuAzpmHuF01eMztVb2RRIYLS9?usp=drive_link)
- [Task Summary VS Story Points](https://drive.google.com/drive/folders/1MX-GuIW6LXinYrcD6cGdivK3Dt8FeUVG?usp=drive_link)

Antes de ejecutar alguno es importante subir a la carpeta de archivos de Google Colabs el dataset correspondiente de la siguiente manera

<p float="left">
  <img src="images\google_colabs_paso_1.png" width="100" />
  <img src="images\google_colabs_paso_2.png" width="100" /> 
  <img src="images\google_colabs_paso_3.png" width="100" />
  <img src="images\google_colabs_paso_4.png" width="100" />
</p>

**Colocar el nombre de la carpeta exactamente como se indica en la imagen 3**

## ¿Qué prosigue con la investigación?
