# pyinstaller��װ��ʹ��˵��

## ��������
pip��װ��ɺ󣬽���Ҫ�����py�ļ�����Ŀ¼  
�����������  
* [ pyinstaller ./{py�ļ���} ]  # Ч������һ�ѵ������ļ���dist�ļ�����   
* [ pyinstaller -F ./{py�ļ���} ]  # ��dist�ļ�����ֻ����һ��exe�ļ�  

## �����ų�
* �������У����ܻ����`failed to create process`������pip3��bug��·���Ŀո�������ʶ��     
**���������**   
����`C:\Program Files\python\3.7\Scripts`�����Կ�����һ��`pyinstaller-script.py`��`pyinstaller.exe`    
�ı��༭����`pyinstaller-script.py`����һ�еĴ���������������    
`#!c:\program files\python\3.5\python3.exe`   
��һ�����ű�ɣ�`#!"c:\program files\python\3.5\python3.exe"`  
* exe����ʧ��  
UnicodeDecodeError:"gbk" codec can't decode byte 0xaa in position 160:illegal multibyte sequence    
����������ļ����ĳ�Ӣ��

## ��������  
* [ pyinstaller ./{py�ļ���} ]         - Ч������һ�ѵ������ļ���dist�ļ�����  
* [ pyinstaller -F ./{py�ļ���} ]      - ��dist�ļ�����ֻ����һ��exe�ļ�  
* [ pyinstaller -c ./{py�ļ���} ]      - ����һ�������г��򣨾����Ǹ�С�ڿ򣩣�����Ĭ�ϵ�ѡ��  
* [ pyinstaller -w ./{py�ļ���} ]      - ������������  
* [ pyinstaller -i ./{py�ļ���} ]      - Ϊ����ָ��һ��ͼ�꣬��Ҫ����ͼ���·�����������ĩβ���-i test.ico��    

**�������** pyinstaller python.py -F -w -i test.io  

# python�������������Ч�˿ںţ�1024-65535��
* [ python -m http.server 7777 ]    - ʹ��������������

���Կ�����������ʹ���ֻ���������루**����IP��ַ:�˿ں�**����ֱ�����ص����ڵ��ļ�  
