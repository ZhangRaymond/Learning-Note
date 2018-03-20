
## pip默认把安装包都装哪了？
用下面命令得到该pip版本信息，其中包含python路径，即表示该pip将包都默认安装在该路径下
```
pip --version
或
pip -V
```
eg:
```
>> pip --version
pip 9.0.2 from c:\users\raymond\anaconda3\lib\site-packages (python 3.6)
```

## 为pip指定python版本
Linux中默认的python和pip一般是2.7版本。如果你又自己装了python3，则可通过```python -m```告诉pip哪个python版本安装包
```
python3 -m pip install requests    # 告诉pip给python3安装包
python -m pip install requests     # 告诉pip给python2.7安装包
```
