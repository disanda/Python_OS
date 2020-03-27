# python
## fraction模块

```py
from fractions import Fraction
x=Fraction(1,3)
#指的是1/3
float(x)
#0.33333
```

## gcd(a,b)
>返回a,b的最大公约数(Maximum common divisor)

```py
import fractions
x=fractions.gcd(10,15)
#x为5
```
math.gcd()和其类似

求最小公倍数(Least common multiple)
>def lcm(a,b): return abs(a * b)/fractions.gcd(a,b) if a and b else 0
