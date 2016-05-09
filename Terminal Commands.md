Some commands can be found in the `bin` directory.

`ls` - list files<br>
`ls -a` - display hidden files and folders<br>
`ls -R` - provide a tree listing of directory structure.<br>
`ls -s` - list sorted according to size<br>
`ls -t` - list sorted according to time of modification<br>
`ls -r` - reverses sorting<br>
`ls -l` - displays extra details like size, user, date, permissions<br>

`cd <path>` -> change directory<br/>
(`cd ..` -> takes to parent directory<br/>
 `cd` -> takes to user directory[denoted by ~]<br/>
 `cd -` -> takes to the previous directory we were in)<br/>

- **Trivia:** `user` directory is present in the `home` directory which is present in the `root` directory. Then there is no upper directory.

`pwd` - print working directory

`^` symbol is used for representing 'ctrl'  ... e.g. `^C` = ctrl key + c

`touch <filename>`- creates a new file with any extension we want.

- **Trivia:** Some text editor like **nano** ,**vim** and **emacs** can be used to edit the code on the terminal itself.(writing `nano hello.cpp` opens file `hello.cpp` in terminal)

`rm` - used to remove a file.<br/>
`rm -r` - used to remove a directory.<br/>
`mkdir` - makes a directory<br/>
`rmdir` - removes an **empty** directory<br/>

`cp file1 file2` - used to copy file1 to file2.<br>
`mv file1 file2` - used to move file1 to file2.

- **Trivia:** `mv oldfilename newfilename` is the best method to rename a file.

`grep <text to search> <files to search in>`

`cut` is used to cut a part of a file<br>
`cut -c 2-5 file` - cut characters 2 to 5 from each line of file<br>
`cut -d"x" -f 1 file` - returns each part of every line before first occurance of 'x' (-d is delimiter and -f is field)


`clear` or `^l` - scrolls down to an empty screen

`reset` - change terminal to default settings

`find <query>` - finds files and directories with name `query` in the current directory and its subdirectories<br/>
`find -d <query>` - looks for a directory with name `query`<br/>
`find -f <query>` - looks for a file with name `query`<br/>

`history` - shows all typed commands history<br>
`history n` -shows last n commands

`!<text>` - repeats a previous command in history which started with 'text'
`!!` - repeats the previous command
`sudo !!` - repeats the previous command as sudo

`man <command>` - shows manual for that command. Manual contains all the flags realated to that command.

`.` - refers to current directory<br/>
`..` - refers to parent directory<br/>

- **Trivia:** Files with file names starting with `.` are hidden.

`echo "hello"` - prints hello on the terminal

`>` - used to store the output of a task in some file(overwrites if file with same name is present) rather than displaying it on the terminal.<br/>
`>>` - same task as `>` but does not overwrites just appends to the file with the same name.<br/>

`|` - piping is used to give the output of a command as input to another command ..for e.g `history | grep "find"` will search for "find" in the output of `history`

`<command> | tee <filename>` - used to show output of `command` on terminal as well as writing the output to a file `filename`.<br/>

`cat` - used to open a file in terminal in read-only format<br>
`cat file1 > file2` - copies content of file1 one to file2<br>
Unless you have infinite scrolling turned on (available in Profile Preferences -> Scrolling tab of the terminal), there is a limit to how many lines you can see on the screen.

Piping the output using `less` allows the user to advance through the content by pressing SPACE, move backwards by pressing 'b' and quit using 'q'. Pressing ESC followed by SPACE allows you to scroll down one screen at a time.

`cat file | less`<br>

`history | less` or `cat ~/.bash_history` will let you scroll through previously typed commands.

Piping the outmout using `more` is similar to using `less`, but allows viewing one screen at a time.

- **Trivia:** All commands typed in the terminal are saved in `history` or the `.bash_history` file in the home directory.

##### Aliases <br/>
An alias is a word assigned to a statement, and acts as a keyboard shortcut.

`alias foo='bar'` - would pass "bar" whenever foo is entered.

This alias lasts as long as the terminal is running. To create a permanent alias, append this line to `~/.bash_profile` or `~/.bash_aliases`

##### Some common network debugging commands <br/>
`ifconfig` - when used without any flags, used to display the status of all active network interfaces.<br/>

`iwconfig` - similar to `ifconfig`, but used for wireless network interfaces. <br/>

##### Extracting .tar files <br/>
`tar -xvzf file.tar.gz` - used to extract the .tar.gz file<br>
-f: this must be the last flag of the command, and the tar file must be immediately after. It tells tar the name and path of the compressed file.<br>
-z: tells tar to decompress the archive using gzip<br>
-x: tar can collect files or extract them. x does the latter.<br>
-v: makes tar talk a lot. Verbose output shows you all the files being extracted.

##### Process Management <br/>
`ps` returns the snapshot of current processes.<br>
`ps -e` returns every process running on the system<br>
`ps -u <useraccount>` returns list of processes running on user account.<br>
`ps -u <useraccount> | grep <Application>` - fetches all processes of "Application"

The left most number returned by the `ps` command is called the Process ID (PID).
A particular process can be terminated using `kill`

`kill <PID>` - kills the process having PID as that entered.<br>
`kill -9 <PID>` - performs a violent kill<br>
`killall <processname>` - kills all instances of processname

##### Flags

`-f` forcefully do a task i.e. without asking for confirmation<br/>
`-r` recursively do a task(looks in subdirectories too)
