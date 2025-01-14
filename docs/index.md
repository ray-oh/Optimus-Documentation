# About OPTIMUS  
Optimus is an RPA (Robotic Process Automation) solution designed with an **Excel front end** for creation of automation flow steps.  
Making it accessible for the typical data analyst who is comfortable using Excel, but not very technical savy.  

Optimus stands out for its user-friendly approach while maintaining robust features and extensibility:  

1. **Ease of Use**: Optimus simplifies the creation of automation flows using Excel and predefined templates.  
2. **TagUI and Microsoft Playwright Integration**: Choice of TagUI or Microsoft Playwright RPA engine.  Known for their rich scripting language and support for web browser automation.  
3. **Prefect Workflow Engine**: Provides powerful orchestration, management, and monitoring of workflows.  
4. **Python-Based**: Developed in Python, allowing access to a wide range of libraries and integration with Jupyter Notebooks.  
5. **Enterprise-Level Security**: Secure by design, running on-premise and managing passwords locally, ensuring no sensitive data is sent to the cloud.  

## Key Features  
OPTIMUS differentiates itself from other RPA solutions including market leading commercial packages like UiPath in terms of its ease of use and extensibility. But at the sametime, it does not compromise on features and capabilities.  

OPTIMUS RPA borrows many concepts from leading open-source RPA solutions like ***[TagUI](https://github.com/aisingapore/TagUI)*** and ***[Robot Framework](https://github.com/robotframework/robotframework)***:  
1. **Keyword-Driven**: making automation scripts easy to create, readable and maintainable.  Keywords can be reused across different automation cases, enhancing efficiency.  
2. **Extensibility**: supports extensions through libraries written in Python. This allows you to integrate various tools and technologies.  Apart from Python, Optimus can also run Excel macros and batch scripts.  As Optimus scripts are created using Excel, it is easy to enhance the automation flow with Excel formulas and macros.  
3. **Versatile Syntax**: uses a plain text syntax, which is accessible to both technical and non-technical users. This makes it easier for teams to collaborate on automation.  
4. **Reporting and Logs**: generates detailed reports and logs to help analyze automation results and debug issues effectively.  
5. **Enterprise Level Security**:  solution is installed locally, and user has full control on how his/her data is stored and managed.  

A special call out to Ken Soh who developed TagUI and inspired the creation of OPTIMUS RPA. You can check out this article by Matthew David (Digital Leader at Accenture) [comparing TagUI with other top 5 opensource RPA solutions](https://techbeacon.com/enterprise-it/top-5-open-source-rpa-frameworks-how-choose).  

The current version of OPTIMUS has been enhanced to use ***[Microsoft Playwright](https://playwright.dev/)*** as the web browser automation engine. Microsoft Playwright is a leading open-source framework designed for web browser automation and testing.  It is a modern successor to Selenium, and supports all modern browsers and automation in a number of programming languages.  With features like automatic waiting for elements and mobile web testing, Playwright takes web automation to another level of reliability and efficiency.  

And with the latest generation of OPTIMUS, you also get the full fleged orchestration platform for managing all your automation flows.  ***[PREFECT](https://www.prefect.io/)*** is a second-generation open source orchestration platform that has been developed specifically with dataflow automation in mind.  It provides OPTIMUS with powerful and scalable capabilities for workflow orchestration, management and monitoring.  

And finally, as OPTIMUS is developed in Python - *the language for data analytics* - you have easy access to the rich set of libraries that Python has to offer.
Including support for Jupyter Notebooks for automating data analysis and machine learning projects. You can directly call and run Jupyter Notebook scripts.  And you can easily parameterize the Jupyter Notebook scripts to run under various conditions.  

## Audience
Guide for different to documentation for various audience:  
***Data analysts and Business users***  
2. Getting Started  
  - Installation: Step-by-step guide to installing OPTIMUS RPA.  
  - Quick Start Guide: A simple example to get users up and running quickly.  
  - Configuration: Instructions on configuring the software for first-time use.  
3. User Interface  
  - Excel Front End: Detailed explanation of the Excel interface and its components.  
  - Navigation: How to navigate through the different sections of the software.  
4. Creating Automation Flows  
  - Basic Concepts: Introduction to automation flows and key concepts.  
  - Using Templates: How to use and customize Excel templates for automation.  
  - TagUI Integration: Explanation of how to leverage TagUI within OPTIMUS.  
8. Examples and Use Cases  
  - Sample Projects: Detailed examples of automation projects.  
  - Industry Use Cases: How different industries can benefit from using OPTIMUS.  
10. Appendices  
  - Glossary: Definitions of key terms used in the documentation.  
  - References: Additional resources and references for further reading.  

***Automation Engineers and Developers***  
5. Advanced Features  
  - Prefect Workflow Engine: Detailed guide on using the Prefect workflow engine.  
  - Python Integration: How to integrate and use Python scripts within OPTIMUS.  
  - Jupyter Notebooks: Instructions for using Jupyter Notebooks with OPTIMUS.  
6. Security and Data Management  
  - Security Features: Overview of the security features and best practices.  
  - Data Storage: How to manage and store data securely.  
7. Troubleshooting and FAQs  
  - Common Issues: List of common issues and their solutions.  
  - FAQs: Frequently asked questions and answers.  
9. Community and Support  
  - Community Forums: Links to community forums and discussion groups.  
  - Support: How to get help and support from the OPTIMUS team.  

## Prerequisites  
Required knowledge or tools before using OPTIMUS RPA.  
Refer to the DOCUMENTATION section below for further technical information on the solution.  

## INSTALLATION
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
| Library | Description | Commands |
|----------|----------|----------|
| Studio | GUI for OPTIMUS | Row 1, Col 3 |
| BuiltIn | Standard library with command commands | rem, print, if, exit, exitError, raiseError, checkVariable, set|
| Browser_playwright | Microsoft Playwright | click, rclick, hover, present, exist, closeRPA, url, initializeRPA, wait for url, wait |
| Browser_tagui | TagUI support | click, rclick, hover, present, exist, closeRPA, url, title, select, snap, telegram, download, upload |
| Python | Run Python scripts | runJupyterNb |
| Flows | Flow processing logic | iterate, arguments, runModule, codeList |
| Email_Exchange | Email processing | email, waitEmailComplete, refreshMail |
| LibraryTemplate | Template for user defined libraries |  |



DataFrame

Excel
FileSystem
Formulas
Github
Image

PDF
Prefect

Table
Vault
Windows



OPTIMUS is based on TagUI for RPA automation.  Almost all of TagUI's features are ported and available in Optimus.  And some have also been enhanced.
- As many of OPTIMUS core RPA functionality is based on TagUI, a good reference on the core RPA functionality is available from the TagUI official sites, in particular:
  - [Official TagUI site](https://aisingapore.org/tagui/) and [the python version of TagUI](https://github.com/tebelorg/RPA-Python)
  - The list of keywords and commands currently supported by OPTIMUS Excel script can be [referenced from here](./docs/scriptKeywords.xlsx).
  > TagUI by design does not deploy or save any user data on the cloud.  Passwords or credentials are not saved in the scripts, but cached in the browser or secret files on the user's local computer.  

## References to other libraries used by OPTIMUS:
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

## CLONING REPO, CONTRIBUTION AND LICENSE

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
