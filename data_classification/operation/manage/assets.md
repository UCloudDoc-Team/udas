# 1. 数据库资产

![](/images/operation/manage/assets/assets_1.png)

## 1.1 数据库资产-添加

点击页面的添加按钮①，用于添加数据库资产，弹窗提示（资产名称、数据库类型、数据库主机IP、端口为必填项）添加页面：

 ![](/images/operation/manage/assets/assets_2.png)

添加成功页面会展示出添加的资产：

![](/images/operation/manage/assets/assets_3.png)

 

**注：添加数据库资产后，每天晚上两点都会对该数据库资产进行一次扫描，可联系服务人员进行关闭**

分类分级系统支持添加的数据库类型及版本有：

 Oracle：10g,11g,12c，19c； 

SqlServer：2005,2008,2012,2014,2016,2017,2019；

 MySQL：5.5,5.6,5.7,8.0；

DB2：10.5,11.1； 

MongoDB：3.4.7,3.6.2,4.0.7； 

PostgreSQL：9.4,9.6,10.1,10.7,11.2；

达梦：DM7，DM8； Sybase：15.7、16.0； 

Caché：2010 2016； 

GaussDB：6.5.1； 

Kingbase：（人大金仓）V7； 

Elasticsearch：6.0以上； 

Teradata：14.X Informix：12;

Hive：2.X（Apache平台），支持不带Kerberos认证

## 1.2 数据库资产-集群设置

点击页面集群设置按钮①，可将有关联的数据库资产添加为一个集群，可将多个数据库设置为一个集群。

被关联的数据库将不会在数据库列表中展示，也将不会被应用其他模块（可在数据资产概览->数据库资产信息统计中被统计）。

被关联的数据库可以在主数据库的数据库概览->数据库集群情况下展示，被关联的数据库可以取消关联。

添加页面如下图所示：

![](/images/operation/manage/assets/assets_4.png)

 

![](/images/operation/manage/assets/assets_5.png)

添加后的主数据库和关联数据库的信息如图所示：

![](/images/operation/manage/assets/assets_6.png)



## 1.3 数据库资产-删除

1、点击数据库资产卡片的操作按钮①，选择“删除”②，可以删除数据资产，删除时有弹窗提示：

2、也可以勾选需删除的数据库资产后，点击删除按钮③进行批量的删除，如图所示： 

![](/images/operation/manage/assets/assets_7.png)

![](/images/operation/manage/assets/assets_8.png)

## 1.4 数据库资产-修改

点击数据库资产卡片中的操作按钮①，选择“修改”②，可对数据资产进行修改，修改界面会把已有的条件带过去，其中数据库类型、数据库主机IP、端口为不可编辑）

![](/images/operation/manage/assets/assets_9.png) 

## 1.5 数据库资产-查询

页面查询条件：点击选择框①，可筛选已存在数据库资产的数据库类型，在输入框②中输入资产名称关键字可查询到对应的数据库资产；默认查询条件为空展示的是多有的资产。可以手动输入或者选择需要展示的数据，点击查询，可以展示：

![þÿ](/images/operation/manage/assets/assets_10.png)

##  1.6 数据库资产-导入导出

点击页面中的按钮①，可对已添加的资产进行导入导出操作。导出所有：可选择导出所有来导出所有的数据库资产；

导出选中：也可勾选想要导出数据库资产后点击选中导出，导出选中的数据库资产；下载模板：点击下载模板，可下载以文档形式进行导入数据库资产的模板;

导入文件：可将填入内容后的模板导入分类分级系统中成为数据库资产。

如图所示：

![](/images/operation/manage/assets/assets_11.png)

![](/images/operation/manage/assets/assets_12.png)

 
