# Understanding Computer Hardware 

- __Motherboard__ : It is the main hardware board which contains central processing unit(CPU), Random Access Memory(RAM) and other connected components.
- If a hardware system has more than one processor, the system is referred to as a multiprocessor.
- If more than one processor is combined into a single overall processor chip, then it is called multi-core.
- arch : show the architecture of the system.
- lscpu : shows the configuration of the cpu.
- free -m : shows the configuration of a RAM and swap memory (In MB).
    - To see the details in GB use the flag -g.

- __Buses__ : A bus is a high-speed connection that allows communication between computers or the components inside a computer. The motherboard has buses that allow for multiple devices to connect to the system, including the Peripheral Component Interconnect (PCI) and Universal Serial Bus (USB). 

- __Peripheral devices__ : Peripheral devices are components connected to a computer that allow input, output or data storage. Keyboards, mice, monitors, printers and hard disks are all considered peripherals and are accessed by the system in order to perform functions outside of central processing.
- ls pci : shows the list of all the connected devices with the pci.
-  Universal Serial Bus Devices - (USB)
    - Cold plug : To connect the component device must to shutdown and restart.
    - Hot plug : No need to restart device. USB is a hot plug device.
- Master Boot Record (MBR) 
- GUID Partitioning Table (GPT)
- fdisk : can be used to display the information about the partition.
- Optical drives, often referred to as CD-ROMs, DVDs, or Blu-Ray, are removable storage media. 
- lspci command with the -k option to show devices along with the kernel driver and modules used.
- lsmod : used to view the currently loaded modules.

