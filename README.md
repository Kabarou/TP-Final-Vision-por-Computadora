# TP Final Vision por Computadora: Buscador/Clasificador de Razas de Perro
Este proyecto implementa un sistema de Búsqueda Visual y Clasificación de 70 razas de perros utilizando la Transferencia de Aprendizaje (ResNet50 / ResNet18) y la Base de Datos Vectorial FAISS para la similitud. La aplicación final se ejecuta en Gradio.

## 1.1. Crear Entorno Virtual (Recomendado)
Abre la terminal de Visual Studio Code y ejecuta los siguientes comandos para crear y activar un entorno virtual, aislando las dependencias del proyecto:

### Crear el entorno (llamado 'venv')
python -m venv venv

### Activar el entorno (Linux/macOS)
source venv/bin/activate

### Activar el entorno (Windows - PowerShell)
.\venv\Scripts\activate


## 1.2. Versión de Python
Este proyecto fue desarrollado y probado con Python 3.10 o superior. Asegúrate de que tu entorno virtual esté configurado con una versión compatible.


## 1.3. Instalación de Dependencias
Instala todas las librerías necesarias (PyTorch, TensorFlow, FAISS, Gradio, etc.) utilizando el archivo requirements.txt:
pip install -r requirements.txt


# Ejecución del código
Las celdas a ejecutar solo serán las de preprocesamiento y las celdas que traen los embeddings del drive. Ya que dentro del drive estan los pesos y embeddings de los modelos entrenados.


# Aplicacion Gradio: Modos de Operación
Para poder probar la aplicación se debe tomar una imagen de un perro, ya sea sacada de internet o de donde sea, y posteriormente clickear en la celda donde dice "Haga click para Cargar" o "Coloque la Imágen aquí". 
La aplicación es unificada y ofrece tres modos seleccionables:

## ResNet50
Muestra la Imagen de Entrada y las 10 imágenes más parecidas del dataset (vecinos). El reporte incluye la raza más probable por voto mayoritario y las distancias FAISS.

## ResNet18
Muestra la Imagen de Entrada. El reporte solo indica la Raza Predicha y su Nivel de Confianza (predicción Top-1).

## Modelo Custom
Muestra la Imagen de Entrada. El reporte solo indica la Raza Predicha y su Nivel de Confianza (predicción Top-1).