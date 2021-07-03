# -*- coding: utf-8 -*-
"""
Created on Sat Jul  3 09:49:26 2021

@author: Steve
"""

1  At labelme, run "pyinstaller main.py"
2  edit main.spec and add the following lines for datas:
   a = Analysis(['main.py'],
             #pathex=['D:\\temp\\Qt\\labelme'],
             pathex=['.'],
             binaries=[],
             datas=[('config\\default_config.yaml','config'),
                    ('agentClient\\AnalyticAgent.dll','agentClient'),
                    ('setup\\setting.ini','setup')
                    ],
3. run "pyinstaller main.spec" or pyinstaller  --noconfirm main.spec
   the dist\main\main.exe is the result
Or:    
3.1 pyinstaller --onefile --noconfirm --add-data="config\\default_config.yaml;config" --add-data="agentClient\\AnalyticAgent.dll;agentClient"  --add-data="setup\\setting.ini;setup" main.py

4 Visual Studio is free software to create .MSI file

https://docs.microsoft.com/en-us/answers/questions/256664/is-it-possible-to-create-a-setup-filemsi-in-visual.html
https://stackoverflow.com/questions/9226760/how-to-add-an-entire-folder-to-setup-project-in-visual-studio-2008/14293969

It works in my computer. You can install/uninstall.
You have to learn how to use Visual Studio and create project first !
