# AnalyzerProject.Convention

"Analyzer with Code Fix" project template with ConventionCodeFixVerifier test project

## How to use

Install the template:

```sh
dotnet new -i AnalyzerProject.Convention
```

NuGet: [https://www.nuget.org/packages/AnalyzerProject.Convention/](https://www.nuget.org/packages/AnalyzerProject.Convention/)

Create a new project:

```sh
dotnet new AnalyzerConvention
```

## Contents

This project template contains:

- C# "Analyzer with Code Fix (.NET Standard)" project
- with [ConventionCodeFixVerifier](https://github.com/ufcpp/ConventionCodeFixVerifier)
- with [XUnit](https://www.nuget.org/packages/xunit/)

### ConventionCodeFixVerifier

Extends the CodeFixVerifier class in the "Analyzer with Code Fix" project template to read test cases from .csx files by naming convention.

#### Convention

- Put the following files in `/DataSource/[test class name]/[test method name]` folder
  - `*.cs` in `Source` folder: inputs for your Analyzer/Code Fix
  - `*.json` in `Diagnostic` folder: diagnostic results of the Source.cs by your Analyzer
  - `*.cs` in `Expected{n}` folder: output source codes by the n-th action of your Code Fix

![Sample Screenshot](doc/screenshot.png)
