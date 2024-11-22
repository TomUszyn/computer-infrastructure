# Welcome to my assessment repository for computer infrastructure module.

<img src="img/ai-generated-8988757_640.jpg"  width="640" height="356" img align='center'>

## About This Repository.

The repository represent base for assessment for Computer Infrastucture module. 
The assessment is broken into three overlapping components: a set of tasks, a small project, and a presentational component. 

There are nine tasks listed below and there is the project where is neccesary to automate weather.sh script to run daily and push the new data to the repository.

Here is the list of tasks:

1. Create Directory Structure
Using the command line, create a directory (that is, a folder) named data at the root of your repository. Inside data, create two subdirectories: timestamps and weather.

2. Timestamps
Navigate to the data/timestamps directory. Use the date command to output the current date and time, appending the output to a file named now.txt. Make sure to use the >> operator to append (not overwrite) the file. Repeat this step ten times, then use the more command to verify that now.txt has the expected content.

3. Formatting Timestamps
Run the date command again, but this time format the output using YYYYmmdd_HHMMSS (e.g., 20261114_130003 for 1:00:03 PM on November 14, 2026). Refer to the date man page (using man date) for more formatting options. (Press q to exit the man page). Append the formatted output to a file named formatted.txt.

4. Create Timestamped Files
Use the touch command to create an empty file with a name in the YYYYmmdd_HHMMSS.txt format. You can achieve this by embedding your date command in backticks ` into the touch command. You should no longer use redirection (>>) in this step.

5. Download Today's Weather Data
Change to the data/weather directory. Download the latest weather data for the Athenry weather station from Met Eireann using wget. Use the -O <filename> option to save the file as weather.json. The data can be found at this URL:
https://prodapi.metweb.ie/observations/athenry/today.

6. Timestamp the Data
Modify the command from Task 5 to save the downloaded file with a timestamped name in the format YYYYmmdd_HHMMSS.json.

7. Write the Script
Write a bash script called weather.sh in the root of your repository. This script should automate the process from Task 6, saving the weather data to the data/weather directory. Make the script executable and test it by running it.

8. Notebook
Create a notebook called weather.ipynb at the root of your repository. In this notebook, write a brief report explaining how you completed Tasks 1 to 7. Provide short descriptions of the commands used in each task and explain their role in completing the tasks.

9. Pandas
In your weather.ipynb notebook, use the pandas function read_json() to load in any one of the weather data files you have downloaded with your script. Examine and summarize the data. Use the information provided data.gov.ie to write a short explanation of what the data set contains.

Here is the Project:
In the project the following steps should be done to create the necessary GitHub Actions workflow.

1. Create a GitHub Actions Workflow: In your repository, create a folder called .github/workflows/ (if it doesn't already exist). Inside this folder, create a file called weather-data.yml. This file will define the GitHub Actions workflow.

2. Run Daily at 10am: Use the schedule event with cron to set the script to run once a day at 10am. Include also the workflow_dispatch event so you can test the workflow.

3. Use a Linux Virtual Machine In the workflow file, specify that a Ubuntu virtual machine should be used to run the action.

4. Clone the Repository Have the workflow clone your repository.

5. Execute the weather.sh Script Add a step that runs your weather.sh script.

6. Commit and Push Changes Back to the Repository Finally, configure the workflow to commit the new weather data and push those changes back to your repository.

7. Test the Workflow Commit and push the workflow to your repository. Check the logs in GitHub to ensure that the weather.sh script runs correctly, that new data is being committed.



## Use of This Repository


## Get Started

If you want to be sure that you have the right programming environment for this repository, you should follow these extra steps:

1. Install Anaconda: 
    - Download the Anaconda distribution for your operating system from the official Anaconda website: https://www.anaconda.com/products/individual
    - Follow the installation instructions provided on the website. 
      During instalation MAKE SURE you check the two check boxes
       * Add to PATH variable
       * Make this version your default Python


<img src="img/advanced_option.png"  width="300" height="200" img align='center'>
   

2. Install Git:
    - Download Git for your operating system from the official Git website: https://git-scm.com/downloads
    - Follow the installation instructions provided on the website.

3. Install Visual Studio Code (VS Code):
    - Download Visual Studio Code for your operating system from the official VS Code website: https://code.visualstudio.com/download
    - Follow the installation instructions provided on the website.

4. Configure Git:
    - Open a terminal or Git Bash.
    - Set your name and email address using the following commands:
      ```
      git config --global user.name "Your Name"
      git config --global user.email "your.email@example.com"
      ```

5. Clone the repository to your local machine using the following command:
    ```
    git clone https://github.com/TomUszyn/computer-infrastructure.git
    ```

6. Navigate to the cloned repository:
    ```
    cd computer-infrastructure
    ```

Notice: Make sure you are in the correct patch for the file you are trying to execute. Otherwise, you may encounter an error.

7. Open the [weather.ipynb](https://github.com/TomUszyn/computer-infrastructure/blob/83a3b08d953480f6a6e0b0a56d4d7ecdfac3c3a4/weather.ipynb) in VS Code.


Now the proper programming environment is set up and repository can be explored.

## Get Help

Feel free to reach out if you have any questions or want to talk more about data analysis. I am excited to connect with
other data enthusiasts and share ideas.
Here is my e-mail address: tomaszuszynski3@gmail.com

## Author

Tomasz Uszynski
