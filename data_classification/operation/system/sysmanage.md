# 2. 系统管理

 系统管理模块主要是分为：系统安全、部署管理、日志管理、设备管理、系统升级、系统信息模块，对我们产品最基本的操作进行维护和记录，实时更新操作信息数据。

## 2.1 系统安全

### 2.1.1 安全等级 

点击页面右上角系统设置按钮①，选择系统管理②下的系统安全③，可进入系统安全界面；安全等级有默认的高中低三种，用户也可自定义选择各个条件组合成适合自己的安全策略。更改配置后需要点击下方保存按钮才可生效。

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_1.png)



![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_2.png)

1、密码过期时间：选项为 7 天、14 天、21 天、28 天、3 个月、6 个月、12 个月、永不过期。选择具体值 X 天，包括当前时间 X 天后，密码过期，此时打开登录界面，输入用户名密码，页面会跳转到强行修改密码界面，必须使用新密码才可以继续登录。

2、密码复杂度：修改密码时，新密码必须要满足设置的复杂度才可修改成功。

高（密码长度不小于15位，需要由数字、大写字母、小写字母或其他特殊符号当中的三种以上组成）

中（密码长度不小于12位，需要由数字、大写字母、小写字母或其他特殊符号当中的两种组成）

低（密码长度不小于8位，需要由数字、大写字母、小写字母或其他特殊符号当中的一种组成）

3、系统防火墙：防火墙指定了开放的端口，对于指定端口之外的不能建立连接。指定开发的端口为：22、80、8443、443、9999（端口需要确认），除此之外其他端口如果需要建立连接需要关闭防火墙或者在开放端口中加入。建议为了设备安全不要轻易关闭系统防火墙。

4、连续登陆失败：默认为3次，不可修改。连续登录失败超过该次数后，会禁止登录。与锁定时间配合使用。

5、锁定：默认为60秒，不可修改。禁止登录后需要等待超过该时间秒数后才能再次登录。

6、界面：默认为1800秒，不可修改。预防用户长时间离开，信息泄露，判断界面在该时间内没有操作就会超时退出。

### 2.1.2 黑白名单

 为了控制具体的PC端IP登录的权限，用户可采用黑白名单的方式。双层保障信息不会被泄露，即使密码被泄露，但PC端IP无登录权限也无法使用。用户可配置平台所有的管理员子用户使用的PC端IP进行白名单配置。这样除了配置的IP外，在其他PC端就不能进行登录，比如配置192.168.0.1为白名单，成功后，只有使用该IP的客户端才能登录数据安全分类分级界面或者可配置黑名单IP，指定哪几个IP不能登陆，比如配置192.168.0.1为黑名单，成功后，使用该IP无法登录数据安全分类分级界面。

输入黑白名单时可输入IP段（IP段的格式为：1.1.1.1-1.1.1.10），黑白名单中可同时存在单个IP和IP段

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_3.png) 

注：以黑名单优先，比如黑名单设置 1.1.1.1-1.1.1.10，白名单设置 1.1.1.2，那么白名单设置无效，1.1.1.2IP还是不能登录。

## 2.2 部署管理

点击系统设置按钮①，选择系统管理②下的部署管理③，可进入部署管理页面；管理口配置是对管理口的各项网络信息，包括 IP、子网掩码、网关、DNS 等进行配置。网络测试可以检测 ip 是否可用（无人使用的 IP 为可用 IP，正在被使用的 IP 为不可用 IP），网关是否能连通，帮助用户判断是否可以修改管理口信息。

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_4.png)

 ![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_5.png)

注：修改 IP 时，应保证所修改的网段与修改前的网段网络可达，避免修改时占用了正在使用的

## 2.3 日志管理

### 2.3.1  系统日志

 点击系统设置按钮①，选择系统管理②下的日志管理③，可查看分类分级系统的日志。在日志类型选择下拉框中选择系统日志，系统安装后的所有系统日志

 ![](C:\Users\User\Documents\GitHub\data_classification\images\operation\dc\system\sysmanage\sysmanage_6.png)

![](C:\Users\User\Documents\GitHub\data_classification\images\operation\dc\system\sysmanage\sysmanage_7.png)

系统日志主要记录一些重要操作日志。包括操作时间系统日志类型，时间内部评定等级，操作结果以及动作描述。

 ![](C:\Users\User\Documents\GitHub\data_classification\images\operation\dc\system\sysmanage\sysmanage_8.png)

系统日志筛选支持时间范围筛选以及日志类型，时间登记的筛选或者查询。

点击右上角导出按钮，可以将操作日志以默认为 excel 的格式进行导出，并且导出也是支持带条件的导出，时间范围选择或者搜索框输入条件之后，点击导出即可。

### 2.3.2 操作日志

在日志类型选择下拉框中选择操作日志，系统安装后的所有操作日志

![](C:\Users\User\Documents\GitHub\data_classification\images\operation\dc\system\sysmanage\sysmanage_9.png)

操作日志主要记录何用户在何 ip 在何时间在对什么模块进行了什么操作。

![](C:\Users\User\Documents\GitHub\data_classification\images\operation\dc\system\sysmanage\sysmanage_10.png)

操作日志支持时间范围内日志的筛选以及对用户名、ip 以及模块名称的查询。

点击右上角导出按钮，可以将操作日志以默认为 excel 的格式进行导出，并且导出也是支持带条件的导出，时间范围选择或者搜索框输入条件之后，点击导出即可。

## 2.4 设备管理

点击系统设置按钮①，选择系统管理②中的设备管理③，可进入设备管理界面；该功能模块只要是展示，磁盘空间，CPU 和内存，设备管理功能主要是启动、关闭、恢复出厂、业务数据清除，数据维护：备份、清除、恢复等操作。

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_11.png)

### 2.4.1 监控墙

 监控墙可对后台资源包括磁盘空间、内存使用率、CPU使用率进行监控 

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_12.png)

 可在磁盘空间界面查看磁盘的使用率百分比、数据盘总量数据及剩余空间百分比、系统盘总量数据及剩余空间百分比

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_13.png)

 

 在 CPU 和内存界面可以查看 CPU 和内存的实时使用百分比

 ![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_14.png)

### 2.4.2 设备管理

 在设备管理界面，通过点击按钮来可以直接的进行设备的重启、设备的关闭、恢复出厂设置以及清除业务数据操作

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_15.png)

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_16.png)

 **注：进行设备的重启、设备的关闭、恢复出厂设置以及清除业务数据操作时都需要输入登录密码。**

### 2.4.3 数据维护

提供用户在页面进行数据备份、数据清理、数据恢复的功能

 ![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_17.png)

1、数据备份主要针对系统日志和操作日志进行备份，同时可选择需备份数据的时间段

 ![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_18.png)

2、数据清理针对系统日志和操作日志进行清理，同时也可选择时间段进行清理

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_19.png)

3、数据恢复可以将备份的数据恢复到系统中，但文件格式只能为 zip 格式、文件大小不能超过 500M

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_20.png)

## 2.5 系统升级

点击系统设置按钮①，选择系统管理②中的系统升级③，可进入系统升级界面；该模块可以提供用户在前台进行升级的能力，用户可以直接上传升级包来进行数据安全分类分级系统的系统升级。页面展示图如下

 ![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_21.png)

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_22.png)

1、点击系统升级按钮①，会出现系统升级弹窗，上传的升级包只能是 zip 格式，且文件的大小不能超过 500M，且对升级包名称有要求，否则升级包无法上传成功，无法进行系统升级。上传完成后，点击升级按钮，会出现确认弹窗，点击确认后开始进入系统升级 ![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_23.png)

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_24.png)

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_25.png)

**注：为保证升级成功，系统的内存、CPU、磁盘使用率应小于 70%，否则会升级失败**

2、升级完成后，会展示升级后的信息：文件大小、更新时间、版本信息；

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_26.png)

3、点击回退按钮①，若没有上一个版本的信息，则无法回退，若存在上一个版本，则会有版本回退确认弹窗：

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_27.png)

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_28.png)

4、点击下载最新升级日志①，可以下载最新的系统升级及系统回退日志 TXT 文件，页面下方简介展示历史系统升级及系统回退的升级及操作结果。

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_29.png)

![](/data_classification/images/operation/dc/system/sysmanage/sysmanage_30.png) 
