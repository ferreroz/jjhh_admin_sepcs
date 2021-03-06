### 品牌商管理后台 - 创建经销商账户

##### 页面布局说明(通用)
		管理后台的页面布局通用；
		头部高度固定；
		左栏高度等于浏览器高度减去头部高度；
		右侧内容区高度等于浏览器高度减去头部高度；
		右侧内容滚动显示。


##### 表单字符控制
基本信息

+   账户名： >=6 & <=20 个字节
+   密码： >=6 & <=20 个字节
+   所属品牌商： 自动关联当前品牌商名称，显示为静态文本。
+   公司名： >=10 & <=40 个字节
+   负责人： <=10 个字节
+   负责人手机号：<=20 个字节

<br />
对接人信息

+   对接人：  <=10 个字节
+   手机号： <=20 个字节
+   固定电话： <=20 个字节
+   Email： <=40 个字节
+   客服QQ： <=20 个字节（用作客服在线咨询QQ号）

<br />
门店信息

+   门店地址： <=60 个字节
+   电话：<=30  个字节

<br />
证件信息

+ 营业执照副本： 限jpg格式，文件大小不超过600kb。
+ 税务登记证： 限jpg格式，文件大小不超过600kb。

<br />
##### 内容规则

所属品牌商

		自动关联当前进行操作的品牌商账户，读取品牌商名称；
		不可选择其他。

所在地区

		第一级为直辖市和省；
		如果第一级为直辖市，第二级为直辖市下的行政区（包含“全市”选项），无第三级选项；
		如果第一级为省，第二级为城市（包含“全省”选项）；
		第三级为城市下的县级行政区（包含“全市”选项）。

400电话

		此行默认不显示；
		当用户选择所在地区后自动生成；
		分机号为所在区号（如果该区号下存在下一级地区经销商，则在区号后随机添加一个2位数的数字）。

门店信息

		可添加多个；
		点击添加按钮，验证当前两个文本输入框，验证通过后，将信息保存，并允许继续添加。
		
<br/>
##### 表单验证

+   必填项：效果图上标星号的字段。
+   当用户将光标移出当前文本输入框，验证字段有效性。
+   当输入框内字段长度超过字节限制时，显示提示信息块。具体内容为“您输入的内容过长”。
+   长度低于最小字节时，显示提示信息块。“请您正确填写”。
