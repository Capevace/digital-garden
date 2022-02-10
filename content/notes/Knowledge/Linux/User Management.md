# Linux User Management
#linux

## Create a new user

```shell
sudo useradd <username>
```

### Create with home directory

```shell
sudo useradd -m <username>
```

## Change user password

```shell
sudo passwd <username>
```


## Add group to user

```shell
sudo usermod -aG <group> <username>
```