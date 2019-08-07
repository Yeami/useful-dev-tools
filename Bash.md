# Ubuntu Bash
---

## The Basics

#### First Commands, Navigating the Filesystem

```sh
Print the user working directory: $ pwd
```
```sh
List the contents of this directory: $ ls
```
```sh
Change directory: $ cd
```
```sh
Go to parent directory: $ cd .. 
```
```sh
Go to home directory: $ cd || cd ~
```
```sh
Go back to the most recent directory: $ cd - 
```
```sh
Commands chaining: $ cd path && pwd && ls
#But with &&, the command to the right will not run if the command to the left fails.
```
```sh
Commands chaining: $ cd path ; pwd ; ls
#But with ;, the second command will run even if the first one fails.
```
```sh
Clear terminal: $ clear
#Move the current terminal line to the top of the screen.
```
#### Getting Help
```sh
Bring up a help menu for any command: $ command --help
```
```sh
Bring up a manual for any command: $ man command 
```
#### Viewing and Editing Files
```sh
Outputs the first few lines of a file: $ head {name}
#The -n flag after head specifies the number of lines to show (the default is 10).
```
```sh
Outputs the last few lines of a file: $ tail {name}
#The -n flag after tail specifies the number of lines to show (the default is 10).
#Or you can get the end of the file beginning from the N-th line with tail -n +N.
```
```sh
Outputs file contents : $ cat {name}
#Can be used with just a single file, or multiple files.
```
```sh
Quickly viewing a file in read-only window: $ less {name} || more {name}
```
```sh
Minimalistic command-line text editor: $ nano {name}
```
#### Creating and Deleting Files and Directories
```sh
Create new empty file: $ touch {name} 
```
```sh
Remove any file: $ rm {name} 
```
```sh
Create new directory: $ mkdir {name} 
```
```sh
Remove empty directory: $ rmdir {name} 
```
```sh
Remove directory and all of its contents: $ rm –rf {name} 
```
#### Moving and Copying Files, Making Links, Command History
```sh
Moves a file: $ mv {name} path
```
```sh
Renames a file: $ mv {first-name} {second-name}
```
```sh
Copies a file: $ cp {name} {copy-name}
```
#### Disk, Memory, and Processor Usage
```sh
Displays all currently-running processes: $ top || htop
#And their owners, memory usage, and more
```
#### REPLs and Software Versions
```sh
Open the programming language REPL: $ {language-name}
#python, scala, R, jshell...
```
```sh
Get software version: $ {name} --version 
```
#### Finding Things
```sh
Searches for "possibly useful": 
$ whereis {name}
#It will attempt to return the location of the binary, source and man page for that command.
$ which {name}
#It will return the location of the binary.
$ whatis {name} 
#It will return the one-line description of a command from its man page.
```
```sh
Finds a file anywhere on the system: $ locate {name}
```
#### APT Package Manager
apt-get is a package management utility
```sh
: $ sudo apt-get install {name} - Установить пакет {name}. 
```
```sh
: $ sudo apt-get update - Обновить информацию о пакетах, содержащихся в репозиториях.
```
```sh
: $ sudo apt-get upgrade - Обновление пакетов, для которых в репозитории доступны новые версии.
```
```sh
: $ sudo apt-get remove {name} - Удаление пакета {name} из системы.
```
```sh
: $ sudo apt-get purge {name} - Удаление пакета {name} и очистка системы от его конфигурационных файлов.
```
apt-cache is utility that allows to execute requests to APT cache.
```sh
: $ sudo apt-cache search - Поиск пакета по части названия или описания. Поддерживает регулярные выражения.
```
```sh
: $ sudo apt-cache show - Информация о пакете: версия, размер, описание и т.п.
```
```sh
: $ sudo apt-cache depends - Зависимости указанного пакета.
```
```sh
: $ sudo apt-cache rdepends - Обратные зависимости пакета.
```