Currently, Project64 builds under Windows platforms.
It can be fully compiled using Microsoft Visual Studio compilers, versions 2008 to 2015.

# Command line
In a command prompt enter:
```
MSBuild.exe Project64.sln
```
This will build the Debug|Win32 variant, using the Visual Studio 2015 (MSVC 14) compiler toolset.

## Specific builds
Use the following MSBuild properties to set the platform, configuration, and tool set for the build:
* Platform<br/>
  Can be either Win32 or x64
* Configuration<br/>
  Either Debug or Release. It will determine either to use code optimizations or produce debugging information.
* PlatformToolset<br/>
  Compiler collection to use. Default is v140_xp (Visual Studio 2015 with Windows XP support).<br/>
  Other accepted values/versions: v140, v120, v120_xp, v110, v110_xp, v100, v90 (Note: You need to have the corresponding Visual Studio version installed).

Sample comand to build Project64, Release|x64 variant for MSVC 14 without XP support:
```
MSBuild.exe Project64.sln /p:Platform=x64 /p:Configuration=Release /p:PlatformToolset=v140
```

# Visual Studio IDE (2010 and later)
1. Open the solution in Visual Studio (Project64.sln)
2. Right-click the solution in the Project panel, and choose Build.<br/>
   Alternatively, type SHIFT+CTRL+B

Notes:
* In the Build toolbar, you can select the Platform and Configuration needed.
* To change the platform tool set, edit the file PropertySheets\Platform.props, and set the <PlatformToolSet> property.