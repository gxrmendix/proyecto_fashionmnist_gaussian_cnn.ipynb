# Proyecto 2: Clasificación de Imágenes Fashion-MNIST aplicando Suavizado Gaussian

## Descripción del Proyecto

Este proyecto aplica un filtro de Suavizado Gaussian sobre el conjunto de datos Fashion-MNIST, seguido por la implementación de una red neuronal convolucional (CNN) para clasificar las imágenes de prendas de vestir en 10 categorías distintas.

El objetivo es demostrar el impacto positivo del suavizado en la eliminación de ruido y su efecto sobre el rendimiento de modelos de clasificación de imágenes.

## Estructura del Repositorio

```
Proyecto2_Filtros_CNN_FashionMNIST/
├── README.md
├── requirements.txt
├── proyecto_fashionmnist_gaussian_cnn.ipynb
```

## Instrucciones de Ejecución

1. Clonar el repositorio:
```bash
git clone https://github.com/tu_usuario/Proyecto2_Filtros_CNN_FashionMNIST.git
```

2. Instalar las dependencias:
```bash
pip install -r requirements.txt
```

3. Ejecutar el notebook `proyecto_fashionmnist_gaussian_cnn.ipynb` ubicado en la carpeta `notebook/`.

## Justificación del Uso de Suavizado Gaussian

Se aplicó un filtro de Suavizado Gaussian previo al entrenamiento para:

- Reducir el ruido de alta frecuencia presente en las imágenes.
- Mejorar la generalización del modelo CNN evitando el aprendizaje de patrones espurios.
- Enfatizar contornos suaves y formas relevantes, facilitando la tarea de clasificación.

El parámetro `sigma=1.0` fue elegido como un valor moderado que preserva detalles esenciales sin destruir la información estructural de las imágenes.

## Arquitectura del Modelo CNN

- **Conv2D**: 32 filtros (3x3), activación ReLU
- **MaxPooling2D**: 2x2
- **Conv2D**: 64 filtros (3x3), activación ReLU
- **MaxPooling2D**: 2x2
- **Flatten**
- **Dense**: 128 unidades, ReLU
- **Dropout**: 0.5 (regularización)
- **Dense**: 10 unidades de salida (Softmax)

Optimizado utilizando **Adam** con `learning_rate=0.001`.

## Resultados Principales

- La red CNN entrenada logra una precisión elevada en el conjunto de prueba.
- La aplicación de suavizado contribuye a una mejor convergencia del modelo y a una reducción del overfitting.
- Las curvas de pérdida y precisión muestran un comportamiento estable y consistente.

## Dependencias Principales

- tensorflow
- keras
- numpy
- pandas
- matplotlib
- scipy

## Autor

- **Nombre:** Victor A. Garmendia Fuentes
- **Curso:** Deep Learning
- **Fecha:** Abril 2025

---

Este repositorio forma parte del proyecto de entrega del curso de Deep Learning.
