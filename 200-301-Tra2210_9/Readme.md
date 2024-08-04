## set password to router

enable secret [password]
```
enable secret 123
```
## passsword recovery step router

1. during boot press CTRL+PAUSE and go to bootloader shell
2. set register to 2142
```
>confreg 2142
```
3. reset
```
>reset
```  
4. copy startup config to running config
```
#copy startup_config running_config
```
5. remove password or set new one
```
no secret
enable secret 0000
``` 
6. config reg to 2102
```
#config-register 2102
```
<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/3layer.PNG" alt="CCNA ||" width="500"/></a>

## vlan types:

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/vlantypes.PNG" alt="CCNA ||" width="500"/></a>

1:12:00
