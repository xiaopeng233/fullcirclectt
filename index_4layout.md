# 摘要 #
排版过程涉及到很多细节问题，其解决方案可以被总结归类成为文档，方便排版时参阅。本文档就是FC中文翻译团队（fcctt）排版组的排版经验总结。

本指南关注以下几个话题：






# FC中文翻译团队之排版组工作指南 #


## 工作流程 ##
### 排版模式 ###
  * 可以单人排版，也可以协作排版。协作时人数不超过3人为佳。
### 排版流程（顺序、计划和截止日期） ###
  * 从wiki得到中文文本-->排版（录入、排版、生成pdf）-->pdf勘误-->修订排版（Alpha、Beta阶段）-->发布pdf。
  * 每期排版需要一名主排人员，作为这次排版主要负责人。每期排版应该制定排版计划，拟定期限。计划还需要包括排版后的“校对和修改”人员安排。
  * 排版期间需要保持沟通，及时反馈和解决疑难问题。适当督促进度。

## 具体问题 ##
### 脚本和文本预处理 ###
  * scribus\_space\_del.py（附件，作用是防止文本空白、短横线导致断行）
  * 文本预处理见http://oppih.realax.me/?p=449
### scribus排版技巧FAQ ###
  * Q：”Q来A去“排版时需要翻译成“问来答去”吗？
    * A：不需要。另外，文章中每个问题都以Q开始，回答都以A开始，这个字母也不需要在排版中改成"问","答"。这个排版组没有讨论过，我认为用Q，A，页面更美观。

  * Q：有的中文在scribus后，段落中显示出非自然断行，怎么办？
    * A：原因是中文文字中有空格，没有使用正确的scribus插入式空格（可以通过xxxxxxx的方式插入）。或者改用预处理过的翻译文本。

  * Q：母页下面的Full Circle Magazine如何改成中文？
    * A：编辑->编辑母页->(选中sla文件的cover层)开始编辑。完成编辑后直接关闭母页图层编辑对话框。

  * Q：如何插入链接：
    * A：
      1. 在“故事编辑器”中设置文本颜色为“HTML蓝色”，退出故事编辑器
      1. 找到工具栏一排图标处的两个黑色脚印的“链接”图标（有时候显示为一个黄色纸张的“pdf文本”按钮），选择黑色脚印的图标。这时候在需要设置链接的文本上方点击，出现红点。调整红点大小成为蓝色虚线框，直到覆盖链接文字。最后在上面右击右键，选择“pdf选项”->"注释属性"。在弹出窗口中输入要链接的目标地址。就能完成scribus中链接的添加了。

  * Q：如何编辑“编辑寄语”页的右侧的“本杂志基于以下软件创建”以及“什么是Ubuntu”部分？
    * A：选中图层“Created using”，点击“编辑寄语”页的右侧文本框编辑。38期(?)开始“什么是Ubuntu”已经从杂志中删除了。

  * Q：如何编辑母页？
    * A：编辑页眉页角，可通过：“编辑－>母页...”，这时默认显示为“编辑母页”的“普通”，不需更改。在母页的“图层”中选择“cover”图层即可编辑母页。

  * Q：如何从其他sla文件导入排版内容？
    * A：当分工完成不同页面的时候，最终需要把各部分整合到一个文件中，这就需要scribus的”导入“功能：页面->导入->选择“来自文档”和导入页。具体导入选项有多中，请根据实际情况选择。

  * Q：sla导出成pdf需要注意什么？
    * A：
      1. 首先设定杂志信息：在菜单中选择“文件->文档设置”，选择“文档信息”，填写“标题”为
```
FullCircle 中文杂志 第##期
```
作者为
```
FullCircle 中文团队
```
描述为
```
http://www.fullcirclemagazine.org
http://fcctt.org/
```
      1. 在“进一步信息->日期”中填写发布日期。
      1. 接着生成PDF文件：在菜单中选择“文件->导出->保存为PDF->忽略错误”，在“常规->文件选项”中，选择“生成缩图”；在“字体->嵌入的字体”中，只选择需要嵌入的字体显示到“Fonts to outline”中。保存。

  * Q：如何重用往期杂志的文字样式？
    * A：进入样式编辑器，点击“导入” -- 选择样式来源sla文件 — 确定。更多关于排版复用的话题，请参考这里（附件《排版复用探讨》）。

  * Q：如何让一篇文章占据多页，让文字能自然排布
    * A：“让文字能自然排布”的意思是，当前面的文字增/删后，多页之间的文字能自动调整前后位置。注意这里的文字是放在不同文本框中的，且属于同一篇文章。请研究一下scribus软件工具栏处的“串联文本框”和“解链文本框”按钮的用法。

### 字体和段落样式 ###
  * 排版所需要的字体，参考附件《fcm\_fonts.rar》。
  * 段落样式，参考“3.2  sla公共模板、公共文字”部分。

### 排版校对 ###
  * 任务
> > 校对人员需要通读pdf上的文章，发现pdf的部件的位置、文字、语句是否正确。对发现的问题修改后，重新生成pdf，再次发布校对。
  * 校对方式
    1. 首先，排版组成员自己粗略校对一次，查看是否存在重大问题并全部改正。
    1. 接着，发送校对邮件到，请大家参与校对，等待大家捉虫后反馈问题，排版人员进行修正。
    1. 反复校对两轮，得到Alpha、Beta版，经过排版负责人或者团队相关负责人审核，最终发布杂志。



## 排版文件 ##
### 排版成员名单 ###
  * 专门网页，保存了翻译人员和排版人员名单(?)。
### sla公共模板、公共文字 ###

> 每次排版时使用的文字样式都从模板文件“fcm\_cn\_public\_style.sla”导入，公共文字都从“fcctt排版可复用文字.txt”复制。
  * 模板：附件《fcm\_cn\_public\_style.sla》
  * 公共文字：《fcctt排版可复用文字.txt》

### FAQ ###
参考：[排版常识](http://code.google.com/p/fullcirclectt/wiki/publishing_common_sense)，不断更新。



## 加入排版，获得帮助 ##
### 订阅邮件列表 ###
  * 通过邮件申请加入排版
> 发送申请到fullcircle\_clt+subscribe@googlegroups.com，我们会给你发送《排版新人入门指南》。
    * 订阅失败会提示：Subscribus\_fail.jpeg，订阅成功会提示：subscribus\_ok.jpeg。
  * 如何订阅
> 发邮件至 fullcircle\_clt+subscribe@googlegroups.com；
  * 如何退订
> 发邮件至 fullcircle\_clt+unsubscribe@googlegroups.com。成功订阅后会有如下提示：
```
 CODE
```
  * 有任何疑问，订阅者还可发送邮件至fullcircle\_clt@googlegroups.com获得订阅帮助。



## 软件和工具 ##
### scribus排版软件 ###
  * 软件安装和软件版本
> 参考[如何安装Scribus软件](http://code.google.com/p/fullcirclectt/wiki/scribus_setup_howto)和[使用Scribus](http://code.google.com/p/fullcirclectt/wiki/procedureOfLayoutWithScribus)。
  * 排版协作平台使用
> 排版时用svn/hg作源文件管理工具，hg的使用方法请参考[用Mercurial进行源文件排版协作](http://code.google.com/p/fullcirclectt/wiki/CorperateWithMercurialVCS)
  * 上传/下载杂志
> 可以在[fc中文杂志下载地址](http://code.google.com/p/fullcirclectt/downloads/list)上传/下载pdf文档，在[fc中文杂志源文件](http://code.google.com/p/fullcirclectt/source/browse/)commit/checkout排版源文件。



## 附件 ##
  1. fcctt排版可复用文字.txt [fcctt排版可复用文字](http://blog.163.com/kjpioo2006@126/blog/static/890131442010113102041571/).
  1. fcm\_cn\_public\_style.sla
  1. 使用这个文件作为样式来源：[排版样式模板](http://code.google.com/p/fullcirclectt/source/browse/issue38_zh-CN/issue38.sla).
  1. fcm\_fonts.rar [http:// 排版使用的字体下载].
  1. 《排版复用探讨》