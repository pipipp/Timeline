# DOS Commands

## 基本命令：
* [ dir ]                         - 查看当前所在目录的文件和文件夹【dir /w 以紧凑方式显示，dir /a 显示并包括隐藏文件】  
* [ cd  ]                         - 进入指定的目录【cd\ 退回根目录，cd.. 退回上一级目录】  
* [ cls ]                         - 清除屏幕内容  
* [ tasklist ]                    - 显示所有任务进程  
* [ taskkill /im python.exe /f ]  - 根据进程名选择删除  
* [ taskkill /pid 11111 ]         - 根据进程ID选择删除  

## 创建文件命令：
* [ md ]          - 创建文件夹【md sample 创建名字为sample的文件夹】  
* [ rd ]          - 删除文件夹【rd sample 删除名字为sample的文件夹】  
* [ type ]        - 可用于创建空文件【type nul > text.txt 创建一个空的text.txt文件】  
* [ echo ]        - 可用于创建非空文件【echo hello > text.txt 创建一个包含hello文本的文件】  
* [ \> ]          - 写入格式保存命令结果到文件中【ipconfig >> text.txt 保存ipconfig命令的结果到text.txt文件中，如果文件存在会被覆盖】  
* [ \>> ]         - 追加格式保存命令结果到文件中【ipconfig >> text.txt 保存ipconfig命令的结果到text.txt文件中，如果没有该文件会自动创建】  

## 转移文件命令：
* [ copy ]        - 复制文件【copy sample.txt C:\Users\Desktop\sample.txt 复制当前目录下的sample.txt到桌面】  
* [ move ]        - 移动文件【move sample.txt C:\Users\Desktop\sample.txt 移动当前目录下的sample.txt到桌面】  

## 修改文件命令（del不能删除文件夹）：
* [ rename ]      - 重命名文件【rename sample.txt 123.txt 重命名sample.txt为123.txt】  
* [ del ]         - 删除文件【del sample.txt 删除sample.txt】  
* [ del *.* ]     - 删除当前目录下的所有文件  
* [ deltree ]     - 删除文件夹和它下面的所有子文件，递归删除，要谨慎使用  

## 显示文件命令：
* [ type ]        - 显示文本文件【type sample.txt 打开sample.txt文件并显示内容】
