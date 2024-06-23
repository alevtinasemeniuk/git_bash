# Working with Git and Bash 

The ability to work with the bash command line provides a tester with numerous advantages, 
including the ability to quickly view and analyze application and server logs for diagnosing and resolving errors.

Here is my practical work with bash commands as part of my Quality Assurance training.

## Task 1  
**Working with directories and files**
```bash
cd                                                        # Go to home directory
mkdir task                                                # Create a working directory 'task'
cd task                                                   # Go to the 'task' directory
pwd                                                       # Print current directory path
mkdir test1                                               # Create a 'test1' directory into the 'task' working directory
cd test1                                                  # Go to the 'test1' directory
touch file{1,2,3}.txt                                     # Create three files into the current 'test1' directory
ls                                                        # Check directory 'test1' content
cd ..                                                     # Go to the parent directory
mkdir test2                                               # Create a 'test2' directory into the 'task' working directory
rmdir test2                                               # Delete the 'test2' directory
rm test1/file2.txt                                        # Delete the 'file2.txt' from 'test1' directory
mkdir test3 && touch test3/file{1,2}.txt                  # Create a 'test3' directory and two files in it
rm -rf test3                                              # Delete the 'test3' directory and its contents
mkdir test4                                               # Create a 'test4' directory
mv test1/file{1,3}.txt test4/                             # Move 'file1.txt' and 'file3.txt' from 'test1' directory to 'test4' directory
echo line1 >> test4/file1.txt                             # Add three lines with the word "line" to 'file1.txt' of 'test4' directory
echo line2 >> test4/file1.txt
echo line3 >> test4/file1.txt
cat test4/file1.txt                                       # View the contents of 'file1.txt' of 'test4' directory
echo line4 >> test4/file3.txt                             # Add three lines with the word "line" to 'file3.txt' of 'test4' directory
echo line5 >> test4/file3.txt
echo line6 >> test4/file3.txt
cat test4/file{1,3}.txt                                   # View the contents of both files (file1.txt and file3.txt) at the same time
vim test4/file1.txt                                       # Open the vim editor to edit 'file1.txt'
i                                                         # Enable the insert mode of the Vim editor
:wq                                                       # Save and exit the vim editor
```
## Task 2
**Editing files, checking and killing proccesses, pinging websites**
```bash
cd /Users/alevtinasemeniuk/task                                           # Go to working directory
mkdir test3                                                               # Create the 'test3' directory
echo -e "row1\nrow2\nrow3\nrow4" > test3/file4.txt                        # Add three files 4, 5 and 6 to the 'test3' directory, each of which should contain 4 lines row1, row2, row3, row4
echo -e "row1\nrow2\nrow3\nrow4" > test3/file5.txt
echo -e "row1\nrow2\nrow3\nrow4" > test3/file6.txt
grep "row2" test3/file5.txt                                               # Find the line 'row2' in 'file5.txt'
grep -r "row" test3                                                       # Find the line 'row' in the 'test3' directory
grep -c "row" test3/file6.txt                                             # Count how many lines with the content 'row' in the 'file6.txt'
find test3 -name "file5.txt"                                              # Find 'file5.txt' inside the 'test3' directory
find test3 -name "file5.txt" -delete                                      # Using the find command, delete 'file5.txt'
echo "test" > test3/file4.txt                                             # Using the echo command, add the word 'test' to 'file4.txt'
sed 's/test/fail/g' test3/file4.txt                                       # Replace the word 'test' in 'file4.txt' with 'fail'
echo "test" >> test3/file4.txt                                            # Add the word 'test' to 'file4.txt' so that the contents are preserved
ps aux                                                                    # View all processes for users not only in the console that occur in the system
kill 666                                                                  # Terminate process '666' in console
ping artsiomrusau.com                                                     # Find out the availability of the resource artsiomrusau.com using ping
ping -c 5 artsiomrusau.com                                                # Send 5 packages to artsiomrusau.com
curl "https://petstore.swagger.io/v2/pet/findByStatus?status=available"   # Using GET and the curl command, get information about registered pets from https://petstore.swagger.io/
curl -X POST -H "Content-Type: application/json" --data '{                # Using POST and the curl command, create a new user at https://petstore.swagger.io/
  "id": 1,
  "username": "QA",     
  "firstName": "Joe",   
  "lastName": "Black",
  "email": "joeblack@example.com",
  "password": "password123",
  "phone": "1234567890"
}' "https://petstore.swagger.io/v2/user"

```
