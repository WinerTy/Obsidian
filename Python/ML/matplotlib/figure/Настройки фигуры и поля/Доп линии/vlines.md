### `vlines`

**Описание**: Добавляет вертикальные линии на график.

**Аргументы**:

- `x`: Массив координат x, на которых будут проведены линии.
    
- `ymin`: Начало линий по оси y.
    
- `ymax`: Конец линий по оси y.
    
- `colors` (опционально): Цвета линий.
    
- `linestyles` (опционально): Стили линий.
    
- `linewidths` (опционально): Толщины линий.
    

**Пример**:
```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
ax.vlines(x=[0.2, 0.4, 0.6], ymin=0, ymax=1, colors='red', linestyles='dotted', linewidths=2)
plt.show()
```
#Функции