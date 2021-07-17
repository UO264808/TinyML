# TinyML

Recopilación de experimentos, arquitecturas y conjuntos de datos utilizados en el Trabajo Fin de Grado "<i>Optimización del consumo energético en redes neuronales </i>". Aparecen experimentaciones con diveros métodos de poda y cuantización, además de conversión de modelos mediante TensorFlow Lite.

## Organización 📋

  - Las arquitecturas se encuentran almacendadas en el directorio `models`. Está subdividido en directorios para cada modelo. Dentro de éstos se encuentra el Jupyter notebook en el que se creó y entrenó el modelo, así como éste almacenado en formato h5.
  - Los conjuntos de datos se pueden encontrar en `datasets`. Dado que sólo Imagenette fue el único descargado de forma manual, tanto CIFAR-10 como MNIST no aparecen aqui.
  - Los tres directorios restantes guardan las ejecuciones de los experimentos. Están dividos según el método de pruning utilizado, `APOZ`, `L1`, y `Random`. Dentro de ellos. Dentro de cada uno de los tres directorios se encuentran otros con el nombre de la siguiente manera: X_Y. Y es el porcentaje podado de la red en el experimento y X es el nombre de la red a la que se le aplica la poda. A su vez, dentro de estos directorios se encuentran guardados los modelos podados sólo, podados y en formato TFLite y podados, cuantizados y en formato TFLite, además de los Jupyter notebooks con la ejecución guardada de cada experimento.
  
## Dependencias 📦

En caso de necesitar volver a repetir alguna experimento será necesario instalar las siguientes dependencias haciendo uso de `pip`:
```
matplotlib 3.3.4
Keras 2.4.3
kerassurgeon 0.2.0
tensorflow 2.3.0
sklearn 0.0
h5py==2.10.0
pandas 1.1.5
zipp 3.4.1
numpy 1.18.5
folium0.2.1
imgaug0.2.6
```
<strong>* Resulta de suma importancia utilizar las versiones 2.3.0 de TensorFlow y 0.20 de Keras Surgeon. Si esto no es así fácilmente pueden surgir problemas de compatibilidad.</strong>

## Ejecución ⚙️

Para ejecutar los notebooks tan sólo tienen que ser abiertos bien en un IDE como Visual Code o PyCharm y conectando un kernel o bien lanzando la aplicación web de Jupyter desde terminal de la siguiente manera:
```
lucas@remote:~/Desktop/TinyML$ jupyter notebook
```

## Autoría y referencias ✒️

El diseño y desarrollo de los experimento ha sido propio. Sin embargo los métodos para la creación de los ranking de poda han sido tomados de un <a href=https://blog.dataiku.com/making-neural-networks-smaller-for-better-deployment-solving-the-size-problem-of-cnns-using-network-pruning-with-keras>artículo<a> de Vincent Houdebine y la librería para realizar la poda de la redes neuronales <a href=https://github.com/BenWhetton/keras-surgeon>Keras Surgeon</a> es obra de Ben Whetton.

  
  
