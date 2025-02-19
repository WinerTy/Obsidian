### `grid`

**Описание**: Добавляет сетку на график.](библиотеке [[Matplotlib]] термин **"grid"** (сетка) относится к набору линий, которые помогают визуально ориентироваться на графике. Сетка обычно состоит из горизонтальных и вертикальных линий, которые проходят через основные и/или вспомогательные деления осей.
### Основные функции для работы с сеткой:

1. **`plt.grid(True)`**: Включает отображение сетки на графике. По умолчанию сетка будет отображаться на основных делениях осей.
    
2. **`plt.grid(False)`**: Отключает отображение сетки.
    
3. **`plt.grid(which='major')`**: Отображает сетку только на основных делениях осей.
    
4. **`plt.grid(which='minor')`**: Отображает сетку только на вспомогательных делениях осей.
    
5. **`plt.grid(which='both')`**: Отображает сетку как на основных, так и на вспомогательных делениях осей.
    
6. **`plt.grid(axis='x')`**: Отображает сетку только по оси X.
    
7. **`plt.grid(axis='y')`**: Отображает сетку только по оси Y.
    
	1. **`plt.grid(axis='both')`**: Отображает сетку по обеим осям (по умолчанию).>)

**Аргументы**:

- `b` (опционально): Булево значение, указывающее, включить ли сетку.
    
- `which` (опционально): Тип сетки (`'major'`, `'minor'`, `'both'`).
    
- `axis` (опционально): Ось, для которой включается сетка (`'both'`, `'x'`, `'y'`).
    
- `linestyle` (опционально): Стиль линий сетки.
    
- `linewidth` (опционально): Толщина линий сетки.
    
- `color` (опционально): Цвет линий сетки.
    

**Пример**:
```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
ax.plot([0, 1], [0, 1])
ax.grid(True, which='both', axis='both', linestyle='--', linewidth=1, color='gray')
plt.show()
```
#Функции