# BAT Commands

## 关闭命令回显
1. `ECHO OFF` 关闭所有命令回显功能
2. `@`字符放在命令前将关闭该命令回显，无论此时echo是否为打开状态

## 加暂停
PAUSE

## 指定暂停时间：（30为暂停的秒数，其他都是必要项）
ping -n 30 127.1>nul

# VBS Commands

## 调用bat文件隐藏cmd框：
Set obj = CreateObject("Wscript.Shell")  
obj.run "cmd /c C:\Users\evan\Desktop\test.bat", vbhide

## 关闭指定的任务进程：
msgbox "确认关闭？"  
Set obj = CreateObject("Wscript.Shell")
obj.run "taskkill /im wscript.exe /f", 0

## 循环模拟点击键盘（1000等于1秒）：  
msgbox "确认打开？"  
Set obj = CreateObject("Wscript.Shell")  
do while true    
Wscript.Sleep 1000*120  
obj.SendKeys "{numlock}"  
Wscript.Sleep 50  
obj.SendKeys "{numlock}"  
loop  
