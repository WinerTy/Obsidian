### `annotate`

**Описание**: Добавляет аннотацию (текст с возможностью указания стрелки) на график.

**Аргументы**:

- `text`: Текст аннотации.
    
- `xy`: Координаты точки, на которую указывает стрелка.
    
- `xytext` (опционально): Координаты текста аннотации.
    
- `arrowprops` (опционально): Словарь свойств стрелки.
    

**Пример**:
```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
ax.plot([0, 1], [0, 1])
ax.annotate('Point', xy=(0.5, 0.5), xytext=(0.7, 0.7),
            arrowprops=dict(facecolor='black', shrink=0.05))
plt.show()
```
#Функции