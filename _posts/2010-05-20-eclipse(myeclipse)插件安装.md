---
layout: post
category: Eclpse
tagline: "Supporting tagline"
tags: [Eclipse ,java]
---
{% include JB/setup %}

将Eclipse选作开发工具，对不同的应用要求需要导入不同的插件。对于插件的安装，很容易出现莫名奇妙的问题，有些问题的解决方法甚至Google不到。而就算找到的解决方案也许当时解决了，但或许有些运气的成分。因此，先将常用的插件安装方法总结如下(假设Eclipse安装目录：`C：\eclipse`)：

一、直接拷贝到相应文件夹
    解压下载的目标插件，分别将其文件夹下的features和plugins两个文件夹复制粘贴到Eclipse相应的文件夹下。重启eclipse即可。注意：直接将 插件包解压到`plugins`文件夹下之后，重启eclipse，可能不会加载新的插件。解决方法是：1、打开命令行，到当前eclipse的目录下，输入`eclipse-clean`，重新启动eclipse，这样eclipse就会加上新的插件了。2、如果还不行，则请将`eclipse\configuration\org.eclipse.update`目录删除后再启动eclipse。(这种方法很少成功过)

二、软件更新
    选择`Help > Software Updates > Manager Configuration`
再选择`Add > ExtensionLocation`找到你要安装插件的目录就可以了。使用eclipse的`help->SoftwareUpdates->Find and install... search for newfeatures...`输入软件安装地址。
 
三、Links安装
   a.查看`C:\Eclipse`文件夹下是否有links文件夹(没有新建一个)。
   b.将下载的插件解压到Eclipse文件夹下(假如下载的插件为a.b.all.zip)，目录结构如下`a.b.all->eclipse->features+plugins`(注意，解压出来的features和plugins这两个文件夹必须在eclipse下。)
   c.在links文件夹下新建一个文本文件，命名为a.b.all.txt,在文本中输入：
        `path=C：\\eclipse\\a.b.all`
注意：link文件中path=插件目录的path路径分隔要用\\或是/。
 
以上虽然总结了常用的安装方法，我认为最好的优先顺序是：2、3、1。
