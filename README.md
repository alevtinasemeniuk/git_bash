# Working with Git and Bash 
## Table of Contents
- [Working with Bash](#working-with-directories-and-files)
- [Working with Git]()

## Working with Bash
The ability to work with the bash command line provides a tester with numerous advantages, including the ability to quickly view and analyze application and server logs for diagnosing and resolving errors.

Here is my practical work with bash commands as part of my quality assurance training.

## Task 1  
**Working with directories and files**
```bash
cd                                                    # Go to home directory
mkdir task                                            # Create a working directory 'task'
cd task                                               # Go to the 'task' directory
pwd                                                   # Print current directory path
mkdir test1                                           # Create a 'test1' directory into the 'task' working directory
cd test1                                              # Go to the 'test1' directory
touch file1.txt file2.txt file3.txt                   # Create three files into the current 'test1' directory
ls                                                    # Check directory 'test1' content
cd ..                                                 # Go to the parent directory
mkdir test2                                           # Create a 'test2' directory into the 'task' working directory
rmdir test2                                           # Delete the 'test2' directory
rm test1/file2.txt                                    # Delete the 'file2.txt' from 'test1' directory
mkdir test3 && touch test3/file1.txt test3/file2.txt  # Create a 'test3' directory and two files in it
rm -rf test3                                          # Delete the 'test3' directory and its contents
mkdir test4                                           # Create a 'test4' directory
mv test1/file1.txt test1/file3.txt test4/             # Move 'file1.txt' and 'file3.txt' from 'test1' directory to 'test4' directory
echo line1 >> test4/file1.txt                         # Add three lines with the word "line" to 'file1.txt' of 'test4' directory
echo line2 >> test4/file1.txt
echo line3 >> test4/file1.txt
cat test4/file1.txt                                   # View the contents of 'file1.txt' of 'test4' directory
echo line4 >> test4/file3.txt                         # Add three lines with the word "line" to 'file3.txt' of 'test4' directory
echo line5 >> test4/file3.txt
echo line6 >> test4/file3.txt
cat test4/file1.txt test4/file3.txt                   # View the contents of both files (file1.txt and file3.txt) at the same time
vim test4/file1.txt                                   # Open the vim editor to edit 'file1.txt'
i                                                     # Enter the insert mode of vim editor
:wq                                                   # Save and exit the vim editor
```
