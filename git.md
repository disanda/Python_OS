# 同步本地和github上的项目

## 1.设置git账户密钥
参考:https://www.cnblogs.com/xiaoxiaodevlog/p/10704977.html

## 2.克隆一个项目到本地
两种方法：
- 下载项目
>git clone xxx
- 添加项目
> git remote add origin xxx


## 3.传输文件

> git pull origin master #拉到本地第一次用
> git push origin master #从本地上传

## 4.断点续传
大文件下载用git clone会断.
建一个本地仓库(文件夹)，之后用fetch和checkout解决
```
>git mkdir xxx
>cd xxx
>git fetch https://xxxxx.git
#可以反复用fetch续传，直到下载完毕，出现以下字样:
#*branch HEAD -> FETCH_HEAD
>git checkout FETCH_HEAD
#项目就完整生成在本地了
```

## 其他

https://blog.csdn.net/weixin_30699831/article/details/101982286?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task
