---
title: Порядок init, new и call
keywords: 
---

# Порядок init, new и call

## Вопрос

Каков порядок вызовов методов `__init__`, `__new__`, `__call__` ?

## Ответ

```python
class Test:
    def __new__(cls):
        print('new')
        return object.__new__(cls)

    def __init__(self):
        print('init')

    def __call__(self):
        print('call')


test = Test() 
# new 
# init
test() 
# call
```
