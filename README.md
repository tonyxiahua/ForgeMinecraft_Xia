# ForgeMinecraft_Xia
一个自动的Minecraft 服务器备份~

添加记录push信息就好了
而且利用python 来进行系统自动备份

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

example code 

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


