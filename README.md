## 如何使用conda为Anaconda Python发行版设置虚拟环境   
> 虚拟环境是Python的一个命名的，隔离的，工作的副本，用来维护他的文件，目录和路径以至于你可以在不影响其他Python项目的情况下使用特定版本的库或者Python它本身。虚拟环境可以轻松的分开不同的项目并且可以避免不同依赖关系和跨版本组件要求所带来的问题。`Coda`是[Anaconda](https://www.anaconda.com/download/) Python发行版管理安装和虚拟环境配置的首选接口。如果你有一个普通的Python安装或者其他Python发行版请参照[virtualenv](http://virtualenv.readthedocs.io/en/latest/)   
> 
## 大纲  
***  
* 检查conda是否安装并可用  
* 必要时更新coda  
* 创建虚拟环境
* 激活虚拟环境
* 安装额外的Python包
* 禁用虚拟环境
* 删除虚拟环境  
## 连接路径  
***  
* 链接路径  

## 要求  
***  
* 安装并访问Anaconda Python发行版  
## 1. 检查conda是否安装在路径中  
***  
1. 打开终端客户
2. 将`conda -V`输入到终端命令行并按Enter
3. 如果安装了conda你将会看到类似下面的东西  
```  
$ conda -V  
conda 3.7.0  
```
## 2.检查conda是最新的  
***  
1. 在终端客户输入  
`conda update conda`  
2. 必要时通过键入`y`来进行更新包  
## 3.为你的项目创建一个虚拟环境  
***  
1. 在终端客户输入下面的代码，其中*yourenvname*是你想要调用的环境名称，并使用你想要使用的Python的版本来替换x.x（首先查看可用的Python版本列表，键入`conda search "^python$"`并且按回车。）  
`conda create -n yourenvname python=x.x anaconda`  
2. 键入`y`，这将在“path\_to\_your\_anaconda\_location/anaconda/envs/yourenvname”中安装Python版本和所有相关的anaconda包的库  
## 4.激活你的虚拟环境  
***  
1. 要激活或者切换到你的虚拟环境，只需要简单的键入下面代码，其中*yourenvname*是你在创建时给你环境取的名字 
`source activate yourenvname`  
2. 激活conda环境可以修改PATH和shell变量以指向你创建的特定的独立Python设置。这个命令提示将改变指向你当前正在使用的conda环境（yourenvname),要查看您所有的环境列表，可使用命令`conda info -e`
## 5.安装附加的Python包到虚拟环境中  
1. 要在虚拟环境中安装额外的包，请输入以下命令，其中yourenvname是您的环境名称，而*[package]*是您希望安装的包的名称。未能成功指定“-n yourenvname”将安装包到根Python安装  
`conda install -n yourenvname [package]`  
## 6.禁用您的虚拟环境  
***  
1. 结束当前环境的会话，键入下面的代码，没有必要去指定envname--当前激活的envname将被禁用，PATH和shell变量将恢复正常  
`source deactivate`  
## 7.删除不再需要的虚拟环境  
***  
1. 要删除conda环境，键入下面的代码，其中*yourenvname*是你想要删除的环境名称  
`conda remove -n yourenvname -all`  
## 相关信息  
Coda的官方信息可以在[这里](https://conda.io/docs/intro.html)
查找
