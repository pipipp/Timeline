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
value = msgbox("Confirm stop?", vbOkCancel, "Stop Window")  
if value=vbOK Then  
    Set obj = CreateObject("Wscript.Shell")  
    obj.run "taskkill /im wscript.exe /f", 0  
End if 

## 循环模拟点击键盘（1000等于1秒）：  
value = msgbox("Confirm open?", vbOkCancel, "Run Window")  
if value=vbOK Then
    Set obj = CreateObject("Wscript.Shell")  
    do while true    
    Wscript.Sleep 1000*120  
    obj.SendKeys "{numlock}"  
    Wscript.Sleep 50  
    obj.SendKeys "{numlock}"  
    loop  
End if  

## 模拟打开IE浏览器，输入网址，循环点击
value = msgbox("Confirm open?", vbOkCancel, "Run Window")  
if value=vbOK Then  
	set obj=WScript.CreateObject("WScript.Shell")  
	app=obj.Run("iexplore")  '打开IE浏览器  
	WScript.Sleep 1000  '停顿1000毫秒即1秒  
	obj.AppActivate app  
	obj.SendKeys "+{TAB}"  '移动光标到浏览器地址栏  
	obj.SendKeys "https://www.baidu.com"  '输入网页地址  
	obj.SendKeys "{ENTER}"  '按回车键  
	Do while true  
	Wscript.Sleep 10000  '10秒刷新一次  
	obj.SendKeys "{F5}"  '按F5刷新页面  
	Loop  '开启无限循环  
End if  