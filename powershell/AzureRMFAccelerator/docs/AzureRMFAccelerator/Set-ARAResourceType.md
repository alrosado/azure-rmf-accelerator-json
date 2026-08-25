---
document type: cmdlet
external help file: AzureRMFAcceleratorModule.Cmdlet.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/14/2026
PlatyPS schema version: 2024-05-01
title: Set-ARAResourceType
---

# Set-ARAResourceType

## SYNOPSIS

Updates an existing ARA resource type in the connected ARA file.

## SYNTAX

### Properties (Default)

```
Set-ARAResourceType [-Key] <string> [[-Provider] <string>] [[-FriendlyName] <string>]
```

### Object

```
Set-ARAResourceType -ResourceType <ResourceType>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Updates an existing ARA resource type in the connected ARA file.

## EXAMPLES

### Example 1

PS C:\\> Set-ARAResourceType

Supports two parameter sets: provide a ResourceType object, or provide individual properties.

## PARAMETERS

### -FriendlyName

The updated friendly name.
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

### -Key

The resource type key to update.

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

### -Provider

The updated provider name.
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

### -ResourceType

The updated ResourceType object.

```yaml
Type: AzureRMFAccelerator.Core.ResourceType
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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable,
-InformationAction, -InformationVariable, -OutBuffer, -OutVariable, -PipelineVariable,
-ProgressAction, -Verbose, -WarningAction, and -WarningVariable. For more information, see
[about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

Accepted from the pipeline.

### AzureRMFAccelerator.Core.ResourceType

Accepted from the pipeline.

## OUTPUTS

### System.Object

See command description for output behavior.

## NOTES

Generated from XML documentation comments.


## RELATED LINKS

- [Online Version]()
