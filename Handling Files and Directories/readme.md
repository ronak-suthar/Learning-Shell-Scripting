## Handling Files and Directories

- File Statistics
  1.  Print line count, word count and chararter count
  ```bash
  	wc <file1>
  	wc <file1> <file2> <file3>
  ```
- Reading the Exit Status
  1.  After a command is executed a exit status is set. this status indicates success or error of execution
  ```bash
  	echo $?
  ```
- Paths and Navigation

  1.  Linux File system follows a hierarchical pattern and it starts from root '/'
  2.  Types of path

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

  3.  Navigating

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

  4.  Creating Directories

      1. Creating one/multiple new directories

      ```bash
      	mkdir dir1 dir2 dir3
      ```

      2. Creating directories recursively

      ```bash
      	mkdir -p Movies/ActionMovies/Posters
      ```

  - Copying Files and Directories

  1.  Copy files from source to destination

  ```bash
  	cp <source> <destination>
  	cp file1 file2 file3 <dest dir>
  ```

      -i can be used for confirmation of overwriting

  2.  Copy directories from source to destination

  ```bash
  	cp -r <source> <destination>
  	cp -r <dir1> <dir2> <dir2> <dest dir>
  ```

      -i can be used for confirmation of overwriting

- Renaming/Moving Files
  1.  Renaming files/directories
  ```bash
  	mv <src> <dest>
  	mv fileOldName.txt fileNewName.txt
  	mv dirOldName dirNewName
  ```
  2.  Move files/directories
  ```bash
  	mv <file.txt> <dest dir>
  	mv <dir1> <dir2> <dir3> <dir4> <dest Dir>
  ```
- Deleting files/directories
  ! Carefully use these commands as there is no way back

  1. Deleting file

  ```bash
  	rm file1 file2 file3.....
  ```

  Example : Below deletes all files with name starting with r

  ```bash
  	rm r*
  ```

  2.  Deleting Directories

      - Delete Empty Directories

      ```bash
      	rmdir <dir1> <dir2> ... <dirN>
      ```

      - Deletes directories recusrsively and its contents

      ```bash
      	rm -r <dir1> <dir2> ... <dirN>
      ```
