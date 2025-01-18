# About OPTIMUS  

!logo

![logo](/docs/assets/images/logo.png)

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

2. **Getting Started**  
    - Installation: Step-by-step guide to installing OPTIMUS RPA.  
    - Quick Start Guide: A simple example to get users up and running quickly.  
    - Configuration: Instructions on configuring the software for first-time use.  

3. **User Interface**  
    - Excel Front End: Detailed explanation of the Excel interface and its components.  
    - Navigation: How to navigate through the different sections of the software.  

4. **Creating Automation Flows**  
    - Basic Concepts: Introduction to automation flows and key concepts.  
    - Using Templates: How to use and customize Excel templates for automation.  
    - TagUI Integration: Explanation of how to leverage TagUI within OPTIMUS.  

8. **Examples and Use Cases**  
    - Sample Projects: Detailed examples of automation projects.  
    - Industry Use Cases: How different industries can benefit from using OPTIMUS.  

10. **Appendices**  
    - Glossary: Definitions of key terms used in the documentation.  
    - References: Additional resources and references for further reading.  

***Automation Engineers and Developers***  

5. **Advanced Features**  
    - Prefect Workflow Engine: Detailed guide on using the Prefect workflow engine.  
    - Python Integration: How to integrate and use Python scripts within OPTIMUS.  
    - Jupyter Notebooks: Instructions for using Jupyter Notebooks with OPTIMUS.  

6. **Security and Data Management**  
    - Security Features: Overview of the security features and best practices.  
    - Data Storage: How to manage and store data securely.  

7. **Troubleshooting and FAQs**  
    - Common Issues: List of common issues and their solutions.  
    - FAQs: Frequently asked questions and answers.  

9. **Community and Support**  
    - Community Forums: Links to community forums and discussion groups.  
    - Support: How to get help and support from the OPTIMUS team.  

## Prerequisites  
Required knowledge or tools before using OPTIMUS RPA:  

- Assumes you are comfortable using Excel.  And have Excel installed.  
- OPTIMUS RPA currently works for windows.  It has not been setup to work for Linux or Mac.  Although technically, it is possible to do so.  
There may be some libraries used by OPTIMUS that will break in Linux or Mac. And the installation process is currently developed for windows only.  
- For full operation of OPTIMUS in an enterprise context, you may need One Drive or Google Drive installed to enable transfer of files between your computer and the one running OPTIMUS.  

For more details on the system requirements and the various setup configurations, you can refer to the [installation documentation](basics/install.md).  
