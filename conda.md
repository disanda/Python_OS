python环境管理工具，可同时管理不同Python版本的运行环境，可在不同环境之间来回切换。



# conda命令

## 0.更新&安装


```
conda install python=3.5 
#安装固定版本包(也可以用该方法进行升降级)
conda install packagename 
#为当前环境安装某包
conda install -n envname packagename 
#为某环境安装某包
conda search packagename 
#搜索某包
conda updata packagename 
#更新当前环境某包
conda update -n envname packagename 
#更新某特定环境某包
conda remove packagename 
#删除当前环境某包
conda remove -n envname packagename 
#删除某环境环境某包
```



## 1.创建新的环境
>-n 或 --name 参数


```

conda create --name xxx  
  
conda create -n xxx

# 指定版本或包
conda create -n xxx python=3.5
如果你要指定多个包 可以用
conda create -n xxx python=3.5 numpy pandas

```

## 2.切换环境


```
#参考帮助
conda env --help

#显示可用环境
conda env list

#激活某个虚拟环境
activate xxx

#放弃当前虚拟环境
deactivate
```

另外在jupter中切换环境还需要额外操作


```
　　1.首先在anaconda中创建一个虚拟环境，安装python2.7版本

　　2.激活python2.7，命令为”activate D:\Anaconda\envs\py27“

　　3.在python2.7下安装ipykernel，安装命令为“pip install ipykernel“

　　4.输入命令“python -m ipykernel install --name python2 ”

　　5.输入命令"jupyter notebook"后打开jupyter查看，已经安装好了python2环境，可以进行切换了
```


## 3.克隆和删除环境


```
#创建一个新环境想克隆一部分旧的环境
conda create -n xxx_clone --clone xxx_origin

#删除某个环境
conda remove -n xxx --all
```


## 4.导入导出配置环境(.yml文件)
>非常有用，比如你想帮朋友安装和你一模一样的环境，你可以直接导出一个配置文件给他，就能免除很多人力安装调试

```
#导出环境配置文件
conda env export > environment.yml
#导入环境
conda env create -f environment.yml
```

https://www.jianshu.com/p/742dc4d8f4c5
