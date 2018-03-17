
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
