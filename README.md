
# Visualizador de Búsqueda Algorítmica

Este repositorio contiene una aplicación web interactiva desarrollada para la visualización, análisis y comprensión del funcionamiento de algoritmos clásicos de búsqueda en grafos. La herramienta se ejecuta íntegramente a través de un único archivo HTML, lo que facilita su despliegue y uso sin necesidad de configuración ni entornos de servidor.

**[Demostración funcional en línea](https://josearosano.github.io/BusquedaAlgoritmica/)**

## Funcionalidades Principales

*   **Algoritmos Implementados:** 
    *   Búsqueda en Anchura (BFS - Breadth-First Search).
    *   Búsqueda en Profundidad (DFS - Depth-First Search).
    *   Búsqueda de Coste Uniforme (UCS - Uniform Cost Search).
*   **Edición Interactiva del Entorno:** Interfaz que permite al usuario modificar la topología de la cuadrícula, insertando obstáculos mediante clics y reubicando los nodos de Inicio y Meta a través de acciones de arrastrar y soltar (drag and drop).
*   **Configuración Dinámica de Costes:** Sistema de priorización de movimientos (Arriba, Abajo, Izquierda, Derecha) mediante el reordenamiento de filas en la interfaz. Permite además el ajuste manual del coste numérico de cada transición para evaluar su impacto directo en el algoritmo UCS.
*   **Control de Ejecución:** Motor de simulación iterativo que soporta la navegación paso a paso por el historial de búsqueda, así como una reproducción automatizada con velocidad de renderizado ajustable.
*   **Monitorización y Analítica:** Visualización en tiempo real de métricas de rendimiento, incluyendo la longitud y coste de la solución, iteraciones, nodos expandidos, tamaño máximo de la lista abierta y un registro detallado del historial de acciones del algoritmo.

## Instrucciones de Uso

El proyecto está diseñado para ser funcional de manera independiente, sin requerir instalación de dependencias ni procesos de compilación.

1.  Descargue el archivo `index.html` del repositorio.
2.  Ábralo en cualquier navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari).
3.  Utilice el panel de control lateral para configurar el entorno, seleccionar el algoritmo deseado y ejecutar la simulación.

## Tecnologías Utilizadas

*   **HTML5 y CSS3:** Estructuración semántica y diseño base de la interfaz.
*   **JavaScript (Vanilla):** Implementación de la máquina de estados, el modelo de datos de los algoritmos de búsqueda, la gestión de eventos del usuario y el motor de renderizado gráfico.
*   **Tailwind CSS (vía CDN):** Sistema de utilidades CSS empleado para estructurar un diseño responsivo y una interfaz gráfica moderna.

## Consideraciones Técnicas

El motor de búsqueda implementa una lógica de Búsqueda en Grafos (Graph Search) estricta, diseñada para reflejar el comportamiento teórico de los algoritmos de inteligencia artificial clásica:

*   **Tratamiento de estados repetidos:** El sistema mantiene un registro de nodos cerrados. No se re-evalúan ni contabilizan como nuevas iteraciones aquellos nodos que ya han sido expandidos previamente.
*   **Orden de evaluación e inserción:** En situaciones de empate de costes (o durante la ejecución de algoritmos no informados como BFS y DFS), el orden de evaluación configurado por el usuario en el panel lateral determina la secuencia exacta en la que los nodos adyacentes son generados e insertados en la lista abierta (frontera).
---

Desarrollado para explorar la inteligencia artificial clásica y el diseño de algoritmos interactivos.

