## What is Virtualization? 
* **Virtualization** - is the replication of hardware to simulate a virtual machine inside a physical machine. Virtualization allows the same host to run multiple "guest" operating systems, and easily move virtual machines between hosts. 

### Benefits of Virtualization
There are some cost-effective benefits of using virtualization. A lot of IT organizations and businesses have started to use virtualization because it enables them to run more than one virtual system on a single server which helps maintain the data center and IT infrastructure. There are reduced capital and operating costs and can increase IT productivity, efficiency, and responsiveness within the organization. There is also improvements in scalability in which there are greater resources to improve server's workload without buying hardware to upgrade system's memory, bandwidth, and CPU. Plus, it allows applications to be tested before installing on a host machine and experiment with programs without viruses and malware. There is a lot more faster provisioning of applications and resources and simplified data center management which makes virtualization a great tool to use. 
  
## Types of Virtualization
There are two types of virtualization:   
  * **Server-side virtualization** - is the process of dividing a physical server into multiple virtual servers by means of a software application. 

![server-side virtualization](server-side-virtualization.png)


> **Figure 1** displays how each virtual machine is split up using server-side virtualization. Each virtual server can run its own operating systems independently and run its own applications. This is useful because having each physical server divided into multiple virtual servers can make it less costly to have individual machines as well as increasing the capacity and utilization of resources of the physical machine. Each virtual server has its own virtual desktop infrastructure (VDI). 

### What is Virtual Desktop Infrastructure (VDI)? 
**Virtual Desktop Infrastructure** - is a technology that refers to the use of virtual machines to provide and manage virtual desktops. 

![thin vs thick vs zero clients](thin-thick-zero-clients.png)

> **Figure 2** shows the relationship between thin, thick, and zero clients. To host virtual desktops, it is important to determine what client would make the request to the server. It is important to note that the VDI is hosted on the server and the end user interacts with their virtual desktop interface locally on the client device. 
> * **Thin clients** serves as a terminal to the back-end server
> * **Thick clients** is basically a full-fledged PC running thin client software
> * **Zero client** are slimmer and more cost-effective than thin clients. These are client devices that require no configuration and have nothing stored on them. 

  * **Client-side virtualization** is software installed on a computer to manage virtual machines and allows communication to talk to the virtual desktop server.
  
  <br/>
  
  ![client-side virtualization](client-side-virtualization.jpg)

  > **Figure 3** Client-side virtualization is technology that allows users to simulate a workstation load to access a desktop from a connected device. There are benefits of working with virtual desktops.The user will have better security because data is not saved on the actual machine. This supports remote workers by giving IT control over how desktops are deployed across the organization's devices. Users can interact with the operating system and applications through the virtual desktop. Lastly, it helps to consolidate resources in a data center. Instead of buying lots of physical machines, the IT department does not have to worry about assessing how much computing is needed at the endpoint devices for end users. 

### Hypervisor

* For client-side virtualization, the computer needs a *hypervisor* and *hardware support*. 
* **Hypervisor** - is software that allows the management of virtual machines and makes virtualization possible. 
  * It allows one host computer to support multiple guest virtual machines by virtually sharing its resources such as memory and processing. 
* **Hardware support** includes:
  * Capable CPU
  * Enough RAM
  * Enough storage  


### Types of hypervisors

![hypervisor-type](type1-type2-hypervisor.png)

> **Figure 4**: 
> **Type 1 Hypervisor** runs directly on the hardware. 
> 
> **Type 2 Hypervisor**: runs on a host operating system.

#### Type 1 Hypervisor 
Type 1 Hypervisor is a layer of software that is installed directly on top of a physical server and its underlying hardware. It provides great performance and stability since it does not run inside any operating system. Type 1 hypervisors are  an OS themselves. The physical machine the hypervisor is running on serves virtualization purposes only. 

* Some examples include: 
  * VMware ESX and ESXi
  * Citrix XenServer

#### Type 2 Hypervisor
**Type 2 Hypervisor** runs inside of an operating system of a physical host machine. This type of hypervisor have one software layer underneath as depicted in **Figure 4**. Type 2 hypervisors are typically found in environments with a small number of servers. Type 2 Hypervisors act as management consoles for virtual machines where you can perform any task using built-in functionalities. This type of hypervisor is convenient for testing new software. 
  
* Some examples include: 
  * VMware Workstation Player/Pro
  * Oracle VirtualBox

## Virtualbox

![virtualbox-logo](virtualboxlogo.png)

### What is Virtualbox? 
**Virtualbox** is a powerful virtualization product for enterprise as well as home use. It is also the only professional solution that is freely available as Open Source Software under the terms of the GNU General Public License (GPL). 

Virtualbox runs on: 

* Windows
* Linux
* Macintosh
* Solaris 

It supports a large number of guest operating systems. 


### How to install virtualbox in Windows 10
* **Step 1**: Check if virtualization is enabled on your computer. You can check TWO ways: 
  * 1. Tap CTRL + ALT + DEL on your keyboard and click on *Task Manager*. A windows pop up shows and you will click on the *Performance* tab. You will see the CPU screen and automatically see *Virtualization: Enabled* or *Not Enabled*. 

![virtualbox-downloads-W10](virtualbox-setup-Win10.png)

  * 2. You can also check with Securable. Here is the link: [https://www.grc.com/securable.htm](https://www.grc.com/securable.htm). Click on *Download* and you can see that Virtualization has been enabled.

![Securable](check-virualization-2.png)

If you see that your PC has virtualization enabled, you can skip to Step 3. 
  

* **Step 2**: If you do not have virtualization enabled, you must enable Virtualization in the Bios/UEFI. Here are the steps to complete this task: 
  * 1. Power off your computer. 
  * 2. Then press the specific hotkey to enter BIOS. (*Please note, hotkeys vary by brand. It can be the Esc, F2 or Del, etc. button on your keyboard*)
  * 3. Then navigate to the *Advanced* tab, press *Enter* to continue. 
  * 4. Select *Virtualization* and enable it. 
  * 5. After that, save the changes and reboot your computer.
  
<br/>

* **Step 3**: Download virtualbox installer from [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads). Please make sure you select the package that is compatible with your operating system. Since I have a Windows machine, I would click on *Windows hosts*. * In addition, make sure to download the Virtualbox Extension Pack. The Extension Packs extends the functionality of the Oracle VM Virtualbox base package.  

![website-Virtualbox](website-Virtualbox.png)


**Here is a step by step guide on the installation process of the Virtualbox:**

 * 1. The popup window will show a welcome message. 
  
  ![welcome](welcome-virtualbox.png)

  <br/>

 * 2. You can leave the custom setup as default unless you would like virtualbox to be in another location. Click on *Next*.

![virtualbox2](virtualbox2.png)

<br/>

 * 3. The 3rd window are just settings related to how you want features to be installed and all have been selected so you can just click on *Next*. 

![virtualbox3](virtualbox3.png)

<br/>

* 4. The next popup gives a warning that temporarily you will be disconnected from the network because installing the Oracle VM Virtualbox Networking feature will reset the network connection. Click on *Yes* to proceed with installation.
  
![virtualbox4](virtualbox4.png)

<br/>

* 5. The final popup reveals that the installation has been completed. Click on *Finish*. 

![virtualbox5](virtualbox5.png)

<br/>

* To launch Virtualbox, you can double-click on the Oracle VM VirtualBox icon on your desktop. 

![launch](launch-Virtualbox.png)


### How to create a virtual machine
* **Step 1**: Open Virtualbox and click on *New* to create new Virtual Machine. 

![VM-launch-new](VM-launch-new.png)
<br/>

* **Step 2**: Name your VM and you can move it to another folder but you can leave it as the default. In this example, I named the virtual machine *test* and I chose Linux as the type of operating system along with the Ubuntu (64-bit) version. Click on *Next*.

![newVM.png](name-VM.png)
<br/>

* **Step 3**: The next screen wants you to set the amount of memory (RAM) in megabytes to be allocated to the virtual machine. It is important to be mindful of speed times and storage. In this case, I set it for at least 2 gigabytes (2048 mb). Click on *Next*.

![memory-VM](VM-memory.png)
<br/>

* **Step 4**: The next screen discusses if you would like to add a virtual hard disk to the new machine. In this example, we would want to create a virtual hard disk and click on *Next*. 

![create-VM](create-VM.png)
<br/>

* **Step 5**: Now that we chose to create a virtual hard disk, we must determine the hard disk file type. In this case, we will choose VDI (Virtualbox Disk Image). Click on *Next*. 

![hard-drive](hardrive-VM.png)
<br/>

* **Step 6**: The next screen shows how you would like the storage on the physical hard disk. In this case, we are going to choose the dynamically allocated because we want the VM to store as much as is needed. 

![dynamic](dynamic-VM.png)
<br/>

* **Step 7**: Once we click *Next* on the previous screen, the next prompt has to deal with the file location and size. I will keep the location as the default but you can select a different folder. I am going to adjust the size of the virtual hard disk to 25gb. Click on *Create*. 

![file-size](file-data-VM.png)
<br/>

* **Step 8**: Once the virtual machine is created, on the right, we can see the settings of the VM. You can always modify any of the settings by clicking on *Settings*. 

![preview-VM](VM-test-created.png)
<br/>

## Installing Ubuntu Server in Virtualbox
Once you get your VM created and set up, we can start to install the Ubuntu Server in Virtualbox. 

* **Step 1**: Since we set our virtual machine in Linux operating system with version Ubuntu, when we start our system in Virtualbox, it will start with providing two options and we want to click on *Install Ubuntu*.

![step1](step1-Ubuntu.png)
<br/>
 
* **Step 2**: The main step is to make sure we are launching the installation wizard to start the process of installing Ubuntu.  

![step2](step2-Ubuntu.png)
<br/>

* **Step 3**: This is the welcome page for Ubuntu's installer. Please keep in mind to set the language that you understand and know. The default is English so I will click on *Continue*. 
  
![step3](step3-Ubuntu.png)
<br/>

* **Step 4**: Set the default language to English for the keyboard layout and click on *Continue*. 
  
![step4](step4-Ubuntu.png)
<br/>

* **Step 5**: The screen prompt gives you options on updates and other software which allows you to customize how you want to install software and apps.
  
![step5](step5-Ubuntu-png.png)
<br/>

* **Step 6**: The next thing you want to do is set the installation. In this case, we will click on *Erase disk and install Ubuntu* and click on *Install Now*. 
  
![step6](step6-Ubuntu.png)
<br/>

* **Step 7**: Then, you can click on *Continue* once everything looks good so that he changes listed will be written to the disks. You can make further changes manually. 

![step7](step7-Ubuntu.png)
<br/>

* **Step 8**: You can then select your location via your time zone. 
  
![step8](step8-Ubuntu.png)
<br/>

* **Step 9**: This screen allows you to input your computer information like your name, the computer's name, username and password. 
  
![step9](step9-Ubuntu.png)
<br/>

* **Step 10**: While the system is installing, Ubuntu shows a slideshow about useful information. 
  
![step10](step10-Ubuntu.png)
<br/>

* **Step 11**: The installation is completed and you can continue testing or you can restart the computer. Just remember, any changes you make or documents you save can disappear so it is recommended you save your work first, then restart. 
  
![step11](step11-Ubuntu.png)
<br/>

* **Step 12**: Press *Enter* and the virtual machine will continue rebooting. 
  
![step12](step12-Ubuntu.png)
<br/>

### Updating Ubuntu
It is important to keep the Ubuntu server updated due to bug fixes, system updates, and new features added for ease of use and security. There are two ways to update Ubuntu. 
  * 1. Using Ubuntu Software Update
     ![update-Ubuntu](Update-Ubuntu.png)
  * 2. Using the command line
    * To upgrade the software, you must use the following command. 
       `sudo apt update; sudo apt upgrade -y; sudo apt full-upgrade -y`

      * The `sudo apt update` command is used to download and update the package information from all of the configured sources. 
  
  ![update command](update-command.png)
  > **Figure 5** explains how to update any Debian distro. Each element provides a function of the command. 


* Here is an example: 
   * 1. Open the Terminal. 
   * 2. Type in the following the command. 
            
     ![Example](examle-Installing-Ubuntu.png)
  * 3. Type in the password and the system updates.  

### Installing and Removing Software in Ubuntu
* Formula used for installation: **sudo + apt + install + Package name**
* Formula used for removal of software: **sudo + apt + remove + Package name**
* **install** option installs the specified package
* **remove** option removes the specified package.
* You can install/remove multiple programs by adding the package name with a space between each package. 
* You can also remove packages by adding an - sign at the end of the package name. 
* You can add and remove packages at the same time by using a + and - at the end of each package.   

**Examples:**
| Install/Remove Commands | Examples                      |
| ----------------- | ----------------------------- |
| Install several programs in a single command | `sudo apt install firefox flameshot caffeine -y`      |
| Remove several programs in a single command | `sudo apt remove firefox flameshot caffeine -y`            |
| Install and remove programs in a single command  | `sudo apt install firefox+ flameshot- caffeine- vlc+` |
| Remove programs and all remaining traces | `sudo apt purge firefox+ flameshot- caffeine- vlc+`        |

#### Searching for software
How to search for software with Apt: 

| Search Commands | Examples                        |
| --------------- | ------------------------------- |
| Search for all programs that matches the text in quotes | `apt search "web browser"`                   |
| Search for information about a given package including dependencies | `apt-cache search firefox`                           |
| Search a package name only | `apt search -n firefox`                                            |

* Apt works using the list of repositories in the `/etc/apt/sources.list`
* You can add more repositories (or remove them) using the command `sudo apt edit-sources`. 
* Edit-sources opens the `sources.list` file using your default text editor. 

## Basic linux commands

### Navigating the files system

| Commands  | Description | Usage | Examples       |
| ---------  | ----------- | ----- | -------------- |
| pwd command | used for displaying the current working directory |  `pwd` | ![pwd](pwd.png)  |
| cd command | used for changing the current working directory. When no directory is given, cd changes the current working directory to the home directory of the current user. | `cd + destination` | ![cd](cd.2.png)                  |
| ls command | used for listing the content of a given directory or the file/directory itself | `ls`  | ![ls](ls.1.png) ![ls](ls.2.png)                  |

### Managing files and directories

| Commands  | Description  | Usage  | Examples    |
| --------- | ------------ | ------ | ----------- |
| mkdir command | used for creating a single directory or multiple directories | `mkdir + the name of the directory` | ![mkdir](mkdir.png)      |
| touch command | used for creating files | `touch` | ![touch](touch.png) |          
| rm command  | removes files | `rm` | ![rm.1](rm.png) ![rm.2](rm.2.png)                                             
| mv command | moves directories | `mv + source + destination` | ![mv](mv.png)
| mv command | renames directories | `mv + file/directory to rename + new name` |     ![mv](mv-rename.png) ![nv,2](mv-rename-2.png)           |
| cp command | copies files/directories from a source to a destination | `cp + files to copy + destination` | ![cp](cp.png)                   |




Sources
* https://www.hysolate.com/learn/vdi-windows/virtualization-for-windows-10-a-practical-guide/#:~:text=Virtualization%20allows%20the%20same%20host,hypervisor%2C%20called%20Hyper%2DV.
* https://www.vmware.com/solutions/virtualization.html
* https://studycorgi.com/the-effect-of-scalability-on-virtualization/#:~:text=Scalability%20in%20virtualization%20deals%20with,memory%2C%20bandwidth%2C%20and%20CPU.
* https://www.vmware.com/topics/glossary/content/server-virtualization.html#:~:text=Server%20Virtualization%20Definition,its%20own%20operating%20systems%20independently.
* https://www.techtarget.com/searchvirtualdesktop/feature/VDI-hardware-comparison-Thin-vs-thick-vs-zero-clients
* https://www.citrix.com/solutions/vdi-and-daas/what-is-desktop-virtualization.html#:~:text=Desktop%20virtualization%20is%20technology%20that,device%20used%20to%20access%20it.
* https://www.vmware.com/topics/glossary/content/hypervisor.html
* https://phoenixnap.com/kb/what-is-hypervisor-type-1-2
* https://www.virtualbox.org/
* https://www.minitool.com/news/enable-virtualization-windows-10.html