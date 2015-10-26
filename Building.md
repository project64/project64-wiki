Currently, Project64 builds under Windows platforms.
It can be fully compiled using Microsoft Visual Studio compilers, versions 2008 to 2015.

# Visual Studio 2010 and later
In a command prompt (this example uses Windows PowerShell, enter:
```
MSBuild.exe Project64.sln /p:PlatformToolset=$toolset
```

Where $toolset is one of: v100, v110_xp, v120_xp, v140_xp.
The default value is v140_xp (Visual Stidio 2015).