# 🌀 Diffusion Model - Imagen desde Ruido

Este proyecto implementa un modelo generativo **desde cero** basado en **modelos de difusión (Diffusion Models)**, específicamente del tipo **DDPM (Denoising Diffusion Probabilistic Models)**, utilizando el conjunto de datos **Stanford Cars**. El objetivo es generar imágenes realistas a partir de ruido blanco, entrenando un modelo con arquitectura tipo **U-Net**.

## 🧠 Conceptos Clave

- **Forward Process**: Agrega ruido gaussiano a las imágenes de forma progresiva.
- **Reverse Process**: Utiliza una red U-Net para revertir el ruido y recuperar imágenes realistas.
- **DDPM**: Modelo probabilístico que aprende a denoising imágenes a través de múltiples pasos.
- **FID (Fréchet Inception Distance)**: Se utiliza como métrica de evaluación de calidad.

## 📁 Estructura del Proyecto

- `01_diffusion_model.ipynb`: Notebook principal con toda la implementación del modelo desde el preprocesamiento hasta la evaluación.
- Imágenes generadas durante el entrenamiento.
- Métricas registradas como FID y muestras visuales por épocas.

## 🚀 Requisitos

Asegúrate de tener instalado Python 3.8 o superior y las siguientes dependencias:

```bash
pip install torch torchvision matplotlib tqdm
```

Además, se recomienda tener soporte CUDA si se desea acelerar el entrenamiento con GPU.

## 🏁 Cómo ejecutar

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git
   cd tu_repositorio
   ```

2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

3. Abre el notebook en Jupyter o VSCode:
   ```bash
   jupyter notebook 01_diffusion_model.ipynb
   ```

## 📊 Resultados

- El modelo alcanza un FID aproximado de **140** tras 100 épocas.
- Se observa una mejora progresiva en la generación de imágenes.
- Las imágenes muestran buena aproximación al dataset incluso con pocos datos.

Ejemplo de imágenes generadas:

![sample](https://github.com/Sebastian-Cepeda-Ch/SIS421-2025-ASCC/blob/main/Final/Sample.png)

## 📚 Dataset

Se utilizó el dataset **[Stanford Cars](https://ai.stanford.edu/~jkrause/cars/car_dataset.html)**, que contiene imágenes de diferentes modelos de autos etiquetadas por clase.

## 🤝 Créditos

- Implementación inspirada en el paper original de DDPM (Ho et al., 2020).
- Dataset provisto por Stanford AI Lab.