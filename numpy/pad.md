## pad

用于数组填充

```py
>>>a = [1, 2, 3, 4, 5]
>>>np.pad(a, (2, 3), 'constant', constant_values=(4, 6)) 
array([4, 4, 1, ..., 6, 6, 6]) # 边界填充 填充值为常数（constant), 左2右3

>>>np.pad(a, (2, 3), 'edge')
array([1, 1, 1, ..., 5, 5, 5]) # 边界填充 填充值为边界数

>>>np.pad(a, (2, 3), 'linear_ramp', end_values=(5, -4))
array([ 5,  3,  1,  2,  3,  4,  5,  2, -1, -4]) #填充值为斜坡直线值

>>>np.pad(a, (2, 3), 'reflect') #映射填充
array([3, 2, 1, 2, 3, 4, 5, 4, 3, 2])

>>>a = [[1, 2], [3, 4]]
>>>np.pad(a, ((3, 1), (2, 4)), 'constant') #填充为上3行，下1行. 左2列，右4列.
array([[0, 0, 0, 0, 0, 0, 0, 0],
       [0, 0, 0, 0, 0, 0, 0, 0],
       [0, 0, 0, 0, 0, 0, 0, 0],
       [0, 0, 1, 2, 0, 0, 0, 0],
       [0, 0, 3, 4, 0, 0, 0, 0],
       [0, 0, 0, 0, 0, 0, 0, 0]])


```
## reference 
- https://github.com/disanda/Python_OS/new/master/numpy
