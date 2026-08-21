---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Set-ARASystem
---

# Set-ARASystem

## SYNOPSIS

Set operation for ARASystem

## SYNTAX

### __AllParameterSets

```
Set-ARASystem [[-Customer] <string>] [-RmfProvider <RmfProvider>]
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Updates the ARA system metadata (customer name and RMF provider information).

## EXAMPLES

### Example 1

Set-ARASystem -Customer "New Customer Name" -RmfProvider $rmfProviderObject

Changes are stored in memory until saved using Save-ARAFile.
            Connect-ARAFile must be called first to load an ARA file.

## PARAMETERS

### -Customer

The updated customer name.
If not provided, the existing value is unchanged.

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

### -RmfProvider

The updated RMF provider information.
If not provided, the existing value is unchanged.

```yaml
Type: AzureRMFAccelerator.Core.RmfProvider
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

### AzureRMFAccelerator.Core.RmfProvider

Information about the RMF provider for the system being modeled.

## OUTPUTS

### System.Object

{{ Fill in the Description }}

### AzureRMFAccelerator.Core.ARAResult

Result of running a command.

## NOTES




## RELATED LINKS

- [Online Version]()
- [Online Version]()
- [Online Version]()
- [Online Version]()
- [Online Version]()
