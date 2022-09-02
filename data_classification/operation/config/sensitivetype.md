# 2. 敏感类型配置

 敏感类型配置具有内置的敏感类型，并且用户可以按照自己的需求选择增加敏感类型。敏感类型列表的展示内容包括敏感类型名，系统属性（自定义、系统默认），分区方式（数据分区、制定分隔符），敏感类型示例，分区数，类别以及级别展示。操作包括修改敏感类型、查看详情以及删除。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_1.jpg)

 2.1 基本操作

### 2.1.1 敏感类型添加

 点击添加按钮①，可添加敏感类型，首先填写敏感类型名、行业分类（分类标准）、示例、扫描方式:指定分割符或数据分区；如果选择了指定分隔符扫描方式，示例将必须填写带有分隔符之后才能点击获取分区，然后选择或填写合适的分区匹配规则相关配置，点击添加，添加敏感类型。必填项之前标注了“*”。

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_2.jpg)

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_3.jpg)



 

1、扫描方式-指定分隔符：选择指定分隔符分区方式，并输入分隔符后，点击获取分区按钮①，获取分区信息。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_4.jpg)

例：输入以下示例可匹配所有的邮箱

| 类型名       | 电子邮箱                          |
| ------------ | --------------------------------- |
| 行业分类     | 通用标准                          |
| 示例         | [Andy@qq.com](mailto:Andy@qq.com) |
| 扫描方式     | 指定分隔符                        |
| 指定分隔符   | @                                 |
| A 区匹配规则 | 无校验                            |
| B 区匹配规则 | 数据字典（选择电子邮箱域名）      |

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_5.jpg)

2、扫描方式-数据分区：选择数据分区方式，出现分区设置。点击添加分区按钮①，添加分区设置，最大分区数为 26 个，最小分区数为 1。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_6.jpg)

3、数据分区-删除分区：点击数据分区右上角的关闭按钮，可以删除分区。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_7.jpg)

4、数据分区-数据分段方式-字符长度：数据分区方式可以获取多个分区，数据分段方式选择字符长度时，所有分区的总长度相加应等于示例的字符长度，否则无法校验成功。如下：

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_8.jpg)

5、数据分区-数据分段方式-以某字符结尾：数据分区方式可以获取多个分区，数据分段方式选择以某字符结尾时，可以通过示例中的某个字符将示例分开。如下：

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_9.jpg)

6、数据分区-数据分段方式-不指定：数据分区方式可以获取多个分区，数据分段方式选择不指定时，无需规则就可将示例分开。三种分段方式可组合使用。

7、匹配规则：七种可选择的匹配规则。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_10.jpg)



a、匹配规则-无校验：没有校验规则，任何数据都可匹配到该敏感类型。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_11.jpg)

b、匹配规则-正则匹配：需要输入正则表达式，对区间数据进行校验。例：输入以下示例可匹配所有以银行/分行/支行结尾的银行名称

| 类型名       | 银行名称                              |
| ------------ | ------------------------------------- |
| 行业分类     | 金融行业分类标准                      |
| 示例         | 中国建设银行分行                      |
| 扫描方式     | 数据分区                              |
| 数据分段方式 | 不指定                                |
| A 区匹配规则 | 正则匹配                              |
| 正则表达式   | [\u4e00-\u9fa5]{0,}?[银\|分\|支]?[行] |

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_12.jpg)

c、匹配规则-数据字典：选择数据字典，对区间数据进行校验。例：输入以下示例可匹配所有学历

| 类型名       | 学历             |
| ------------ | ---------------- |
| 行业分类     | 金融行业分类标准 |
| 示例         | 本科             |
| 扫描方式     | 数据分区         |
| 数据分段方式 | 不指定           |
| A 区匹配规则 | 数据字典         |
| 数据字典     | 学历             |

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_13.jpg)



d、匹配规则-包含：选择包含内容，匹配区间数据是否包含选中的内容。例：输入以下示例可匹配所有车牌号

| 类型名       | 车牌号                         |
| ------------ | ------------------------------ |
| 行业分类     | 通用标准                       |
| 示例         | 粤 B·11111                     |
| 扫描方式     | 数据分区                       |
| 数据分段方式 | 不指定                         |
| A 区匹配规则 | 包含                           |
| 包含内容     | 数字、大写字母、中文、特殊字符 |

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_14.jpg)

e、匹配规则-等于：输入关键字，匹配区间数据是否等于关键字。例：输入以下示例可匹配到性别

| 类型名       | 性别             |
| ------------ | ---------------- |
| 行业分类     | 医疗行业分类标准 |
| 示例         | 男               |
| 扫描方式     | 数据分区         |
| 数据分段方式 | 不指定           |
| A 区匹配规则 | 等于             |
| 关键字       | 女,男            |

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_15.jpg)

f、匹配规则-区间：选择区间类型，并填写区间值，匹配区间数据是否属于设置的区域。例：输入以下示例可匹配到日期

| 类型名       | 交易日期         |
| ------------ | ---------------- |
| 行业分类     | 金融行业分类标准 |
| 示例         | 20220610         |
| 扫描方式     | 数据分区         |
| 数据分段方式 | 不指定           |
| A 区匹配规则 | 区间             |
| 区间类型     | 日期             |
| 日期格式     | yyyyMMdd         |

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_16.jpg)

g、匹配规则-其他敏感类型：选择其他敏感类型。例：输入以下示例可匹配到姓名

| 类型名       | 投资人           |
| ------------ | ---------------- |
| 行业分类     | 金融行业分类标准 |
| 示例         | 张三             |
| 扫描方式     | 数据分区         |
| 数据分段方式 | 不指定           |
| A 区匹配规则 | 其他敏感类型     |
| 其他敏感类型 | 姓名             |

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_17.jpg)

5、扫描方式-字段名称：可以输入完整字段名称或字段名称中的部分内容，多个字段名称用逗号“,”隔开。进行敏感数据匹配时，若匹配到完整的字段名称，则匹配到为 100%；若匹配到一个字段名称中的部分内容，则匹配率为 33%；若匹配到三个或三个以上的字段名称中的部分内容时，匹配率会变为 100%

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_18.jpg)
6、敏感类型-添加校验：输入敏感类型信息，并设置各分区的校验规则后，点击校验按钮①，可以对各区间数据进行匹配，并弹出校验结果。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_20.jpg)

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_21.jpg)

7、添加时可点击左上角上一步按键，可退回到敏感类型配置页面

### 2.1.2   敏感类型-删除

 勾选需要删除的敏感类型后点击删除按钮①，可删除自定义敏感类型，内置敏感类型无法删除，删除时有确认提示，如下图所示：

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_22.jpg)

![image-20220809110438047](/../../../AppData/Roaming/Typora/typora-user-images/image-20220809110438047.png)

### 2.1.3 敏感类型-修改

 点击列表右侧的修改操作图标①，进入编辑页面，可进行相关信息的修改。部分内置敏感类型不可修改②。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_23.jpg)

###  2.1.4 敏感类型-查询

 在所属行业下拉框①中选择配置标准类型，敏感类型框②中输入敏感类型名称，点击查询按钮③，可查询到关联内容，点击重置按钮④，即可以清空所属行业框和类型名输入框的查询内容。

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_24.jpg)

### 2.1.5 敏感类型-详情

 点击列表右侧的详情操作图标①，打开敏感类型校验详情展示弹窗。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_25.jpg)

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_26.jpg)

2.1.6敏感类型-导出

 点击页面右上角按钮①，选择导出所有②，即可以 Excel 文档格式导出所有敏感类型

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_27.jpg)

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_28.jpg)

### 2.1.7 敏感类型-导入

1、下载模板：点击页面右上角按钮①，选择下载模板③，即可下载可以导入分类分级系统的文件模板

2、导入文件：工具模板提示编写敏感类型后，点击页面右上角按钮①，选择导入文件②，即可将已完成的文件导入到分类分级系统中

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_29.jpg)

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_30.jpg)

## 2.2 数据字典

点击敏感类型自动发现列表右上角的数据字典按钮①，进入数据字典管理页面。 ![image-20220809112718629](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_31.jpg)

数据字典：本功能用于自定义敏感类型校验-匹配规则为数据字典使用，系统有内置数据字典，用户可以对数据字典进行增删改查（内置的数据字典不能删除与修改）。

数据字典内容：本功能用于为指定的数据字典增加、修改、删除数据字典内容。对内置的数据字典一样会有内置的数据字典内容，用户可以对数据字典内容进行增删改查（内置的数据字典内容不能删除、修改、添加）

  ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_32.jpg)

### 2.2.1   数据字典-添加

 点击数据字典列表左上角的添加按钮①，打开添加弹窗，输入正确的字典名称与描述，然后点击确定按钮进行添加。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_33.jpg)

 

### 2.2.2 数据字典-删除

 选择自定义的数据字典，点击列表左上角的删除按钮①，进行删除。内置的数据字典不可删除。删除时有弹窗提示。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_34.jpg)

 

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_35.jpg)

###  2.2.3 数据字典-修改

 点击列表右侧的修改图标①，打开修改弹窗，进行数据字典名称与描述的修改。内置的数据字典不可修改②。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_36.jpg)

 

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_37.jpg)

### 2.2.4 数据字典-查询

 在输入框中①输入数据字典名称，点击查询按钮②，可查询的指定内容

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_38.jpg)

### 2.2.5 数据字典内容-添加

点击数据字典内容列表左上角的添加内容按钮①，打开添加弹窗。

 ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_39.jpg)



![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_40.jpg)
添加方式-手动添加：

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_41.jpg)

添加方式-文件添加： ![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_42.jpg)

### 2.2.6 数据字典内容-删除

 选择数据字典内容，然后点击数据字典内容左上角的删除按钮①，进行内容删除。内置数据字典内容无法删除。删除时有弹窗提示。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_43.jpg) 

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_44.jpg)

 

2.2.7 数据字典内容-修改

点击列表右侧的修改图标①，进行内容修改。

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_45.jpg)



![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_46.jpg)

###  2.2.8  数据字典内容-查询

在输入框①输入数据字典内容，点击查询按钮②，可查询到指定内容

![](/data_classification/images/operation/dc/config/sensitivetype/sensitivetype_47.jpg)
