# WSL2でsystemctlが動かない
## 原因
エラーの内容としては、
```
systemdがPID 1(init system)ではないので操作できない。
```
Linuxが起動するときすべてのプロセスの最初として`systemd`が起動し、すべてのプロセスの親としてふるまうようである。  
https://dev.classmethod.jp/articles/systemd-getting-started/#toc-2

```bash
% ps aux
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.0    992   468 ?        Sl   Mar05   0:00 /init
root     11332  0.0  0.0    992   176 ?        Ss   09:45   0:00 /init
root     11333  0.0  0.0    992   176 ?        R    09:45   0:00 /init
ustamot  11334  0.0  0.0  10176  5356 pts/0    Ss   09:45   0:00 -bash
ustamot  11417  0.0  0.0  10612  3284 pts/0    R+   09:53   0:00 ps aux
```

## systemdをPID 1にする
https://snowsystem.net/other/windows/wsl2-ubuntu-systemctl/#  
を参考にする。事前に`OpenSSH`をインストールしていおくこと。
