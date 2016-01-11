# Introduction #

如何使用svn工具kdesvn进行源文件排版协作的流程。

# Details #
> 注意：这里以issue32期位例。

  1. 浏览器打开网址http://code.google.com/p/fullcirclectt/source/checkout

> 2、安装好svn的一个客户端“kdesvn”。在命令行终端中cd到你pc上的任意一个空目录中；执行命令行svn checkout https://fullcirclectt.googlecode.com/svn/trunk/ fullcirclectt --username youEmail@gmail.com。这样能将文件下载到你本地。

> 3、进入下载后的“issue32\_zh-CN”目录，用scribus编辑属于你的文件。

> 4、每次完成编辑后，用kdesvn打开“issue32\_zh-CN”目录，点击kdesvn的commit按钮。在提示对话框中输入你的youEmail@gmail.com和密码（在http://code.google.com/p/fullcirclectt/source/checkout的googlecode.com password链接处点击后获得密码），就能提交你的修改到google code svn。


上面提到的“你的文件”，指第32期英文sla文件，排版人员可以根据自己喜好，在自己电脑上命名为各种名字。如

Li.Ci： I32P34-42[CN](CN.md).sla  (p 34-42)

fwoncn： issue32\_fwoncn\_1-18.sla  (p 1-18)

kjpioo： issue32\_fwoncn\_1-18.sla  (p 19-33)

daniel： 校对
王殿进： 校对


# 使用scribus进行排版存在的实际问题（多人排版时） #

我上一个邮件中说的“导致本地文件被覆盖”的问题，是因为排版文件.sla是纯文本，用类似xml的格式存储，信息量很大，一次scribus的修改操作，可能导致sla文件的多处改变。所以如果大家都去修改一个google code svn上的sla文件，那么edit conflict时，不能轻易对比和合并冲突。

单人排版时不会有这些问题。


## 所以我们采取了一些措施，来避免复杂的sla格式 ##

1、组员只负责完成指定范围页面的排版。

2、最后的人工整合：最后组长完成各部分的整合（scribus的页面导入功能就非常适合于整合）

3、排版时，不同责任人不对同一个sla文件进行提交：为了排版需要，在google code上，组员可以开辟自己的branch，对自己的sla进行排版、提交。完成后可以通知组长（整合），组长从branch中获取相应排版文件。