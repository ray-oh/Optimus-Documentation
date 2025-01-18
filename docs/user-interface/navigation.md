# Navigation

Navigating various functions in OPTIMUS via the launcher.

# OPTIMUS RPA Launcher
GUI for launching OPTIMUS.  And also settings management.  
Simplifies the management of command lines actions for users.  

![Program icon](../assets/images/shortcut-optimus-rpa.PNG)

Some key features:  

1. OPTIMUS CORE

    ![Main screen](../assets/images/gui-core.PNG)  

    - `Run Script`: RUN/EDIT/DEPLOY automation script with debug, log, LIVE/interactive mode and other settings  
        ![Run Script](../assets/images/gui-run-script.png)  

    - `Interactive mode`  
        ![Interactive Mode](../assets/images/gui-run-script-interactive.png)  

    - `OPTIMUS Command Builder`: Helps input of OPTIMUS keyword actions  
        ![Optimus Command Entry Aid](../assets/images/gui-studio-command-builder.png)  

    - Jupyter Notebook

    - `Studio`: Look up keywords and usage  
        ![Studio](../assets/images/gui-studio.png)  

    - Quit VM

    - Close

2. SETTINGS

    ![Settings](../assets/images/gui-settings.PNG)  

    - `Notifications` - set TELEGRAM ID, activate/deactivate notifications

    - `Recording`  - activate/deactivate recording

    - `Logging`
        - `Debug Level` - activate DEBUG logging
        - `Info Level`  - activate INFO level logging

    - Inspect

    - Optimus folder

3. AGENTS

    ![agents](../assets/images/gui-agents.PNG)  

    - `Services`  - setup services for PREFECT orchestrator and agent
        ![services config](../assets/images/gui-services-config.PNG)  

    - `Workflow`  - query and delete automation flow executions  
        ![workflow management](../assets/images/gui-workflow-management.png)  

    - `Task Scheduler`  - opens windows task scheduler to manage specific automation job flows

4. UPGRADE

    ![upgrade](../assets/images/gui-upgrade-menu.PNG)  

    - `Upgrade`   - upgrade current installation to latest version.  Download from github or take existing optimus_package_upgrade.zip in app directory.  
        ![upgrade](../assets/images/gui-upgrade.png)

    - `Help`      - generate help file  

    - `Package`   - create packages for current DEV installation  

    - `Shortcut`  - create key shortcuts to desktop  
        ![image](../assets/images/gui-shortcuts.png)  

    - `Libraries` - launch CMD for virtual environment.  Allow `pip install` of additional libraries.  
        ![image](../assets/images/terminal-install-lib.png)  



## OPTIMUS RPA Studio

Application to help launch and edit scripts.  Also provides features like: recording, debugging, inspect browser locators.  

**Shortcut**:  

![launcher icon](../assets/images/shortcut-optimus-rpa.PNG)  

**Optimus RPA menu**:  

![menu](../assets/images/gui-core.PNG)  
  
Using OPTIMUS RPA studio.  Typical steps:
- Select script
- Edit script
- Debug script
- Log - special beta logging
- Break - if word matches action
- Run script  

![Run Script](../assets/images/gui-run-script.png)  
  
**Debug / Interactive Run mode**:  

![interative](../assets/images/gui-run-script-interactive.png)  

**Record and Save**:  

![record](../assets/images/gui-record-save2.png)  

- Record and Save - to insert and save new actions
- auto save - to automatically save created actions in new "Record" sheet in Excel  
- Other options:
  - Step - to next action
  - Continue - to next action that contains defined step
  - Terminate - run
  - Edit - script
  - Studio - launch help and builder for actions
  - Variables / Resolve - to inspect variable values  
  
**Studio - action builder / help**:  

![studio](../assets/images/gui-studio-command-builder.png)  

### Determining selectors/locators

### Playwright Inspector - Pick locator

Use `pause:` to trigger pause and enable playwright inspector window  

![playwright inspector](../assets/images/gui-playwright-inspector.png)
  
Playwright Inspector and Pick locator:  
- Pick locator displays useful info on selector to use for selected elements in browser  

![select locator](../assets/images/playwright-inspector-select.png)  

![locator results](../assets/images/playwright-inspector-locator-log.png)  

