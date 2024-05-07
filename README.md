# Expanding An Array, Extending and Migrating A Logical Drive Using HPE Smart Storage Administrator (SSA)

IMPORTANT: An array expansion, logical drive extension, or logical drive migration takes about 15 minutes per gigabyte. While this process is occurring, no other expansion, extension, or migration can occur simultaneously on the same controller. Controllers that do not support a battery-backed write cache do not support this process.

## Expanding an array
You can increase the storage space on an array by adding physical drives. Any drive that you want to add must meet the following criteria:
		- It must be an unassigned drive. 
		- It must be of the same type as existing drives in the array (for example, SATA or SAS). 
		- It must have a capacity no less than that of the smallest drive in the array.

