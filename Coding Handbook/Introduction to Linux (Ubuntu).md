
### 1. Introduction

Linux is a family of **open-source** operating systems based on the Linux kernel, which is highly customizable as its kernel and operating system code is available on the internet, allowing anyone to fork and modify the code in order to suit their needs.

As such, Linux is a **popular choice** both as a **server** and as a **desktop** for people to interact with. Some distributions of Linux may include **Ubuntu**, **Debian**, as well as Remnux. While Ubuntu and Debian are usually for people who generally like the style of Linux, Remnux is an operating system built for malware analysis, and as such the operating system comes pre-packed with hundreds of tools for people to test their malware and perform other tasks with.

Linux and Windows have their similarities, just that they come in different forms. With the first example being the command-line interface, also known as CLI.


### 2. Command-Line Interface (CLI)

The command-line interface in Windows is also known as Command Prompt, within Linux, it's simply called a **Terminal**.

In Linux, you don't get a friendly Desktop interface like you do in Windows. Usually, all you get is just the Terminal. As such, it is a powerful tool which is able to manipulate almost anything on the computer.

If you are logged in as `student` and the name of the computer is called `student-vm`, opening the Terminal will greet you with this line:
```shell
student@student-vm:~$ 
```
From this format, you can determine that this format is used:
```bash
(logged_in_username)@(computer_name): (current_directory)$  
```

When you start in the `~` directory, you are in the root directory of the filesystem. That is where you will find all your other directories, such as `/boot`, `/etc`, `/cdrom`, `/home`, `/dev`, `/proc`, `/sys` and `/bin`. 


### 3. The File System Hierarchy

In Windows, many things about the kernel is hidden from you, but it doesn't mean they don't exist. Things that are hidden in Windows are mostly data about the kernel, as well as how it loads.

Since Linux is open-source, they have no reason to hide data about the kernel. In Linux, everything is a file. Your loaded drivers, plugged in USB devices all have a file inside the file system, containing data about the device itself.

As such, the most common directories mentioned above are their own compartments for storing files related to different parts about the computer.

  - `/boot` - Used to store critical system files for booting the system.
  - `/etc` - Used to store system configuration files for different applications and services, of which some may include user account information (`/etc/passwd`) and DNS resolution data (`/etc/hosts`).
  - `/cdrom` - Used to mount the inserted CD/DVD drive into the computer.
  - `/home` - Similar to accessing your profile's documents, desktop, downloads, pictures and videos, this directory stores this data inside here with the following format: `/home/(username)/`. For example, if you want to access the `student`'s downloads folder, you can use `cd` and go into `/home/student/Downloads`.
  - `/dev` - Used to store device files that each represent a connected device, whether virtual or physical. Hard drives (such as `/dev/sda`, `/dev/sdb`), USB devices (`/dev/usb`) and serial ports (`/dev/ttyUSB0`) data are stored here.
  - `/proc` - Used to store information about running processes, and stores real-time information about the system's CPU usage, memory usage and also mounted filesystems. Files in `/proc` are real-time and will always change according to the computer's current state.
  - `/sys` - Used to store information about the system's hardware and devices. Hardware configurations and device drivers may be stored here.
  - `/bin` - Used to store executable programs. Similar to how `.exe` files may be stored on the Desktop to access, executable programs to the most basic of commands such as `ls`, `cp` and `rm` are stored here.


### 4. File Permissions

Permissions in Windows exist too, which basically define which Users or Groups can access and modify what resource. Similar to Windows, Linux also has its file permissions.

These can be displayed using `ls -l` (List files using long listing, which also displays permissions and other information).

Consider the following example:
```bash
drwxr-xr-x 2 student student 4096 May 31 04:51 Desktop
```

1. `d` at the start means that `Desktop` is referring to a directory, not a file.
2. `rwxr-x-r--` - When you encounter this string of 9 characters, break it down 3 by 3.
      - `r` means Read, `w` means Write and `x` means Execute.
      - `rwx` - This represents the permissions for the owner of the file/directory. (All allowed)
      - `r-x` - This represents the permissions for the user group. (Read and execute only)
      - `r--` - This represents the permissions for other users. (Read only)
3. `2` refers to the amount of links to the directory.
4. First `student` - This is the owner of the directory.
5. Second `student` - This is the group associated with the directory.
6. `4096` - This number represents the size of the directory in bytes.
7. `May 31 04:51` - This date represents when the directory was last modified.


In order to modify file permissions, you may do it using the `chmod` and `chown` commands. However, you have to be `root` first, which you can grant by doing `su`.

`chmod` modifies file permissions, while `chown` grants you ownership of the files.

`chmod` can be used like so:
```bash
chmod (permission) (file/directory)
```

`permission` can be created using a format, where `+` is grant permission and `-` is remove/deny permission, `u` for user, `g` for group and `o` for others.

Example:
`u+w` - This will **grant** the current user permission to write to a file/directory.
`o-r` - This will **deny** other users permission to read a file/directory.
`g-x` - This will **deny** members in the group permission to execute the file.

While `chown` can be used like so:

```bash
chown [options] user[:group] file(s)
```
where `[ ]` are optional fields.


For example, if you want to grant ownership of `Desktop` to only a user called Harry, you can do `chown Harry Desktop`.

However, if you want to grant ownership of `Desktop` to both the user Harry and also a group called `Students`, you may do `chown Harry:Students Desktop`.

If you want to grant ownership of `Desktop` to only the group `Staff`, you can do `chown :Staff Desktop`.



