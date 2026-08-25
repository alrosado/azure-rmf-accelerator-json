---
document type: cmdlet
external help file: AzureRMFAcceleratorModule.Cmdlet.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/14/2026
PlatyPS schema version: 2024-05-01
title: Remove-ARAStig
---

# Remove-ARAStig

## SYNOPSIS

Removes an ARA STIG requirement from the connected ARA file.

## SYNTAX

### __AllParameterSets

```
Remove-ARAStig [-TargetKey] <string> [-TargetType] <string>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Removes an ARA STIG requirement from the connected ARA file.

## EXAMPLES

### Example 1

PS C:\\> Remove-ARAStig

Use Save-ARAFile to persist changes.

## PARAMETERS

### -TargetKey

The target key to remove the STIG from.

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

### -TargetType

The target type: "resourceType" or "software".

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: (All)
  Position: 1
  IsRequired: true
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

## NOTES

Generated from XML documentation comments.


## RELATED LINKS

- [Online Version]()
