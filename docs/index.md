# AWR ANALYSIS OVERVIEW


## Automatic Workload Repository (AWR) Overview

* AWR contains vast amounts of database performance data
* Analyzing the Oracle AWR report is a fundamental task for diagnosing database performance issues.
* The AWR collects, processes, and maintains performance statistics
* These statistics can be used for problem detection and self-tuning purposes.
* AWR report provides a detailed overview of the database environment and its performance over a specific period.
* Most recent week by default, or from any recent peak workload periods, preferably.


## AWR report Analysis – Structured approach

1. **Understand the Snapshot Interval**
    **Time Period:**Check the snapshot interval (start and end snapshots) to ensure it covers the period during which performance issues were observed.
    
2. **Review Database Load Profile:**

    **DB Time:**Represents the total time spent in the database by user processes.

    **DB CPU:**Time spent on the CPU - high values indicate CPU pressure.

    **Physical Reads/Writes:**High values could indicate disk I/O issues.

    **Parses/Executes:**High parse to execute ratios might suggest inefficient application SQL coding

3. **AWR SQL Statistics**
    **SQL ordered by CPU Time, Executions, Reads, etc.:** Identifies top SQL queries consuming resources.
    * Look for queries with high values in these areas, as they are candidates for optimization

### **vCPU - virtual Central Processing Unit** 

* vCPU refers to a virtualized CPU instance allocated to a virtual machine (VM) or an instance in a cloud computing environment.

**Hypervisor** is also known as a virtual machine monitor or VMM, is software that creates and runs virtual machines (VMs). A hypervisor allows one host computer to support multiple guest VMs by virtually sharing its resources, such as memory and processing.

**Virtualization** In a virtualized environment, such as a hypervisor-based virtualization platform (e.g., VMware, Hyper-V, KVM) or a cloud computing service (e.g., AWS EC2, Azure Virtual Machines, Google Compute Engine),physical CPUs are divided into multiple virtual CPUs called vCPUs.

**Allocation** : Each virtual machine is allocated one or more vCPUs, which are mapped to physical CPU ==cores or threads== on the host machine. The hypervisor or cloud management platform manages the allocation of vCPUs to virtual machines based on resource availability and configuration settings.

#### Cores and Threads

**Cores:**
 **Definition:** A core is a physical processing unit within a CPU chip that can independently execute instructions. Each core consists of its own arithmetic logic unit (ALU), registers, and other components necessary for processing instructions.

 **Functionality:** Cores are capable of executing instructions and performing calculations. Multiple cores allow a CPU to execute multiple tasks concurrently, improving overall performance and multitasking capabilities.

 **Parallelism:** Cores provide true parallelism, meaning that each core can execute its own set of instructions simultaneously with other cores on the same CPU chip.

**Threads:**

 **Definition:** A thread is a sequence of instructions that can be executed by a CPU core. Threads represent the smallest unit of execution within a process and can be scheduled by the operating system for execution on CPU cores.

 **Concurrency:** Threads allow multiple tasks or processes to run concurrently on a CPU core. This concurrency is achieved through time-sharing, where the CPU switches between executing different threads rapidly.

!!! note "NOTE"

    Increasing the number of cores generally leads to improved performance

##### Read IOPS & Write IOPS 

 * Read IOPS & Write IOPS are performance metrics used to measure the input and output operations of a storage device, such as a 
    hard disk drive (HDD), 
    solid-state drive (SSD), or 
    storage area network (SAN).

* Read IOPS (Input/Output Operations Per Second)
The number of read operations (data reads) that a storage device can perform in one second. 
It measures how quickly the storage device can retrieve data from storage and deliver it to the system or application requesting it

* Write IOPS(Input/Output Operations Per Second)
   The number of write operations (data writes) that a storage device can perform in one second.
   It measures how quickly the storage device can store data sent to it by the system or application.




    
