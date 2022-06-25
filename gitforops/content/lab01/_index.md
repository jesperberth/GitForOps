---
title: "Lab 1 Install Software"
---

In this lab we will install git, Windows terminal and Visual Studio Code on your local computer

## Table of Contents

- [Task 1 Install Git](#task-1-install-git)
- [Task 2 Install Visual Studio Code](#task-2-install-visual-studio-code)
- [Task 3 Install Windows Terminal](#task-3-windows-terminal)

## Installation

Today we can use several methods to install software on a windows workstation, you can choose the method you prefer.

Winget and chocolatey has a package update function so its easy to maintain the installed software, if you install through Microsoft Store the installed software will be updated automaticly

### Winget

[winget - package manager](https://docs.microsoft.com/en-us/windows/package-manager/)

Winget is Microsofts newest package management system with a simple command line interface, winget is opensource and can be found on github - winget is available for Windows 10 and Windows 11

### Chocolatey

[chocolatey.org](https://chocolatey.org/install)

Chocolatey is a powershell based package management system, with an enterprise option that allows for private repositories

## Task 1 Install Git

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency

[git-scm.com](https://git-scm.com/download/win)

Start powershell with elevated credentials (Run As Administrator)

### Using winget to install git

```cmd

winget install git.git

```

### Using Chocolatey to install git

[chocolatey.org](https://chocolatey.org/)

```cmd

choco install git

```

## Task 2 Visual Studio Code

Open Source Code Editor with many extentions

[code.visualstudio.com](https://code.visualstudio.com/download)

Start powershell with elevated credentials (Run As Administrator)

### Using winget to install VSCode

```cmd

winget install Microsoft.VisualStudioCode

```

### Using Chocolatey to install VSCode

[chocolatey.org](https://chocolatey.org/)

```cmd

choco install vscode

```

### Using Microsoft Store to install VSCode

Search for __Visual Studio Code__ click install

## Task 3 Windows Terminal

[github.com/microsoft/terminal](https://github.com/microsoft/terminal)

Start powershell with elevated credentials (Run As Administrator)

### Using winget to install Windows Terminal

```cmd

winget install Microsoft.WindowsTerminal

```

### Using Chocolatey to install Windows Terminal

[chocolatey.org](https://chocolatey.org/)

```cmd

choco install microsoft-windows-terminal

```

### Using Microsoft Store to install Windows Terminal

Search for __Windows Terminal__ click install
