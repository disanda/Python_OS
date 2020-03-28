## 列表推导

迭代列表不要For循环，这是Python列表推导式最基本的概念

可以一直用for或者if推导下去，如:

>a = [x for x in os.listdir(path1) if x.endswith('jpg') or x.endswith('png') ]

- 嵌套循环

>[ y for x in range(5) for y in range(x)] #[0, 0, 1, 0, 1, 2, 0, 1, 2, 3]

- if在前
>[v**2 if v%2 == 0 else v+1 for v in [2, 3, 4, -1] if v>0]#[4,4,16]

- 多维平铺

>vec = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
>[j for i in vec for j in i ]#[[1, 2, 3, 4, 5, 6, 7, 8, 9]]


## lambda
常和几个参数为函数的自带函数配合用：

- filter
过滤集合
- map
匹配
- reduce
求和
