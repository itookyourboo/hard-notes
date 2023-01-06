---
title: enumerate
keywords: python, фишки, списки, кортежи, генераторы
---

# enumerate

## Было

```python
array = [2, 4, 6, 8]
for i in range(len(array)):
    print(i, array[i])
```

```
0 2
1 4
2 6
3 8
```

## Стало

```python
array = [2, 4, 6, 8]
for i, element in enumerate(array):
    print(i, element)
```

```
0 2
1 4
2 6
3 8
```

Также можно указать стартовый индекс:

```python
array = [2, 4, 6, 8]
for i, element in enumerate(array, 5):
    print(i, element)
```

```
5 2
6 4
7 6
8 8
```
