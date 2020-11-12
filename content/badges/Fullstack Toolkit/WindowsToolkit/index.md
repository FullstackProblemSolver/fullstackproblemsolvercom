---
title: "Fullstack Setup On A Windows Machine"
date: 2019-11-18T23:53:00+01:00
draft: false
hideLastModified: false
summary: "A list and setup instruction for common fullstack tools and installs for Windows based machines"
summaryImage: "images/0-Live_v3.png"
tags: ["Windows", "Toolkit"]
pinned: true
weight: 5
series: "notfeatured"
---

November 2020

# Background

Each of the three most common operating system flavors macOs, Windows, and Linux will install technologies differently. While macOs and Linux share some common methods, Windows, in general, will have it own flavor. This post includes common fullstack tools with brief overviews and the steps for install on Windows machines (and only Windows machines). 

# Prerequisites

-A Windows Machine (with admin privileges )


##### <span style="color:red">Disclaimer:<span>

You will be installing software as administrator so things can go wrong. While this is not expected, please have backups of your life and your machine before going crazy here. Sometimes things with software/hardware can and will go wrong.


## Tool #1: Chocolatey For Package Management

Chocolatey is a package manager for Windows. The goal of Chocolatey, and other package managers, is to allow users to download other software (aka packages) using a command line (aka terminal). Lots of people are used to installing software from (GUI) Graphical User Interface ie. downloading software from a website as an exe and using Window's install wizards to install the software. Chocolatey and other package manager complete install using commands in a command line interface. In the following instructions we are assuming that as a Windows user you will be using PowerShell as your command line interface. For fullstack development there will be a lot of efficiencies in using command line for installation. If this is unfamiliar to you just remember that practice makes perfect. 

### Abbreviated Instructions

Go to https://chocolatey.org/ and follow the install instructions. They are shown here for completeness, but may vary


### Detailed Instructions (That Worked For Us)

Step 1. Open PowerShell from Windows Menu but make sure to right click and "Run As Administrator"

Step 2. Query Execution polity in PowerShell by entering:

{{< code language="term" >}}
Get-ExecutionPolicy 
{{< /code >}}


```
Get-ExecutionPolicy 
```

3. Following the Chocately instructions - run command 
Get-ExecutionPolicy 

mine returned Restricted so I followed instructions to run

the next command and then hit Yes


Hit enter a few times to make space on console