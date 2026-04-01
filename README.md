# Unidad-2 Componentes y Lirerias
## 2.1 Definición conceptual de componentes,paquetes / librerías.
En el contexto de nuestro proyecto de Dashboard:


* Componente: Cada elemento individual de la interfaz (los contenedores de gráficas, los botones y los textos). Por ejemplo, un ft.Container es un componente visual que encapsula una gráfica.

* Paquete / Librería: Conjuntos de funciones externas que extendieron las capacidades de nuestro código base. En este caso, utilizamos flet para la interfaz, matplotlib para la generación de gráficos y flet_charts como puente entre ambos.
## 2.2 Uso de librerías proporcionadas por el lenguaje
El lenguaje Python incluye librerías estándar que facilitan tareas comunes. En este proyecto, utilizamos la librería random, la cual viene preinstalada con Python, para simular datos dinámicos en las gráficas.
* Ejemplo de uso en el proyecto:
  ``` python
  import random # Librería estándar del lenguaje
  #Generación de datos aleatorios para la gráfica de barras
  ventas = [random.randint(10, 50)for _ in range(4)]
  ```
 ## 2.3 Creación de componentes (visuales y no visuales) definidos por el usuario
  Un componente definido por el usuario es una función o clase que agrupa lógica específica. En nuestro Dashboard:

 1. Componentes No Visuales: Las funciones generar_grafica_barras(), generar_grafica_lineas(), etc., actúan como componentes lógicos que procesan datos y retornan un objeto de figura.

2. Componentes Visuales: La configuración de los ft.Container (con sus bordes, radios y paddings) define la estética de los componentes visuales personalizados del tablero.
* Ejemplo de componente lógico (No Visual):
``` python
def generar_grafica_pastel():
    # Lógica encapsulada para crear un objeto específico (Pie Chart)
    fig, ax = plt.subplots(figsize=(3, 2.5))
    ax.pie(valores, labels=categorias, autopct="%1.1f%%", colors=colores)
    return fig
```
## 2.4 Creación y uso de paquetes/librerías definidas por el usuario
Para escalar este proyecto, el código se organiza de manera que las funciones de graficación podrían moverse a un archivo externo (ej. graficas.py), convirtiéndose en un paquete local reutilizable por otros módulos de la aplicación.
## Bibliografía (Formato APA)
* Flet Dev. (2024). Flet Controls: Matplotlib Chart. Recuperado de https://flet.dev/docs/controls/matplotlib-chart/

* Hunter, J. D. (2007). Matplotlib: A 2D Graphics Environment. Computing in Science & Engineering, 9(3), 90-95.

* Python Software Foundation. (2024). random — Generate pseudo-random numbers. Recuperado de https://docs.python.org/3/library/random.html

* Sommerville, I. (2011). Software Engineering (9th ed.). Addison-Wesley.
