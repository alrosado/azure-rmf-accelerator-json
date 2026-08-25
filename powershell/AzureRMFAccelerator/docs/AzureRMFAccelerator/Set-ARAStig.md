---
document type: cmdlet
external help file: AzureRMFAcceleratorModule.Cmdlet.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/14/2026
PlatyPS schema version: 2024-05-01
title: Set-ARAStig
---

# Set-ARAStig

## SYNOPSIS

Updates an existing ARA STIG requirement in the connected ARA file.

## SYNTAX

### Properties (Default)

```
Set-ARAStig [-TargetKey] <string> [-TargetType] <string> [[-Name] <string>]
 [[-ApplierRoleKey] <string>] [-Description <string>]
```

### Object

```
Set-ARAStig -Stig <Stig>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Updates an existing ARA STIG requirement in the connected ARA file.

## EXAMPLES

### Example 1

PS C:\\> Set-ARAStig

Supports two parameter sets: provide a Stig object, or provide individual properties.

## PARAMETERS

### -ApplierRoleKey

The updated applier role key.
If not provided, existing value is unchanged.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 3
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Description

The updated description.
If not provided, existing value is unchanged.

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
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Name

The updated STIG identifier.
If not provided, existing value is unchanged.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 2
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Stig

The updated Stig object.

```yaml
Type: AzureRMFAccelerator.Core.Stig
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

### -TargetKey

The target key to update.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
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
- Name: Properties
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

### AzureRMFAccelerator.Core.Stig

Accepted from the pipeline.

## OUTPUTS

### System.Object

See command description for output behavior.

## NOTES

Generated from XML documentation comments.


## RELATED LINKS

- [Online Version]()
