# Using Templates

How to use and customize Excel templates for automation.  

1. Organizing large automation processes across multiple Excel files and worksheets:
    - Worksheets and Files can be used to organize large flows into smaller logical sections to promote reuse.  
    - To call the steps in another worksheet, use `runModule: worksheet name , name of action object`  
    - To call the steps in another file, use `runOptimus: .... `.  This launches a separate RPA flow run.  

