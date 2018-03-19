
（以CentOS为例）
### 1. 安装必要的组件
```
yum -y install wget gcc make  zlib-devel readline-devel  bzip2-devel ncurses-devel sqlite-devel gdbm-devel xz-devel tk-devel openssl-devel
```

### 2. 下载官网源码包   
```
wget https://www.python.org/ftp/python/3.6.1/Python-3.6.1.tar.xz
```   
    

### 3. 解压、切换目录   
```
tar -xvf Python-3.6.1.tar.xz   
cd Python-3.6.1
```

### 4. 配置安装位置   
#### 4.1 root用户
可选默认安装路径  
``` bash
./configure --prefix=/usr/local/python3.6 --enable-optimizations
``` 
> --enable-optimizations 可以加快编译速度     

#### 4.2 非root用户
由于非root用户没有/etc/目录的权限，只能安装在该用户目录下（不太建议，但不影响使用）   
``` bash
./configure --prefix=/home/Raymond/python3.6 --enable-optimizations
```   
   
### 5. 编译 
这一过程比较耗时
```
make
make install
```  

### 6. 配置命令
#### 6.1 root用户
root用户可以直接使用软链接
```
ln -s /usr/local/python3.6/bin/python3 /usr/bin/python3
ln -s /usr/local/python3.6/bin/pip3 /usr/bin/pip3
```
#### 6.2 非root用户
非用户没有使用软链接的权限，这里可以用alias这一讨巧的方法：   
**修改用户目录下的bashrc文件**
```
vim ~/.bashrc
```
填入下面两行，保存退出   
```
alias python3=/home/Raymond/python3/bin/python3.6
alias pip3=/home/Raymond/python3/bin/pip3
```  
   
> 使用alias方式时，在所写的sh脚本中如果要调用python3和pip3命令时，需在sh脚本前加一条（否则无法找到命令，会报错）
>```
>source ~/.bashrc
>```

然后就可以在shell中放肆地使用python3和pip3了



