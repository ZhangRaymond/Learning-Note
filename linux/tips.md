
## crond定时任务
1. 列出定时任务    
``` crontab -l```  
2. 编辑定时任务   
```crontab -e```   

## ln命令 软连接 硬链接
## rsync 同步工具
## mail
1. 查看：```mail```   
2. 删除：```cd /var/spool/mail/``` 然后清空指定用户下的所有邮件 ```echo ''>用户名```         
3. 外加一个发现： sh脚本调用python脚本时，print()函数由于没法输出到命令行，print()输出的内容则被重定向到了mail里面。（无意中发现我的邮件有34w多条mail之后的领悟...）

## unix2dos/dos2unix    
两种系统之间文本文件（的回车符）转换   
```
dos2unix a.sh
```
## du 查看文件或文件夹大小
```
du                查看当前目录下各文件大小
du -sh a/         查看a文件夹的总大小
du -sh a.txt      查看a.txt大小
du a.txt b.txt    查看多个文件大小
```
选项   
```-s```或```--summarize```       &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp; 仅显示总计，只列出最后加总的值   
```-h```或```--human-readable```   &nbsp;   &nbsp; 以K，M，G为单位，提高信息的可读性 

ref：[每天一个linux命令（34）：du 命令](http://www.cnblogs.com/peida/archive/2012/12/10/2810755.html)
