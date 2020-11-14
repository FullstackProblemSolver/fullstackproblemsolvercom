---
title: "Fullstack Setup On A Windows Machine"
date: 2019-11-18T23:53:00+01:00
draft: false
hideLastModified: false
summary: "A list and setup instruction for common fullstack tools and installs for Windows based machines"
summaryImage: "images/WindowToolkitBadge.png"
tags: ["Windows", "Toolkit"]
pinned: true
weight: 5
series: "notfeatured"
---

November 2020

# ***Background***

Each of the three most common operating system flavors macOs, Windows, and Linux will install technologies differently. While macOs and Linux share some common methods, Windows, in general, will have it own flavor. This post includes common fullstack tools with brief overviews and the steps for install on Windows machines (and only Windows machines). Unless otherwise noted, the installs are lightweight. Lightweight means they should take up little storage space and in general be self contained. If you are using these tools to support other tutorials (such as online portofio build), you can install in order.

#### Prerequisites

-A Windows Machine (with admin privileges )


##### <span style="color:red">Disclaimer:<span>

You will be installing software as administrator so things can go wrong. While this is not expected, please have backups of your life and your machine before going crazy here. Sometimes things with software/hardware can and will go wrong.





{{< box >}}
# ***Tool #1: Chocolatey For Package Management***


{{<rawhtml>}}
<div class="columns">
<div class="column is-4"></div>
    <div class="column is-4">
       <img src="./images/chocolately.svg" alt="Chocolatey Icon" style="width:80%">
<div class="column is-4"></div>
</div>
</div>
{{</ rawhtml>}}




Chocolatey is a package manager for Windows. The goal of Chocolatey, and other package managers, is to allow users to download other software (aka packages) using a command line (aka terminal). Lots of people are used to installing software from (GUI) Graphical User Interface ie. downloading software from a website as an exe and using Window's install wizards to install the software. Chocolatey and other package manager complete install using commands in a command line interface. In the following instructions we are assuming that as a Windows user you will be using PowerShell as your command line interface. For fullstack development there will be a lot of efficiencies in using command line for installation. If this is unfamiliar to you just remember that practice makes perfect. 

## Installation


Go to https://chocolatey.org/install and follow the install instructions. They are shown here for completeness, but may vary
<div class="columns">
<div class="column is-2"> </div>
    <div class="column is-8 has-text-centered">
       {{< youtube id="n1KYu8pQWp8" >}}
{{<rawhtml>}}
<div class="column is-2"> </div>
</div>
</div>
{{</ rawhtml>}}
## Detailed Instructions (That Worked For Us)


**Step 1.** Open PowerShell from Windows Menu but make sure to right click and "Run As Administrator"

**Step 2.** Query Execution polity in PowerShell by entering:

{{< code language="term" >}}
Get-ExecutionPolicy 
{{< /code >}}


This will likely come back as Restricted. If it comes back as unrestricted, then skip the next step.

**Step 3.** (if required). Bypass restrictions, with the command as documented in the chocately instructions
 
{{< code language="term" >}}
Set-ExecutionPolicy Bypass -Scope Process
{{< /code >}}


**Step 4.** Copy the install script from the Chocolatey website https://chocolatey.org/install (as part of install instructions).

At the time of the writing this was the command (for example) but it is better to copy from website.

{{< code language="term" >}}
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
{{< /code >}}

**Step 5.** Confirming install by typing

{{< code language="term" >}}
choco
{{< /code >}}


If install was successful this command should return something similar to

{{< code language="term" color="green" >}}
Chocolatey v0.10.15
Please run 'choco -?' or 'choco <command> -?' for help menu.
{{< /code >}}

Leave this PowerShell terminal/console up and use it for installing Tool #2 Git and Tool #3 Hugo.

{{< /box >}}


{{< box >}}
## Tool #2:  Install Git:

Git is by far the most popular version control software and will be vital for all projects.

Since we have Chocolatey installed (see tool #1) installing Git is easy. Using PowerShell with admin and bypassed restrictions, install Git. 

Referencing https://chocolatey.org/packages/git


{{< code language="term" >}}
choco install git
{{< /code >}}

Type "Y" to proceed
{{< /box >}}


{{< box >}}
## Tool #3: Install Hugo:

Hugo is a static website generator, a framework we can use to build websites. There are TONS of website generators out there with different advantages and disadvantages. We some other tutorials using Hugo so we are installing it here.

Since we have Chocolatey installed (see tool #1) installing Hugo is easy. Using PowerShell with admin and bypassed restrictions, install Hugo: 

https://gohugo.io/getting-started/installing/


{{< code language="term" >}}
choco install hugo-extended -confirm
{{< /code >}}

Type "Y" to proceed
 Note, installing Hugo extended. We are covered if this is needed.
{{< /box >}}
 







{{< box >}}
## Tool #4: Install Text Editor = Visual Studio Code

We will need a robust text editor. There are lots out there Sublime, Atom, Visual Studio Code.

We recommend Visual Studio Code.

It's free and here:
https://code.visualstudio.com/download

Since you may be using Visual Studio Code to write some content, it is worth install an extension for Spell Checking.

Here is how to install an useful extension called "Code Spell Checker".  The video does not show hitting "Install" since it had been previously installed.

<div class="columns">
<div class="column is-2"> </div>
    <div class="column is-8 has-text-centered">
       {{< youtube id="lI3HKuZr78s" >}}
{{<rawhtml>}}
<div class="column is-2"> </div>
</div>
</div>
{{</ rawhtml>}}

{{< /box >}}


