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

Para ejecutar este proyecto localmente se deben instalar ciertas de dependencias

**Ejemplo de instalación con pip:**

```bash
pip install tensorflow tensorflow-docs scikit-learn numpy matplotlib pandas seaborn ipython netron jupyter

**Recomendaciones**:

- Utilizar la version de python 3.10 
- Crear un entorno virtual separado al ejecutar la rama `task-summary-VS-story-point`.

Con todo lo anterior instalado, ya se prodra ejecutar el script !!

### Google Colabs

## ¿Qué prosigue con la investigación?
