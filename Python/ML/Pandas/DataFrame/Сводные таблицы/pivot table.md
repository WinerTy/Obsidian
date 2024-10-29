`pivot_table` в [[Pandas]] — это более гибкий метод, чем `pivot`, который позволяет вам создавать сводные таблицы с агрегацией данных. Он полезен, когда у вас есть дубликаты в комбинациях индексов и столбцов, и вы хотите агрегировать данные по определенной функции (например, сумма, среднее, максимум и т.д.).

### Основные параметры метода `pivot_table`:

- **values**: Имя столбца или список имен столбцов, значения которых будут агрегироваться.
    
- **index**: Имя столбца или список имен столбцов, которые будут использоваться в качестве индекса (строки) в новом [[DataFrame]].
    
- **columns**: Имя столбца или список имен столбцов, значения которых будут использоваться для создания новых столбцов.
    
- **aggfunc**: Функция или список функций, которые будут использоваться для агрегации данных. По умолчанию используется `mean`.
    
- **fill_value**: Значение, которое будет использоваться для заполнения пропущенных значений в результирующем [[DataFrame]].
    
- **margins**: Булево значение, которое определяет, следует ли добавлять строки и столбцы с общими итогами.
    
- **margins_name**: Строка, определяющая имя строки и столбца с общими итогами, если `margins=True`.

## Примеры

#### №1
Предположим, у вас есть [[DataFrame]] с данными о продажах по месяцам, городам и продуктам:
```python
import pandas as pd

# Создаем DataFrame
data = {
    'City': ['New York', 'New York', 'Los Angeles', 'Los Angeles', 'Chicago', 'Chicago', 'New York', 'New York'],
    'Month': ['Jan', 'Feb', 'Jan', 'Feb', 'Jan', 'Feb', 'Jan', 'Feb'],
    'Product': ['A', 'A', 'A', 'A', 'B', 'B', 'B', 'B'],
    'Sales': [100, 120, 200, 210, 150, 160, 110, 130]
}
df = pd.DataFrame(data)
print(df)
```
Вывод
```bash
         City Month Product  Sales
0     New York   Jan       A    100
1     New York   Feb       A    120
2  Los Angeles   Jan       A    200
3  Los Angeles   Feb       A    210
4      Chicago   Jan       B    150
5      Chicago   Feb       B    160
6     New York   Jan       B    110
7     New York   Feb       B    130
```
```python
# Используем pivot_table для создания сводной таблицы
pivot_table_df = df.pivot_table(index='City', columns='Month', values='Sales', aggfunc='sum')
print(pivot_table_df)
```
Вывод 2
```bash
Month      Jan  Feb
City                
Chicago    150  160
Los Angeles 200  210
New York   210  250
```
### Агрегация по нескольким функциям:

Вы можете агрегировать данные по нескольким функциям, передавая список функций в параметр `aggfunc`:
```python
# Агрегируем данные по среднему и сумме
pivot_table_df = df.pivot_table(index='City', columns='Month', values='Sales', aggfunc=['sum', 'mean'])
print(pivot_table_df)
```
```bash
# Агрегируем данные по среднему и сумме
pivot_table_df = df.pivot_table(index='City', columns='Month', values='Sales', aggfunc=['sum', 'mean'])
print(pivot_table_df)
```
```bash
          sum                mean          
Month      Jan  Feb       Jan  Feb
City                                
Chicago    150  160  150.000000  160.000000
Los Angeles 200  210  200.000000  210.000000
New York   210  250  105.000000  125.000000
```

### Добавление общих итогов:

Вы можете добавить строки и столбцы с общими итогами, используя параметр `margins`:
```python
# Добавляем общие итоги
pivot_table_df = df.pivot_table(index='City', columns='Month', values='Sales', aggfunc='sum', margins=True, margins_name='Total')
print(pivot_table_df)
```
Вывод
```bash
Month      Jan  Feb  Total
City                        
Chicago    150  160    310
Los Angeles 200  210    410
New York   210  250    460
Total      560  620   1180
	```