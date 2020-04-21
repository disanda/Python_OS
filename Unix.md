# Unix命令

## 1.压缩与解压缩
### zip
- 压缩:
zip -r xxx.zip yyy
- 解压缩:
unzip -o xxx.zip -d yyy #覆盖
unzip -n xxx.zip -d yyy #不覆盖
unzip -v test.zip#查看压缩包但不解压

### rar 
一般需要先安装
```
apt-get install rar unrar
```
- 解压缩:
```
unrar x a.rar #参数x代表解压到一个文件夹下
unrar e a.rar #解压到当前文件夹,不创建新文件夹
```
## 2.统计文件数量
>当文件夹内文件非常多时
```
ls -l | grep -c '^-' #正则表达式
或
ls -l | wc -l #字数统计命令
```

## 3.百度云盘
由于百度PCS API权限限制，程序只能存取百度云端/apps/bypy目录下面的文件和目录，一次只能上传2G
https://github.com/houtianze/bypy
