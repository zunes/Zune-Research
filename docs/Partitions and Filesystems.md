# Partitions and Filesystems
As the Zune is built on top of the NVIDIA Tegra APX 2600 platform it might use something similar to the default partition layout.

## Partition Layout from the Registry
``HKEY_LOCAL_MACHINE\System\StorageManager\PartitionTable`` shows the partition layout of the Zune.

```reg
"01"="FATFS"
"04"="FATFS"
"06"="FATFS"
"07"="MSIFS"
"0B"="FATFS"
"0C"="FATFS"
"0E"="FATFS"
"0F"="FATFS"
"20"="BOOT"
"21"="ZBINFS"
"22"="RAWFS"
"23"="RAWFS"
"25"="IMGFS"
"26"="BINARY"
```

## Default Partition Layout from NVIDIA
``C:\Program Files (x86)\NVIDIA Corporation\ce6_tegra_250_5265393\os\wince600_nand.cfg``
```ini
[device]
type=nand
instance=0

[partition]
name=BCT
id=2
type=boot_config_table
allocation_policy=sequential
filesystem_type=basic
size=3145728
file_system_attribute=0
partition_attribute=0
allocation_attribute=8
percent_reserved=0

[partition]
name=PT
id=3
type=partition_table
allocation_policy=sequential
filesystem_type=basic
size=4096
file_system_attribute=0
partition_attribute=0
allocation_attribute=8
percent_reserved=0

[partition]
name=EBT
id=4
type=bootloader
allocation_policy=sequential
filesystem_type=basic
size=4194304
file_system_attribute=0
partition_attribute=0
allocation_attribute=8
percent_reserved=0
filename=EBOOT.NB0

[partition]
name=BMP
id=5
type=data
allocation_policy=sequential
filesystem_type=basic
size=5260
file_system_attribute=0
filename=nvlogo_64x39_rgb565_wheader.raw
allocation_attribute=8
percent_reserved=0

[partition]
name=CE6
id=7
type=data
allocation_policy=sequential
filesystem_type=basic
size=157286400
file_system_attribute=0
partition_attribute=0
allocation_attribute=8
percent_reserved=3
filename=NK.NB0

[partition]
name=ARG
id=8
type=data
allocation_policy=sequential
filesystem_type=basic
size=2048
file_system_attribute=0
allocation_attribute=8
percent_reserved=5
start_location=0

[partition]
name=DRM
id=9
type=data
allocation_policy=sequential
filesystem_type=basic
size=102400
file_system_attribute=0
partition_attribute=0
allocation_attribute=8
percent_reserved=300
filename=nvstorage.dat

# update information partition
[partition]
name=UIP
id=11
type=data
allocation_policy=sequential
filesystem_type=basic
size=2048
file_system_attribute=0
partition_attribute=0
allocation_attribute=8
percent_reserved=10

# update staging partition
[partition]
name=USP
id=12
type=data
allocation_policy=sequential
filesystem_type=basic
size=167673856
file_system_attribute=0
partition_attribute=0
allocation_attribute=8
percent_reserved=5

[partition]
name=USR
id=13
type=data
allocation_policy=sequential
filesystem_type=basic
size=0xFFFFFFFFFFFFFFFF
file_system_attribute=0
partition_attribute=0
allocation_attribute=0
percent_reserved=5
```

## Filesystems
### ZCSTFS 
_Zune Content File System_
**DLL:** zcstfs.dll
This is the Filesystem for the XNA Storage containers stored as [[ZCP Files]].

### ZBINFS
_Zune Binary File System_
**DLL:** zbinfs.dll

### FATFS
_FAT File System_
**DLL:** zexfat.dll

### EXFAT
**DLL:** zexfat.dll
exFAT File System

### MSIFS
MSIFS uses the ``EXFAT`` format.

### ObjectStore
**DLL:** filesys.dll

---
[[🗺️ Windows CE 6.0]]