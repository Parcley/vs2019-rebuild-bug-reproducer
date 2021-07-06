# Visual Studio 2019 16.10.3 rebuild bug reproducer

this solution can be built (Build/Build Solution) with VS 16.10.3, but not rebuilt (Build/Rebuild Solution).
rebuilding was possible with VS 16.7.5
rebuilding is also possible with `dotnet build --no-incremental` (dotnet --version 5.0.301)

when rebuilding with CS 16.10.3, these errors show up:
- `Error	MSB3030	Could not copy the file "<repo>\bin\netcoreapp3.1\MainProject.runtimeconfig.json" because it was not found.	MainProject.Test	C:\Program Files (x86)\Microsoft Visual Studio\2019\Professional\MSBuild\Current\Bin\Microsoft.Common.CurrentVersion.targets	4964`
- `Error	MSB3030	Could not copy the file "<repo>\bin\netcoreapp3.1\MainProject.runtimeconfig.dev.json" because it was not found.	MainProject.Test	C:\Program Files (x86)\Microsoft Visual Studio\2019\Professional\MSBuild\Current\Bin\Microsoft.Common.CurrentVersion.targets	4964`
- `Error	MSB3030	Could not copy the file "<repo>\bin\netcoreapp3.1\MainProject.deps.json" because it was not found.	MainProject.Test	C:\Program Files (x86)\Microsoft Visual Studio\2019\Professional\MSBuild\Current\Bin\Microsoft.Common.CurrentVersion.targets	4964`
