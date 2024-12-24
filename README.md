# Blazor WebAssembly Project with ScottPlot Integration

This repository demonstrates how to set up a Blazor WebAssembly project targeting .NET 8.0 with ScottPlot integration for data visualization. Follow the steps below to replicate the environment and run the project.

## Prerequisites
- .NET SDK installed on your system. Confirm your versions:
  ```ps1
  > dotnet --list-sdks
  7.0.410 [C:\Program Files\dotnet\sdk]
  8.0.307 [C:\Program Files\dotnet\sdk]
  8.0.404 [C:\Program Files\dotnet\sdk]
  9.0.100 [C:\Program Files\dotnet\sdk]
  ```
- Installed workloads for WebAssembly development. Check with:
  ```ps1
  > dotnet workload list
  wasm-tools              9.0.0/9.0.100      SDK 9.0.100, VS 17.12.35521.163
  ```

## Install Required Workloads
Install the WebAssembly tools for .NET 8.0:
```ps1
dotnet workload install wasm-tools-net8
```
Verify the installation:
```ps1
> dotnet workload list
wasm-tools              9.0.0/9.0.100      SDK 9.0.100, VS 17.12.35521.163
wasm-tools-net8         9.0.0/9.0.100      SDK 9.0.100
```

## Create and Set Up the Project
1. Create a new Blazor WebAssembly project targeting .NET 8.0:
   ```ps1
   dotnet new blazorwasm -f net8.0
   ```

2. Add the ScottPlot.Blazor package for data visualization:
   ```ps1
   dotnet add package ScottPlot.Blazor
   ```

3. Create a solution file and add the project:
   ```ps1
   dotnet new sln
   dotnet sln add .
   ```

4. Reference the [ScottPlot Blazor Quickstart Documentation](https://scottplot.net/quickstart/blazor/) for integration details.

## Run the Project
Run the application locally:
```ps1
dotnet run
```

## Publish the Project
1. Publish the project for production:
   ```ps1
   dotnet publish try-blazorwasm-with-plot.csproj -c Release -o publish
   ```

2. Serve the published files:
   ```ps1
   dotnet serve -o -S -p:5143 -b -d:.\publish\wwwroot\
   ```

## Notes
- Ensure your .NET SDK is up to date to avoid compatibility issues.
- ScottPlot.Blazor provides an easy-to-use API for embedding interactive plots in Blazor WebAssembly applications.

## Resources
- [ScottPlot Blazor Documentation](https://scottplot.net/quickstart/blazor/)
- [.NET Official Documentation](https://learn.microsoft.com/en-us/dotnet/)
- [dotnet CLI Commands](https://learn.microsoft.com/en-us/dotnet/core/tools/)

<!---
Feel free to raise issues or contribute enhancements to this repository!
-->
