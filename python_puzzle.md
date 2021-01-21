# Python 常见问题

## 日常编码

### 文件的绝对和相对路径 
    Python里的路径分相对路径和绝对路径。

###### 绝对路径
Girl.py
**`"E:/Python/Lib/site_packages/Girl.py"`**

###### 相对路径

相对路径呢，就是相对于目前.py文件的路径。

**例子：**

文件路径： `"E:/Python/Lib/site_packages/Boy1.py"`
书写路径：**`"Boy1.py"`**
说明：跟Girl.py在同一个文件夹里。

文件路径： `"E:/Python/Lib/site_packages/set/Boy2.py"`
书写路径：**`"set/Boy2.py"`**
说明：Boy2.py 位于与 Girl.py 同级的set文件夹下

文件路径：`"E:/Python/Lib/site_packages/Boy3.py"`
书写路径：**`"./Boy3.py"`**
说明：跟Girl.py在同一个文件夹里。

文件路径： `"E:/Python/Lib/Boy4.py"`
书写路径：**`"../Boy4.py"`**
说明：Boy3.py位于Girl.py上一级文件夹里的。