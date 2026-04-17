[Project Factory Script Explanation Request - Google Gemini.html](https://github.com/user-attachments/files/26835568/Project.Factory.Script.Explanation.Request.-.Google.Gemini.html)# Automated Project Bootstraping

Clone this repository to your local machine:
<img width="776" height="149" alt="image" src="https://github.com/user-attachments/assets/df465e96-bea9-4ce6-8702-21baaa14985d" />


Grant execution permission to the script:

<img width="359" height="142" alt="image" src="https://github.com/user-attachments/assets/d03eefa3-4eb8-48c7-a8c3-15a5077a02d5" />

run the script from your terminal:

<img width="285" height="141" alt="image" src="https://github.com/user-attachments/assets/fc37a075-a408-4df5-a3f2-c841642f79b4" />

The Setup Flow
 You will be prompted to enter a project name. The script creates a parent directory named attendance_tracker_[your_name].

Organization: Files are automatically moved into a structured hierarchy (Helpers/ and reports/).

Configuration: You will be asked if you want to update attendance thresholds.

If 'y': Enter new values for Warning and Failure. The script uses sed to update config.json automatically.

If 'n': The script retains the default values (75% and 50%).

 The script validates your local Python installation before finishing.


The script includes a Process Management Trap designed to handle unexpected interruptions gracefully. This prevents "half-baked" or messy directory structures from cluttering your workspace if you decide to cancel the setup.

How to trigger it:
Run the script: ./setup_project.sh

At any point during the input prompts (e.g., when asked for the project name or thresholds), press Ctrl + C on your keyboard.

Result:

The script catches the SIGINT signal.

It immediately compresses the current project folder into a .zip file named attendance_tracker_[name]_archive.zip.

It deletes the incomplete directory structure.


Once the script completes successfully, your project will look like this:

<img width="776" height="280" alt="image" src="https://github.com/user-attachments/assets/4e2e154f-39df-4622-86d3-0b3a5f53cd12" />
