# Отображения, по другому - map, карта

Отображения - структура данных, неупорядоченная коллекция пар "ключ-значение", в которой все ключи различны, а значение, связанное с заданным ключом, можно получить, обновить или удалить независимо от размера карты (отображения).

Отображение в [[GOLANG]] представляет собой ссылку на хеш-таблицу, а его тип записывается как map[K]V, где К и V являются типами его ключей и значений.

Все ключи в данном отображении имеют один и тот же тип, как и все значения имеют один и тот же тип, но тип ключей не обязан совпадать с типом значений. Тип ключа К должен быть сравниваемым с помощью оператора ==, чтобы отображение могло проверить, равен ли данный ключ одному из имеющихся в нем.

## Создание отображений

Объявление map выглядит так:

```go
var users map[string]int
// string - ключ, int - значения
```

**Но так делать опасно**, так мы не инициализировали его и при добавлении значений будут ошибки. (см. ниже)

Поэтому есть 2 более правильных способа создания отображений в Go:

```go
// с помощью встроенной функции make:
m1 := make(map[int]int)

// с помощью использования литерала отображения:
m2 := map[int]int{
    // Пары ключ:значение указываются при необходимости
    12: 2,
    1:  5,
}

fmt.Println(m1) // map[]
fmt.Println(m2) // map[1:5 12:2]
```

Почему мы не можем просто объявить отображение с помощью ключевого слова var? Объявляя переменную с использованием ключевого слова var, но не присваивая ей явно начальное значение, мы присваиваем ей нулевое значение. Отображение в Go - ссылка на хэш-таблицу, а нулевое значение ссылки nil. Попытавшись в дальнейшем добавить значение для определенного ключа мы получим ошибку "assignment to entry in nil map", которая приведет к панике:

```go
var m map[int]int
m[12] = 3
fmt.Println(m)

// Вывод (сработает паника):
// panic: assignment to entry in nil map
```