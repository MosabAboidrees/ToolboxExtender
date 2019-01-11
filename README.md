# Toolbox Extender

Improve your custom toolbox (app) and develop process with powerful features:

- Easily install/uninstall toolbox and check current version ([Extender](./README.md/#extender-class))
- Access to toolbox documentation and examples ([Extender](./README.md/#extender-class))
- Automatic toolbox building and deployment to GitHub ([Dev](./README.md/#dev-class))
- Ability of installed toolbox to automatically update itself to the latest version from GitHub ([Updater](./README.md/#updater-class))
- Toolbox ability to store any data within itself, i.e. settings ([Storage](./README.md/#storage-class))

File Exchange entry: [Toolbox Extender](https://www.mathworks.com/matlabcentral/fileexchange/69126)

## Requirements

- **MATLAB R2018b**
- Installed **Git** for **Dev** functionality
- Public toolbox project on GitHub for **Updater** functionality

## Extender Class

Contains core functions. Required for other classes and functionality.

Can be useful itself:

- open toolbox documentation or examples
- get current toolbox version
- uninstall toolbox

See [ToolboxExtender (class) documentation](https://htmlpreview.github.io/?https://raw.githubusercontent.com/ETMC-Exponenta/ToolboxExtender/master/doc/ToolboxExtender.html)

## Dev Class

Helps you to build toolbox and deploy it to GitHub:

- update toolbox version and build .mltbx
- commit and push project to GitHub
- create tag with version number and push it to GitHub
- create release page and upload .mltbx binary

See [ToolboxDev (class) documentation](https://htmlpreview.github.io/?https://raw.githubusercontent.com/ETMC-Exponenta/ToolboxExtender/master/doc/ToolboxDev.html)

## Updater Class

Updater class will add to your custom evergreen toolbox:

- feature to check the latest version on GitHub
- ability to automatically download and install the latest version

See [ToolboxUpdater (class) documentation](https://htmlpreview.github.io/?https://raw.githubusercontent.com/ETMC-Exponenta/ToolboxExtender/master/doc/ToolboxUpdater.html)

## Storage Class

Helps you easily store any data within installed toolbox, i.e. user settings

- store all toolbox data in one .mat file in convenient Add-ons folder
- load any data you need by name
- clear storage if you don't need it

See [ToolboxStorage (class) documentation](https://htmlpreview.github.io/?https://raw.githubusercontent.com/ETMC-Exponenta/ToolboxExtender/master/doc/ToolboxStorage.html)

## Examples of Toolbox Extender usage

- MATLAB WEB API
- MATLAB Course for Educators
- (send us your examples)

## Installation

Download and run [ToolboxExtender.mltbx](https://github.com/ETMC-Exponenta/ToolboxExtender/raw/master/ToolboxExtender.mltbx)

## Toolbox Extender App

You can use **Toolbox Extender App** to work with the main Toolbox Extender functionality.

The app can be found in APPS section of main MATLAB Window or

```ToolboxExtenderApp```

## How to open documentation

Use [Toolbox Extender App](./README.md/#toolbox-extender-app) or

```ToolboxExtender.help```

## How to use

1. In toolbox project directory create toolbox project file (.prj)

2. Upload your project to GitHub (optionally)

3. Use [Toolbox Extender App](./README.md/#toolbox-extender-app) to initialize required classes or run command

```ToolboxExtender.add([classname])```

This will initialize in the curent toolbox project folder a copy of the ToolboxExtender class and classname (optional):

- 'all' - ToolboxExtender, ToolboxDev, ToolboxStorage, ToolboxUpdater classes
- 'extender' or without argument - only ToolboxExtender class
- 'dev' - ToolboxExtender, ToolboxDev classes
- 'storage' - ToolboxExtender, ToolboxStorage classes
- 'updater' - ToolboxExtender, ToolboxUpdater classes

Initialized classes will have names depended on the project name, i.e.: *ProjectNameExtender*, *ProjectNameDev*, etc.

4. Also files will be generated in project directory: **ToolboxConfig.xml** with project and Extender info, **dev_on.m** script to activate developer tools (optionally). **Do not delete ToolboxConfig.xml**!

5. Manually add *...Dev.m* class and *dev_on.m* script to excluded files of your project

## How to update installed Toolbox Extender

Use **Toolbox Extender App** or...

Check installed and latest version

```ToolboxExtender.ver```

Update to the latest version if available

```ToolboxExtender.update```

***
by Pavel Roslovets, ETMC Exponenta
