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

# Generación de datos aleatorios para la gráfica de barras
ventas = [random.randint(10, 50) for _ in range(4)]
```
