```
dpkg: unrecoverable fatal error, aborting:
files list file for package 'x11-common' contains empty filename
E: Sub-process /usr/bin/dpkg returned an error code (2)
```

- A mensagem de erro significa que o arquivo /var/lib/dpkg/info/x11-common.list foi corrompido de alguma forma. Para corrigir isso, exclua-o:

```$ sudo rm /var/lib/dpkg/info/x11-common.list```

- e reinstale o pacote:

```$ sudo apt --reinstall install x11-common```
