# Description

Тестирует решатель простых квадратных уравнений типа ax**2+bx+c=0.

# Options

Непосредственно сам test.py проверяет тождественно решатель уравнений. На сам решатель подаются аргументы a,b,c и программа выводит значения х1 и х2, обрабатывая случаи при отрицательном дискриминанте и равном нуле.
```python
from math import sqrt


def get_roots(a, b, c):
    discriminant = b ** 2 - 4 * a * c
    if discriminant < 0:
        return None, None
    root1 = (-b - sqrt(discriminant)) / (2 * a)
    root2 = (-b + sqrt(discriminant)) / (2 * a)
    if discriminant == 0:
        return root1, None
    return root1, root2
```

# Running the tests

Скрипт требует для своей работы установленного интерпретатора Python версии 3.5

```python
python test.py
```

# Цели проекта

Код создан в учебных целях. В рамках учебного курса по веб-разработке ― [DEVMAN.org](https://devman.org)
