#Zspaces

A Zsh version of [this Python script](https://github.com/jeffreysbrother/spaces). See comparison below.

####Zsh script:

```zsh
#!/bin/zsh

autoload -U zmv
zmv '* *' '$f:gs/ /-'
zmv '(*)' '${(L)1}'
```

####Python script:
```python
#!/usr/bin/python
import os

path  = os.getcwd()
filenames = os.listdir(path)
for filename in filenames:
    os.rename(os.path.join(path, filename), os.path.join(path, filename.replace(' ', '-').lower()))
```
