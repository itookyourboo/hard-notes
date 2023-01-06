---
title: XOR swap
keywords: битовые операции
---

# XOR swap

## Условие

Поменяйте значения переменных `a` и `b` с помощью побитовой операции ^ ([XOR](https://realpython.com/python-bitwise-operators/#bitwise-xor))

```python
a, b = 7, 11
print(a, b)      # 7 11
...
print(a, b)      # 11 7
```

## Решение

```python
a, b = 7, 11
print(a, b)      # 7 11
a ^= b
b ^= a
a ^= b
print(a, b)      # 11 7
```
