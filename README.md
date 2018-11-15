# market_environment
# 市场环境
市场环境是其他数据和Python对象的一个合集的一个名称。  
市场环境由三个字典组成：  
* 常量
* 列表
* 曲线
定义一个`class`：
```Python
class market_environment(object):
```  
然后加上我们的各种函数，`'add_sonstant'`,`'get_constant'`等等
# 框架组建的包装器模块  
```Python
import datatime as dt
from get_year_deltas import get_year_deltas
from constant_short_rate import constant_short_rate
from market_environment import market_environment
```    
这样太麻烦的话，我们可以打包一个Python文件

# Python打包文件
将有关模块保存在一个（子）目录，但是这个目录要有一个`__init__`文件进行导入工作，`__init__`中要对`__all__`进行定义，这样可以调动命令:  
```Python
import dx 
或者
from dx import *
'''
