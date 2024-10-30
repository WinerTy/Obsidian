### `hlines`

**Описание**: Добавляет горизонтальные линии на график.

**Аргументы**:

- `y`: Массив координат y, на которых будут проведены линии.
    
- `xmin`: Начало линий по оси x.
    
- `xmax`: Конец линий по оси x.
    
- `colors` (опционально): Цвета линий.
    
- `linestyles` (опционально): Стили линий.
    
- `linewidths` (опционально): Толщины линий.
    

**Пример**:
```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
ax.hlines(y=[0.2, 0.4, 0.6], xmin=0, xmax=1, colors='blue', linestyles='dashed', linewidths=2)
plt.show()
```
#Функции