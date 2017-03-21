# NuGet-issue-4532
Demo repo for https://github.com/NuGet/Home/issues/4532

`"C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\MSBuild\15.0\Bin\msbuild.exe" "D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.sln" /t:Restore;Build`

```
"C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\MSBuild\15.0\Bin\msbuild.exe" "D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.sln" /t:Restore;Build
Microsoft (R) Build Engine version 15.1.548.43366
Copyright (C) Microsoft Corporation. All rights reserved.

Building the projects in this solution one at a time. To enable parallel build, please add the "/m" switch.
Build started 21.03.2017 19:08:43.
Project "D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.sln" on node 1 (Restore;Build target(s)).
ValidateSolutionConfiguration:
  Building solution configuration "Debug|Any CPU".
Restore:
  Restoring packages for D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.csproj...
  Restoring packages for D:\Repos\NuGet-issue-4532\ClassLibrary1\ClassLibrary1.csproj...
  Committing restore...
  Committing restore...
  Generating MSBuild file D:\Repos\NuGet-issue-4532\ConsoleApp1\obj\ConsoleApp1.csproj.nuget.g.props.
  Generating MSBuild file D:\Repos\NuGet-issue-4532\ClassLibrary1\obj\ClassLibrary1.csproj.nuget.g.props.
  Generating MSBuild file D:\Repos\NuGet-issue-4532\ClassLibrary1\obj\ClassLibrary1.csproj.nuget.g.targets.
  Generating MSBuild file D:\Repos\NuGet-issue-4532\ConsoleApp1\obj\ConsoleApp1.csproj.nuget.g.targets.
  Writing lock file to disk. Path: D:\Repos\NuGet-issue-4532\ConsoleApp1\obj\project.assets.json
  Writing lock file to disk. Path: D:\Repos\NuGet-issue-4532\ClassLibrary1\obj\project.assets.json
  Restore completed in 347,62 ms for D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.csproj.
  Restore completed in 347,58 ms for D:\Repos\NuGet-issue-4532\ClassLibrary1\ClassLibrary1.csproj.
[...]

CopyFilesToOutputDirectory:
  Copying file from "obj\Debug\ClassLibrary1.dll" to "bin\Debug\ClassLibrary1.dll".
  ClassLibrary1 -> D:\Repos\NuGet-issue-4532\ClassLibrary1\bin\Debug\ClassLibrary1.dll
  Copying file from "obj\Debug\ClassLibrary1.pdb" to "bin\Debug\ClassLibrary1.pdb".
Done Building Project "D:\Repos\NuGet-issue-4532\ClassLibrary1\ClassLibrary1.csproj" (default targets).

C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\MSBuild\Microsoft\NuGet\15.0\Microsoft.NuGet.targets(197,5): error : The project.json is referencing the project 'D:
\Repos\NuGet-issue-4532\ConsoleApp1\ClassLibrary1\ClassLibrary1.csproj', but an output path was not specified on an item in the ProjectReferencesCreatingPackages property. [D:\Rep
os\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.csproj]
Done Building Project "D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.csproj" (default targets) -- FAILED.

Done Building Project "D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.sln" (Restore;Build target(s)) -- FAILED.


Build FAILED.

"D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.sln" (Restore;Build target) (1) ->
"D:\Repos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.csproj" (default target) (2:4) ->
(ResolveNuGetPackageAssets target) ->
  C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\MSBuild\Microsoft\NuGet\15.0\Microsoft.NuGet.targets(197,5): error : The project.json is referencing the project '
D:\Repos\NuGet-issue-4532\ConsoleApp1\ClassLibrary1\ClassLibrary1.csproj', but an output path was not specified on an item in the ProjectReferencesCreatingPackages property. [D:\R
epos\NuGet-issue-4532\ConsoleApp1\ConsoleApp1.csproj]

    0 Warning(s)
    1 Error(s)

Time Elapsed 00:00:02.10
```
