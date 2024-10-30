### `fill_between`

**Описание**: Заполняет область между двумя кривыми.

**Аргументы**:

- `x`: Массив координат x.
    
- `y1`: Массив координат y для первой кривой.
    
- `y2` (опционально): Массив координат y для второй кривой (по умолчанию 0).
    
- `where` (опционально): Условие, определяющее, где заполнять область.
    
- `color` (опционально): Цвет заполнения.
    
- `alpha` (опционально): Прозрачность заполнения.
    

**Пример**:
```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

fig, ax = plt.subplots()
ax.plot(x, y1, label='sin(x)')
ax.plot(x, y2, label='cos(x)')
ax.fill_between(x, y1, y2, where=(y1 > y2), color='green', alpha=0.5)
ax.fill_between(x, y1, y2, where=(y1 <= y2), color='red', alpha=0.5)
plt.show()
```
#Функции