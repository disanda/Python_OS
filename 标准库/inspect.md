# 审查 (inspect)

## 审查元素

 ```py
import inspect
import os
 
class Test(object):
    """Test Class """
 
    def test(self):
        self.fuc = lambda x: x
 
class Testone(Test):
    pass
 
print(inspect.ismodule(os))         # True
print(inspect.isclass(Test))        # True
print(inspect.getdoc(Test))         # Test Class
 
print(inspect.getsourcefile(Test))   # 文件路径
print(inspect.getsourcelines(Test))  # 代码块，每行一个元素，组成数组
print(inspect.getsource(Test))       # 获取代码块原本内容，带缩进
 ```
 
 ## reference
 
 - https://www.cnblogs.com/feifeifeisir/p/10627854.html
