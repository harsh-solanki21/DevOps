# Linux Command Line Notes

## Basic Commands

- `sudo`: Allows regular users to run programs with the security privileges of the superuser or root
- `apt-get`: Command used to install and update packages

## Command Prompt Structure

`harsh21@harsh:~$`

- `harsh21` is the username
- `harsh` is computer name or the host name
- `:` is a simple separator
- `~` sign shows that the user is working in the home directory. If you change the directory, this sign will vanish
- `$` sign suggests that you are working as a regular user in Linux. While working as a root user, '#' is displayed

## Special Characters

- `|`: pipe operator
- `/`: root directory
- `/home`: where all the user home directories are saved
- `/boot`: files required to start(boot) a linux machine
- `/bin`: contains the executable files
- `/var`: contains variable data like logs, databases, websites content etc.

## Navigation Commands

- `cd`: change directory
- `cd /`: moving to root directory
- `cd ..`: moving up one directory level
- `cd ~` or `cd`: take you to your home directory
- `pwd`: present working directory

## Listing Contents

- `ls`: to list the contents of directory
- `ls -R`: to shows all the files not only in directories but also subdirectories
- `ls -a`: to see hidden files
- `ls -l`: to list the contents to directory with details like date, time, etc.
  `drwxrwxr-x 2 harsh harsh 4096 Jul 18 17:26 Linux`
  - 1st Column: File type and access permissions
  - 2nd Column: # of HardLinks to the File
  - 3rd Column: Owner and the creator of the file
  - 4th Column: Group of the owner
  - 5th Column: File size in Bytes
  - 6th Column: Date and Time
  - 7th Column: Directory or File name
- `ls -h`: prints file sizes in human readable format like KB, MB etc

## File Operations

- `cat > filename`: to create new file
- `touch filename`: to create new file
- `cat filename`: to view file
- `cat file1 file2 > newfilename`: to combine two files
- `rm`: to remove file
- `rmdir`: to remove directory
- `mv`: to rename file/directory (mv file1 file2)
- `mv`: to move file (mv filename new_file_location)
- `mkdir`: to create directory
- `cp`: to copy file
- `chmod`: change the access mode of a file (read, write, execute)
- `nano`: to edit file

## Useful Commands

- `tree`: to print out a layout of files and directories under it
- `history`: History command shows all the basic commands in Linux that you have used in the past for the current terminal session
- `grep`: command is used to filter/search for text using strings or patterns. (grep <pattern> <file>)
- `awk`: It uses space as a field separator and separates text into columns. (awk '{print $1,$4}' employee.txt )
- `head -n 5 filename`: it will fetch first 5 entries of file
- `tail -n 4 filename`: it will fetch last four entries of file

## Process Management

- `ps`: lists currently active user processes
- `ps -aux` or `ps -ef`: lists all active processes in long format
- `kill n`: kill process with process id = n
- `kill -9 n`: force to kill process id = n
- `CTRL+z`: force process to move to background
- `fg`: bring process to foreground
- `top`: provides system utilization information
- `time`: calculate time for a given command

## Other Commands

- `find`: search for files in directory hierarchy
- `sed`: stream editor for filtering and transforming text

## Shortcuts and Tips

- "up arrow" key: to bring up the last command that was executed. Each press will bring up the previous command executed
- "tab" key: pressing the tab key can be used to auto-complete the directory and file names while typing paths or filenames
- `#`: is used to write comments

## Special Variables

- `$$`: process id (PID) of current shell
- `$0`: shell script filename being executed
- `$1`, `$2`, `$3`…`$n`: command line argument
- `$#`: number of command line argument
- `$?`: exit status of last command executed
- `$!`: PID of last background command

## Path Navigation

- Absolute paths: start from the root (/)
- Relative paths: relative to the present working directory
  - `.`: present working directory
  - `..`: parent directory
  - `-`: previous working directory
