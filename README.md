# 1. Table of content
- [1. Table of content](#1-table-of-content)
- [2. What is this template](#2-what-is-this-template)
- [3. Features](#3-features)
- [4. How to use it](#4-how-to-use-it)
- [5. Support / Feedback](#5-support--feedback)

# 2. What is this template
This is a Loupedeck .NET Template and I've created this so it is easier and more productive for me, to create Loupedeck Windows Plugins and release them to my users.

# 3. Features
- On release-build, creates automatically a installer (lplug4 file) for the plugin
- Has support for git
- Uses commitizen and github workflow to automatically bump version, generates changelog and tags it
- Uses conventionalcommits to better organize commit history and is helping changelog generation
- Includes github repository workflow (to enable, go into .github/workflows and rename to release.yml)
- Includes github repository issue templates
- Includes giant/useful `.gitignore` file
- Includes run/debug options (for rider). **Please double check the execution path!**

# 4. How to use it
1. Install the template (``dotnet new -i XeroxDev.Loupedeck.Template``)
2. Create a project from template (``dotnet new loupedeck-template -n PROJECT_NAME``)
   - **If you create a project with an IDE, please check "Put solution and project in the same folder" or similar option.** 
   - Available options:
     - `--AddSln` Add a solution file to the project.
     - `--CreateInRoot` Create the project in the root folder
3. If not worked automatically, restore nuget packages with ``nuget restore``
4. If you installed your loupedeck to a different location, change it in your .csproj file (``<LoupedeckInstallation>...</LoupedeckInstallation>``)
5. Change plugin information in the metadata files (``/LoupedeckPackage.yaml``, ``/package.json``, ``/ProjectNamePlugin/PluginConfiguration.json``, ``/ProjectNamePlugin/Properties/AssemblyInfo.cs`` and so on)
6. Start coding your plugin
7. Debug code with ``Debug|AnyCPU`` profile
8. To create installer, choose the ``Release|AnyCPU`` profile and build project
9. Release your ``.lplug4``

# 5. Support / Feedback
Feel free to join our discord [here](https://s.tswi.me/discord)!
