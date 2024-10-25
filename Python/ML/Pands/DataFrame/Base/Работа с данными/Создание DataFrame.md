Создание таблицы


```python
def create_table():
    myindex = ["Class_1", "Class_2", "Class_3"]
    mydata = [
        "42",
        "53",
        "43",
        "46",
        "43",
        "34",
        "123",
        "63",
        "12",
        "323",
        "53",
        "43",
    ]
    mycolums = ["Sep", "Oct", "Nov", "Dec"]

    return pd.DataFrame(np.array(mydata).reshape(3, 4), myindex, mycolums)
```
 
В данном примере мы создаем **Таблицу** ТИПА [[DataFrame]]
