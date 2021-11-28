# Shell Scripting Learning Repo

## Basic Commands

- Basic Commands
	1. Listing Files
	```bash
		ls
	```
	2. Todays Date and Time
	```bash
		date
	```
	3. Logged in User
	```bash
		who
	```
	4. Logged in User Name
	```bash
		whoami
	```
	5. Display Line of text
	```bash
		echo
	```
	6. Reading/Writing from/to file
	```bash
		cat
	```
- Listing Files
	1. list recursively
	```bash
		la -R
	```
	2. classify files
	```bash
		ls -F
	```
	3. reverse alphabetical order
	```bash
		ls -r
	```
	4. long listing format
	```bash
		ls -l
	```
	5. human readable size
	```bash
		ls -h
	```
	6. sort by time
	```bash
		ls -t
	```
	7. sort by size
	```bash
		ls -S
	```
	8. show hidden files
	```bash
		ls -a
	```
- Concatenate files
	1. Print contents of files
	```bash
	cat <filename>
	cat <file1> <file2>
	```
	2. Output file content with line numbers
	```bash
	cat -n <filename>
	```
	3. Create create a copy of file
	```bash
	cat file1 > file2
	```
	4. Appending Conent
		- Append Content from std input
		```bash
		cat >> file
		```
		- Append Content to another file
		```bash
		cat file1 >> file2
		```
- File Statistics
	1. Print line count, word count and chararter count
	```bash
		wc <file1>
		wc <file1> <file2> <file3>
	```
- Reading the Exit Status
	1. After a command is executed a exit status is set. this status indicates success or error of execution
	```bash
		echo $?
	```
	
- Paths and Navigation
	1. Linux File system follows a hierarchical pattern and it starts from root '/'
	2. Types of path
		1. Absolute Path : Full Path Starting from Root
		
			Example
			```bash
			  /home/user/Desktop/Movies
			```
		2. Relative Path : Refers to location that is relative to current directory

			Example
			```bash
				/user/Desktop/Movies
			```
			Assuming Current Directory is home
	3. Navigating 
		1. Change Directory
		```bash
			cd path
		```

		2. One Level Up to Parent Directory
		```bash
			..
		```
		
		3. Present/Print Working Directory 
		```bash
			pwd
		```
	4. Creating Directories
		1. Creating one/multiple new directories
		```bash
			mkdir dir1 dir2 dir3
		```

		2. Creating directories recursively
		```bash
			mkdir -p Movies/ActionMovies/Posters
		```
	



