#  Scene Classification with Deep Learning

Este proyecto aborda el problema de **clasificación de imágenes de escenas naturales** provenientes de distintas regiones del mundo.  
El objetivo es construir y comparar distintos modelos de **Deep Learning** capaces de asignar cada imagen a una de las **seis categorías predefinidas**.

---

##  Objetivos

- Entrenar y evaluar modelos de clasificación de imágenes utilizando distintas arquitecturas:
  - Redes Neuronales Densas (Fully Connected Networks)
  - Redes Neuronales Convolucionales (CNN)
  - Arquitecturas basadas en **ResNet**
  - Modelos con **Transfer Learning** (EfficientNetB0)
- Comparar el desempeño de cada enfoque según su precisión en el conjunto de validación/test.
- Analizar los resultados y observar la generalización de los modelos ante escenas similares.

---

##  Modelos Implementados

1. **Red Densa**
   - Arquitectura simple con capas `Dense` y `Dropout`.
   - Sirve como punto de partida para comparar el efecto de las convoluciones.

2. **CNN**
   - Varias capas `Conv2D`, `MaxPooling` y `Dropout`.
   - Entrenamiento completo con `data augmentation`.

3. **ResNet**
   - Implementación modular con bloques residuales (`Conv2D` + conexiones de salto).
   - Mejora la propagación del gradiente en redes profundas.

4. **Transfer Learning**
   - Uso de una red preentrenada (**EfficientNetB0**).
   - Fase 1: capas base congeladas.
   - Fase 2: fine-tuning parcial para ajustar pesos.

---

##  Dataset

El conjunto de datos proviene de un repositorio y contiene imágenes de **seis clases de escenas naturales**.

> Las imágenes no están incluidas en este repositorio.  

---

##  Tecnologías Utilizadas

- **Python**
- **TensorFlow / Keras**
- **NumPy, Pandas**
- **Matplotlib, Seaborn**
- **scikit-learn**

---

##  Resultados

- Se evaluó cada modelo mediante su **accuracy** en el conjunto de prueba.
- Los modelos basados en **Transfer Learning** mostraron el mejor rendimiento y generalización. Test Accuracy: 0.9287.
- Se observaron errores lógicos entre clases visualmente similares (por ejemplo, *buildings* vs *street*).


---
