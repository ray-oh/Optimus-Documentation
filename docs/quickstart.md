# Getting Started  
## Installation
Step-by-step guide to installing OPTIMUS RPA.    
## Quick Start Guide  
A simple example to get users up and running quickly.  
### Demo of OPTIMUS RPA  
![logo](https://user-images.githubusercontent.com/115925194/210501100-910d4f94-10cd-428a-980a-c2984a7ed739.png)  
Here is a demo of OPTIMUS RPA completing the RPA challenge in under 10 seconds [demo video](https://www.youtube.com/watch?v=BWfCpwz76io)   
Action was defined by less than 10 steps of actions defined in following Excel script:  
![Optimus Excel script](https://github.com/user-attachments/assets/977200e5-bb31-4d04-9d12-d8955d15f1a0)
This Excel script demonstrates a few key features and versatility of the OPTIMUS automation language:  
1. **keyword-driven**: intuitive key words to perform various automation actions e.g. url (to go to specified url), click, download etc.  
2. **modular actions**: define your own complex blocks of action comprising of a list of automation steps e.g. fill form.  
3. **iteration and loops**: support more complex automation flows like performing a block of actions for every item in the table.  
4. **variables and tables**: rich user defined parameters to support complex automation flows.
5. **extensibility**:  combine OPTIMUS commands with Excel formulas and macros for more complex actions. Or extend OPTIMUS commands with user defined libraries.  
The automation language used by OPTIMUS is really **easy for beginners** to learn to develop your own flows.  But at the same time, it is rich enough to support sophisticated automation flows.  And has various modular constructs to support reuse and scalability for larger automation projects.  

## Usage
- Use `runRPA.bat` to launch RPA program.  Requires to specify an Excel script file.
- Example with Excel script file sample.xlsm :   >> `runRPA -f sample`  
- Sample script files "sample" available to test various RPA functionality
- All excel script files are to be placed in `\scripts`
    And they can include RPA images (for Visual automation of your desktop and websites)

- To launch the Prefect workflow engine, run startOrion.bat to launch the orion workflow server in background.
  - And open the [Prefect dashboard](http://127.0.0.1:4200) in your browser
  - Refer to the documentation here for more details on [managing automation flows and deployments in the workflow dashboard](./docs/ORCHESTRATION.md).

## Documentation
### OPTIMUS Studio
OPTIMUS Studio is a GUI front end for operation of OPTIMUS RPA.  
![Optimus RPA GUI](https://github.com/user-attachments/assets/8d6571ea-bee5-4a8b-8857-da885df14948)  
Some of the cool features include:  
1. Run automation scripts - with support for interactive and record mode, that allows recording of automation steps.  
2. Recording - video of automation run.
3. Notifications - via Telegram.
4. Remote services - launch automation flows on your robot remotely via Telegram.
5. Quick Patch - to update OPTIMUS with latest functionality and release.  
Refer here for details on use of OPTIMUS Studio.  


## Configuration  
Instructions on configuring the software for first-time use.  




# Quick Usage Guide
Assumes that your computer has already been installed and setup with Optimus.
Follow the usage guide below on how to use Optimus RPA.

## Navigating Optimus Program

### Optimus Program Folder
Optimus is installed by default to your root directory e.g. `D:\Optimus`  
`runRPA.bat` is used to launch the RPA program.
![Optimus folder](https://github.com/ray-oh/Optimus/assets/115925194/04de44d5-d496-4e1c-b2a7-21ea4968ba6d)

### Useful shortcuts
As a best practice, you can place shortcuts to frequently used Optimus programs on the desktop for easy access.  Here are some of the useful shortcuts for Optimus:
- open `Optimus folder`
- launch `Jupyter notebook`
- launch `Prefect Orion dashboard` - which is used for monitor and manage your automation flows
- `Quit VM` - to quit your current virtual machine session without logging off the computer. This is necessary if you are running Optimus on an "always on" computer.
  If the computer is logged off, Optimus will not be able to launch the automations properly especially if the automation flow requires visual automation.

![Desktop shortcuts](https://github.com/ray-oh/Optimus/assets/115925194/526682f0-7dd9-43b9-8845-a12c19f48222)

### Scripts Folder
Optimus automation scripts are created in Excel and do not require any programming skills.  
These scripts are stored in the `scripts` folder.  
A `test-sample` script is available in the `scripts` folder for you to learn how to write Optimus automation scripts.

![Scripts folder](https://github.com/ray-oh/Optimus/assets/115925194/23cf3b34-307b-453c-b6b5-521934a973d7)

### How to run a RPA script
You can run the "test-sample" script as follows:  
`runRPA -f test-sample`  
![Running a script](https://github.com/ray-oh/Optimus/assets/115925194/8239b111-d2e8-4c23-b517-288f329a8fe5)

For help on how to use runRPA utility: `runRPA -help` or `runRPA -h`
![runRPA help](https://github.com/ray-oh/Optimus/assets/115925194/b381cde0-4ec8-491e-b809-c7faf63bc127)

### Outputs from the execution of RPA script
Each step of the script that is executed is displayed in the output for reference.  
![Standard script run log](https://github.com/user-attachments/assets/43c06c81-c6e5-490b-a7bd-38e97dbf9538)  

Additional DEBUG details in the output can be shown by activating `D:\Optimus\autobot\setLogLevelDEBUG.bat`
![Script run log with DEBUG info](https://github.com/ray-oh/Optimus/assets/115925194/1d046b31-6719-4b99-a0da-d9cec6ed68ef)

### Monitoring automation flows
All executed flows can be monitored in the `Prefect Orion Dashboard`
![Workflow dashboard](https://github.com/ray-oh/Optimus/assets/115925194/446396b7-05d9-4cdb-bdd0-4bac404e7c59)

Details of the execution logs of each flow can be drilled down from the dashboard.
![Flow run details](https://github.com/ray-oh/Optimus/assets/115925194/96a7029d-f0c4-4206-a3a8-e462607d1e93)

### Working with Jupyter Notebook
Juypter notebook can be launched from the shortcut.
An example of how the jupyter notebook can be executed from the automation script is shown below:
`runJupyterNb:DataPreparationv3.ipynb, {"forceRun":"True","strSearch":"<strSearch>", "runDownload":"FALSE", "runJupyter":"FALSE", "generatedDateTime":"19/10/2023 14:01:16"}`  
runJupyterNb is the action keyword.  
First parameter is the notebook file name.  
And the next parameter are the parameters to be passed to the notebook in JSON format e.g.  `{key1:value1, key2:value2}`

![image](https://github.com/ray-oh/Optimus/assets/115925194/c27fd5c6-4d5d-4e38-a14a-1f8efafcbbd6)

![Launch Jupyter](https://github.com/ray-oh/Optimus/assets/115925194/723a5a0f-a211-4653-a25b-a94329d427e5)



