# Unix命令

## 压缩与解压缩

- 压缩:
zip -r xxx.zip yyy
- 解压缩:
unzip -o xxx.zip -d yyy #覆盖
unzip -n xxx.zip -d yyy #不覆盖
unzip -v test.zip#查看压缩包但不解压
## 统计文件数量
>当文件夹内文件非常多时
```
ls -l | grep -c '^-' #正则表达式
或
ls -l | wc -l #字数统计命令


```
