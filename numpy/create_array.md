

## np.identity()

这个函数和np.eye()的区别在于，这个只能创建方阵，也就是N=M

函数的原型：np.identity(n,dtype=None)

参数：n，int型表示的是输出的矩阵的行数和列数都是n

dtype：表示的是输出的类型，默认是float

返回的是主对角线为1，其余地方为0的数组
