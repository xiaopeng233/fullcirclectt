# Introduction #

如何使用mercurial进行源文件排版协作的流程。

# Details #
> 由于只有排版的结果文件有必要提交到服务器上，而排版过程中的一些小改动都不需要提交。在这种模式下，使用svn时为了保持更改，需要不断向服务器提交修改；或者在本地建立svn仓库，先提交到本地，排版完成后再把结果文件提交到服务器，但是这样需要额外建立一个svn仓库，很麻烦。所以使用svn不是一个最好的选择。目前Google Code支持Mercurial进行VCS，Mercurial支持离线提交，替代了svn在本地建立仓库的麻烦，所以我们在2011年1月开始，将服务器的版本管理方式改成Merurial（在“Analysis of Git and Mercurial”http://code.google.com/p/support/wiki/DVCSAnalysis中，Google Code团队对两个工具进行了分析比较，并解析选择Mercurial的原因）。
> 改用Mercurial后，从issue44\_zh-CN及之前的文件仍可用svn checkout，但是不再支持svn commit。

> 注意：这里以issue32期位例介绍如何用Mercurial辅助排版；并且只在命令行中操作（如果需要GUI方式，建议使用TortoiseHG，用法请自行摸索）。
  1. 浏览器打开网址http://code.google.com/p/fullcirclectt/source/checkout

> 2、获得排版文件：在命令行终端中cd到任意一个空目录中；输入命令行“hg clone https://fullcirclectt.googlecode.com/hg/ fullcirclectt”。这样能将排版文件下载到fullcirclectt目录中（该目录不需要预先建立）。等待完成下载。

> 3、进行排版，用scribus对你的issue32\_zh-CN目录下的sla文件进行排版。

> 4、保存修改：每次完成一个关键排版内容，在scribus中保存后，还要在本地的Mercurial仓库中保存：在命令行中切换到fullcirclectt目录，执行命令“hg commit”，按照提示行输入必要的信息，保存修改后可以通过“hg status”或“hg summary”或“hg log”查看是否保存成功。

> 4、提交修改：当你负责的排版任务完成时，可以将你的排版结果提交到服务器。在命令行中切换到fullcirclectt目录，执行命令“hg push https://fullcirclectt.googlecode.com/hg/”。如果提示输入用户名和密码，请输入你的youEmail@gmail.com和密码（项目成员的密码在http://code.google.com/p/fullcirclectt/source/checkout的googlecode.com password链接处点击后获得密码），就能提交你的修改到google code服务器。


上面提到的“你的文件”，指第32期英文sla文件，排版人员可以根据自己喜好，在自己电脑上命名为各种名字。如

Li.Ci： I32P34-42[CN](CN.md).sla  (p 34-42)

fwoncn： issue32\_fwoncn\_1-18.sla  (p 1-18)

kjpioo： issue32\_fwoncn\_1-18.sla  (p 19-33)

daniel： 校对
王殿进： 校对