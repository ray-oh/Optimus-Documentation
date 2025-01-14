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


# Library of reusable function scripts
Resuable Excel script steps can be stored in a private (optimusLib.xlsm) or public (optimusLibPublic.xlsm) shared file that is accessible to all scripts in Optimus.

Loaded in sequence of 'optimus script', 'optimusLib.xlsm', 'optimusLibPublic.xlsm' - if the file exist in script folder.

***optimusLibPublic.xlsm*** - exposed to public and downloadable from github.  User contributed content validated by publisher.  This file is published to Github and not ignored by .gitignore

> Some reusable functions published in optimusLibPublic:
>  - for the functions below - call them using dot notation e.g. shareX.screenrecord.start to start screen recording with shareX
>  - function({json string}) syntax can be used to pass variables to functions e.g. chrome.password.change({"chrome.password.change.duration"="60"})
>      - variables declared in Optimus Excel script with 'variables' Object.
>      - Templated or subtitued in Excel script using syntax `{{variable name}}` or `<variable name>`
>      - Declared in python script using variables dictionary.
>      - Modify or create in Excel script using `set:variable name=value`

> shareX - using shareX utility (separately download and installed, and operated using default hotkeys)
>  - launch, screen record, screenshot 
> win - general window automation
>  - leveraging keyboard shortcuts: [keyboard shortcuts](https://support.microsoft.com/en-us/windows/keyboard-shortcuts-in-windows-dcc61a57-8ff0-cffe-9796-cb9706c75eec)
>  - minimize.all, close, switch, undo, copy, paste, desktop.show.hide, maximize, minimize.alterative, minimize, restore

> chrome - browser automation using keyboard shortcuts
>   - zoom.in, zoom.out, zoom.reset, addressbar, window.new, tab.new, tab.switch.up, tab.switch.down, tab.switch, tab.search, reload
>   - https://support.google.com/chrome/answer/157179

> chrome.password.change({"chrome.password.change.duration"="60"})
>   - used to access chrome password manager of optimus/tagui's chrome browser automation session.  All passwords cached during automation run are stored and managed here.  You can use this to modify or update your passwords - only accessible locally on your optimus hosted computer, and requires your computer account sign in to access.

> whatsapp - web automation
>   - keyboard shortcuts https://www.xda-developers.com/whatsapp-keyboard-shortcuts/
>   - launch (using url), focuslaunch (using pywinauto keyboard)

> teams - microsoft teams web automation
>   - using keyboard shortcuts:
>       - [13 best keyboard shortcuts for teams](https://helpdeskgeek.com/office-tips/the-13-best-keyboard-shortcuts-for-microsoft-teams/)
>       - [keyboard shortcuts for teams](https://support.microsoft.com/en-gb/office/keyboard-shortcuts-for-microsoft-teams-2e8e2a70-e8d8-4a19-949b-4c36dd5292d2#bkmk_global)
>   - launch

> Various logon functions.  Called with example syntax - okta.logon.  Available for:
>   - okta, qlik, servicenow

> Most of the above steps leverage pywinauto.keyboard function:
>   - [pywinauto keyboard reference](https://pywinauto.readthedocs.io/en/latest/code/pywinauto.keyboard.html)
>   - [Get urls of opened tabs in browser with pywinauto](https://stackoverflow.com/questions/72594066/get-urls-of-opened-tabs-in-browser-pywinauto-python)

***optimusLib.xlsm*** - private to installed optimus program.  Shared library of functions accessible by all script runs.  Can also store private library of constants, variables.

# New functions
This is a temporary place for sharing some new functions avaiable in optimus python library
```
keyboard_pwa:key string  - using pywinauto.  Does not require tagui RPA intialization.
keyboard:key string - using tagui RPA.  Needs Intitializing of RPA to work.

focus: application name     - focus and activate application for RPA.  Uses tagui RPA.

```

# Using library functions as normal python function  
To use the function as normal python function - add bypass=True e.g. telegram('id', 'Some text', bypass=True)