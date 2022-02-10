**QHM-D461** : `72:16:03:00:D4:61`

```sh

gatttool -I -b 72:16:03:00:D4:61

gatttool -i hci0 -b 72:16:03:00:D4:61 --char-write-req -a 0x0009 -n 5600FF0001F0AA

```

``` 


**Characteristics:**
```sh
[72:16:03:00:D4:61][LE]> characteristics
handle: 0x0002, char properties: 0x02, char value handle: 0x0003, uuid: 00002a00-0000-1000-8000-00805f9b34fb
handle: 0x0005, char properties: 0x10, char value handle: 0x0006, uuid: 0000ffda-0000-1000-8000-00805f9b34fb
handle: 0x0008, char properties: 0x0c, char value handle: 0x0009, uuid: 0000ffd9-0000-1000-8000-00805f9b34fb
handle: 0x000b, char properties: 0x10, char value handle: 0x000c, uuid: 0000ffd4-0000-1000-8000-00805f9b34fb
handle: 0x000e, char properties: 0x04, char value handle: 0x000f, uuid: 0000ffd1-0000-1000-8000-00805f9b34fb
```



## Command Structure

**Example**
```sh
> char-write-cmd 9 56006E7B01F0AA
```


| `56`  | `00` | `00`  | `00` | `01F0AA` |
| ----- | ---- | ----- | ---- | -------- |
| Const | Red  | Green | Blue | Const    |


### Example Colors

**Red**:  `56FF000001F0AA`
**Green**:  `5600FF0001F0AA`
**Blue**:  `560000FF01F0AA`



## Using hcitool & gattool

Find MAC-Address of BLE Controller

```
$ sudo hcitool lescan

LE Scan ...
78:BD:BC:C7:D1:22 (unknown)
78:9C:60:00:06:28 LEDBLE-000628 # ITS NOT THIS ONE
78:9C:60:00:06:28 (unknown)
76:35:A3:1C:BB:60 (unknown)
5E:C4:18:04:DB:1D (unknown)
88:C6:26:3F:96:59
88:C6:26:3F:96:59 (unknown)
C0:28:8D:8A:76:B5
72:16:03:00:D4:61 QHM-D461 # <--- IT'S THIS ONE
```


Connect using gatttool
```
$ gatttool -I -b 72:16:03:00:D4:61
[72:16:03:00:D4:61][LE]>
[72:16:03:00:D4:61][LE]> connect
Attempting to connect to 72:16:03:00:D4:61
Connection successful
[72:16:03:00:D4:61][LE]> characteristics
handle: 0x0002, char properties: 0x02, char value handle: 0x0003, uuid: 00002a00-0000-1000-8000-00805f9b34fb
handle: 0x0005, char properties: 0x10, char value handle: 0x0006, uuid: 0000ffda-0000-1000-8000-00805f9b34fb

### THIS IS THE SERVICE WE WANT ###
handle: 0x0008, char properties: 0x0c, char value handle: 0x0009, uuid: 0000ffd9-0000-1000-8000-00805f9b34fb 
### THIS IS THE SERVICE WE WANT ###

handle: 0x000b, char properties: 0x10, char value handle: 0x000c, uuid: 0000ffd4-0000-1000-8000-00805f9b34fb
handle: 0x000e, char properties: 0x04, char value handle: 0x000f, uuid: 0000ffd1-0000-1000-8000-00805f9b34fb
[72:16:03:00:D4:61][LE]> char-write-cmd 9 56006E7B01F0AA
```



## Links

[https://elinux.org/RPi_Bluetooth_LE](https://elinux.org/RPi_Bluetooth_LE)

[https://github.com/kquinsland/JACKYLED-BLE-RGB-LED-Strip-controller/blob/master/Magic_numbers.md](https://github.com/kquinsland/JACKYLED-BLE-RGB-LED-Strip-controller/blob/master/Magic_numbers.md)