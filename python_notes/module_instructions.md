# pyinstaller��װ��ʹ��˵��

## ��������
* [ pyinstaller ./{py�ļ���} ]         - Ч������һ�ѵ������ļ���dist�ļ�����  
* [ pyinstaller -F ./{py�ļ���} ]      - ��dist�ļ�����ֻ����һ��exe�ļ�  
* [ pyinstaller -c ./{py�ļ���} ]      - ����һ�������г��򣨾����Ǹ�С�ڿ򣩣�����Ĭ�ϵ�ѡ��  
* [ pyinstaller -w ./{py�ļ���} ]      - ������������  
* [ pyinstaller -i ./{py�ļ���} ]      - Ϊ����ָ��һ��ͼ�꣬��Ҫ����ͼ���·�����������ĩβ���-i test.ico��  

## ���һ��py�ű�����
�������ļ����ڵ�·����Powershell������ָ�  
pyinstaller -F -w main.py

## ������py�ű�����
�������ļ����ڵ�·����Powershell������ָ�
1. pyinstaller -F main.py
2. ɾ�������������ļ���ֻ����`setup.spec`�ļ�
3. �༭`setup.spec`�ļ�
4. �༭��Ϻ�ʹ��pyinstaller -F setup.spec�������ļ���distĿ¼

**setup.spec�ļ��޸�λ��**
* ���`py_files`�б�������Ŀ��Ҫ������python�ű�������['1.py', '2.py']
* ���`pathex`�б�������Ŀ�õ�������python�ű�·��
* ���`datas`�б������漰����������Դ�ļ���ÿ���ļ�����Ԫ�����ʽ��ţ�����[('images\\\\happy.ico', 'images'), ('images\\\\*.jpg', 'images')]
* `name`='Tool'���ƶ���ִ�г�������
* `console`=False���ƶ���ִ�г���ִ��ʱ����ʾ����̨����
* `icon`='C:\Users\15057\Desktop\FlappyBird\images\flappy.ico'�����ó���ͼ�꣬ʹ�þ���·����ico��ʽΪ��16*16��

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

# python�������������Ч�˿ںţ�1024-65535��
* ����Ҫ������ļ����´�Powershell����ָ��������������python -m http.server

���Ὺ��һ�� http://0.0.0.0:7777/ ���������  
��ͬһ�������ڵ��豸���Դ���������루**�����ļ��ĵ���IP��ַ:�˿ں�**�����빲����ļ��У�Ԥ���������ļ�  
