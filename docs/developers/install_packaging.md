`VM93 currently used for packaging`
# Creating installation package for Optimus-Installation repo
## New code to be updated into Optimus Enterprise Github
- update __version__.py file e.g. 2.1.6 and description of updates
- commit and sync changes directly to master branch of Optimus Enterprise Github  
    Commit msg: 2.1.6 and short description  
  ![image](https://github.com/user-attachments/assets/864ad6c5-d238-4be0-9a96-a6bb120546c0)

## Create packages using installation\packaging_tool scripts
- Option 1 : manually using command line and batch scripts   
![image](https://github.com/user-attachments/assets/ad172cdb-a81b-4834-bc1a-a53db7894b98)
![image](https://github.com/user-attachments/assets/e4428a0a-f41e-4df7-a684-f7e917b0db07)  
![image](https://github.com/user-attachments/assets/2f34d0fa-8b66-4732-aa03-451228a8150d)
  - use minify scripts to secure code
    - full minified package with template folder structures for new install
      - D:\OptimusEnterprise\OptimusEnterprise>.\installation\package_tools\optimus_package_mini.bat
    - minified upgrade package
      - D:\OptimusEnterprise\OptimusEnterprise>.\installation\package_tools\optimus_package_mini_upgrade.bat
- Option 2 : from launcher
  - Package code:  
Launch OPTIMUS RPA program in program directory.  And select PACKAGE option.  Run.
![image](https://github.com/user-attachments/assets/7cfc40b7-7555-4c02-8874-d16bf02a5df5)  
Generates optimus_package and optimus_package_upgrade (smaller version).  Both minified.  
Move files to Optimus-Installation/installation/packages - overwriting previous package.  
Sync the files to Github.  Commit msg like before: 2.1.6 and short description  

## Create a release in the Optimus-Installation repo
Add new release to Optimus-Installation:  
Draft a new release  
Create new tag e.g. 2.1.6  
Copy paste from _version_ annotation and preview  
Add packages.  And also include install.bat from Optimus-installation repo.  

![image](https://github.com/user-attachments/assets/6307b963-a2f5-4441-ae5f-d22d6b404a01)

## Upload the latest package files into the repo
Update `optimus_package.zip` and `optimus_package_upgrade.zip`  
![image](https://github.com/user-attachments/assets/ce31eb18-f5ed-4326-ad90-65784ed2fa46)  
Update also `install.bat` if its been changed.  
![image](https://github.com/user-attachments/assets/dd74d372-38ac-47e2-ae28-55827ef286bc)  

## TODO: Create a Windows Installer with Inno Setup
Inno Setup or IExpress are tools that can be used to create a windows installer.  
Typically, either tool allows to combine both the `install.bat` and `optimus_package.zip` into a windows installer `setup.exe` file.  
Inno Setup has following added features over IExpress:
- choice of installation directory
- link to and acceptance of license before installation
- link to readme after installation
- additional installation tasks e.g. install python, playwright and other 3rd party tools
- add shortcuts to program startup menu and desktop
- allow download of packages from links
- create uninstaller  
![image](https://github.com/user-attachments/assets/e453cd24-d271-4fad-840d-1e14acda75ce)

> [Inno Setup](https://youtu.be/qKh6gAxrahs?si=ez8nBXKzuu0wEq2j)  
  https://jrsoftware.org/isinfo.php  


