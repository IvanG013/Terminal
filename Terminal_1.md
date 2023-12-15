# Homework | Linux Terminal | part_1
___
All the commands are written in GitBash
___

1. Check where am I:

>pwd

2. Make a new folder:

>Mkdir Itest

3. Go to the created folder:

>cd Itest

4. Make 3 new folders:

>mkdir folder_1 folder_2 folder_3 or

>mkdir -p {folder_1,folder_2,folder_3}

5. Go to any of these 3 folders:

>cd folder_1

6. Create 5 files (3 txt, 2 json)

>touch app {file_1.txt,file_2.txt,file_3.txt,file_4.json,file_5.json}

7. Create 3 new folders:

>mkdir folder_4 folder_5 folder_6

8. Show the list of current folder elements:

>ls folder_1

9.  Open one of txt files

>vim file_1.txt

10. Write anything in this file

>I - to edit

11.  Save and quit:

>esc,shift+:,w,q,enter

12. Go to the directory located 1 level above:

>cd ..

13. Move any 2 files to any folder:

>mv folder_1/file_1.txt folder_2/file_1.txt

>mv folder_1/file_2.txt folder_2/file_2.txt

14. Copy any 2 files to any folder:

>cp folder_1/file_4.json folder_3/file_4.json

>cp folder_1/file_5.json folder_3/file_5.json

15. Find a file by name:

> find -iname file_3.txt

16.  Show file content in real time, filtered by a keyword:

>tail -f file_1.txt

>ctrl+c - to exit

17. Show several of the first lines from the text file:

>head -4 file_1.txt

18. Show several of the last lines from the text file:

>tail -4 file_1.txt

19. Show content of a large file:

>less file_2.txt

>type -N to show string numbers
>press space to go to the next page
>q - to exit

20. Show current date and time:

>date

___
___
Additional tasks:*

1) Send an http request to the server http://162.55.220.72:5006/terminal-hw-request.

>I've sent: curl http://162.55.220.72:5006/terminal-hw-request

>Answer: "Hello!! This is your the first response from server"
___
___

2) Write a bash script which does the steps above 3, 4, 5, 6, 7, 8, 13

Create a file: touch script.sh

Editing the file: vim script.sh

Press the button "i"

Write:

>#!/bin/bash

>cd Itest

>mkdir folder_1 folder_2 folder_3

>cd folder_1

>touch app {file_1.txt,file_2,file_3.txt,file_4.json, file_5.json}

>mkdir folder_4 folder_5 folder_6

>ls -la

>cd ..

>mv folder_1/file_1.txt folder_2/file_1.txt

>mv folder_1/file_2.txt folder_2/file_2.txt

>Save and exit: esc,:,w,q,enter

>Executing the script: ./script.sh 







