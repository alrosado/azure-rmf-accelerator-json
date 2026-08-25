---
document type: cmdlet
external help file: AzureRMFAcceleratorModule.Cmdlet.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/14/2026
PlatyPS schema version: 2024-05-01
title: Get-ARAEnvironment
---

# Get-ARAEnvironment

## SYNOPSIS

Gets one or all ARA environments from the connected ARA file.

## SYNTAX

### __AllParameterSets

```
Get-ARAEnvironment [[-Key] <string>]
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Gets one or all ARA environments from the connected ARA file.

## EXAMPLES

### Example 1

PS C:\\> Get-ARAEnvironment

If Key is not provided, returns all environments in the system.
Connect-ARAFile must be called first.

## PARAMETERS

### -Key

The environment key to retrieve.
If not provided, returns all environments.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: (All)
  Position: 0
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
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

### System.String

Accepted from the pipeline.

## OUTPUTS

### System.Object

See command description for output behavior.

### AzureRMFAccelerator.Core.Environment

{{ Fill in the Description }}

## NOTES

Generated from XML documentation comments.


## RELATED LINKS

- [Online Version]()
