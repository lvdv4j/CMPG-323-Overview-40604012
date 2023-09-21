# CMPG-323-Overview-40604012

## Project Description:

Welcome to my CMPG 323 Overview repository! This project is part of the CMPG 323 module and aims to set up a GitHub repository and a GitHub Kanban project to plan and track work effectively throughout the semester. The primary goal is to enhance project management skills using Agile principles and tools like Scrum and Kanban.

## Table of Contents:

- [Repositories for Each Project](#repositories-for-each-project)
- [Project and Repository Integration](#project-and-repository-integration)
- [Branching Strategy](#branching-strategy)
- [Storage of Credentials and Sensitive Information](#storage-of-credentials-and-sensitive-information)
- [.gitignore Usage](#gitignore-usage)
- [References](#references)

## Repositories for Each Project:

A GitHub Repository (Henceforth referred to as a "github repo" or just "repo" for short) will be created for each project. Since there are 5 Projects, 5 repos will be created in total. You can find a map to all the Projects and the links to their repos below*:

1. CMPG-323-Overview-40604012: (You are here)
2. CMPG-323-Project-2-40604012 [repository](https://github.com/lvdv4j/CMPG-323-Project-2-40604012)
3. CMPG-323-Project-3-40604012 [repository](https://github.com/lvdv4j/CMPG-323-Project-3-40604012)
4. CMPG-323-Project-4-40604012 [repository](https://github.com/lvdv4j/CMPG-323-Project-4-40604012)
5. CMPG-323-Project-5-40604012 [repository](https://github.com/lvdv4j/CMPG-323-Project-5-40604012)

***Note that the repos for projects 4 - 5 are currently empty**

## Project and Repository Integration:

![CMPG 323 Repo Diagram drawio](https://github.com/lvdv4j/CMPG-323-Overview-40604012/assets/104925498/58a4d21a-d171-4d1e-86dd-c9ab7ff14520)

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

To prevent storing sensitive information within my project code, and thus being committed to GitHub, I made use of my appsettings.json file and used my gitignore file to prevent it from being published to GitHub. (Please see the section below detailing my use of .gitignore). I attempted using Azure Key Vault, however I was unfortunatly not successful in my implementation and kept getting errors when trying to publish my Web App to Azure. After doing countless training exercises and reading microsoft documentation, I wasn't able to resolve my error, so I opted to use this method instead. 

No sensitive information such as the data stored within the database has been committed to GitHub, and authentification has been set up within my project 2 app to prevent unauthorized users from accessing the information within the database.

## .gitignore Usage:

In this project, I will be using a .gitignore file to exclude certain files and directories from version control. The .gitignore file helps keep the repository clean and prevents unnecessary or sensitive files from being committed. As I am using Visual Studio, C#, .NET Core 6, and ASP.NET, there are several files and directories I want to exclude.

The following is what my .gitignore file contains:

```plaintext
# The following command works for downloading when using Git for Windows:
# curl -LOf http://gist.githubusercontent.com/kmorcinek/2710267/raw/.gitignore
#
# Download this file using PowerShell v3 under Windows with the following comand:
# Invoke-WebRequest https://gist.githubusercontent.com/kmorcinek/2710267/raw/ -OutFile .gitignore
#
# or wget:
# wget --no-check-certificate http://gist.githubusercontent.com/kmorcinek/2710267/raw/.gitignore

# User-specific files
*.suo
*.user
*.sln.docstates

# Build results
[Dd]ebug/
[Rr]elease/
x64/
[Bb]in/
[Oo]bj/
# build folder is nowadays used for build scripts and should not be ignored
#build/

# NuGet Packages
*.nupkg
# The packages folder can be ignored because of Package Restore
**/packages/*
# except build/, which is used as an MSBuild target.
!**/packages/build/
# Uncomment if necessary however generally it will be regenerated when needed
#!**/packages/repositories.config

# MSTest test Results
[Tt]est[Rr]esult*/
[Bb]uild[Ll]og.*

*_i.c
*_p.c
*.ilk
*.meta
*.obj
*.pch
*.pdb
*.pgc
*.pgd
*.rsp
*.sbr
*.tlb
*.tli
*.tlh
*.tmp
*.tmp_proj
*.log
*.vspscc
*.vssscc
.builds
*.pidb
*.scc

# Visual C++ cache files
ipch/
*.aps
*.ncb
*.opensdf
*.sdf
*.cachefile

# Visual Studio profiler
*.psess
*.vsp
*.vspx

# Guidance Automation Toolkit
*.gpState

# ReSharper is a .NET coding add-in
_ReSharper*/
*.[Rr]e[Ss]harper

# TeamCity is a build add-in
_TeamCity*

# DotCover is a Code Coverage Tool
*.dotCover

# NCrunch
*.ncrunch*
.*crunch*.local.xml

# Installshield output folder
[Ee]xpress/

# DocProject is a documentation generator add-in
DocProject/buildhelp/
DocProject/Help/*.HxT
DocProject/Help/*.HxC
DocProject/Help/*.hhc
DocProject/Help/*.hhk
DocProject/Help/*.hhp
DocProject/Help/Html2
DocProject/Help/html

# Click-Once directory
publish/

# Publish Web Output
*.Publish.xml

# Windows Azure Build Output
csx
*.build.csdef

# Windows Store app package directory
AppPackages/

# Others
*.Cache
ClientBin/
[Ss]tyle[Cc]op.*
~$*
*~
*.dbmdl
*.[Pp]ublish.xml
*.pfx
*.publishsettings
modulesbin/
tempbin/

# EPiServer Site file (VPP)
AppData/

# RIA/Silverlight projects
Generated_Code/

# Backup & report files from converting an old project file to a newer
# Visual Studio version. Backup files are not needed, because we have git ;-)
_UpgradeReport_Files/
Backup*/
UpgradeLog*.XML
UpgradeLog*.htm

# vim
*.txt~
*.swp
*.swo

# Temp files when opening LibreOffice on ubuntu
.~lock.*
 
# svn
.svn

# CVS - Source Control
**/CVS/

# Remainings from resolving conflicts in Source Control
*.orig

# SQL Server files
**/App_Data/*.mdf
**/App_Data/*.ldf
**/App_Data/*.sdf


#LightSwitch generated files
GeneratedArtifacts/
_Pvt_Extensions/
ModelManifest.xml

# =========================
# Windows detritus
# =========================

# Windows image file caches
Thumbs.db
ehthumbs.db

# Folder config file
Desktop.ini

# Recycle Bin used on file shares
$RECYCLE.BIN/

# OS generated files #
Icon?

# Mac desktop service store files
.DS_Store

# SASS Compiler cache
.sass-cache

# Visual Studio 2014 CTP
**/*.sln.ide

# Visual Studio temp something
.vs/

# dotnet stuff
project.lock.json

# VS 2015+
*.vc.vc.opendb
*.vc.db

# Rider
.idea/

# Visual Studio Code
.vscode/

# ASP.NET specific files and folders
wwwroot/
appsettings.json
appsettings.Development.json

# Output folder used by Webpack or other FE stuff
**/node_modules/*
**/wwwroot/*

# SpecFlow specific
*.feature.cs
*.feature.xlsx.*
*.Specs_*.html

# UWP Projects
AppPackages/

#####
# End of core ignore list, below put you custom 'per project' settings (patterns or path)
#####
```

## My Burndown Chart

![Burndown_Chart](https://github.com/lvdv4j/CMPG-323-Overview-40604012/assets/104925498/dba5c18f-d5ea-417e-8882-6898ff4cb24c)

*Please note that 'sprint 0" and "sprint 9" are not actual sprints but are included for visualization purposes. Where "sprint 0" specifies the amount of effort remaining at the beginning of the semester (which according to the study guide is 160 hours) and "sprint 9" is the amount of effort remaining at the end of the semester which should be 0. The actual sprints run from 1-8.

## References
### References used for project 2
[References.xlsx](https://github.com/lvdv4j/CMPG-323-Overview-40604012/files/12481513/References.xlsx)

### References used for project 3
[Project3References.xlsx](https://github.com/lvdv4j/CMPG-323-Overview-40604012/files/12679676/Project3References.xlsx)
