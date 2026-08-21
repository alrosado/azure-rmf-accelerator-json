---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Set-ARAArchitectureDiagram
---

# Set-ARAArchitectureDiagram

## SYNOPSIS

Set operation for ARAArchitectureDiagram

## SYNTAX

### Properties (Default)

```
Set-ARAArchitectureDiagram -Name <string> [-Path <string>] [-Description <string>]
```

### Object

```
Set-ARAArchitectureDiagram -Diagram <ArchitectureDiagram>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Updates an existing architecture diagram in the connected ARA file.

## EXAMPLES

### Example 1

Set-ARAArchitectureDiagram -Name "MyDiagram" -Path "C:\Diagrams\UpdatedDiagram.png" -Description "This is my updated architecture diagram."

Changes are stored in memory until saved using Save-ARAFile.

## PARAMETERS

### -Description

The description of the architecture diagram to update.
Optional; if not provided, the existing value is unchanged.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: Named
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Diagram

The ArchitectureDiagram object to update.
If provided, other parameters are ignored.

```yaml
Type: AzureRMFAccelerator.Core.ArchitectureDiagram
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Object
  Position: Named
  IsRequired: true
  ValueFromPipeline: true
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Name

The name of the architecture diagram to update.
Mandatory if using the Properties parameter set.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: Named
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Path

The file path of the architecture diagram to update.
Optional; if not provided, the existing value is unchanged.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: Named
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable,
-InformationAction, -InformationVariable, -OutBuffer, -OutVariable, -PipelineVariable,
-ProgressAction, -Verbose, -WarningAction, and -WarningVariable. For more information, see
[about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### AzureRMFAccelerator.Core.ArchitectureDiagram

Diagram used to define a component within the architecture of the system.

## OUTPUTS

### AzureRMFAccelerator.Core.ARAResult

Result of running a command.

## NOTES




## RELATED LINKS

- [Online Version]()
- [Online Version]()
- [Online Version]()
- [Online Version]()
