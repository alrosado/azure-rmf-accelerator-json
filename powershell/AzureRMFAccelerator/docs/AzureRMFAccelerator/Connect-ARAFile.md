---
document type: cmdlet
external help file: AzureRMFAcceleratorModule.Cmdlet.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/14/2026
PlatyPS schema version: 2024-05-01
title: Connect-ARAFile
---

# Connect-ARAFile

## SYNOPSIS

Creates the ARA context for a directory and optionally connects to an existing ARA file.

## SYNTAX

### __AllParameterSets

```
Connect-ARAFile [[-System] <string>] [[-Version] <string>] [-PassThru]
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Creates the ARA context for a directory and optionally connects to an existing ARA file.

## EXAMPLES

### Example 1

PS C:\\> Connect-ARAFile

This cmdlet must be called before using any other ARA cmdlets.
It initializes the context that provides access to the ARA file repository.
If System and Version are provided, it also loads the corresponding ARA file.

## PARAMETERS

### -PassThru

If specified, outputs the connected ARA file object to the pipeline.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### -System

The system name of the ARA file to connect to.
Optional; if not provided, only context is initialized.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: (All)
  Position: 1
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Version

The version of the ARA file to connect to.
Optional; required if System is provided.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: (All)
  Position: 2
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

### AzureRMFAccelerator.Core.ARAFile

{{ Fill in the Description }}

## NOTES

Generated from XML documentation comments.


## RELATED LINKS

- [Online Version]()
