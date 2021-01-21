# Openpyxl 学习姿势


    这周打工人突然被要求处理excel文档，因为在多个文档间来回切换太累了，就上网找教程写了个python脚本，用来处理讨厌的数据(打工人永不加班)。

    下面讲一件所学知识，openpyxl是一个用于读取处理 xlsx (xls也可) 文件的python库。

## 导包
```python
    from openpyxl import load_workbook
    from openpyxl.styles import colors, Font, Fill, NamedStyle
    from openpyxl.styles import PatternFill, Border, Side, Alignment
 ```

## 基本类
- workbook： 工作簿，一个excel文件包含多个sheet。
- worksheet：工作表，一个workbook有多个，表名识别，如“sheet1”,“sheet2”等。
- cell： 单元格，存储数据对象


## 加载文件和表格实体

```python 
wb = load_workbook('./5a.xlsx')

sheet_names = wb.sheetnames   # 返回一个列表
ws2 = wb[sheet_names[0]]    # index为0为第一张表
```