###Disk

1.First sector: 
  * MBR: the most important sector, where bootloader installs, has 446 bytes
  * Partition talbe: record partition state, has 64 bytes.
2.Primary, extended, logical partition
  * 1 extended partition at most(os limit),
  * 4 primary or extended partitions at most(disk limit, partition table only has 64 bytes)
  * extended partition can't be formatted
  * logical partition come from extended primary
  * each partition has a bootsector, where can also install bootloader, not only MBR.
