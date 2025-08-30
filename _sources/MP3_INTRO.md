# ***Introducción al miniproyecto*** 

Este proyecto hace parte del curso de *Machine Learning* y tiene como objetivo poner en práctica modelos de regresión y clasificación como: `Ridge`, `Lasso` y `Regresión logística`.

## Autoría
* **Autoras:** Guirlessa De La Hoz y Mariangel Mercado.
* **Curso:** Machine Learning
* **Fecha:** Agosto 2025

## 1. Introducción a la Base de Datos

* **Nombre del dataset:** `vehicles.csv`
* **Número de instancias:** 426880 
* **Número de variables:** 26

### 1.1. Contexto del dataset

El mercado de autos usados es una parte fundamental del sector automotriz, especialmente en países como Estados Unidos, donde millones de personas compran y venden vehículos de segunda mano cada año. A diferencia de los autos nuevos, los usados ofrecen precios más accesibles y una mayor variedad de opciones, lo que los convierte en una alternativa atractiva para quienes buscan movilidad sin realizar una gran inversión inicial. Sin embargo, este mercado también presenta desafíos: el estado del vehículo, el historial de uso, el tipo de título legal, y el kilometraje son factores que influyen directamente en su valor y confiabilidad. Plataformas como Craigslist juegan un papel importante al permitir que vendedores particulares y concesionarios publiquen anuncios de forma directa, generando grandes volúmenes de datos que reflejan las tendencias, precios y características de los vehículos en venta en distintas regiones del país.

### 1.2. Objetivo

El objetivo principal de este proyecto es desarrollar modelos predictivos que permitan estimar el **precio de autos usados** y evaluar si un vehículo tendrá una **alta demanda** o no, en función de sus características. Para ello, se utilizan algoritmos de regresión regularizada, específicamente **Ridge** y **Lasso**, que ayudan a mejorar la precisión de las predicciones al reducir el sobreajuste y seleccionar las variables más relevantes. Paralelamente, se implementa un modelo de **regresión logística** para clasificar los vehículos según su probabilidad de ser altamente demandados, tomando como base variables como el año de fabricación, condición, kilometraje, tipo de combustible, entre otras. Este análisis permite entender qué factores influyen tanto en el valor de mercado como en la probabilidad de venta, brindando herramientas útiles para compradores, vendedores y plataformas de comercio de autos usados.

