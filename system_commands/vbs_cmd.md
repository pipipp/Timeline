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
obj.SendKeys "^{ESC}"  
Wscript.Sleep 50  
obj.SendKeys "^{ESC}"  
loop  
