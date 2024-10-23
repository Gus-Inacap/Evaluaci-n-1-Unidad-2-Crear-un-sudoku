# Sudoku Solver: Algoritmos para Resolver Sudoku

Este proyecto implementa cuatro algoritmos para la resolución de **Sudoku** y proporciona un análisis detallado de su rendimiento en distintos entornos. Cada algoritmo se evalúa en función de su eficiencia temporal y complejidad, tomando como referencia fuentes académicas reconocidas.

---

## **Tabla de Contenidos**
- [Introducción](#introducción)
- [Descripción de los Algoritmos](#descripción-de-los-algoritmos)
- [Tiempos de Ejecución](#tiempos-de-ejecución)
- [Conclusiones](#conclusiones)
- [Referencias](#referencias)

---

## **Introducción**

El **Sudoku** es un problema que ha captado la atención tanto de matemáticos como de desarrolladores de software, debido a su estructura combinatoria y su complejidad creciente en función del tamaño del tablero y de las celdas vacías (Russell & Norvig, 2020). Resolverlo de forma automática implica aplicar algoritmos de búsqueda y optimización, que se comparan en este proyecto mediante cuatro enfoques: **Backtracking**, **Hill Climbing**, **A\*** y **Búsqueda Aleatoria**.

---

## **Descripción de los Algoritmos**

## 1. Backtracking

El **algoritmo de backtracking** (o retroceso) es un enfoque clásico basado en fuerza bruta, ampliamente utilizado para problemas de búsqueda combinatoria (Russell & Norvig, 2020). En este algoritmo, se intentan todas las posibilidades secuencialmente hasta encontrar una solución válida, retrocediendo en caso de que una opción no funcione. Su eficiencia depende significativamente del tamaño del tablero y de la posición de las celdas vacías.

**Ventajas:**
- Es completo y siempre encontrará una solución si existe.
- Sencillo de implementar y entender.

**Desventajas:**
- Su rendimiento disminuye rápidamente con problemas de gran escala debido a su complejidad \(O(b^d)\), donde \(b\) es el número de opciones por nodo y \(d\) es la profundidad del árbol de búsqueda (Cormen et al., 2009).

**Análisis de rendimiento:**
- En Colab: 0.0042 segundos.
- En Jupyter Notebook: 0.0955 segundos.
- En ejecución directa en terminal: 0.0242 segundos.

El rendimiento de este algoritmo varía sustancialmente entre entornos, mostrando mejor desempeño en plataformas optimizadas como Colab.

---

## 2. Hill Climbing (Ascenso de Colinas)

El **algoritmo de Hill Climbing** pertenece a la categoría de algoritmos de optimización local, donde se busca mejorar una solución iterativamente hasta llegar a un máximo local (Russell & Norvig, 2020). El objetivo es minimizar los conflictos en el tablero del Sudoku hasta encontrar una configuración válida.

**Ventajas:**
- Puede ser más rápido que backtracking, especialmente en problemas donde la búsqueda completa no es factible.
- Requiere menos memoria.

**Desventajas:**
- Tiende a quedarse atrapado en máximos locales, lo que puede impedir alcanzar la solución global.
- Su éxito depende de la calidad de la solución inicial aleatoria.

**Análisis de rendimiento:**
- En Colab: 0.0153 segundos.
- En Jupyter Notebook: 0.0047 segundos.
- En ejecución directa: 0.0053 segundos.

Hill Climbing es una opción eficiente para entornos donde la rapidez es prioritaria, pero su dependencia de soluciones iniciales puede ser un obstáculo en algunos casos.

---

## 3. A*

El **algoritmo A\*** es una técnica de búsqueda informada que utiliza una heurística para priorizar las celdas más prometedoras (Norvig, 1992). En el contexto del Sudoku, evalúa qué tan cerca está la solución completa, asignando prioridad a las celdas con menos opciones disponibles.

**Ventajas:**
- Equilibra la búsqueda sistemática con la aleatoriedad, lo que mejora la eficiencia.
- Garantiza encontrar la solución óptima si la heurística es admisible.

**Desventajas:**
- Requiere más memoria y procesamiento en comparación con backtracking.
- Su rendimiento puede depender de la calidad de la heurística utilizada.

**Análisis de rendimiento:**
- En Colab: 0.0105 segundos.
- En Jupyter Notebook: 0.1653 segundos.
- En ejecución directa: 0.0431 segundos.

El algoritmo A* se muestra consistente en la mayoría de los entornos, aunque es más lento en sistemas menos optimizados, como Jupyter.

---

## 4. Búsqueda Aleatoria

La **búsqueda aleatoria** intenta resolver el problema llenando el tablero de manera completamente aleatoria hasta encontrar una solución válida o alcanzar un límite de intentos. Esta técnica sirve más como referencia que como una estrategia práctica de resolución.

**Ventajas:**
- Es fácil de implementar y no requiere conocimiento previo del problema.

**Desventajas:**
- Su eficiencia es extremadamente baja, con complejidad alta debido a la falta de dirección en la búsqueda.
- No garantiza encontrar una solución dentro de un tiempo razonable.

**Análisis de rendimiento:**
- En Colab: 4.8412 segundos.
- En Jupyter Notebook: 4.3739 segundos.
- En ejecución directa: 3.1919 segundos.

Este método es significativamente más lento en comparación con los otros algoritmos, reflejando la ineficiencia de la búsqueda sin un enfoque heurístico.

---

## **Tiempos de Ejecución**

El rendimiento de cada algoritmo se evaluó en tres entornos diferentes: Google Colab, Jupyter Notebook y ejecución directa en terminal. 

| **Algoritmo**       | **Colab**       | **Jupyter Notebook** | **Terminal**     |
|---------------------|----------------|----------------------|-----------------|
| Backtracking        | 0.0042 s       | 0.0955 s             | 0.0242 s        |
| Hill Climbing       | 0.0153 s       | 0.0047 s             | 0.0053 s        |
| A*                 | 0.0105 s       | 0.1653 s             | 0.0431 s        |
| Búsqueda Aleatoria | 4.8412 s       | 4.3739 s             | 3.1919 s        |

---

## **Conclusiones**

Cada uno de los algoritmos analizados presenta ventajas y desventajas claras, lo que permite seleccionar el más adecuado según las circunstancias. En entornos donde la rapidez es esencial, **Hill Climbing** es una opción viable, aunque su limitación de quedar atrapado en máximos locales puede ser un inconveniente. **Backtracking** es ideal para obtener una solución garantizada, pero su rendimiento varía según el entorno de ejecución. **A\*** ofrece un equilibrio entre búsqueda exhaustiva y aleatoriedad, destacando en entornos computacionales más robustos. Por otro lado, la **Búsqueda Aleatoria** es ineficaz y solo es útil para propósitos comparativos.

---

## **Referencias**
- Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2009). Introduction to Algorithms. MIT Press.
- Norvig, P. (1992). Paradigms of Artificial Intelligence Programming: Case Studies in Common Lisp. Morgan Kaufmann.
- Russell, S., & Norvig, P. (2020). Artificial Intelligence: A Modern Approach. Pearson.
