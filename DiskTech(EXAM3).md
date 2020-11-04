Mean Time to failure MTTF

Wear leveling
Optical Storage - pits and lands

Magnetic tape storage- Linear tape-open(LTO)-Open specification, and was to have multiple capacity. It can store 30TB per take.Move data with 900mb per seconds.LTO tape costs $150.Large
Storage management is done using robotic 

RAID :- Uses many small disks and was less expensive than SLED.(Redundant Array of Inexpensive Disks"[1] or "Redundant Array of Independent Disks)
SLED:- It was used to build with one disk and was expensive and big.

RAID :- proposed 5 levels of RAID, 1 through 5
Two or more disk configure together to store data
booctly- create RAID array and have to tell which level of raid to be used.
         -c 1 -l/dev/sd0a,/dev/sd1a softraid0                          

Concepts:-
* Striping - storing consecutive chunks of data across multiple drives.
* Mirroring - data is replicated across multiple drives.
* parity - error detection that is used to recover damaged data

Levels:-
* RAID 0 - stripes data across multiple disks, total available storage is the sum of all disks.Any single disk failure breaks the entier array.
* RAID 1 - mirrors data across 2 or more drives. All data is stored on every part of array. It is also known as redundant array.Writes are slower but read are faster. Total storage is half the sum of all disks, any single disk failure can be recovered.
* RAID 2 - stripes bits across multiple disks with a hamming code. Data is written one bit at a time and when 1 byte of data to be written 8 surface is used. All the disk should be synchronized.(READ MORE)The total storage is sum of all drives, any single data disk failure can be recovered.
* RAID 3 - stripes bytes across multiple disks and a parity code is written to a single parity drive, any single drive failure is recoverable, total storage is the sum of the data disks.
* RAID 4 - stripes blocks of data across multiple disks and a parity code is written to a single parity drive , total storage is sum of the data disks, any single disk can be recovered using the parity disk.
* RAID 5 - stripes blocks across multiple disks with a parity code to one of several disks, any single disk failure is recoverable using the parity disk, total storage is the sum of all the data disks(Assuming all disks are same size). RAID 5 is pretty popular and lots of enterprise system use this.
* RAID 6- stripes blocks across multiple disks with parity codes, Reed-Solomon ECC(Error correcting code), tolerates loss of 2 disks, its more expensive than RAID 5, requires more disks than RAID 5, total storage is sum of all the data disks.

* RAID DP(double parity) 
* RAID 10 - its RAID 1 and RAID 0, RAID 1 inside a RAID 0. striping mirroring parity
