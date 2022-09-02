# 1. 数据库扫描任务

## 1.1 数据库扫描任务-添加

数据资产发现-添加扫描任务：点击添加按钮①，出现添加任务弹窗。输入正确的数据库主机 IP 或 IP 段，选择端口扫描模式（内置或自定义），点击确定按钮②，添加任务成功。可添加的 IP 和 IP 段的格式如下（具体 IP 依现场网络情况而定）：

| 数据库主机   IP | 192.168.1.1 或 192.168.1 或 192.168.1.1-255 或 192.168.1-2 |                                                          |
| --------------- | ---------------------------------------------------------- | -------------------------------------------------------- |
| 端口扫描方式    | 内置                                                       | 3306 或 80,8080(可以添加单个或多个端口，多个端口用,隔开) |
| 自定义          | 3306 或 80-8080(可以添加单个端口或端口段)                  |                                                          |

 添加内置端口扫描任务（扫描 IP 段内的数据库的常用端口，如 MySQL：3306、Oracle：1521等）：

![](/data_classification/images/operation/discovery/dbtask/dbtask_0.jpg)

![](/data_classification/images/operation/discovery/dbtask/dbtask_1.jpg)

添加自定义端口扫描任务（扫描 IP 段内自定义端口范围的所有端口）：

![](/data_classification/images/operation/discovery/dbtask/dbtask_2.jpg)

## 1.2 数据库扫描任务-删除

1、可点击删除按钮①，可对要删除的任务进行删除，删除时有弹窗提示

2、也可勾选列表中的任务，然后点击删除按钮②，进行批量删除，删除时有弹窗提示

![](/data_classification/images/operation/discovery/dbtask/dbtask_3.jpg)

![](/data_classification/images/operation/discovery/dbtask/dbtask_4.jpg)

## 1.3 数据库扫描任务-执行

1、在添加任务时可勾选立即执行，添加任务后就会执行任务

![](/data_classification/images/operation/discovery/dbtask/dbtask_5.jpg)

2、点击扫描任务列表操作列中的执行按钮①，或勾选任务后点击批量执行按钮②，可执行扫描任务。

![](/data_classification/images/operation/discovery/dbtask/dbtask_6.jpg)

 **注：扫描状态（未开始、正在扫描、扫描成功、扫描失败、未发现数据库）**

## 1.4 数据库扫描任务-查询

在查询框①中输入数据库主机 IP 关键字，点击查询便可查询到指定任务

 ![](/data_classification/images/operation/discovery/dbtask/dbtask_7.jpg)

## 1.5 数据库扫描任务-修改

点击扫描任务列表操作列中的修改按钮①，修改任务后点击确定按钮②，即可对已添加的扫描任务进行修改

![](/data_classification/images/operation/discovery/dbtask/dbtask_8.jpg) 

![](/data_classification/images/operation/discovery/dbtask/dbtask_9.jpg)

 1.6 数据库扫描任务-详情

点击扫描任务列表操作列中的详情按钮①，可查看扫描任务配置情况。

![](/data_classification/images/operation/discovery/dbtask/dbtask_10.jpg)

![](/data_classification/images/operation/discovery/dbtask/dbtask_11.jpg)

