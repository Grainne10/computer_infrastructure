# computer_infrastructure

**by Grainne Boyle**

![clockimage](img/watch.jpg)

**README Contents:**

1. [Overview](README.md/#overview)
2. [Contents](README.md/#repository-contents)
3. [Tasks](README.md/#tasks)
4. [Research](README.md/#research)

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
For a detailed explanation of each task, please refer to the Jupyter notebook weather.ipynb, where I have documented the steps taken and the commands used.  

### weather.ipynb  
**You can run the notebook on your local machine using either Visual Studio Code (VSCode) or Anaconda:**    
Install Visual Studio Code: If you don’t have VSCode installed, download and install it from [Visual Studio Code](https://code.visualstudio.com/).  
Install Anaconda: If you don't have Anaconda installed, download it from [Anaconda](https://www.anaconda.com/download). Anaconda will help you manage the necessary dependencies for running the Jupyter notebook.  
Clone the Repository: Clone the repository to your local machine using  ```git clone https://github.com/your-username/your-repository-name.git```. Replace `your-username/your-repository-name` with the actual path to your repository.  
Install Dependencies: In your terminal, navigate to the project directory and create a virtual environment, refer to the requirements.txt file on which dependencies are needed.  
Open the Project in VSCode: Launch VSCode and open the project folder by navigating to File > Open Folder and selecting your project directory.  
Launch Jupyter Notebook: In VSCode, open the integrated terminal and open the Jupyter notebook in your browser, where you can navigate to and open weather.ipynb.  

**You can run the notebook in GitHub Codespaces:**  
Open the Repository in GitHub: Navigate to the repository page on GitHub.  
Launch GitHub Codespaces: On the repository page, click the green Code button and then select Open with Codespaces.  
Install Dependencies: In the Codespace terminal, install the necessary dependencies as outlined in the requirements.txt file in the repository.    

### .github/workflow/weather-data.yml  
**Weather Data Automation with GitHub Actions**  
This project automates the process of collecting, storing, and updating weather data using the weather.sh script and GitHub Actions. The automation ensures that weather data is regularly collected and committed to the repository on a daily basis.  
Script Execution: The `weather.sh` script fetches the latest weather data from the Met Eireann website and stores it in the `data/weather/` directory of the repository.      
Automation: The project uses a GitHub Actions workflow to automate the entire process. The `.github/workflows/weather-data.yml` file defines the GitHub Actions workflow, which uses cron scheduling to automate the process at a fixed time daily.    
Execution on Ubuntu VM: The workflow runs on the latest Ubuntu virtual machine to ensure a consistent environment.      
Repository Cloning: The workflow clones the repository to access the required files and directories.  
Script Execution: The `weather.sh` script is run to collect the weather data.  
Commit and Push: After the weather data is collected, any new data is committed and pushed to the repository to the 'data/weather/' directory to keep it up-to-date.    
Automatic Execution: The workflow runs daily at 3 AM UTC as scheduled by cron.    
Manual Trigger: The workflow can also be manually triggered via the GitHub Actions interface for testing or immediate execution.   
Note: Initially, I encountered some issues running the workflow, but this was resolved after ensuring that the necessary permissions were correctly configured. 
Since then,  I verified that the workflow is running correctly by navigating to GitHub Actions and confirming that the daily task has executed. A green checkmark will appear next to the workflow run, indicating its success, and you can review the details of each step that were completed. Additionally, I checked the data/weather/ directory and confirmed that a new file, timestamped for the current day, was generated daily.  

**If you have already cloned the repository and want to confirm or trigger the workflow:**  
Check Workflow Status: Navigate to the Actions tab of the GitHub repository. Here you can see a list of all workflow runs. If the workflow has run successfully, you will see a green checkmark next to the run. Click on the run to view detailed logs of each step.    
Manually Trigger the Workflow: To manually trigger the workflow, go to the Actions tab, select the workflow named Run Weather Daily, and click the Run workflow button.   
 

## Research
1. [mkdir command](https://askubuntu.com/questions/731721/is-there-a-way-to-create-multiple-directories-at-once-with-mkdir) - This shows the code to create a sub-directory within a parent directory.  
2. [sh files](https://medium.com/@andrewdass/how-to-execute-sh-files-71d8885d8ef3#:~:text=A%20file%20with%20the%20%E2%80%9C.,files%20in%20Unix%20or%20Linux.) - This shows you simply what an .sh file is and how explains how it can be used. I used it to set up a simple script which could then be automated.
3. [Met Eireann](https://www.met.ie/climate/available-data/daily-data) - reviewing the daily summary information from one of Met Eireanns weather stations.
4. [GitHub Permissions](https://www.raulmelo.me/en/til/how-to-solve-permission-to-x-denied-to-github-actions-bot#:~:text=Go%20to%20your%20project%20Settings,button%20and%20rerun%20your%20pipeline.) - I had problems getting my workflow to run , this explained how to give permission in my repository to the github.bot on running the workflow.
5. [Cron](https://en.wikipedia.org/wiki/Cron) - Understanding what Cron is and how it works. I used the cron command-line utility as a job scheduler to run the script periodically at a fixed time daily.
6. [Yaml Files](https://spacelift.io/blog/yaml) - I have saved my weather data workflow in a yaml file. YAML is used for configuration files that are parsed and read by a programming language or framework. The programming languages reads the text file, breaks it down into its components and converts it into data that the program can work with.
7. [Github Actions/workflow](https://docs.github.com/en/actions/writing-workflows/quickstart) - I researched how to set up the workflow using this clear documentation alongside following the classes for this course.
8. [Internal Links](https://stackoverflow.com/questions/6695439/how-to-link-to-a-named-anchor-in-multimarkdown#7015050) - I tried several different ways of fixing the Internal links, they worked in codespaces but not in the repository.


------------------------------------------
## END

![clock2image](img/clockwork.jpg)
