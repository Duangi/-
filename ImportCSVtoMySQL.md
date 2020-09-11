# 把csv文件导入MySQL

### 1.MySQL 编码要求

![1](D:\Material\Notes\deploysNotes\ImportCSVtoMySQL.assets\1.png)

### 2. 调整csv编码

> 把csv导入MySQL需要**严格**要求使用utf-8



注意：以下两种转码方式亲测无效

1. ~~使用excel另存为utf-8~~

> 如果使用excel直接另存为文件 保存类型设置为：utf-8，该方法行不通。
>
> ![2](D:\Material\Notes\deploysNotes\ImportCSVtoMySQL.assets\2.png)
>
> 因为使用excel 进行另存为，文件实际上会被存储为 utf-8 (+bom)编码格式，并不是严格的utf-8，导入mysql会出现导入失败的错误。

2. ~~使用记事本打开，再另存为编码格式为utf-8的csv格式~~

> 另存为之后的csv打开出现了乱码

### 3. **转码方法**

**Notepad++**

使用notepad++对文件进行转码

![3](D:\Material\Notes\deploysNotes\ImportCSVtoMySQL.assets\3.png)

- 使用notepad++打开文件
- 点击  编码-使用utf-8编码
- 保存文件

### 导入Mysql

![4](D:\Material\Notes\deploysNotes\ImportCSVtoMySQL.assets\4.png)

- 在workbench中打开需要导入的数据库

- 右键Tables - Table Data Import Wizard

- 选择刚刚转码成utf-8的文件

  ![5](D:\Material\Notes\deploysNotes\ImportCSVtoMySQL.assets\5.png)

- 根据自己需要选择使用已有的Table/新建Table

  ![6](D:\Material\Notes\deploysNotes\ImportCSVtoMySQL.assets\6.png)

- 后面一直按next 应该不会出现其他问题了
- 最后在相应的tables中就能看到成功导入的数据了