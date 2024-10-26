**Apply** - он позволяет применить ту или иную функцию сразу для всех значений колонки [[DataFrame]] (в режиме broadcast).
## Пример 

```python
import numpy as np
import pandas as pd

def last_four(num):
    return str(num)[-4:]

if __name__ == "__main__":
    table = pd.read_csv("/tips.csv")
    table["last_symbols"] = table["CC Number"].apply(last_four)
    print("Таблица с новой колонкой: ", table)
```

### Лямбда функции 

```python
import numpy as np
import pandas as pd


if __name__ == "__main__":
    table = pd.read_csv("/tips.csv")
    print(
        "Таблица с использованием лямбда функции:",
        table["total_bill"].apply(lambda bill: bill * 0.5),
    )
```

### Пример с вычислением длины имени
```python
import pandas as pd

if __name__ == "__main__":
    table = pd.read_csv("/tips.csv")
    print(
        "Таблица с использованием лямбда функции:",
        table["total_bill"].apply(lambda bill: bill * 0.5),
    )
	table["name_lenght"] = table["Payer Name"].apply(len)
	print(table)
```