# Linux Directory Size (`du`)
#linux #dev 

## Get occupied size of directory

```shell
sudo du -sh /var
```

```shell
# Output
85G	/var
```

## Get occupied sizes of subdirectories

```shell
sudo du -shc /var/*
```

```shell
# Output
24K		/var/db
4.0K	/var/empty
4.0K	/var/games
77G		/var/lib
4.0K	/var/local
0		/var/lock
3.3G	/var/log
0		/var/mail
4.0K	/var/opt
0		/var/run
196K	/var/spool
28K		/var/tmp
85G	total
```