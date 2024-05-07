# Expanding An Array, Extending and Migrating A Logical Drive Using HPE Smart Storage Administrator (SSA)

IMPORTANT: An array expansion, logical drive extension, or logical drive migration takes about 15 minutes per gigabyte. While this process is occurring, no other expansion, extension, or migration can occur simultaneously on the same controller. Controllers that do not support a battery-backed write cache do not support this process.
<br />
<br />

## HPE Smart Storage Administrator
The HPE SSA is a configuration and management tool for HPE Smart HBA and Smart Array controller options. The HPE SSA exists in the following interface formats:

- HPE SSA GUI
- HPE SSA CLI
- HPE SSA Scripting

Although all formats support configuration tasks, some of the advanced tasks are available in only one format.<br />

HPE SSA can be accessed in both online and offline modes. In online mode, SSA is only accessible from the local server.

To access, install, and launch HPE SSA in an online environment, download the HPE SSA executables from the Hewlett Packard Enterprise Support Center website (http://www.hpe.com/support/hpesc). Under Select your HPE product, enter the product name or number, and then click Go.

To access, install, and launch HPE SSA in an offline environment, download the HPE SSA ISO image from the HPE Smart Storage Administrator website:

http://www.hpe.com/servers/ssa
<br />
<br />

## Expanding an array using SSA GUI
You can increase the storage space on an array by adding physical drives. Any drive that you want to add must meet the following criteria:

- It must be an unassigned drive. 
- It must be of the same type as existing drives in the array (for example, SATA or SAS). 
- It must have a capacity no less than that of the smallest drive in the array.

### Procedure

- Select the storage controller on the left pane
- Click on 'Configure'
- Go to 'Logical Devices' on the left pane
- Select the array that you are going to add the existing drive to from the middle pane
- Click on 'Manage Data Drives' on the right pane
<br>

  ![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/fc4923ca-0d08-44f4-ab37-0c0c35686bfb)

<br>


- In the next page make sure to choose 'Add Drive(s) - Expand Array' and select the physical drive and click on 'OK' to continue

<br>

![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/bab85300-b6cd-4546-8f97-f42ac4b834f0)

<br>

- In the next page, review the logical drive summary and click on 'Finish'
<br>

![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/02cd4498-3088-4e06-acfa-78a7bfcc4496)

<br>

- You will be able to see an extra physical drive added to the array in the middle pane <br><br>
![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/f5f4c777-176c-4b8c-8690-0c16a9435fdf)
<br>
<br>

## Extending A Logical Drive using SSA GUI
If the operating system supports logical drive extension, you can use any unassigned capacity on an array 
to enlarge one or more of the logical drives on the array.

### Procedure
- Select the storage controller on the left pane
- Click on 'Configure'
- Go to 'Logical Devices' on the left pane
- Select the logical drive that you want to extend in the middle pane
- Click on 'Extend Logical Drive' on the right pane

<br>

![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/2c5a443a-0b81-415c-b6ce-3ee5029daaf7)
<br>

- Choose the available size to extend the logical drive to

<br>

![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/439153c3-0917-42dc-94f8-d10c5aec6df7)
<br>
<br>

## Migrating A Logical Drive
A RAID migration allows you to convert a RAID-Ready system into a RAID 0, 1, 5, or 10 configuration, or from a RAID 0, 1, or 10 volume to a RAID 5 volume

Consider the following factors before performing a migration:
- For some RAID-level migrations to be possible, you might need to add one or more drives to the 
array.
- For migration to a larger stripe size to be possible, the array might need to contain unused drive 
space. This extra space is necessary because some of the larger data stripes in the migrated array 
are likely to be filled inefficiently


### Procedure
Below we can see a logical drive of RAID level RAID 1
<br>

![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/7457fe18-a882-42bf-b8fa-0e3bc24d5414)

- Click on 'Migrate RAID/Strip size' on the right pane
<br>

![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/390b10e3-1580-45c1-b9d2-7f8cbc59ac55)

- Choose the RAID level to migrate to, here we get the option to migrate to RAID 0 only as there are only physical drives in the logical drive and click on 'OK'
<br>

![image](https://github.com/fayas1290/Expanding-Extending-Migrating/assets/157561213/88c955e3-5f2b-4521-9345-80bc19035af5)



