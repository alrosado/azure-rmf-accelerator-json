---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Get-ARAArchitectureDiagram
---

# Get-ARAArchitectureDiagram

## SYNOPSIS

Get operation for ARAArchitectureDiagram

## SYNTAX

### __AllParameterSets

```
Get-ARAArchitectureDiagram [-Name <string>]
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Gets the architecture diagram settings from the connected ARA file.

## EXAMPLES

### Example 1

Get-ARAArchitectureDiagram -Name "MyDiagram"

Returns the ArchitectureDiagram object(s) from the currently connected ARA file.

## PARAMETERS

### -Name

The name of the architecture diagram to retrieve.
If not provided, all diagrams are returned.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: (All)
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

## OUTPUTS

### AzureRMFAccelerator.Core.ArchitectureDiagram

Diagram used to define a component within the architecture of the system.

## NOTES




## RELATED LINKS

- [Online Version]()
- [Online Version]()
- [Online Version]()
- [Online Version]()
