# pyinstaller安装和使用说明

## 基本命令
* [ pyinstaller ./{py文件名} ]         - 效果是有一堆的依赖文件在dist文件夹下  
* [ pyinstaller -F ./{py文件名} ]      - 在dist文件夹下只生成一个exe文件  
* [ pyinstaller -c ./{py文件名} ]      - 创建一个命令行程序（就是那个小黑框），这是默认的选项  
* [ pyinstaller -w ./{py文件名} ]      - 不弹出命令行  
* [ pyinstaller -i ./{py文件名} ]      - 为程序指定一个图标，需要跟上图标的路径（在命令的末尾添加-i test.ico）  

## 打包一个py脚本程序
进入打包文件所在的路径打开Powershell，输入指令：  
pyinstaller -F -w main.py

## 打包多个py脚本程序
进入打包文件所在的路径打开Powershell，输入指令：
1. pyinstaller -F main.py
2. 删除其他打包后的文件，只保留`setup.spec`文件
3. 编辑`setup.spec`文件
4. 编辑完毕后，使用pyinstaller -F setup.spec，生成文件在dist目录

**setup.spec文件修改位置**
* 添加`py_files`列表，包含项目需要的所有python脚本，例：['1.py', '2.py']
* 添加`pathex`列表，包含项目用到的所有python脚本路径
* 添加`datas`列表，包含涉及到的所有资源文件，每个文件是以元组的形式存放，例：[('images\\\\happy.ico', 'images'), ('images\\\\*.jpg', 'images')]
* `name`='Tool'，制定可执行程序名字
* `console`=False，制定可执行程序执行时不显示控制台窗口
* `icon`='C:\Users\15057\Desktop\FlappyBird\images\flappy.ico'，设置程序图标，使用绝对路径，ico格式为（16*16）

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

# python开启网络服务（有效端口号：1024-65535）
* 进入要共享的文件夹下打开Powershell输入指令开启网络服务，例：python -m http.server

将会开启一个 http://0.0.0.0:7777/ 的网络服务  
在同一个网络内的设备可以打开浏览器输入（**共享文件的电脑IP地址:端口号**）进入共享的文件夹，预览并下载文件  
