---
title: NuGet CLI spec command | Microsoft Docs
author: kraigb
ms.author: kraigb
manager: ghogen
ms.date: 01/18/2018
ms.topic: reference
ms.prod: nuget
ms.technology: null
description: Reference for the nuget.exe spec command
keywords: nuget spec reference, spec command
ms.reviewer:
- karann-msft
- unniravindranathan
ms.workload: 
 - "dotnet"
 - "aspnet"
---

# spec command (NuGet CLI)

**Applies to:** package creation &bullet; **Supported versions:** all

Generates a `.nuspec` file for a new package. If run in the same folder as a project file (`.csproj`, `.vbproj`, `.fsproj`), `spec` creates a tokenized `.nuspec` file. For additional information, see [Creating a Package](../create-packages/creating-a-package.md).

## Usage

```cli
nuget spec [<packageID>] [options]
```

where `<packageID>` is an optional package identifier to save in the `.nuspec` file.

## Options

| Option | Description |
| --- | --- |
| AssemblyPath | Specifies the path to the assembly to use for metadata. |
| Force | Overwrites any existing `.nuspec` file. |
| ForceEnglishOutput | *(3.5+)* Forces nuget.exe to run using an invariant, English-based culture. |
| Help | Displays help information for the command. |
| NonInteractive | Suppresses prompts for user input or confirmations. |
| Verbosity | Specifies the amount of detail displayed in the output: *normal*, *quiet*, *detailed*. |

Also see [Environment variables](cli-ref-environment-variables.md)

## Examples

```cli
nuget spec

nuget spec MyPackage

nuget spec -a MyAssembly.dll
```
