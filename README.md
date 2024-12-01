# computer_infrastructure
Assessment for computer infrastructure ** by Grainne Boyle

[Time](https://pixabay.com/photos/clock-pocket-watch-clockwork-3179167/)

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

5. Task 5 : Download Today's weather

 I opened the Met Eireann website and found the weather data for today. I then used wget and   
 ```wget https://prodapi.metweb.ie/observations/athenry/today  ```

 The wget commands allows you to download files from the Internet into your active directory. then i use wget with -O  and this is used to write the output to a file called weather.json

 ```wget+0 weather.json https://prodapi.metweb.ie/observations/athenry/today  ```

 If you open the file, you can see see the data from athenry in json format.

 6. Task 6 : Timestamp the Data

 Using the cURL command,  I downloaded the data again and saved it to a file in my directory with a timestamped name in the format.

 ``` curl -o `date +"%Y%m%d_%H%M%S.json"` https://prodapi.metweb.ie/observations/athenry/today```
This saved the athenry data to a file named "20241116__215129.json which is when the file was created 16th November 2024 at 9:51:29pm. If you open the file you can see the downloaded data from the Athenry weather today.


[https://blog.hubspot.com/website/curl-command](https://blog.hubspot.com/website/curl-command) you can send or retrieve data using this command. cURL is short for "client URL". It can be used instead of the wget command. If you were enter the command with the URL, the URL data will print in the terminal. In our case, we have used it to pull the data and save that data to a file with a stamped name in the format YYYYmmdd_HHMMSS

7. Task 7 : Write the Script

I created a file in my repository called weather.sh. A file with the extension .sh is a shell file or program that can be run in a command line interface. It can be used to automate processes.
The script can command the computer or machine to run  the tasks at a scheduled time. The shebang phrase "#!/bin/bash signifies the file is a shell script and must be the first line of the script.
When I load the command used in the previous step to my script but I want to save the output to the directory data/weather/ that that file is in   ``` curl -o data/weather/`date +"%Y%m%d_%H%M%S.json"` https://prodapi.metweb.ie/observations/athenry/today```
You can also use echo"enter string or variable" By using 'echo', strings or variables can be executed. 

Also, I need to change the mode of the file, when I tried to run it is showed permission denied. The command 'chmod' stands for 'change mode', and 'u+x' instructs the system to give the user(u) permissions to execute (x) the file. I entered ```chmod u+x ./weather.sh``` in the command line. Then when I run the program in the command line,


[https://medium.com/@andrewdass/how-to-execute-sh-files-71d8885d8ef3#:~:text=A%20file%20with%20the%20%E2%80%9C.,files%20in%20Unix%20or%20Linux](https://medium.com/@andrewdass/how-to-execute-sh-files-71d8885d8ef3#:~:text=A%20file%20with%20the%20%E2%80%9C.,files%20in%20Unix%20or%20Linux.)

[Timestamp](https://pixabay.com/photos/clockwork-church-gears-time-clock-4651185/)