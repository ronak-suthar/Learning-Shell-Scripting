## Read and Write Files

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
