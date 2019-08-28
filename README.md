# ForgeMinecraft_Xia
一个自动的Minecraft 服务器备份~

TO-DO
现在的任务是完成用户的客户端配置
依然还没有一个可以供任何平台稳定安装的EXE 文件



添加记录push信息就好了
而且利用python 来进行系统自动备份
这个是具体的push设置内容

.git/config
```
[credential]
    helper = store
```

我们自定义的crontab文件保存在/var/spool/cron/crontabs/目录下
use crond 

```
crontab -e
```

code Format 
minute hour day month week command
my code for cron
```
*/15 * * * * cd /home/xia/ForgeMinecraft_Xia/&&python3 /home/xia/ForgeMinecraft_Xia/autoGithub.py
```

Make sure you changed your 22 port to make your server more secure!
```
nano /etc/ssh/sshd_config
```
uncomment 22 port and change it to something elsey


example recroding code but not running in my system 
just a simple example
```python
#!/usr/bin/env python
# -*- coding: utf-8 -*-

import datetime

def write_file(file):
    with open(file, 'a') as f:
        f.write(str(datetime.datetime.now()) + '\n')
    f.close()

file = 'test.txt'
write_file(file)
```
