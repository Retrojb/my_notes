# Command Line 
#commandline #cmd #scripts

### Command Line: 
#find
Find all files with certain parameters
`sudo find / -iname *.app`

`_EOF_`= End of File

#### I/O redirect: 
Print the results of a command to a file :
	* *creates* a new file everytime	`ls -a > output-file.txt`
	* *appends* to the current file	   `ls -a >> output-file.txt`
	* *input to output* `sort < file_list.txt > sorted_file_list.txt`
##### Common Commands 
* sort : sorts files
* grep : exams input lines and outputs results of the pattern 
* uniq : removes duplicate lines of data
* fmt : format input 
* head : top down display
* tail : down up display of files
* sed : text translator
* awk : programming language for constructing filters

>  *Printing from the command line.* Linux provides a program called  [lpr](http://linuxcommand.org/lc3_man_pages/lpr1.html)  that accepts standard input and sends it to the printer. It is often used with pipes and filters. Here are a couple of examples:
> cat poorly_formatted_report.txt | fmt | pr | lpr
> 
> cat unsorted_list_with_dupes.txt | sort | uniq | pr | lpr 

To use a variable use $variable_name
Calling / printing a variable or function 
	variable: $VARIABLE_NAME
	function: $(function_name)

#if #cmd
If checks like a regular conditional argument. 
	``if command; then 
			command;
		[elif command; then
			command2
		[else command]
			fi``
The `test` is used like a boolean

* -d /file/
	* True if /file/ is a directory.
	
* -e /file/
	* True if /file/ exists.
	
* -f /file/
	* True if /file/ exists and is a regular file.

* -L /file/
	* True if /file/ is a symbolic link.

* -r /file/
	* True if /file/ is a file readable by you.

* -w /file/
	* True if /file/ is a file writable by you.

* -x /file/
	* True if /file/ is a file executable by you.

* /file1/ -nt /file2/
	* True if /file1/ is newer than (according to modification time) /file2/

* /file1/ -ot /file2/
	* True if /file1/ is older than /file2/

* -z /string/
	* True if /string/ is empty.

* -n /string/
	* True if /string/ is not empty.

* /string1/ = /string2/
	* True if /string1/ equals /string2./

* /string1/ != /string2/
	* True if /string1/ does not equal /string2./

