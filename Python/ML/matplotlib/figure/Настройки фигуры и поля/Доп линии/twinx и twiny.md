### `twinx` и `twiny`

**Описание**: Создает вторую ось Y (`twinx`) или вторую ось X (`twiny`) на графике.

**Аргументы**:

- Нет аргументов.
    

**Пример**:
```python
import matplotlib.pyplot as plt

fig, ax1 = plt.subplots()
ax2 = ax1.twinx()

ax1.plot([0, 1], [0, 1], color='blue')
ax2.plot([0, 1], [1, 0], color='red')
plt.show()
```
#Функции