# pfctl notes
* You can get some useful info from the man page for pf.conf:
```
man pf.conf
```
For logging, there isn't any file that is created by default; You actually first turn on a logging interface with:
```
ifconfig pflog0 create
```
You can also suppress it with:
```
ifconfig pflog0 destroy
```
You can then follow what is logged to this interface with:
```
tcpdump -n -e -ttt -i pflog0
```
