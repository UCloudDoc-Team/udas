# 2. 数据库确认

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_1.jpg)

数据库确认模块展示数据是数据库扫描任务模块中的所有已执行扫描任务的扫描结果。

## 2.1 数据库确认-确认

1、自动确认：若在执行扫描时，扫描到的数据库类型所对应的端口为该数据库类型的常用端口（如 MySQL-3306，Oracle-1521，SqlServer-1433 等），则系统会自动将该扫描结果确认到数据支持管理中

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_2.jpg)

2、手动确认：在数据库确认列表数据库确认列中选择要确认为数据库或确认为非数据库

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_3.jpg) 



选择后，可点击确认按钮①，对该扫描结果进行确认，也可勾选多条未确认的数据库后，点击批量确认按钮②，一键将选择的数据库确认为数据库或确认为非数据库。

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_4.jpg)

**注：确认为数据库的同时，该扫描结果会被添加到数据资产管理中；确认为非数据库后，该扫描结果将无法进行操作，若想重新操作，则需删除任务后重新添加并扫描**

## 2.2 数据库确认-删除

1、点击删除按钮①，可以删除选择的扫描结果，删除时会有弹窗提示。

2、勾选扫描结果后，点击删除按钮②，可批量删除扫描结果，删除后，删除的结果会在回收站中存在备份。

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_5.jpg)

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_6.jpg)

## 2.3 数据库确认-查询

数据库确认可针对数据库 IP、类型、确认状态来对扫描结果进行查询，可使用单条件查询，也可进行组合查询。点击重置按钮可重置所有查询条件

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_7.jpg)

## 2.4 数据库确认-导出

点击导出按钮①，可选择导出查询后的内容或导出所有内容 

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_8.jpg)

导出时会导出一个 Excel 表格，展示所有导出的内容

 ![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_9.jpg)

## 2.5 数据库确认-回收站

回收站：它针对数据资产发现扫描到的数据库，对其在数据库确认或数据资产管理中删除的数据库进行回收、恢复、删除处理。而直接在数据资产管理中添加的数据库则不会回收到回收站，被删除后会彻底的删除掉。

### 2.5.1  回收站-恢复

点击恢复按钮①或勾选多条被删除的数据库点击批量恢复按钮②，会将已删除数据库会恢复到数据库确认中去。点击上一步③，页面会回到数据库确认界面。

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_10.jpg)

### 2.5.2  回收站-删除

 点击列表中删除按钮①，或者是勾选多条数据库点击删除按钮②，被删除的数据库在当前产品中永久删除（删除扫描任务后重新添加并执行可再次被发现）。

 ![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_11.jpg)

### 2.5.3  回收站-查询

回收站中可对数据库 IP 和类型进行查询，从而找到想要恢复的数据库或想要彻底删除的数据库

![](/data_classification/images/operation/discovery/dbconfirm/dbconfirm_12.jpg)

  

 
