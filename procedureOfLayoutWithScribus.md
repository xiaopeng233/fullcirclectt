# Introduction #

FCCTT-Scribus排版流程简介


# Details #

可以参考这个文档：

http://blog.oppih.dotcloud.com/?p=337

这是一个图片：FCCTT 排版工作流程( 2010.7 ).jpg

https://mail.google.com/mail/?ui=2&ik=f7f56c07a2&view=att&th=12ae0b1720229d5f&attid=0.2&disp=inline&realattid=f_gdpipci51&zw

原始odt文件在这里：

https://mail.google.com/mail/?ui=2&ik=f7f56c07a2&view=att&th=12b65f173dfe70a5&attid=0.1&disp=attd&realattid=f_geqixte12&zw



排版小组目前采用的方式可以参考附件《FCCTT 排版工作流程( 2010.7 )》。这个流程没有全部实现。但是我个人已经按照这个流程在做了，以后会在排版小组中推广的。

这个流程的好处是：

1、组员排版灵活：

各组员只需要将自己负责的part（一定范围的页）排版好。可以用自己喜欢的方法完成排版。


2、整合方便：

由于scribus支持从另外一个sla文件导入页面的功能，所以整合时，只需要将不同组员完成的页导入到一个文件，就完成了排版文件的初步整合。


3、数据安全：

利用svn的功能，可以将每次修改过程记录到svn电子仓库中，如果本次修改错了，可以从电子仓库中取回（回溯）以前某次修改的版本，继续修改。


4、知识共享：

将排版文件放入google code svn中，以后排版成员可以从google code svn中查看以前排版源文件，学习他们是如何排版的。加上wiki中对排版经验的总结，可以快速上手排版。另，每次svn提交时记录了提交comment，这些说明中也带有解决方法，也算是一种知识共享。


# 排版如何同步？ #
同步了，能加快出版速度。也能最大程度节省大家的排版时间。

这就要求公共模板能快速产生、翻译文本的格式化能和公共模板同时发布。排版前，每个人从svn上下载公共模板和文章文本，经过协商，每位排版员负责指定页。完成后，每位排版员将自己的sla文件提交到svn,组长将这些页合并得到第一次整合后的sla文件;导出成pdf，发布给fcctt社区和排版组校对人员以获得反馈。经过2次循环,达到可以发布的程度。


这里涉及到的资源：

公共模板、翻译文本、字体包。


# scribus使用的版本 #

还是用1.3.3.13版本。如果官方的apt-get库中发布了新的稳定版本，那么可以用新版本。如何克服这个版本存在的问题（中文复制、粘贴、断行）？

There are many ways to place text in Scribus. Here is one way.

# 如何从外部文本文件导入纯文本 #
1. Make a large text frame<br>
2. Right click inside the text frame.<br>
3. Click on "Get Text" in the window that appears.<br>
4. Select the .txt file you want to get. The file name should appear in the File Name<br>
box. Click on OK. The first part of the text should appear in the frame.<br>
5. Since you are importing many pages of text you will have to place text frames on<br>
other pages and link the frames so the text flows to the other frames.<br>


<h1>如何从word文档导入带格式的文本</h1>
首先用openOffice打开word文档，另存为odt格式。<br>
在scribut中导入odt文档，就可以了。scribus不能直接导入带格式的word文档。但是oo能导入word的格式，scribus又能导入带格式的oo文档。