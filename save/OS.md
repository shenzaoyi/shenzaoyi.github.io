# OS

## Linux Syscall Implement

**privilege** - HardWare Design

1. CS: code , last two bit, CPL
2. DS: date, last two bit, RPL

DPL : destination privilege level 

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Priv_rings.svg/1280px-Priv_rings.svg.png" alt="undefined" style="zoom:50%;" />

check : if CPL < DPL or CPL = DPL; RPL < DPL or RPL = DPL

**Interupt**

for Intel x86, INT INTERUPT

```c
#define __LIBRARY__
#include <unistd.h>

_syscall3(int,write,int,fd,const char *,buf,off_t,count)
```


<img src=image.png style="zoom:50%;"/>
<img src=image-1.png style="zoom:80%;"/>

### Vsyscall & Vdso
also look this

### Reference
[Linux 核心設計: System call](https://hackmd.io/@RinHizakura/S1wfy6nQO)  
[System Call (系統呼叫)](https://hackmd.io/@combo-tw/Linux-%E8%AE%80%E6%9B%B8%E6%9C%83/%2F%40combo-tw%2FBJPoAcqQS)