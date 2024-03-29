## Introduction to Linux Command Line Basics

### 01/03/2024

#### Lab Setup

##### Virtualization

* **What is Virtualization?** Virtualization software lets you create virtual machines (VMs) that run within your existing operating system. This allows you to experiment with different operating systems like Kali Linux without affecting your main system.

* **Enabling Virtualization:** The specific steps to enable virtualization depend on your system's BIOS/UEFI. Consult your motherboard's manual for detailed instructions. Generally, you'll find the VT (Virtualization Technology) or AMD-V option in Security settings and need to enable it.

* **Virtualization Software Options:** Here are two options to consider:

    * **[VMware Workstation Player](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html):** (Free for non-commercial use with some limitations)
    * **[VirtualBox](https://www.virtualbox.org/wiki/Downloads):** (Free and open-source)

##### Downloading Kali Linux

Head over to the official [Kali Linux](https://www.kali.org/get-kali/) download page.

##### Choosing the Right Download:

* **Virtual Machine Images:** If you're using virtualization software, these pre-configured images are the easiest option. Download the one compatible with your chosen virtualization software (e.g., VirtualBox Images, VMware Images).
* **Live Images (ISOs):** You can also download Live Images (ISO files) to create bootable media (DVD or USB) and install Kali Linux directly onto a separate hard drive partition (not recommended for beginners).

##### Download [WinRAR](https://www.rarlab.com/download.html) (if using Windows) for Extraction (Optional): (Some virtualization software might handle extraction natively)

##### Installing Kali Linux (Example using VirtualBox)

**Note:** These are general steps. Specific details might vary slightly depending on your VirtualBox version.

1. **Launch VirtualBox** and click "New."
2. **Choose "Expert Mode"** for more control over settings (optional).
3. **Select "Machine Type":** Choose "Linux" for the operating system and "64-bit (x86_64)" for the architecture (unless using a 32-bit system).
4. **Allocate Memory:** Allocate a suitable amount of RAM (2 GB or more recommended for Kali Linux).
5. **Create Virtual Hard Disk:** Select "Create a virtual hard disk now" and choose the VDI (VirtualBox Disk Image) type.
6. **Hard Disk File Type:** Opt for "Dynamically allocated" for efficient storage usage.
7. **Create:** Click "Create" to finish setting up the virtual machine.
8. **Configure Hard Disk:** Select the newly created VM and click "Settings". Go to "Storage" and click the empty controller icon. Choose "Add Hard Disk" and select "Choose existing disk." Navigate to your downloaded Kali Linux virtual machine image (VDI file) and click "Open."
9. **Start the VM:** Click "Start" on the main VirtualBox window and select your Kali Linux VM.
10. **Boot Options:** If prompted, choose the option to boot from the virtual hard disk (Kali Linux image).
11. **Installation:** Follow the on-screen instructions to install Kali Linux on your virtual machine. Be sure to note the default username ("kali") and password ("kali") for later login.

#### Terminal Shortcuts

* **Shortcut for Opening Terminal:** Ctrl + Alt + T (common on many Linux distributions)

#### Terminal Commands

* **User Hostname Prompt:** `kali@kali` (example)
    * `~`: Represents your home directory
    * `$`: Denotes a regular user
    * `#`: Indicates root (administrator) privileges


### 03/03/2024

**Terminal Operations**

* **Listing Files and Folders:** `ls` - Lists the contents of the current directory.
* **Navigating Directories:**
    * `cd directory_name`: Change directory to a specific one.
    * `cd ..`: Move up one directory level (parent directory).
* **Directory Structures**
    * `/`: Root directory, the top level of the filesystem.
    * `/root`: Home directory of the root user.
    * `/home`: Contains user home directories.

**Terminal Help and Documentation**

* `man command`: Provides detailed information about a specific command.
* `command --help`: Many commands offer built-in help documentation.

**Essential Commands and Navigation in Kali Linux**

**16/03/2024**

**Basic Commands**

* **`echo Hello World`:** Prints the string "Hello World" to the terminal.
* **`man <name>`:** Displays the manual page for a command (replace `<name>` with the actual command name).
* **`help`:** Provides a general help message, often listing available commands.
* **`hostname`:** Shows the hostname of the system.
* **`whoami`:** Displays your current username.
* **`who`, `w`:** Lists currently logged-in users and their terminals.
* **`last`, `last root`:** Shows information about previous login attempts (all users and root user, respectively).
* **`history`:** Displays a history of recently used commands.
* **`date`, `cal`:** Shows the current date and a calendar for the current month, respectively.

**File and Directory Management**

* **`nano filename`:** Opens the specified file for editing in the nano text editor.
* **`head filename`:** Displays the first few lines of a file.
* **`tail filename`:** Displays the last few lines of a file.
* **`mv source_file destination_file`:** Renames or moves a file (source to destination).
* **`rm filename`, `rm file*`:** Deletes a file (single file or using wildcards).
* **`mkdir directory_name`:** Creates a new directory.
* **`rmdir directory_name`:** Removes an empty directory.
* **`rm -r directory_name`:** Deletes a directory and all its contents (use with caution!).


**Cron Jobs and Local Disk Management in Linux**

**Cron Jobs**

Cron is a task scheduler in Linux that allows you to automate repetitive tasks at predefined times. This is incredibly useful for various purposes, such as:

- System maintenance (backups, logs cleaning)
- Software updates
- Security checks
- Data processing tasks
- File transfers

Here are some essential cron job commands:

1. **Opening the Crontab File (`crontab -e`)**

   - **Syntax:** `crontab -e`
   - **Example:** `crontab -e`
   - **Description:** Opens the current user's crontab file in the default text editor (usually `nano` or `vim`). This file contains lines defining the cron jobs you want to schedule.

2. **Listing Cron Jobs (`crontab -l`)**

   - **Syntax:** `crontab -l`
   - **Example:** `crontab -l`
   - **Description:** Displays the contents of the current user's crontab file, showing all scheduled cron jobs.

3. **Removing Cron Jobs (`crontab -r`)**

   - **Syntax:** `crontab -r`
   - **Example:** `crontab -r`
   - **Description:** Removes the current user's crontab file, deleting all scheduled cron jobs. Use this command with caution.

4. **System-wide Cron Jobs (`/etc/cron.d/`)**

   - **Directory Path:** `/etc/cron.d/`
   - **Description:** This directory contains system-wide cron jobs that are run by specific users or system services. You can place custom cron job files in this directory (with appropriate permissions) to schedule tasks for the system.

**Cron Job Syntax**

The crontab file uses a specific syntax to define cron jobs. Each line consists of five fields separated by spaces:

* **Minute (0-59):** When the minute the job should run.
* **Hour (0-23):** When the hour the job should run.
* **Day of Month (1-31):** When the day of the month the job should run.
* **Month (1-12):** When the month the job should run.
* **Day of Week (0-6, where 0=Sunday):** When the day of the week the job should run.
* **Command:** The command or script to execute when the specified time arrives.

For more complex scheduling patterns, you can use special characters like `*` (any value), `/` (interval), `,` (list of values), and `-` (range).

**Resources for Learning More About Cron Jobs:**


- [FreeCodeCamp - Automation Tutorials](https://www.freecodecamp.org/news/tag/automation/) (Tutorial)

- [Crontab Guru - Interactive Cron Job Expression Generator](https://crontab.guru/) (Interactive Cron Job Expression Generator)

- [Medium Blog - How to Run Cron Jobs and Schedule It](https://medium.com/@ashishb21/how-to-run-cron-jobs-and-schedule-it-d7c417e9c35e) (Medium Blog)

**Local Disk Management**

Local disk management in Linux involves creating, manipulating, and using disk partitions to organize your storage space effectively. Here are some essential commands and considerations:

1. **Displaying Disk Space Usage (`df -h`)**

   - **Command:** `df -h`
   - **Description:** Shows information about the available and used disk space on all mounted filesystems. The `-h` option displays human-readable output (e.g., GB, MB).

2. **Estimating File Space Usage (`du -h`)**

   - **Command:** `du -h [directory/file]`
   - **Description:**  Estimates the total space occupied by a directory or a specific file. The `-h` option displays human-readable output.

3. **Partition Table Manipulation (`fdisk`)**

   - **Command:** `fdisk /dev/sdX` (replace `/dev/sdX` with your actual disk device)
   - **Description:** Launches the `fdisk` tool for advanced disk management tasks like creating, deleting, or resizing partitions. **WARNING:**  Use `fdisk` with utmost caution as improper use can lead to data loss. It's recommended for experienced users.
## Local Disk Management 

**Building a Linux File System (`mkfs`):**

- This command formats the specified partition with the chosen file system type (e.g., `ext4`, `xfs`, `btrfs`). **WARNING:** Formatting a partition erases all existing data, so back up any important information before proceeding.

1. **Mounting a File System (`mount`)**

   - **Command:** `mount /dev/sdXn /mount/point` (replace `/dev/sdXn` with your partition device and `/mount/point` with the desired mount point)
   - **Description:** Mounts a specific partition, making it accessible by the system. The mount point is the directory where the contents of the filesystem will be available.

2. **Unmounting a File System (`umount`)**

   - **Command:** `umount /mount/point` (replace `/mount/point` with the mount point)
   - **Description:** Unmounts a currently mounted filesystem, making it unavailable until mounted again.

3. **Listing Block Devices (`lsblk`)**

   - **Command:** `lsblk`
   - **Description:** Provides detailed information about block devices connected to the system, including disks, partitions, and their properties.

**Resources for Learning More About Local Disk Management:**

* [GeeksforGeeks - Creating Partitions in Windows](https://www.geeksforgeeks.org/create-partitions-of-hard-drive-in-win/)

* [Official Red Hat Documentation - Storage Administration Guide](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/storage_administration_guide/s3-disk-storage-parted-create-part-mkfs)

* [Arch Linux Wiki Guide - Partitioning](https://wiki.archlinux.org/title/partitioning)



**Important Notes:**

- Always back up your data before making any significant changes to your disk configuration.
- Use these commands with caution, especially `fdisk`.
- Consider using graphical tools like `gparted` for a more user-friendly approach to disk management, especially for beginners.
- For system-critical tasks like creating partitions for the main operating system, refer to specific installation guides for your chosen Linux distribution.
