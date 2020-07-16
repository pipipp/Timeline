# pyinstaller安装和使用说明

## 基本命令
pip安装完成后，进入要打包的py文件所在目录  
输入以下命令：  
* [ pyinstaller ./{py文件名} ]  # 效果是有一堆的依赖文件在dist文件夹下   
* [ pyinstaller -F ./{py文件名} ]  # 在dist文件夹下只生成一个exe文件  

## 问题排除
* 初次运行，可能会出现`failed to create process`，这是pip3的bug，路径的空格不能正常识别     
**解决方法：**   
进入`C:\Program Files\python\3.7\Scripts`，可以看到有一个`pyinstaller-script.py`和`pyinstaller.exe`    
文本编辑器打开`pyinstaller-script.py`，第一行的代码申明是这样的    
`#!c:\program files\python\3.5\python3.exe`   
加一个引号变成：`#!"c:\program files\python\3.5\python3.exe"`  
* exe编译失败  
UnicodeDecodeError:"gbk" codec can't decode byte 0xaa in position 160:illegal multibyte sequence    
解决方法：文件名改成英文

## 进阶命令  
* [ pyinstaller ./{py文件名} ]         - 效果是有一堆的依赖文件在dist文件夹下  
* [ pyinstaller -F ./{py文件名} ]      - 在dist文件夹下只生成一个exe文件  
* [ pyinstaller -c ./{py文件名} ]      - 创建一个命令行程序（就是那个小黑框），这是默认的选项  
* [ pyinstaller -w ./{py文件名} ]      - 不弹出命令行  
* [ pyinstaller -i ./{py文件名} ]      - 为程序指定一个图标，需要跟上图标的路径（在命令的末尾添加-i test.ico）    

**常用命令：** pyinstaller python.py -F -w -i test.io  

# python开启网络服务（有效端口号：1024-65535）
* [ python -m http.server 7777 ]    - 使用命令开启网络服务

电脑开启网络服务后，使用手机浏览器输入（**电脑IP地址:端口号**）可直接下载电脑内的文件  
