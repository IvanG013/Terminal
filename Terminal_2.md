# Homework | Linux Termina2 | part_2
___
All the commands are written in GitBash
___

1. Create a folder named dir_1:

>mkdir dir_1

2. Go to the folder dir_1:

>cd dir_1

3. Create a folder named inner_dir_1:

>mkdir inner_dir_1

4. Check where you are:

>pwd

5. While located inside the dir_1 folder, create an empty text file named tf_1.txt:

>touch tf_1.txt

6. While located the dir_1 folder, create a text file named tf_2.txt using the command cat with the following lines:

-the first 1
-the second 2
-the third 3

>cat > tf_2.txt                    
the first 1
the second 2
the third 3 

>Press Enter and Ctrl+D to save and quit

7.  Use the cat command to create a text file named tf_3.txt with any lines:

>cd inner_dir_1

8. Use the cat command to create a text file named tf_3.txt with any lines:

> cat > tf_3.txt
I want
to improve
my skills

>Press Enter and Ctrl+D to save and quit

9.  Use the cat command to add the line "the second 2" to the text file tf_3.txt:

>cat >> tf_3.txt                  
the second 2

10. Use the cat command to add the line "the sec 2" to the text file tf_3.txt:

>cat >> tf_3.txt                  
the sec 2

11.  Use the cat command to add the line "the sec 3" to the text file tf_2.txt:

>cd . (to inner_dir_1)
>cat >> tf_2.txt
the sec 3
or
>cat >> ../tf_2.txt
the sec 3

12. Use the cat command to add the line "the SeCoNd 2" to the text file tf_3.txt:

>cat >> tf_3.txt
the SeCoNd 2

13. Use the cat command to add the line "the seConD 2" to the text file tf_2.txt:

>cat >> ../tf_2.txt               
the seConD 2

14. Create a text file named tf_4.txt with 15 lines:

>The seq command with cat combination is the best option, if we want just numbers on each line:

>seq 15 | cat > tf_4.txt

15. Create a text file named tF_5.txt with 13 lines

>seq 13 | cat > tf_5.txt

16. Display a list of all files in the folder:

>ls

17.  Go out of the inner_dir_1 folder:

>cd ..

18. Display the contents of the file tf_3.txt in the terminal:

>cat inner_dir_1/tf_3.txt

Result:

>I want    
to improve
my skills

the second 2
the sec 2
the SeCoNd 2


19. Find the path to the file tf_4.txt:

>find command is the best way to search for the files and their paths. Also, adding -name parameter to show that we want to search for the names:

>find ./ -name "tf_4.txt"

Result:

>./inner_dir_1/tf_4.txt

20. Clear the contents of the file tf_4.txt without deleting the file itself:

>Let's use the > operator and redirect the empty output to the file:

>">" inner_dir_1/tf_4.txt (without "")

21. Find the paths to files that have "tf" in their name:

>find ./ -name "*tf*"

22. Find the paths to files that have "tf" in their name with letters in any case:

>find ./ -iname "*tf*"

23. Find lines in files that contain the letter combination "sec" in the current folder:

>grep command is being used to search for strings inside the files. An asterisk (*) means searching for strings in all the files

>grep "sec" ./*

24. Find lines in files that contain the letter combination "sec" in any case in the current folder:

> we can ignore the case sensitivity by -i

>grep -i "sec" ./*

25. Find lines in files that contain only the "sec" letter combination in the current folder:

>To search for the whole words, we have to use -w with grep:

>grep -w "sec" ./*

26. Find lines in files that contain only the "sec" letter combination in any case in the current folder:

>grep -iw "second" ./*

27. Find lines in files that contain the letter combination "second" in the current folder:

>Let's try recursive search with grep -r, which allows us to search also inside inner folders of the current directory:

>grep -r "second" ./*

28. Find lines in files that contain the letter combination "second" in any case in the current folder:
Using grep -ir

>grep -ir "second" ./*

29. Find lines in files that contain the letter combination "second" in all subfolders:
If we want to look for such strings in all subfolders, ignoring the current folder, we have use a simple grep and specify the path and use asterisks (*):

>grep "second" ./*/ *

30. Find only the path and file name in lines that contain the letter combination "second" in the current folder:

>grep -ls "second" ./* 

31. Find all lines in all files that do not contain the combination "second":

>grep -rv "second" ./

32. Find only the names and paths of files that do not contain the combination "second":

>To show only files without matches, we have to use the -L. 

>grep -rL "second" ./*

33. Display the last 4 lines of any text file in the terminal:

>tail command can be used here. We also use -n and type number of strings to be shown.

>tail -n4 inner_dir_1/tf_3.txt

34. Display the first 4 lines of any text file in the terminal:

>using head command:

>head -n4 tf_2.txt

35. One-line command. Create a folder and create a text file with content:

>Here we can combine already known commands mkdir and cat > and use e.g. && to connect these commands. && means 'if the previous command executed successfully, execute the next command':

>mkdir folder_13 && cat > tf_13.txt
I love football

>Then type Enter and Ctrl+D to save and quit

36. One-line command. Move all text files that contain the word "sec" in their content to any single folder.

>The next one-line commands are executed using xargs, which reads items from input and passes them as arguments to a specified command. 

>With mv command:

>grep -rl "sec" ./ | xargs -I{} mv {} folder_13

37. One-line command. Copy all text files that contain the word "sec" in their content to any single folder.

>With cp command:

>grep -rl "sec" ./ | xargs -I{} cp {} inner_dir_1

38. One-line command. Find all lines with "sec" in all text files, copy and paste these lines into one newly created text file.

>Here, with grep -rh (where -h "cuts" the file names as we need only lines) and > operator.

>grep -rh "sec" ./ | xargs -I{} echo {} > tf_07.txt

39. One-line command. Delete text files that contain the word "sec" in their content.

>Combination of grep -rl and rm -f to remove files:

>grep -rl "sec" ./ | xargs -I{} rm -f {}


40. Simply output the string "Good job!!" to the terminal.
echo command gives an opportunity to output any text:

>echo command gives an opportunity to output any text:
___
