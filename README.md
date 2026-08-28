# Órbitas de Kepler: Métodos Numéricos para EDOs

## Descripción del Proyecto

Este repositorio contiene el desarrollo e implementación en Python de métodos numéricos para la resolución de Ecuaciones Diferenciales Ordinarias (EDOs) de primer orden con condiciones iniciales.

El objetivo principal de este trabajo es realizar un estudio comparativo escalar respecto a la precisión y rendimiento de distintos esquemas numéricos (método de Euler y Runge-Kutta de cuarto orden), tomando como referencia la solución analítica exacta de las ecuaciones. Este análisis constituye la fase preliminar antes de adaptar los algoritmos a funciones vectoriales para la simulación del problema de las órbitas de Kepler.

## Contenido y Métodos Implementados

### 1. Solución Analítica de Referencia
* **Módulo `EDO(f, x0, y0)`**: Emplea la librería de cálculo simbólico SymPy (`sp.dsolve`) para resolver analíticamente la ecuación diferencial con sus condiciones iniciales. Permite obtener el valor exacto de referencia para evaluar los errores cometidos por los métodos numéricos.

### 2. Método de Euler
* **Módulo `Euler(f, x0, y0, n, xf)`**: Método explícito de primer orden que aproxima la solución en un intervalo dividiendo este en $n$ particiones de tamaño de paso $h = \frac{x_f - x_0}{n}$.
* **Módulo `error_Euler(f, x0, y0, n, xf)`**: Calcula el error relativo porcentual en el punto final del intervalo respecto a la solución analítica exacta.

### 3. Método de Runge-Kutta de Cuarto Orden (RK4)
* **Módulo `RK4(f, x0, y0, xf)`**: Esquema numérico de mayor precisión que evalúa cuatro pendientes intermedias ($k_1, k_2, k_3, k_4$) para aproximar el valor de la función en el extremo del intervalo.
* **Módulo `error_RK4(f, x0, y0, xf)`**: Calcula el error relativo porcentual del método RK4 frente a la solución analítica exacta.

### 4. Comparación de Rendimiento y Análisis
* Evaluación comparativa de la convergencia del error porcentual frente al número de subintervalos o particiones ($n$).
* Representación gráfica de la variación del error utilizando la biblioteca Matplotlib.
