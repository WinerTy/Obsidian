**Описание**: Добавляет произвольные линии на график.

**Аргументы**:

- `x`: Массив координат x.
    
- `y`: Массив координат y.
    
- `color` (опционально): Цвет линии.
    
- `linestyle` (опционально): Стиль линии.
    
- `linewidth` (опционально): Толщина линии.
    

**Пример**:
```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
ax.plot([0.2, 0.8], [0.5, 0.5], color='purple', linestyle='-', linewidth=2)
plt.show()
```
#Функции