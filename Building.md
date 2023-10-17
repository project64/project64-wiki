Currently, Project64 builds and runs only under Windows platforms.

# Requirements
* Operating System
  * Microsoft Windows 11, 10, 8.1, 8, 7, Vista, XP (and server equivalents).
* Compiler collection
  * Microsoft Visual C++ [2015-2022 (recommended)](https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx), 2013, 2012, 2010, 2008.

# Command line
In a command prompt enter:
```
MSBuild.exe Project64.sln
```
This will build the Debug|Win32 variant, using the Visual Studio 2015 (MSVC 14) compiler tool set.

## Specific builds
Use the following MSBuild properties to set the platform, configuration, and tool set for the build:
* Platform<br/>
  Can be either Win32 or x64
* Configuration<br/>
  Either Debug or Release. It will determine either to use code optimizations or produce debugging information.
* PlatformToolset<br/>
  Compiler collection to use. Accepted values are: v140_xp, v140, v120, v120_xp, v110, v110_xp, v100, v90 (Note: You need to have the corresponding Visual Studio version installed).

Sample command to build Project64, Release|x64 variant for MSVC 14 without XP support:
```
MSBuild.exe Project64.sln /p:Platform=x64 /p:Configuration=Release /p:PlatformToolset=v140
```

# Visual Studio IDE (2010 and later)
1. Open the solution in Visual Studio (Project64.sln)
2. Right-click the solution in the Project panel, and choose Build.<br/>
   Alternatively, press SHIFT+CTRL+B

Notes:
* In the Build toolbar, you can select the Platform and Configuration needed.
* To change the platform tool set, edit the file PropertySheets\Platform.props, and set the <PlatformToolSet> property.
