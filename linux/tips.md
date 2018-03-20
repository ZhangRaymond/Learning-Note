
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

## wget  下载工具   
```
wget [参数] [URL地址]

-c                 断点续传（重新启动下载中断的文件）
-b                 后台下载（文件非常大时，可使用-b进行后台下载）
--limit-rate=300k  限速下载，避免占用所有带宽
...
```
eg:
1. 下载并保存在当前文件夹下   
    ```wget http://www.minjieren.com/wordpress-3.1-zh_CN.zip```
2. 下载后重命名为wordpress.zip，否则系统会自动命名为download.aspx?id=1080   
    ```wget -O wordpress.zip http://www.minjieren.com/download.aspx?id=1080``` 
3. 下载多个文件   
    ```wget -i filelist.txt ```   
    下载链接文件filelist.txt内容：   
    > url1   
    url2   
    url3   
    url4   

ref: [每天一个linux命令（61）：wget命令](http://www.cnblogs.com/peida/archive/2013/03/18/2965369.html)
