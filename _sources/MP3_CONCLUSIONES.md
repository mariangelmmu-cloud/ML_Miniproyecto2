# ***Conclusiones***

## Predicción de la variable `price`: 

### Tabla comparativa de métricas

| Modelo            | MAE Entrenamiento | MAE Test | RMSE Entrenamiento | RMSE Test | R² Entrenamiento | R² Test |
|------------------|-------------------|----------|---------------------|-----------|------------------|---------|
| OLS (Regresión)  | 6315.12           | 6318.23  | 10160.54            | 10122.93  | 0.5626           | 0.5673  |
| Ridge            | 6335.13           | 6334.34  | 10265.28            | 10611.46  | 0.5588           | 0.5605  |
| Ridge (CV)       | 6335.13           | 6334.34  | 10265.28            | 10611.46  | 0.5588           | 0.5605  |
| Lasso            | 6313.41           | 6312.62  | 10161.21            | 10122.58  | 0.5626           | 0.5673  |
| Lasso (CV)       | 6313.49           | 6315.55  | 10161.21            | 10122.57  | 0.5627           | 0.5673  |

---

### Análisis y conclusiones

- **MAE** (Error Absoluto Medio): Todos los modelos tienen un MAE bastante similar, alrededor de 6300, lo que indica que en promedio se equivocan por esa cantidad al predecir.
- **RMSE** (Raíz del Error Cuadrático Medio): El modelo Ridge es el que tiene mayor RMSE, especialmente en el conjunto de prueba, lo que sugiere que puede estar cometiendo errores más grandes de forma más frecuente. En cambio, OLS y Lasso (con y sin validación cruzada) tienen los valores más bajos y estables.
- **R²** (Coeficiente de Determinación): El R² más alto lo obtienen OLS, Lasso y Lasso con validación cruzada, con valores cercanos a 0.567, lo que indica que explican un poco más del 56% de la varianza del precio. Ridge se queda ligeramente por debajo en este aspecto.

---

### ¿Cuál es el mejor modelo?

Después de revisar las métricas, el **mejor modelo** parece ser **Lasso con validación cruzada**. Tiene el MAE y el RMSE más bajos o muy similares al de OLS, pero con la ventaja de incluir regularización y validación cruzada, lo que lo hace más robusto frente a posibles problemas de sobreajuste y colinealidad.

Además, generaliza bien porque el rendimiento es casi igual en entrenamiento y prueba, lo que indica que no está sobreajustado y mantiene su rendimiento con nuevos datos. Aunque las diferencias entre los modelos no son enormes, Lasso (CV) ofrece un equilibrio sólido entre precisión y estabilidad.

---

# Predicción de la variable `high_demand`

### Tabla comparativa de métricas

| Métrica   | Regresión logística simple | Regresión logística con penalización (GridSearch) | Regresión lineal con penalización y validación cruzada |
|-----------|----------------------------|---------------------------------------------------|--------------------------------------------------------|
| Accuracy  | 0.86262                    | 0.86284                                           | 0.86350                                                |
| Precision | 0.86268                    | 0.86290                                           | 0.86356                                                |
| Recall    | 0.86262                    | 0.86284                                           | 0.86350                                                |
| F1-score  | 0.86261                    | 0.86284                                           | 0.86350                                                |

---

### Análisis y conclusiones

- **Regresión logística simple:**  
  Este modelo básico logra un desempeño razonable, con métricas alrededor de 0.86. No usa técnicas para evitar el sobreajuste, por lo que puede limitar su capacidad para generalizar.

- **Regresión logística con penalización L2 y GridSearch:**  
  La penalización y optimización de hiperparámetros mejoran ligeramente todas las métricas, mostrando un mejor ajuste y robustez frente a datos nuevos.

- **Regresión lineal con penalización y validación cruzada:**  
  Aunque menos común para clasificación, este modelo obtuvo el mejor desempeño general. La validación cruzada garantiza estabilidad y la penalización previene sobreajuste, resultando en métricas ligeramente superiores.

---

### ¿Cuál es el mejor modelo?

El modelo de **regresión lineal con penalización y validación cruzada** presenta el mejor rendimiento global según las métricas. Su combinación de penalización y validación cruzada logra un balance óptimo entre sesgo y varianza.

La **regresión logística con penalización y GridSearch** es una alternativa muy válida, especialmente si se prefiere un modelo probabilístico para clasificación.

La **regresión logística simple** funciona, pero queda atrás frente a los otros modelos más sofisticados.
