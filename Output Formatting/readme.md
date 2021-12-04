## Input and Output Formatting

1. echo statement formatting
    - Using \n and \t for new line and tab space respectively.

    - To enable interpretation of escape sequence we use -e

    - Example

    ```bash
        echo -e "Hello\n World"
        echo -e "How \t Are\t You?"
    ```
2. printf statement formatting
    - formats s:String,c:Character,d:Integer,f:Float
    - new line needs to be added at end of statement explictly"
    
    - Examples
        - Syntax for Printing
            ```bash
                printf "%s" "String"
            ```
        - Right Alignment
            ```bash
                printf "%10s" "String"
            ``` 
        - Left Alignment
            ```bash
                printf "%-10s" "String"
            ```
3. Pipe & Tee Operator |,tee 

    - Used to combine output of two or more commands
    - Tee Operator
        - Takes Input and Write it to file and stdout
    - Examples
        - Write output of ls to a file/stream

        ```bash
            ls -al | more
            ls -al | cat > file.txt
            ls -al | tee file.txt
            ls -al | tee -t file.txt
        ``` 
4. Input Redirection
    - command < input file
    - Read input from user
        - ```bash
            read userName
            echo $userName
         ```
    - file descriptor 
        - STDIN : 0
        - STDOUT : 1
        - STDERR : 2
        