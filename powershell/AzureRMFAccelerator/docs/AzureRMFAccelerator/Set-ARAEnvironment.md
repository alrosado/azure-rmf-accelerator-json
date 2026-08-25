---
document type: cmdlet
external help file: AzureRMFAcceleratorModule.Cmdlet.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/14/2026
PlatyPS schema version: 2024-05-01
title: Set-ARAEnvironment
---

# Set-ARAEnvironment

## SYNOPSIS

Updates an existing ARA environment in the connected ARA file.

## SYNTAX

### Properties (Default)

```
Set-ARAEnvironment [-Key] <string> [[-Name] <string>] [-ResourceGroups <ResourceGroup[]>]
 [-Roles <EnvironmentRole[]>]
```

### Object

```
Set-ARAEnvironment -Environment <Environment>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Updates an existing ARA environment in the connected ARA file.

## EXAMPLES

### Example 1

PS C:\\> Set-ARAEnvironment

Supports two parameter sets: provide an Environment object, or provide individual properties.
Use Save-ARAFile to persist changes.

## PARAMETERS

### -Environment

The updated Environment object.

```yaml
Type: AzureRMFAccelerator.Core.Environment
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

### -Key

The environment key to update.

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

### -Name

The updated friendly name.
If not provided, existing value is unchanged.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 1
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -ResourceGroups

The updated array of ResourceGroup objects.
If not provided, existing value is unchanged.

```yaml
Type: AzureRMFAccelerator.Core.ResourceGroup[]
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

### -Roles

The updated array of EnvironmentRole objects.
If not provided, existing value is unchanged.

```yaml
Type: AzureRMFAccelerator.Core.EnvironmentRole[]
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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable,
-InformationAction, -InformationVariable, -OutBuffer, -OutVariable, -PipelineVariable,
-ProgressAction, -Verbose, -WarningAction, and -WarningVariable. For more information, see
[about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

Accepted from the pipeline.

### AzureRMFAccelerator.Core.Environment

Accepted from the pipeline.

### AzureRMFAccelerator.Core.ResourceGroup[]

Accepted from the pipeline.

### AzureRMFAccelerator.Core.EnvironmentRole[]

Accepted from the pipeline.

## OUTPUTS

### System.Object

See command description for output behavior.

## NOTES

Generated from XML documentation comments.


## RELATED LINKS

- [Online Version]()
