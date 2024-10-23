# Sudoku Solver: Algoritmos para Resolver Sudoku

Este proyecto contiene la implementación de varios algoritmos para la resolución de **Sudoku**, incluyendo **Backtracking**, **Hill Climbing**, **A\*** y **Búsqueda Aleatoria**. Además, se mide el rendimiento de cada algoritmo en distintos entornos.

## Estructura del Proyecto

1. **Generación del Tablero de Sudoku**:
   - `create_board()`: Genera un tablero base aleatorio.
   - `remove_numbers(board, difficulty)`: Ajusta la dificultad del puzzle eliminando números.

2. **Algoritmos de Resolución**:
   - **Backtracking**: Algoritmo de fuerza bruta que garantiza una solución.
   - **Hill Climbing**: Optimización iterativa con posibilidad de quedar atrapado en máximos locales.
   - **A***: Algoritmo de búsqueda informada con heurística.
   - **Búsqueda Aleatoria**: Llena el tablero aleatoriamente hasta encontrar una solución.

3. **Funciones Auxiliares**:
   - `print_board(board)`: Imprime el tablero con formato visual.
   - `is_valid(board, row, col, num)`: Verifica si un número puede colocarse en una celda específica.

## Análisis de Algoritmos (APA)

### 1. **Backtracking**  
El algoritmo de **backtracking** busca exhaustivamente una solución mediante prueba y error. Es eficiente para puzzles pequeños, pero su complejidad aumenta exponencialmente con problemas más grandes (Cormen et al., 2009).

**Tiempos promedio**:
- Colab: 0.0042 segundos.
- Jupyter Notebook: 0.0955 segundos.
- Terminal: 0.0242 segundos.

---

### 2. **Hill Climbing**  
Este algoritmo optimiza una solución inicial mediante mejoras iterativas, aunque puede quedar atrapado en máximos locales (Russell & Norvig, 2020).

**Tiempos promedio**:
- Colab: 0.0153 segundos.
- Jupyter Notebook: 0.0047 segundos.
- Terminal: 0.0053 segundos.

---

### 3. **A***  
**A\*** usa una heurística para priorizar celdas con menos opciones, equilibrando eficiencia y exhaustividad (Norvig, 1992).

**Tiempos promedio**:
- Colab: 0.0105 segundos.
- Jupyter Notebook: 0.1653 segundos.
- Terminal: 0.0431 segundos.

---

### 4. **Búsqueda Aleatoria**  
Este método llena el tablero de manera aleatoria, lo que resulta ineficiente, pero sirve como referencia de comparación.

**Tiempos promedio**:
- Colab: 4.8412 segundos.
- Jupyter Notebook: 4.3739 segundos.
- Terminal: 3.1919 segundos.

---

## Conclusiones

Cada algoritmo tiene fortalezas y debilidades, por lo que la elección depende del contexto:

- **Backtracking** es ideal para obtener soluciones garantizadas.
- **Hill Climbing** es rápido pero puede no encontrar soluciones globales óptimas.
- **A\*** ofrece un buen equilibrio, aunque requiere más recursos.
- **Búsqueda Aleatoria** es la opción menos eficiente y solo útil para comparaciones.

---

## Referencias

- Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2009). *Introduction to Algorithms*. MIT Press.  
- Norvig, P. (1992). *Paradigms of Artificial Intelligence Programming: Case Studies in Common Lisp*. Morgan Kaufmann.  
- Russell, S., & Norvig, P. (2020). *Artificial Intelligence: A Modern Approach*. Pearson.


