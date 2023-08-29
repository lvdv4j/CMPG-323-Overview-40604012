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

***Note that the repos for projects 3 - 5 are currently empty**

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

- Codewrinkles (2023) Stop putting your ASp.Net core secrets at risk - use Azure Key Vault! Available at: https://www.youtube.com/watch?v=I8p8j5MuMAo.
- Publishing to Azure from VS2019 failed due to not seeing AddSwaggerGen. - Microsoft Q&A (no date). Available at: https://learn.microsoft.com/en-us/answers/questions/731287/publishing-to-azure-from-vs2019-failed-due-to-not.
- Be sure that the Startup.cs for your application is calling AddSwaggerGen from within ConfigureServices in order to generate swagger file (no date). Available at: https://stackoverflow.com/questions/74064821/be-sure-that-the-startup-cs-for-your-application-is-calling-addswaggergen-from-w.
- change solution file to a different folder (no date). Available at: https://stackoverflow.com/questions/3377917/change-solution-file-to-a-different-folder.
- Zuckerthoben (2023) Get started with Swashbuckle and ASP.NET Core. Available at: https://learn.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle?view=aspnetcore-6.0&tabs=visual-studio.
- Dotnet (no date) Failed to generate swagger.json with Swashbuckle · Issue #20330 · dotnet/AspNetCore.Docs. Available at: https://github.com/dotnet/AspNetCore.Docs/issues/20330.
- Getting error when publishing webAPI to Azure (no date). Available at: https://stackoverflow.com/questions/65295741/getting-error-when-publishing-webapi-to-azure.
- services.AddSwaggerGen() giving error (no date). Available at: https://stackoverflow.com/questions/43707733/services-addswaggergen-giving-error.
- Codewrinkles (2023a) How To Keep SECRET Strings REALLY SECRET in ASP.NET Core? Available at: https://www.youtube.com/watch?v=5TxnLU-SXVg.
- Rolyon (2023) Assign Azure roles using the Azure portal - Azure RBAC. Available at: https://learn.microsoft.com/en-za/azure/role-based-access-control/role-assignments-portal?WT.mc_id=Portal-Microsoft_Azure_KeyVault.
- Access policies not available (no date). Available at: https://stackoverflow.com/questions/76325987/access-policies-not-available#:~:text=If%20you%20want%20to%20use,Portal%20and%20make%20the%20switch.
- Startup.cs class is missing in .NET 6 (no date). Available at: https://stackoverflow.com/questions/70952271/startup-cs-class-is-missing-in-net-6.
- Zuckerthoben (2023b) Get started with Swashbuckle and ASP.NET Core. Available at: https://learn.microsoft.com/en-us/aspnet/core/tutorials/getting-started-with-swashbuckle?view=aspnetcore-7.0&tabs=visual-studio.
- Profile, V. (2022) ASP.NET Core–Generate your swagger.json at build time. Available at: https://bartwullems.blogspot.com/2022/09/aspnet-coregenerate-your-swaggerjson-at.html.
- Azure publish: Failed to update API in Azure (no date). Available at: https://stackoverflow.com/questions/69090118/azure-publish-failed-to-update-api-in-azure/70080593#70080593.
- ASP.NET Core 6 - how to deal with the missing Startup.cs file - Mobiletonster’s Blog (no date). Available at: https://mobiletonster.com/blog/code/aspnet-core-6-how-to-deal-with-the-missing-startupcs-file.
- Azure KeyVault: Azure.Identity.CredentialUnavailableException: DefaultAzureCredential failed to retrieve a token from the included credentials (no date). Available at: https://stackoverflow.com/questions/62817337/azure-keyvault-azure-identity-credentialunavailableexception-defaultazurecrede.
- DefaultAzureCredential failed to retrieve a token (no date). Available at: https://techcommunity.microsoft.com/t5/iis-support-blog/defaultazurecredential-failed-to-retrieve-a-token/ba-p/3038734.
- Bach, P. (2021) Finding Azure App Service FTP credentials. Available at: https://piotrbach.com/azure-app-service-ftp-credentials/#:~:text=Find%20App%20service.,will%20find%20username%2Fpassword%20inputs.
- Git - remove all history prior to a specific commit (no date). Available at: https://stackoverflow.com/questions/73351673/git-remove-all-history-prior-to-a-specific-commit.
- Gitignore not working (no date). Available at: https://stackoverflow.com/questions/25436312/gitignore-not-working.
- Bricelam (2023) Reverse Engineering - EF Core. Available at: https://learn.microsoft.com/en-za/ef/core/managing-schemas/scaffolding/?tabs=dotnet-core-cli.
- Get ConnectionString from appsettings.json instead of being hardcoded in .NET Core 2.0 App (no date). Available at: https://stackoverflow.com/questions/45796776/get-connectionstring-from-appsettings-json-instead-of-being-hardcoded-in-net-co.
- Garzon, C.R. (2022) “HTTP Request Methods – Get vs Put vs Post Explained with Code Examples,” freeCodeCamp.org [Preprint]. Available at: https://www.freecodecamp.org/news/http-request-methods-explained/.
- Entity Framework 6 (no date). Available at: https://www.entityframeworktutorial.net/entityframework6/introduction.aspx.
- Study Mash (2020) Why to use DTO (Data Transfer Objects). Available at: https://www.youtube.com/watch?v=BxWS2E90WHw.
