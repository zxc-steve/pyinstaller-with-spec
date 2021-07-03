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
   
3.1 pyinstaller --onefile --noconfirm --add-data="README;." --add-data="README;." 

4 compress the labelme directory and ditribute to end user