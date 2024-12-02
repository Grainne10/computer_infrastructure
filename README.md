# computer_infrastructure
Assessment for computer infrastructure ** by Grainne Boyle

![https://pixabay.com/photos/clock-pocket-watch-clockwork-3179167/](https://pixabay.com/photos/clock-pocket-watch-clockwork-3179167/)

# Tasks 

1. The first step is to create the repository in Github. I then cloned this repository in my own directory in my personal files.
It is important to regularly push this to my own files.
In the repository I also created a git.ignore files for items I do not want to send to the repository e.g. temp files, sample test files and code.
I created a read me document to document my steps and project.

 
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

Research :
[https://askubuntu.com/questions/731721/is-there-a-way-to-create-multiple-directories-at-once-with-mkdir](https://askubuntu.com/questions/731721/is-there-a-way-to-create-multiple-directories-at-once-with-mkdir) This shows the code to create a sub-directory within a parent directory.

[https://medium.com/@andrewdass/how-to-execute-sh-files-71d8885d8ef3#:~:text=A%20file%20with%20the%20%E2%80%9C.,files%20in%20Unix%20or%20Linux](https://medium.com/@andrewdass/how-to-execute-sh-files-71d8885d8ef3#:~:text=A%20file%20with%20the%20%E2%80%9C.,files%20in%20Unix%20or%20Linux.)



![https://pixabay.com/photos/clockwork-church-gears-time-clock-4651185/](https://pixabay.com/photos/clockwork-church-gears-time-clock-4651185/)