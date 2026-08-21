---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Connect-ARAContext
---

# Connect-ARAContext

## SYNOPSIS

Connect operation for ARAContext

## SYNTAX

### __AllParameterSets

```
Connect-ARAContext [-Path] <string> [-UserObjectId <guid>]
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Initializes the ARA context for a directory where ARA files are stored.

## EXAMPLES

### Example 1

Connect-ARAContext -Path "C:\ARAFiles" -UserObjectId "0DE9C979-BA95-4718-BE6E-2124088E1D44"

This cmdlet creates the internal ARA context object and stores it in the PowerShell session.
            It must be called first before any other ARA cmdlets.
After initialization, use Connect-ARAFile
            to connect to a specific ARA file.

## PARAMETERS

### -Path

The file system path where ARA files are stored.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: (All)
  Position: 0
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -UserObjectId

Optional user object ID for tracking who created/modified ARA files.
Uses current Windows user if not specified.

```yaml
Type: System.Guid
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: (All)
  Position: Named
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

{{ Fill in the Description }}

### System.Guid

{{ Fill in the Description }}

## OUTPUTS

### System.Object

{{ Fill in the Description }}

### AzureRMFAccelerator.Core.ARAFile

Root container for all ARA data.
Represents the complete ARA document structure.

## NOTES




## RELATED LINKS

- [Online Version]()
- [Online Version]()
- [Online Version]()
- [Online Version]()
- [Online Version]()
