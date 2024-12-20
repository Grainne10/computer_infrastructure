# computer_infrastructure

**by Grainne Boyle**

![clockimage](img/watch.jpg)

**README Contents:**

1. [Overview](Overview)
2. [Contents](Repository-Contents)
3. [Tasks](Tasks)
4. [Research](Research)
## Overview

I am a student at the [Atlantic Technological University](https://www.atu.ie/), Galway, studying the Higher Diploma in Science in Data Analytics on a part-time basis over 2 years.  
This repository contains a Jupyter notebook (`weather.ipynb`) and a Bash script (`weather.sh`) that work together to automate weather data collection and analysis.  
The notebook outlines the steps I followed to complete the tasks, while the script automates the downloading of weather data and timestamping of the data. The notebook also includes an analysis of the weather data using the pandas library. I have set up a GitHub Actions workflow to automatically run the weather.sh script daily at 3 AM, download new weather data, and push it to the repository.

## Repository Contents
`weather.ipynb`: A a Jupyter notebook with an explanation of how I completed the tasks, including command usage and data analysis.  
`weather.sh`: A Bash script for automating the download and timestamping of weather data.  
`.github/workflows/weather-data.yml`: GitHub Actions workflow for automating the script to run daily.  
`data/`: Directory containing two subdirectories:  
`timestamps/`: Contains timestamped files and output related to Task 2 and Task 3.  
`weather/`: Contains weather data files saved from Met Eireann in JSON format, as well as timestamped weather data files.  
`requirements/`: A text file listing the dependencies required to run the project, including libraries such as pandas and jupyter.  

## Tasks 

**The tasks in this project involve:** 
Creating a directory and managing Timestamps: Creating and formatting timestamped files.
Downloading Weather Data: Downloading weather data from Met Eireann and automating this process using a bash script.
Data Analysis: Using pandas in a Jupyter notebook to analyze the downloaded weather data.
Automation with GitHub Actions: Setting up a GitHub Actions workflow to automate the weather script execution daily.
For a detailed explanation of each task, refer to the Jupyter notebook weather.ipynb, where I have documented the steps and commands used.

### weather.ipynb
**You can run the notebook on your local machine using either Visual Studio Code (VSCode) or Anaconda:**  
Install Visual Studio Code: If you don’t have VSCode installed, download and install it from Visual Studio Code.  
Install Anaconda: If you don't have Anaconda installed, download it from Anaconda. Anaconda will help you manage the necessary dependencies for running the Jupyter notebook.  
Clone the Repository: Clone the repository to your local machine.  
Install Dependencies: In your terminal, navigate to the project directory and create a virtual environment, refer to the requirements.txt file on which dependencies are needed.  
Open the Project in VSCode: Launch VSCode and open the project folder by navigating to File > Open Folder and selecting your project directory.  
Launch Jupyter Notebook: In VSCode, open the integrated terminal and open the Jupyter notebooks in your browser.  

**You can run the notebook in GitHub Codespaces:**  
Open the Repository in GitHub: Navigate to the repository page on GitHub.  
Launch GitHub Codespaces: On the repository page, click the green Code button and then select Open with Codespaces.  
Install Dependencies: In the Codespace terminal, install the necessary dependencies.  

### .github/workflow/weather-data.yml  
**Weather Data Automation with GitHub Actions**
This project automates the process of collecting, storing, and updating weather data using the weather.sh script and GitHub Actions. The automation ensures that weather data is regularly collected and committed to the repository on a daily basis.  
Script Execution: The weather.sh script fetches the latest weather data from the Met Eireann website and stores it in the data/weather/ directory of the repository.  
Automation: The project uses a GitHub Actions workflow to automate the entire process. The .github/workflows/weather-data.yml file defines the GitHub Actions workflow, which uses cron scheduling to automate the process.  
Execution on Ubuntu VM: The workflow runs on the latest Ubuntu virtual machine to ensure a consistent environment.  
Repository Cloning: The workflow clones the repository to access the required files and directories.  
Script Execution: The weather.sh script is run to collect the weather data.  
Commit and Push: After the weather data is collected, any new data is committed and pushed back to the repository to keep it up-to-date.  
Automatic Execution: The workflow runs daily at 3 AM UTC.  
Manual Trigger: The workflow can also be manually triggered via the GitHub Actions interface for testing or immediate execution.  



Research :
[https://askubuntu.com/questions/731721/is-there-a-way-to-create-multiple-directories-at-once-with-mkdir](https://askubuntu.com/questions/731721/is-there-a-way-to-create-multiple-directories-at-once-with-mkdir) This shows the code to create a sub-directory within a parent directory.

[https://medium.com/@andrewdass/how-to-execute-sh-files-71d8885d8ef3#:~:text=A%20file%20with%20the%20%E2%80%9C.,files%20in%20Unix%20or%20Linux](https://medium.com/@andrewdass/how-to-execute-sh-files-71d8885d8ef3#:~:text=A%20file%20with%20the%20%E2%80%9C.,files%20in%20Unix%20or%20Linux.)



![clock2image](img/clockwork.jpg)