# :baby: BB terminal prompt assistant
BB comes as an option to the default "alias" command and it's a simple program to abbreviate long prompts in GNU/Linux terminal.
You can easily set rules, delete them, list them and update them with a clear list of parameters. It should be functional in any GNU/Linux distribution.

⭐ **FEATURES**

* Simplify your long commands in terminal

* Improve your times at making repetitive tasks

* You don't need to open any config file

* Store, list, update and delete rules

* Run a block of rules easy

* Import rules from a public repository for an specific GNU/Linux distro

* Import rules from a local file

* Export rules to a local file
  

:white_check_mark: **INSTALLATION**

Go to release section and download the latest version, in that page you can find the installation instructions for the binary files.


:ballot_box_with_check: **COMPILE YOURSELF**

If you preffer to compile yourself the source code you need to download the _main.go_ file and create a file named _etc/bb/bb.conf_, then run the following commands:

`go mod init bb`

`go build -o bb`

**Previous requirements to compile:** golang ('gcc-go', 'golang-bin')

To install Golang in your system run

  `sudo dnf install golang` or `sudo apt install golang` depending on your GNU/Linux distribution.
  

:pencil: **CREATING RULES**

First step after install the program is run `bb -h` to know about how the script functions. Some examples to create rules in a Fedora system terminal:

  `bb -n update "sudo dnf update -y && sudo dnf upgrade -y"` this long command will run after with only type `bb update`.

  `bb -n ssh "ssh user@example.com"` will connect to your SSH server only typing `bb ssh`

  Running a block of rules is as easy as run `bb <name1> <name2>`. This command will run two rules continuously but you can set as many as your implementation let.
  

:pencil: **LISTING RULES**

There are two options to list the rules stored in baby.conf file.

  `bb -l` will list all the rules stored in baby.conf file.

  `bb -ln <name>` will list an specific rule.

:pencil: **IMPORTING RULES FROM A URL**

You can import rules previously stored in a file on the web.

  `bb -i <url>` will import all rules stored in a URL.

  To make this possible you must store your rules in this format: `b:<rule> = <command>:b`

  The URL must to point to a file with a valid extension (.txt, .html, .md, etc), i.e: https://example.com/rules.txt

:pencil: **IMPORTING RULES FROM A LOCAL FILE**

  `bb -i <path>` will import all your rules stored in a local file.

  To make this possible you must store your rules in this format: `b:<rule> = <command>:b`

:pencil: **EXPORTING RULES TO A LOCAL FILE**

  `bb -e` will start the export assistant.

:pencil: **REMOVING RULES**

  `bb -r <name>` will remove an specific rule.
  
  `bb -r a` will remove all rules stored in baby.conf.

# ⚙️ **TESTED ON**

🟢 Elementary OS

🟢 Debian

🟢 Linux Mint

🟢 MX Linux

🟢 Fedora

🟢 AlmaLinux

🟢 Zorin OS

🟢 Endeavour OS
