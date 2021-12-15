# 1. Table of content
- [1. Table of content](#1-table-of-content)
- [2. What is this template](#2-what-is-this-template)
- [3. Features](#3-features)
- [4. How to use it](#4-how-to-use-it)
- [5. Support / Feedback](#5-support--feedback)

# 2. What is this template
This is a Loupedeck .NET Template and I've created this so it is easier and more productive for me, to create Loupedeck Plugins and release them to my users.

# 3. Features
- On release-build, creates automatically a installer (lplug4 file) for the plugin
- Has support for git
- Uses standard-version to automatically bump version, generates changelog and tags it
- Uses conventionalcommits to better organize commit history and is helping changelog generation
- Uses husky to ensure commits are correctly

# 4. How to use it
1. Clone this repository
2. Install it to your dotnet templates (``dotnet new -i ./path/to/template``)
3. Create a project from template (``dotnet new loupedeck-template -n PROJECT_NAME``)
4. If not worked automatically, restore nuget packages with ``nuget restore``
5. Install (p)npm packages. Prefered pnpm, but also works with vanilla npm (``pnpm install``)
6. If you installed your loupedeck to a different location, change it in your .csproj file (``<LoupedeckInstallation>...</LoupedeckInstallation>``)
7. Change plugin information in the metadata files (``/LoupedeckPackage.yaml``, ``/package.json``, ``/ProjectNamePlugin/PluginConfiguration.json``, ``/ProjectNamePlugin/Properties/AssemblyInfo.cs`` and so on)
8. Start coding your plugin
9. Debug code with ``Debug|AnyCPU`` profile
10. To create installer, choose the ``Release|AnyCPU`` profile and build project
11. Release your ``.lplug4``


# 5. Support / Feedback
Feel free to join our discord [here](https://s.tswi.me/discord)!
