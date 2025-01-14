# ABOUT OPTIMUS  
Optimus is an RPA (Robotic Process Automation) solution designed with an **Excel front end** for designing automation flow steps.  
Making it accessible for the typical data analyst who is comfortable using Excel, but not very technical savy.  

Optimus stands out for its user-friendly approach while maintaining robust features and extensibility:  

1. **Ease of Use**: Optimus simplifies the creation of automation flows using Excel and predefined templates.  
2. **TagUI and Microsoft Playwright Integration**: Choice of TagUI or Microsoft Playwright RPA engine.  Known for their rich scripting language and support for web browser automation.  
3. **Prefect Workflow Engine**: Provides powerful orchestration, management, and monitoring of workflows.  
4. **Python-Based**: Developed in Python, allowing access to a wide range of libraries and integration with Jupyter Notebooks.  
5. **Enterprise-Level Security**: Secure by design, running on-premise and managing passwords locally, ensuring no sensitive data is sent to the cloud.  

## Demo of OPTIMUS RPA  
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

## Comparison with other RPA solutions
OPTIMUS differentiates itself from other RPA solutions including market leading commercial packages like UiPath in terms of its ease of use and extensibility. But at the sametime, it does not compromise on features and capabilities.

OPTIMUS RPA borrows many concepts from leading open-source RPA solutions like ***[TagUI](https://github.com/aisingapore/TagUI)*** and ***[Robot Framework](https://github.com/robotframework/robotframework)***:  
1. **Keyword-Driven**: making automation scripts easy to create, readable and maintainable.  Keywords can be reused across different automation cases, enhancing efficiency.  
2. **Extensibility**: supports extensions through libraries written in Python. This allows you to integrate with various tools and technologies.  Apart from Python, Optimus can also run Excel macros and batch scripts.  As Optimus scripts are created using Excel, it is easy to enhance the automation flow with Excel formulas and macros.  
3. **Versatile Syntax**: uses a plain text syntax, which is accessible to both technical and non-technical users. This makes it easier for teams to collaborate on automation.  
4. **Reporting and Logs**: generates detailed reports and logs to help analyze automation results and debug issues effectively.  
5. **Enterprise Level Security**:  solution is installed locally, and user has full control on how his/her data is stored and managed.  

A special call out to Ken Soh who developed TagUI and inspired the creation of OPTIMUS RPA. You can check out this article by Matthew David (Digital Leader at Accenture) [comparing TagUI with other top 5 opensource RPA solutions](https://techbeacon.com/enterprise-it/top-5-open-source-rpa-frameworks-how-choose).  

The current version of OPTIMUS has been enhanced to use ***[Microsoft Playwright](https://playwright.dev/)*** as the web browser automation engine. Microsoft Playwright is a leading open-source framework designed for web browser automation and testing.  It is a modern successor to Selenium, and supports all modern browsers and automation in a number of programming languages.  With features like automatic waiting for elements and mobile web testing, Playwright takes web automation to another level of reliability and efficiency.  

And with the latest generation of OPTIMUS, you also get the full fleged orchestration platform for managing all your automation flows.  ***[PREFECT](https://www.prefect.io/)*** is a second-generation open source orchestration platform that has been developed specifically with dataflow automation in mind.  It provides OPTIMUS with powerful and scalable capabilities for workflow orchestration, management and monitoring.  

And finally, as OPTIMUS is developed in Python - *the language for data analytics* - you have easy access to the rich set of libraries that Python has to offer.
Including support for Jupyter Notebooks for automating data analysis and machine learning projects. You can directly call and run Jupyter Notebook scripts.  And you can easily parameterize the Jupyter Notebook scripts to run under various conditions.  

## Typical automation use cases
-  ***Support data report automation***.  Example of a typical architecture for a data automation project.  
![Typical data use case](https://user-images.githubusercontent.com/115925194/210479085-36019993-4048-47a5-a5ee-9baf6d3bffe9.png)

Other example use cases:
> - ***Generate email reports*** out of a legacy reporting solution.  The legacy system did not support email out of the box and also did not support scheduled download of data. Optimus can be used to automate download of data, processing data and formatting the report before sending as an email to users.
> - ***Automate and extend functionality of legacy Excel macro files***.  These files were originally designed for manual run and had plenty of business logic embedded.  The original business developer for the macro has left, and it was risky and would take time to rewrite the entire solution on another platform.  As volume increased, the Excel would take many hours to run on the users laptop. Optimus was used to automate the refresh of the Excel macro with minimal modification to the original macro apart from exposing some key parameter fields.  Entire automation was deployed to a virtual machine on the cloud.  And results from the macro were further transformed for downstream analysis.
> - ***Extract incident and support request data from serviceNow***.  Optimus was used to combine the different datasets into a harmonized data set for monitoring both incident and request trends. The transformed dataset is passed to PowerBI for interactive visualization by users.
> - Automate the monitoring of a website for downtime and failure.  Setting thresholds to trigger alert via email or telegram messaging.
> - Periodically checking a competitor website for pricing updates, and extracting the data to Excel for further analysis.

Refer to the DOCUMENTATION section below for further technical information on the solution.  

## Installation
Get the latest release of OPTIMUS from the [installation repository](https://github.com/ray-oh/Optimus-Installation/releases).  
Install from zipped package file
- Requires: `install.bat` and a `optimus_package*.zip` file.
- optimus_package is in continuous release and new releases are versioned in YYYYMMDD format.
It is advisable you use the latest version available which should be in the *installation* folder.  Check the release notes on what is included in the version.
- Each new release can also be installed over a previous release as an upgrade.  
Normally, an upgrade installation will not remove existing user files.  But it may overwrite existing scripts files with same name.
Backup your scripts folder to avoid problems.
- Click here for the latest stable [installation package](./installation).  And run the installation batch file with the package directly in the root directory of the folder where you wish to install OPTIMUS.  We recommend to keep the name of the program folder as Optimus.  

### Technical Requirements
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

### Release Notes

20220710 - Optimus 1.1.
        Stable release.
        Package and installation scripts.
        Separate autobot and prefect installation folders.
        Separate scripts folder.

20221006 - Stable release. New features: Installation scripts and package updates. Scripts (user files) folders separated from Autobot program folder.

20221018 - Updated installation scripts. Added [python-minifier](https://pypi.org/project/python-minifier/) [github](https://dflook.github.io/python-minifier/installation.html).

#### Installation issues
- [SQLite ‘no such table: json_each’](https://github.com/PrefectHQ/prefect/issues/5970) - potential issue with python / SQLite version.  Ensure python version 3.9 or 3.10 is used.  

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

### Library of Automation Commands
| Library | Description | Command Keywords |
|----------|----------|----------|
| Studio | GUI for OPTIMUS | Launch and Manage Optimus actions |
| BuiltIn | Standard library with command commands | rem, print, if, exit, exitError, raiseError, checkVariable, set|
| Browser_playwright | Microsoft Playwright | click, rclick, hover, present, exist, closeRPA, url, initializeRPA, wait for url, wait |
| Browser_tagui | TagUI support | click, rclick, hover, present, exist, closeRPA, url, title, select, snap, telegram, download, upload |
| Python | Run Python scripts | runJupyterNb |
| Flows | Flow processing logic | iterate, arguments, runModule, codeList |
| Email_Exchange | Email processing | email, waitEmailComplete, refreshMail |
| LibraryTemplate | Template for user defined libraries |  |
| DataFrame | DataFrame manipulation | dropNRowsExcel, DFpromoteHeader, DFsaveToExcel, DFreadExcel, DFsort, DFdropDuplicates, DFconcatenate, DFcreate |
| Excel | Excel processing | mergeFiles, refreshExcel |
| FileSystem | File system actions | copyFile, waitFile, moveFile, makeDir, removeFile, renameRecentDownload, touchFile |
| Formulas | Custom formulas called by RPA {{@formula(arg)}} | fileModifiedDate, fileIsRecent, fileExist |
| Github | Github functions | github_repo_folder_content_files, checkOptimusReleases |
| Image | Image processing | cropImages, resize, start_recording, pause_recording, resume_recording, stop_recording |
| PDF | PDF processing | createPDF, addContentPDF |
| Prefect | Prefect orchestration functions | list_flow_runs_with_state, return_flow_from_run_id, delete_flow_runs, query_flow_runs |
| Table | Template for user defined libraries |  |
| Vault | Password management | get_password |
| Windows | Manage external programs, windows desktop | runExcelMacro, runPowerShellScript, runBatchScript, triggerRPAScript, openProgram, keyboard_pwa, focusWindow, runOptimus, killOptimus |

OPTIMUS is based on TagUI for RPA automation.  Almost all of TagUI's features are ported and available in Optimus.  And some have also been enhanced.
- As many of OPTIMUS core RPA functionality is based on TagUI, a good reference on the core RPA functionality is available from the TagUI official sites, in particular:
  - [Official TagUI site](https://aisingapore.org/tagui/) and [the python version of TagUI](https://github.com/tebelorg/RPA-Python)
  - The list of keywords and commands currently supported by OPTIMUS Excel script can be [referenced from here](./docs/scriptKeywords.xlsx).
  > TagUI by design does not deploy or save any user data on the cloud.  Passwords or credentials are not saved in the scripts, but cached in the browser or secret files on the user's local computer.  

## References to other libraries used by OPTIMUS:
OPTIMUS natively leverages many other python packages for additional features, including:  
| Library | Description | Notes |
|----------|----------|----------|
| [Jupyter](https://pypi.org/project/jupyter/) | Native support for Jupyter Notebooks | <ul><li>[Installing Jupyter Notebook](https://docs.jupyter.org/en/latest/install/notebook-classic.html)</li><li>[Setup Jupyter to use installed virtual env](https://janakiev.com/blog/jupyter-virtual-envs/)</li><li>pip install ipykernel (included in installation libraries)</li><li>python -m ipykernel --name=myenv (Run this command in venv. Replace myenv with any name for kernel in Jupyter.)</li><li>jupyter kernelspec uninstall myenv (to remove the virtual env)</li></ul> |
| [Papermill](https://netflixtechblog.com/scheduling-notebooks-348e6c14cfd6) | Parameterization and automation of Jupyter Notebooks | <ul><li> ... </li></ul> |
| [scrapbook](https://github.com/nteract/scrapbook) | Persist and recall data and visual content in Jupyter notebook | <ul><li>[Building jupyter notebook workflows with scrapbook](https://www.wrighters.io/building-jupyter-notebook-workflows-with-scrapbook/)</li></ul> |
| [Prefect](https://www.prefect.io/opensource/) | Orchestration workflow engine | <ul><li>Prefect is chosen over other orhestration tools as the workflow engine.  [Comparison of Prefect vs Airbnb's Airflow and Spotify's Luigi](https://medium.datadriveninvestor.com/the-best-automation-workflow-management-tool-airbnb-airflow-vs-spotify-luigi-5f4c9832e9fd)</li></ul> |
| [PyPDF4](https://pypi.org/project/PyPDF4/) | for PDF merging, splitting, cropping, encryption | <ul><li> ... </li></ul> |
| [Pandas](https://pypi.org/project/pandas/) | for data analysis | <ul><li> ... </li></ul> |
| [Matplotlib](https://pypi.org/project/matplotlib/) | comprehensive library for creating static, animated, and interactive visualizations in Python | <ul><li> ... </li></ul> |
| [Pillow](https://pypi.org/project/Pillow/) | for image processing | <ul><li> ... </li></ul> |
| [dataframe-image](https://pypi.org/project/dataframe-image/) / [Github](https://github.com/dexplo/dataframe_image) | to export dataframe output as image files | <ul><li>[HTML2Image](https://pypi.org/project/html2image/) / [Github](https://github.com/vgalin/html2image) - alternative.  Also relies on [chrome browser application](https://www.bleepingcomputer.com/news/software/chrome-and-firefox-can-take-screenshots-of-sites-from-the-command-line/)</li></ul> |
| [Visualize and save full dataframes as images](https://randomds.com/2021/12/23/visualize-and-save-full-pandas-dataframes-as-images/) | Native support for Jupyter Notebooks | <ul><li> ... </li></ul> |
| [IMGKit](https://pypi.org/project/imgkit/) | Native support for Jupyter Notebooks | <ul><li> ... </li></ul> |
| [xlwings](https://www.xlwings.org/) | for Excel automation | <ul><li> ... </li></ul> |
| Others | it also leverages common windows COM components for Outlook integration, OneDrive Sync Client for OneDrive / Sharepoint / Teams integration | <ul><li> ... </li></ul> |


OPTIMUS natively leverages many other python packages for additional features, including:
- [Jupyter](https://pypi.org/project/jupyter/): Native support for Jupyter Notebooks  
  - [Installing Jupyter Notebook](https://docs.jupyter.org/en/latest/install/notebook-classic.html)  
  - [Setup Jupyter to use installed virtual env](https://janakiev.com/blog/jupyter-virtual-envs/)  
    - pip install ipykernel (included in installation libraries)  
    - python -m ipykernel --name=myenv (Run this command in venv. Replace myenv with any name for kernel in Jupyter.)  
    - jupyter kernelspec uninstall myenv (to remove the virtual env)  
  - [Papermill](https://netflixtechblog.com/scheduling-notebooks-348e6c14cfd6): Parameterization and automation of Jupyter Notebooks  
  - [scrapbook](https://github.com/nteract/scrapbook): Persist and recall data and visual content in Jupyter notebook  
    - [Building jupyter notebook workflows with scrapbook](https://www.wrighters.io/building-jupyter-notebook-workflows-with-scrapbook/)  
- [Prefect](https://www.prefect.io/opensource/): Orchestration workflow engine  
  - Prefect is chosen over other orhestration tools as the workflow engine.  [Comparison of Prefect vs Airbnb's Airflow and Spotify's Luigi](https://medium.datadriveninvestor.com/the-best-automation-workflow-management-tool-airbnb-airflow-vs-spotify-luigi-5f4c9832e9fd)  
- [PyPDF4](https://pypi.org/project/PyPDF4/): for PDF merging, splitting, cropping, encryption  
- [Pandas](https://pypi.org/project/pandas/): for data analysis  
  - [Matplotlib](https://pypi.org/project/matplotlib/): comprehensive library for creating static, animated, and interactive visualizations in Python  
- [Pillow](https://pypi.org/project/Pillow/): for image processing  
- [dataframe-image](https://pypi.org/project/dataframe-image/) / [Github](https://github.com/dexplo/dataframe_image): to export dataframe output as image files  
  - [HTML2Image](https://pypi.org/project/html2image/) / [Github](https://github.com/vgalin/html2image) - alternative.  Also relies on [chrome browser application](https://www.bleepingcomputer.com/news/software/chrome-and-firefox-can-take-screenshots-of-sites-from-the-command-line/)  
  - [Visualize and save full dataframes as images](https://randomds.com/2021/12/23/visualize-and-save-full-pandas-dataframes-as-images/)  
  - [IMGKit](https://pypi.org/project/imgkit/)  
- [xlwings](https://www.xlwings.org/): for Excel automation   
  - it also leverages common windows COM components for Outlook integration, OneDrive Sync Client for OneDrive / Sharepoint / Teams integration.  

There are some on-going enhancements of OPTIMUS that have yet to be fully incorporated into the solution.  Please contact the developer for further details:
- integrate [data exploration tools like mitos, DTale, Lux](https://github.com/ray-oh/Optimus/blob/master/docs/DATA_EXPLORATION.md).  These are tools that simplify working with Pandas by offering a GUI front end.  
- components that allow further [scaling of the solution to handle big data e.g > 10TB without resorting to Spark](https://github.com/ray-oh/Optimus/blob/master/docs/SCALING.md)  

## Cloning Repo, Contribution and License

### Clone git repository

```sh
    $ git clone "https://github.com/ray-oh/Optimus"
```

You can run and edit the content or contribute to them using [Gitpod.io](https://www.gitpod.io/), a free online development environment, with a single click.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](http://gitpod.io/#https://github.com/ray-oh/tutorialGitHub)

### Contributing New Content
	
* Make your pull requests to be **specific** and **focused**. Instead of contributing "several content" all at once contribute them all one by one separately (i.e. one pull request for "VS Code new link", another one for "Jupyter Notebook link" and so on).

* Every new content must have:
	* **Source link** with comments and readable namings
	* **Background** being explained in README.md along with the content
	
If you're adding new **files** they need to be saved in the `/data` folder. The size of the file should not be greater than `30Mb`.

### Contributing

Before removing any bug, or adding new contributions please do the following: **[Check Contribution Guidelines Before Contribution](Contributing.md)** and also please read **[CODE OF CONDUCT](CODE_OF_CONDUCT.md)**.

### License

Licensed under the [BSD 3-Clause License](LICENSE) 

## Contact
Raymond Oh - for reporting of bugs, questions, requests etc
