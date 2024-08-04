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
## port types

trunk: path to trnasfer all vlan traffic

access: spefific vlan trafic will pass

auto:

## vlan types:

local: meanse exist only on one switch

end to end: meanse exist on multiple switchs and connected using trunk port

<a href="link"><img src="https://github.com/amin-amani/CCNA/blob/main/200-301-Tra2210_9/vlantypes.PNG" alt="CCNA ||" width="500"/></a>

1:12:00
