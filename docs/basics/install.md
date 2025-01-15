# Installation  

Step-by-step guide to installing OPTIMUS RPA.   

## System Requirements  

OPTIMUS has been tested and validated to work under the following environments.

Pre-requisites:  
- **Windows**. Windows 10 or Windows 10 Enterprise Server.  
- **Python**.  Version 3.10.9 (or any version < 3.11 and > 3.9) is the recommended for compatibility with current libraries used by OPTIMUS.  
- **Cloud drive**.  OPTIMUS currently does not have a cloud enabled service option.  But it is possible deploy OPTIMUS on a cloud virtual machine to run the automation in unattended mode.  It is possible to federate an automation task across multiple deployments of OPTIMUS using OneDrive Sync Client or a shared network drive (if running within an enterprise network) to share data, status, and scripts.  Refer to configuration section for details on how to install such a setup.  
- **Other program libraries**.  Will be installed automatically by the installation package, including:
    - **Autobot (RPA component)** - designed to work with TagUI and Microsoft Playwright.  
    - **Microsoft Playwright** or **TagUI** - will be installed automatically by the installation program.  
    - **Prefect (workflow orchestration)** - full fledged orchestration package for dataflow automation.  The on-premise version of Prefect is installed by OPTIMUS.  The current release of OPTIMUS does not provide capability out of the box to support federation of robots across the cloud.  Future releases may make this easier by leveraging the cloud enabled capabilities of Prefect workflow.  
>***Typical cloud deployment architecture***
>![Typical cloud deployment architecture](https://user-images.githubusercontent.com/115925194/210483008-d9d9687f-2602-4ded-bb3d-90d1c8cce8b4.png)

- Python
> Version 3.10.9 (or any version < 3.11 and > 3.9) is the recommended ?version for use with OPTIMUS for compatibility with current libraries.   
>- [Download Python 3.10.9](https://www.python.org/downloads/release/python-3109/)
> For future release, we will keep the library list updated to make it compatible with latest python release or anaconda package.
>- You can [follow this guide](https://docs.jupyter.org/en/latest/install/notebook-classic.html) for installing Jupyter separately from Python.  In future release, Jupyter Notebook will be included in the default installation package.  






# INSTALLATION
Get the latest release of OPTIMUS from the [installation repository](https://github.com/ray-oh/Optimus-Installation/releases).  
Install from zipped package file
- Requires: `install.bat` and a `optimus_package*.zip` file.
- optimus_package is in continuous release and new releases are versioned in YYYYMMDD format.
It is advisable you use the latest version available which should be in the *installation* folder.  Check the release notes on what is included in the version.
- Each new release can also be installed over a previous release as an upgrade.  
Normally, an upgrade installation will not remove existing user files.  But it may overwrite existing scripts files with same name.
Backup your scripts folder to avoid problems.
- Click here for the latest stable [installation package](./installation).  And run the installation batch file with the package directly in the root directory of the folder where you wish to install OPTIMUS.  We recommend to keep the name of the program folder as Optimus.  

### PROGRAM TECHNICAL INFORMATION
Pre-requisites:
- Windows 10 or Windows 10 Enterprise Server.
> OPTIMUS currently does not have a cloud enabled service option.  But it is possible deploy OPTIMUS on a cloud virtual machine to run the automation in unattended mode.
>- It is also possible to federate an automation task across multiple deployments of OPTIMUS using OneDrive Sync Client or a shared network drive (if running within an enterprise network) to share data, status, and scripts.  
>- The current release of OPTIMUS does not provide this capability out of the box and requires some setup to achieve the federation.  Future releases may make this easier by leveraging the cloud enabled capabilities of Prefect workflow.  
>***Typical cloud deployment architecture***
>![Typical cloud deployment architecture](https://user-images.githubusercontent.com/115925194/210483008-d9d9687f-2602-4ded-bb3d-90d1c8cce8b4.png)

- Python
> Version 3.10.9 (or any version < 3.11 and > 3.9) is the recommended ?version for use with OPTIMUS for compatibility with current libraries.   
>- [Download Python 3.10.9](https://www.python.org/downloads/release/python-3109/)
> For future release, we will keep the library list updated to make it compatible with latest python release or anaconda package.
>- You can [follow this guide](https://docs.jupyter.org/en/latest/install/notebook-classic.html) for installing Jupyter separately from Python.  In future release, Jupyter Notebook will be included in the default installation package.  

All other program libraries will be installed automatically by the installation package, including:
- Autobot (RPA component) - based on TagUI and various addon python packages
- Prefect (workflow orchestration) - full fledged orchestration package for dataflow automation.

### RELEASE NOTES:

20220710 - Optimus 1.1.
        Stable release.
        Package and installation scripts.
        Separate autobot and prefect installation folders.
        Separate scripts folder.

20221006 - Stable release. New features: Installation scripts and package updates. Scripts (user files) folders separated from Autobot program folder.

20221018 - Updated installation scripts. Added [python-minifier](https://pypi.org/project/python-minifier/) [github](https://dflook.github.io/python-minifier/installation.html).

#### Installation issues
- [SQLite ‘no such table: json_each’](https://github.com/PrefectHQ/prefect/issues/5970) - potential issue with python / SQLite version.  Ensure python version 3.9 or 3.10 is used.  



# Intallation
2 methods to install and use optimus RPA:
1. Git clone this repo
    - From this Github page (https://github.com/ray-oh/Optimus.git) - click *Code* and *Download ZIP*  
      ![download the zipped package](https://user-images.githubusercontent.com/115925194/212074132-7e504cc0-d24c-4262-b9cf-e5734f7c827e.png)
    - Create a folder for your Optimus program.  And extract the content to the folder  
      ![image](https://user-images.githubusercontent.com/115925194/212080421-f3b20b76-4f13-4dce-9950-6f6946b7d808.png)
    - Multiple copies of Optimus program can be installed one a computer.  Typically, you could have one instance for PRODUCTION and another instance for TESTING / QUALITY ASSURANCE.  For the PRODUCTION instance, it is recommended to use the name `Optimus` for the program directory.  And for testing, you could give a name like `Optimus_QA`.  If you were setting the TEST/QA environment, it should look like the following with the zipped file content extracted:    
      ![image](https://user-images.githubusercontent.com/115925194/212081617-9c9cb96f-8fd2-43c3-8c9a-b2133d78ed02.png)
    - Finally, run the `install.bat` to setup required libraries for TagUI, PREFECT, JUPYTER NOTEBOOK etc.
2. Install from zipped package file
    - Requires: `install.bat` and a `optimus_package*.zip` file.
    - optimus_package is in continuous release and new releases are versioned in YYYYMMDD format.
      It is advisable you use the latest version available which should be in the *installation* folder.  Check the release notes on what is included in the version.
    - Each new release can also be installed over a previous release as an upgrade.  
      Normally, an upgrade installation will not remove existing user files.  But it may overwrite existing scripts files with same name.
      Backup your scripts folder to avoid problems.
    - Click here for the latest stable [installation package](./installation).  And run the installation batch file with the package directly in the root directory of the folder where you wish to install OPTIMUS.  We recommend to keep the name of the program folder as Optimus.  
## Installation issues
- [SQLite ‘no such table: json_each’](https://github.com/PrefectHQ/prefect/issues/5970) - potential issue with python / SQLite version.  Ensure python version 3.9 or 3.10 is used.  
### Installation notes
- On first run of after installation, expect some running time to download and setup TagUI (~200MB) 
![image](https://user-images.githubusercontent.com/115925194/236681790-12e5712a-dd5c-4dd8-a04e-84a008c50013.png)
- When running "send email" command from rpa script, if below error is encountered, its probably because of some security policy that prevents programatic access to outlook. Enable programatic access to resolve the problem.
![image](https://user-images.githubusercontent.com/115925194/236682136-08af34fa-d2c6-45f4-8375-ab745ba83e89.png)
![image](https://user-images.githubusercontent.com/115925194/236682269-55a23610-1e16-4a3c-b37d-b33cbee40656.png)
- To setup a good RPA environment on your workstation or VM, you can add the following shortcuts
  - optimus folder
  - jupyter notebook
  - Prefect dashboard
  - Quit VM
![image](https://user-images.githubusercontent.com/115925194/236682576-00975523-c6a7-4aee-9baa-74b4c96123fa.png)
- Setup key windows task jobs for the optimus
  - optimus agent - activates prefect agent for listening to and processing new RPA jobs
  - optimus orion - activates prefect server
  - run daily reboot - good practice to reboot the RPA workstation on a daily basis
![image](https://user-images.githubusercontent.com/115925194/236682818-a83ec9e5-3eda-49ba-a3bf-197d258dcdcf.png)






