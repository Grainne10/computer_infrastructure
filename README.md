# computer_infrastructure
Assessment for computer infrastructure
** by Grainne Boyle

# Getting started

1. The first step is to create the repository in Github. I then cloned this repository in my own directory in my personal files.
It is important to regularly push this to my own files.
In the repository I also created a git.ignore files for items I do not want to send to the repository e.g. temp files, sample test files and code.
I created a read me document to document my steps and project.

2. Task 1 : '

Using codes spaces, I created a new directory structure called data using mkdir. Then I created two sub-directories called timestamps and weather again using mkdir.

3. Task 2 :Timestamps
In the codespace, I ran the command date, this printed the current date and time . Using double angled brackets, I changed the output direction to a new file "now.txt" creating the file at the same time. date >> now.txt. Then, on the command line, I ran this ten times. By using the double angled brackets , it appends the file and shows the output at each stage the command is run. If I were to use a single angled bracket , >, this would over-write the file each time the command is run. The result of the running this command ten times can be seen in the now.txt file and shows a list of dates and time, in this case the same date and hour but different minutes and seconds.

3. Task 3 : Formatting Timestamps
In the codespace, I formatted the date command using YYYYmmdd_HHMMSS, using higher case for year, hour, minute and second , and using lower case for month and day. You can use man date which shows a manual on the date command, it explains the different commands and letters you can use to format your date. When I entered date +"YYYYmmdd_HHMMSS", this shows the date and time in the command line. Next I appended the formatted output date to a file named formatted.txt. I do this by using double angled brackets . I entered, date +"YYYYmmdd_HHMMSS" >> formatted.txt. This creates a new text file in my folder, if you open this text file you can see the date and time it was created.

4. Task 4 : Create Timestamped File
In the codespace, I used the Touch command to create a new timestamped file. I used backtick to capture the output of the command and use it as part of the touch command. I used touch `date +"YYYYmmdd_HHMMSS"`.txt to create an empty timestamped file.