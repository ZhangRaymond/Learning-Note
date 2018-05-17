# 数据预处理
sklearn和keras中均有专门用于数据预处理的模块。分别为
- sklearn.preprocessing
- keras.preprocessing
## 序列
### 标签编码 category to label  
将数字或文字类别编码为连续的label 0,1,2,3,...
- **LabelEncoder()**            
  ``` python
  from sklearn.preprocessing import LabelEncoder
  ```
  > ref: [Sklearn中LabelEncoder与OneHotEncoder](https://blog.csdn.net/ZK_J1994/article/details/78496565)

### 热编码 label to OneHot code 
将label 1,2,3,... 装换为 onehot 形式
- **OneHotEncoder()**     
  > ref: [Sklearn中LabelEncoder与OneHotEncoder](https://blog.csdn.net/ZK_J1994/article/details/78496565)   
  ``` python
  from sklearn.preprocessing import OneHotEncoder
  ```
- **to_categorical()**
  ``` python
  from keras.utils.np_utils import to_categorical
  ```
