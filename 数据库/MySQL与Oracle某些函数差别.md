### 合并

&emsp;mysql：group_concat(columnName)

&emsp;oracle：string_agg(columnName, ',') -> 可能要用to_char转换类型

### 字符串截取

&emsp;mysql：LOCATE(subStr, String)

&emsp;oracle：INSTR(String, subStr)

### 日期

#### 1.获取年份

&emsp;mysql：year(columnName)

&emsp;oracle：to_number(to_char(columnName), 'yyyy') -> to_char(columnName, 'yyyy')

#### 2.获取月份

&emsp;mysql：month() 

&emsp;oracle：to_char(to_date(columnName, 'yyyymmdd'), 'mm')

#### 3.对比时间

&emsp;mysql：datediff(columnName,CURDATE())

&emsp;oracle：SELECT floor( sysdate - to_date (cloumnName, 'yyyymmdd' )) FROM DUAL

