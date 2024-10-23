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

### 1. **Backtracking**

El algoritmo **Backtracking** explora exhaustivamente todas las posibilidades, regresando a pasos anteriores si encuentra inconsistencias. Según Cormen et al. (2009), “los algoritmos de retroceso generan todas las soluciones posibles mediante una búsqueda sistemática en el espacio de soluciones posibles”.

- **Complejidad**: Exponencial \(O(b^d)\), donde \(b\) es el número de opciones por celda y \(d\) es la profundidad de búsqueda (Cormen et al., 2009).
- **Ventajas**: Asegura encontrar una solución si existe.
- **Desventajas**: Se vuelve ineficiente para puzzles grandes.

---

### 2. **Hill Climbing**

**Hill Climbing** es un algoritmo de optimización que busca mejorar gradualmente una solución inicial aleatoria. Sin embargo, Russell y Norvig (2020) advierten que “puede quedar atrapado en un máximo local, lo que impide encontrar la solución óptima”.

- **Ventajas**: Es rápido y consume menos recursos que el backtracking.
- **Desventajas**: No siempre garantiza una solución global óptima.

---

### 3. **A\***

El **algoritmo A\*** utiliza una heurística para priorizar las celdas más prometedoras, equilibrando eficiencia y exhaustividad. Norvig (1992) señala que “el uso de heurísticas adecuadas permite reducir significativamente el espacio de búsqueda”.

- **Ventajas**: Logra un buen equilibrio entre velocidad y exhaustividad.
- **Desventajas**: Requiere más memoria y procesamiento en comparación con otros algoritmos.

---

### 4. **Búsqueda Aleatoria**

La **Búsqueda Aleatoria** intenta llenar el tablero de forma aleatoria hasta encontrar una solución válida. Aunque simple, es un método altamente ineficiente. Como mencionan Cormen et al. (2009), “las búsquedas no informadas pueden ser costosas en términos de tiempo, especialmente si no se aplican restricciones”.

- **Ventajas**: Fácil de implementar.
- **Desventajas**: Muy ineficiente y no garantiza encontrar soluciones en un tiempo razonable.

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

Los resultados obtenidos muestran que:

- **Backtracking** es efectivo pero consume más tiempo en algunos entornos, siendo ideal para encontrar soluciones garantizadas en tableros pequeños.
- **Hill Climbing** es el algoritmo más rápido, pero puede quedar atrapado en soluciones subóptimas.
- **A\*** proporciona un equilibrio entre eficiencia y exhaustividad, pero puede ser costoso en términos de memoria.
- **Búsqueda Aleatoria** es el método menos eficiente, útil solo como referencia comparativa.

---

## **Referencias**
- Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2009). Introduction to Algorithms. MIT Press.
- Norvig, P. (1992). Paradigms of Artificial Intelligence Programming: Case Studies in Common Lisp. Morgan Kaufmann.
- Russell, S., & Norvig, P. (2020). Artificial Intelligence: A Modern Approach. Pearson.
