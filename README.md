Clasificación de Fashion-MNIST con Perceptrón Multicapa (MLP)
Este repositorio contiene un análisis exhaustivo de 10 experimentos de redes neuronales para clasificar imágenes de prendas de vestir utilizando el dataset Fashion-MNIST.

 Descripción del Problema
El objetivo es clasificar imágenes de 28x28 píxeles en 10 categorías distintas. Se abordó el problema utilizando una arquitectura de Perceptrón Multicapa (MLP), explorando diversas técnicas de regularización y optimización para maximizar la capacidad de generalización del modelo.

Evolución de Experimentos
A lo largo del proyecto se implementaron las siguientes mejoras:

Modelo Base: Uso de SGD y 150 épocas (Overfitting evidente).
Regularización: Incorporación de Dropout (30% y 20%) para reducir la memorización de ruido.
Optimización Adaptativa: Transición de SGD a Adam para una convergencia más veloz.
Estabilización: Implementación de Batch Normalization para normalizar activaciones intermedias.
Ajuste Fino: Reducción del Learning Rate a 0.0005 y del Batch Size a 64.
Control de Entrenamiento: Uso de Early Stopping (manual a 35 épocas) para capturar el punto óptimo de pesos.
 Resultados Clave
Modelo	Val Accuracy	Val Loss	Observación
Exp 1: Base (SGD)	88.0%	0.42	Convergencia lenta.
Exp 7: Optimizado	89.5%	0.32	Modelo más estable y equilibrado.
Exp 3: Adam Base	90.3%	0.40	Alta precisión pero inestable.
Modelo Seleccionado: El Experimento 7 fue elegido como la mejor solución. Aunque no alcanzó el pico máximo de precisión absoluto, demostró la curva de aprendizaje más sana y la menor pérdida (loss) en validación, mitigando eficazmente el sobreajuste.

 Requisitos e Instalación
Python 3.x
TensorFlow / Keras
NumPy / Pandas
Matplotlib / Seaborn
 Conclusiones y Trabajo Futuro
Se identificó que el modelo MLP encuentra un límite natural cerca del 90% de precisión, especialmente con la categoría 'Camisa' (Shirt). Como siguiente paso, se recomienda la implementación de Redes Neuronales Convolucionales (CNN) para extraer características espaciales y superar este plateau de rendimiento.
