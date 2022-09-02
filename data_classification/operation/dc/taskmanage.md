# 1. 扫描任务管理

扫描任务管理主要功能是对“有效数据库--敏感数据扫描”，根据配置的标准进行的数据的行分类分级操作。分类分级完成后，会给出“库、表、列”的分类分级信息，同时支持对扫描任务的执行、停止、删除、查询、详情查看的操作。

 ![](/data_classification/images/operation/dc/taskmanage/taskmanage_1.jpg)

## 1.1 扫描任务管理-添加

 点击添加按钮①会出现添加任务弹窗，可针对不同的数据库资产使用不同的分类分级标准来进行分类分级

![](/data_classification/images/operation/dc/taskmanage/taskmanage_2.jpg)

![](/data_classification/images/operation/dc/taskmanage/taskmanage_3.jpg)

 **注：添加扫描任务前，请先前往“数据资产管理”添加数据库资产。**

 1、选择要进行分类分级的数据库资产后，点击扫描范围①，可选择对数据库资产的扫描范围，全量：对数据库下的全部内容进行扫描；自定义：由用户手动选择要进行分类分级的数据库。增量：首次扫描为全量扫描，之后再次扫描则是只会对增加的表进行扫描

![](/data_classification/images/operation/dc/taskmanage/taskmanage_4.jpg)
②、选择分类分级标准时可选择内置的分类分级标准或自定义的分类分级标准；自定义分类分级标准可进入“配置管理->标准配置”进行添加

![](/data_classification/images/operation/dc/taskmanage/taskmanage_5.jpg)

③、在样本数输入框①中填写抽样样本数后，选择匹配率②，在执行任务时会根据填写的样本来进行敏感扫描。若字段敏感匹配率未达到所设置的阈值则不会展示匹配到的敏感类型，不会进行匹配；若字段敏感匹配率达到了设置的阈值则可以正常展示匹配到的敏感类型，且可正常根据分类分级标准来进行分类分级。

 ![](/data_classification/images/operation/dc/taskmanage/taskmanage_6.jpg)

④、扫描方式可选择手动执行、定时执行、周期执行。手动执行：添加任务后需手动点击执行任务；

定时执行：在选择执行时间后，到达指定的时间时任务会自动开始执行；

![](/data_classification/images/operation/dc/taskmanage/taskmanage_7.jpg)

周期执行：选择执行的间隔时间后，每达到时间点后，任务就会自动开始执行。

![](/data_classification/images/operation/dc/taskmanage/taskmanage_8.jpg)

## 1.2 扫描任务管理-执行

1、点击任务列表中执行按钮①，或者是勾选多条任务点击批量执行按钮②进行批量执行任务，如下图所示：

![](/data_classification/images/operation/dc/taskmanage/taskmanage_9.jpg)

**注：最多同时进行** **10** **个任务**

2、执行中的任务可以点击停止按钮①，可停止执行中的任务。如下图所示：

![](/data_classification/images/operation/dc/taskmanage/taskmanage_10.jpg)

##  1.3 扫描任务管理-查询

在查询输入框，输入数据库的 IP 关键字后，点击查询按钮，方可查询到该 IP 的扫描任务，系统默认查询为空时，查询的结果为全部扫描的任务，也可以通过跳转页面查看。查询结果如图所示：

![](/data_classification/images/operation/dc/taskmanage/taskmanage_11.jpg)

## 1.4 扫描任务管理-修改

点击列表中修改按钮①，数据库名称为不可修改项，可修改扫描范围（全量、自定义）、分类分级标准、样本数、匹配率、扫描方式。如下图所示：

![](/data_classification/images/operation/dc/taskmanage/taskmanage_12.jpg)

![](/data_classification/images/operation/dc/taskmanage/taskmanage_13.jpg)

##  1.5 扫描任务管理-删除

1、点击删除按钮①，可删除指定的扫描任务，删除时有弹窗提示。

2、勾选多条任务后，点击删除按钮②，可一键删除所有勾选的任务。

![](/data_classification/images/operation/dc/taskmanage/taskmanage_14.jpg)

## 1.6 扫描任务管理-详情

 点击详情按钮①，可以查看扫描任务的配置情况和执行的状态结果。如下图所示:![](/data_classification/images/operation/dc/taskmanage/taskmanage_15.jpg) 

![](/data_classification/images/operation/dc/taskmanage/taskmanage_16.jpg)

 
