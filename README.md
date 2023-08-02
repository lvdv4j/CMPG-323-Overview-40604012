# CMPG-323-Overview-40604012

## Project Description:

Welcome to my CMPG 323 Overview repository! This project is part of the CMPG 323 module and aims to set up a GitHub repository and a GitHub Kanban project to plan and track work effectively throughout the semester. The primary goal is to enhance project management skills using Agile principles and tools like Scrum and Kanban.

## Table of Contents:

- [Repositories for Each Project](#repositories-for-each-project)
- [Project and Repository Integration](#project-and-repository-integration)
- [Branching Strategy](#branching-strategy)
- [Storage of Credentials and Sensitive Information](#storage-of-credentials-and-sensitive-information)
- [.gitignore Usage](#gitignore-usage)

## Repositories for Each Project:

A GitHub Repository (Henceforth referred to as a "github repo" or just "repo" for short) will be created for each project. Since there are 5 Projects, 5 repos will be created in total. You can find a map to all the Projects and the links to their repos below*:

1. CMPG-323-Overview-40604012: (You are here)
2. CMPG-323-Project-2-40604012 [repository](https://github.com/lvdv4j/CMPG-323-Project-2-40604012)
3. CMPG-323-Project-3-40604012 [repository](https://github.com/lvdv4j/CMPG-323-Project-3-40604012)
4. CMPG-323-Project-4-40604012 [repository](https://github.com/lvdv4j/CMPG-323-Project-4-40604012)
5. CMPG-323-Project-5-40604012 [repository](https://github.com/lvdv4j/CMPG-323-Project-5-40604012)

***Note that the repos for projects 2 - 5 are currently empty**

## Project and Repository Integration:

(Add content explaining how the project and repository are integrated)

## Branching Strategy:

I am planning on making use of the following branching stategy for my projects:

1. **Main (Master) Branch:** This will be the primary branch for my repos and will respresent the stable, production-ready state of the code relevant to the project. Only tested and fully functional code will be merged with this branch. I will avoid directly commiting to this branch and instead make changes on other branches and merge these changes with the main branch through pull requests.
2. **Development Branch:** This is where most of my work or changes will be done. I will use this branch to add new features, do bug fixes and and perform any other ongoing development.
3. **Feature Branch:** I plan to also make use of a feature branch, this will allow me to isolate significant changes or additions that may require multiple commits, making it easier to track changes and revert to previous commits if any mistakes are made.

My Branching stratergy can be demonstated as below:

```plaintext
             Main
              |
         Development
          /        \
   Feature 1     Feature 2 ...
```



## Storage of Credentials and Sensitive Information:

Credentials and sensitive information should not be accessible to other users and thus will not be stored on GitHub. Sensitive information might have to be encrypted to be further protected.*

According to Project 3 - we will be using an Azure App Service to host our web application, this means that credentials and sensitive information can be handled in the following ways:

1. Configuration with Azure App Configuration: Azure App Configuration allows for the storage of configuartion settings, including sensitive information like connection strings and API keys, in a centralized and secure manner. Thus I can make use of this to store the connection string for me hosted database mentioned in the appsettings.json file.
2. Environment Variables on Azure App Service: This allows for the configuartion of environment variables for the application, thus instead of hardcoding sensitive information in the appsettings.json file, I could possibly set environment variables on the Azure App Service that will be read by the application at runtime.
3. Azure Key Vault Integration: This can be integrated with the Azure App Service to securely store and manage secrets, keys, and certificates and the application can retrieve them securely at runtime.
4. User Secrets: This is a feature in ASP.NET Core to store sensitive information locally on the development machine. User secrets are not commited to version control and thus are kept out of my GitHub repos during development.

***This is still to be decided**

## .gitignore Usage:

In this project, I will be using a .gitignore file to exclude certain files and directories from version control. The .gitignore file helps keep the repository clean and prevents unnecessary or sensitive files from being committed. As I am using Visual Studio, C#, .NET Core 6, and ASP.NET, there are several files and directories I want to exclude.

The following is an **example** of what my .gitignore file might look like:

```plaintext
# .NET Core and Visual Studio specific files
*.obj
*.exe
*.dll
*.pdb
*.user
*.bak
*.cache
*.vs/
*.vscode/

# Build output
/bin/
/obj/
/Debug/
/Release/

# NuGet packages
*.nuget/
packages/

# User-specific files and settings
*.suo
*.user
*.sln.docstates
*.userprefs

# ASP.NET specific files and folders
wwwroot/
appsettings.json
appsettings.Development.json

# Secret and sensitive information
secrets.json

