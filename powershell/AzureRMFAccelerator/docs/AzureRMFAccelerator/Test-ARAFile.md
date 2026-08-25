---
document type: cmdlet
external help file: AzureRMFAcceleratorModule.Cmdlet.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/14/2026
PlatyPS schema version: 2024-05-01
title: Test-ARAFile
---

# Test-ARAFile

## SYNOPSIS

Validates the connected ARA file against its JSON schema without saving changes.

## SYNTAX

### __AllParameterSets

```
Test-ARAFile
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Validates the connected ARA file against its JSON schema without saving changes.

## EXAMPLES

### Example 1

PS C:\\> Test-ARAFile

Returns EvaluationResults containing validation status, errors, and warnings.
No changes are persisted to disk by this cmdlet.

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable,
-InformationAction, -InformationVariable, -OutBuffer, -OutVariable, -PipelineVariable,
-ProgressAction, -Verbose, -WarningAction, and -WarningVariable. For more information, see
[about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object

See command description for output behavior.

### Json.Schema.EvaluationResults

{{ Fill in the Description }}

## NOTES

Generated from XML documentation comments.


## RELATED LINKS

- [Online Version]()
