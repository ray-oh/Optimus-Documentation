# Scripts and Syntax
How to create your own Optimus RPA Excel scripts.

Contents  
- Excel Script Structure
- Basic Syntax
  - Action Steps and Libraries
  - User defined constants, variables, tables
  - Formulas
- OPTIMUS RPA Studio
  - Determining selectors/locators
  - Playwright Inspector - Pick locator

## Excel Script Structure
File requires following header fields: Type, Object, Key, Value and Comments.  
- Type:
  - **key**          - key value pair objects
  - **table**        - table object with column headers and values
  - **list**         - object with list of actions/steps
  - **description**  - for documentation of script  

Recommended structure / template:
- description
- User defined constants
- User defined variables
- User defined tables
- "main" block of actions
  - Additional user defined action blocks
  - Special actions:
    - **\[Setup\]** - if \[Setup\] is defined, the steps are run prior to any steps in "main"
    - **\[Teardown\]** - actions that are run after completion of other actions

## Basic Syntax
### Action Steps and Libraries
OPTIMUS provides various pre-built core actions and also extended actions from user defined libraries/modules:
- Core functions required for basic orchestration and processing of actions: core, dates, email, files, etc.
- User defined modules/libraries: 'Browser_playwright', 'Browser_tagui', 'BuiltIn', 'DataFrame', 'Email_Exchange', 'Excel', 'FileSystem', 'Flows', 'Formulas', 'Github', 'Image', 'LibraryTemplate', 'PDF', 'Prefect', 'Python', 'Table', 'Vault', 'Windows'
  
Some useful actions:
- Flows
  - if: conditions , do this , else do that
    - E.g. if: {{Reports:Run}} , checkIfFileExist
    - conditions - use double quotes E.g. "{{report_to_run}}" in "{{Reports:Title}}"
    - conditions to check for empty celles E.g. "{{Reports:cell_value}}"=="nan"
  - codeList: do this action block
  - iterate: table/list , do this action e.g. iterate: Repports , openPages
- Browser_playwright
  - locate: Period , iframe , click  

### User defined constants, variables, tables
How to reference user defined constants, variables or tables:  
  
constants
  - {{constants key/name}}  
  Special system constants
    - {{iterationCount}} - initial value is 0
    - {{yesterdayYYYYMMDD}}
    - {{object:key}}  e.g. {{URL:SAP System}}  
  
table
  - {{table object:key}} e.g. {{Report:URL}}
  - table object = table name, key = column field name    
  
formulas
  - <@filesRecent('{{file_name}}', {{last_x_hr}})>
  - Prefix all formulas with @.  Syntax similar to python function call e.g. function(argument1, argument2)  

Note:
- Empty cells
  - To check if cell is empty: "nan"=="nan"

## OPTIMUS RPA Studio
Application to help launch and edit scripts.  Also provides features like: recording, debugging, inspect browser locators.  
- Shortcut:  
![image](https://github.com/user-attachments/assets/f543b2f4-4608-433a-981a-25421b1d9ff4)  
  
Optimus RPA menu:  
![image](https://github.com/user-attachments/assets/7a07f6fe-7578-4bb5-9be1-0ee015a52a99)
  
Using OPTIMUS RPA studio.  Typical steps:
- Select script
- Edit script
- Debug script
- Log - special beta logging
- Break - if word matches action
- Run script  
  
![image](https://github.com/user-attachments/assets/4e5aafc0-1f29-4735-b9cf-17569953f3c8)
  
Debug / Interactive Run mode:  
![image](https://github.com/user-attachments/assets/e361af82-3b23-420f-a33c-6313e3e5cdf3)  
Record and Save:  
- Record and Save - to insert and save new actions
- auto save - to automatically save created actions in new "Record" sheet in Excel  
![image](https://github.com/user-attachments/assets/1f52ea9d-fecc-4d06-a08a-984fc46228e9)  
- Other options:
  - Step - to next action
  - Continue - to next action that contains defined step
  - Terminate - run
  - Edit - script
  - Studio - launch help and builder for actions
  - Variables / Resolve - to inspect variable values  
  
Studio - action builder / help:  
![image](https://github.com/user-attachments/assets/44263bfa-6930-453c-9e85-ab142426604a)  

### Determining selectors/locators

### Playwright Inspector - Pick locator
Use pause: to trigger pause  
![image](https://github.com/user-attachments/assets/fe98e077-8f88-4165-82c9-1554139df2ed)
  
Playwright Inspector and Pick locator:  
- Pick locator displays useful info on selector to use for selected elements in browser  
![image](https://github.com/user-attachments/assets/f1d067bb-0ad0-466c-a5ce-ac5777940de7)  
![image](https://github.com/user-attachments/assets/24fad317-ff81-44be-8c81-f93beadac4cc)







