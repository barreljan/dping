# dping(.sh)
> dping packetloss loging timestamp

### Introduction
Dateping - a rudimentary attempt to see when packetloss happens. It is simple but effective and easy to run. Normal situaties with MTR (Mytraceroute) does show loss, but no timestamp is written down somewhe.

### How to use
Set the permissions to execute (by `chmod +x dping`). And place it in '/usr/sbin/' or any best path you like (or symlink it from there).
Best usage is within a `screen` to keep it running in the background.

The 'help' from dping:

```
dping [options] ipaddr

options:
-h, --help              show brief help
-v, --verbose           logging of both success and failure on screen

default is silent. Logging is always done to dping_<ipaddr>_err.log
sending Ctrl-C stops this program
```

### Example output

The text file generated looks like this:

```
Started at Thu May 18 09:50:44 CEST 2017

Thu May 18 18:33:59 CEST 2017: 1 packets transmitted, 0 received, 100% packet loss, time 1000ms
Fri May 19 00:03:18 CEST 2017: 1 packets transmitted, 0 received, 100% packet loss, time 1000ms
```
