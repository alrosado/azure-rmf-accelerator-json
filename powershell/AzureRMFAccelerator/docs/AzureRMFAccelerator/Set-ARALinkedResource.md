---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Set-ARALinkedResource
---

# Set-ARALinkedResource

## SYNOPSIS

Set operation for ARALinkedResource

## SYNTAX

### Properties (Default)

```
Set-ARALinkedResource [-Environment] <string> [-ParentResourceGroup] <string> [-ParentType] <string>
 [-ParentName] <string> [-ChildResourceGroup] <string> [-ChildType] <string> [-ChildName] <string>
 [-LinkType] <string> [-Description <string>] [-Connections <ResourceConnection[]>]
```

### Object

```
Set-ARALinkedResource -ParentResource <Resource> -LinkedResource <LinkedResource>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Updates an existing link between two resources.

## EXAMPLES

### Example 1

Set-ARALinkedResource -ParentResource $parentResource -LinkedResource $linkedResource

Supports two parameter sets: provide Resource and LinkedResource objects, or provide individual properties.

## PARAMETERS

### -ChildName

The name of the child resource.
Mandatory if using the Properties parameter set.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 6
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -ChildResourceGroup

The resource group of the child resource.
Mandatory if using the Properties parameter set.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 4
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -ChildType

The type of the child resource.
Mandatory if using the Properties parameter set.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 5
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Connections

Optional array of network connection details for the link.
If not provided, the existing value is unchanged.

```yaml
Type: AzureRMFAccelerator.Core.ResourceConnection[]
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

### -Description

Optional description of the link relationship.
If not provided, the existing value is unchanged.

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

### -Environment

The environment containing both resources.
Mandatory if using the Properties parameter set.

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

### -LinkedResource

The linked resource object to be associated with the parent resource.

```yaml
Type: AzureRMFAccelerator.Core.LinkedResource
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

### -LinkType

The type of the link between the parent and child resources.
Mandatory if using the Properties parameter set.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 7
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -ParentName

The name of the parent resource.
Mandatory if using the Properties parameter set.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 3
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -ParentResource

The parent resource object that has the linked resource.

```yaml
Type: AzureRMFAccelerator.Core.Resource
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Object
  Position: Named
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -ParentResourceGroup

The resource group of the parent resource.
Mandatory if using the Properties parameter set.

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

### -ParentType

The type of the parent resource.
Mandatory if using the Properties parameter set.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: 2
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

### AzureRMFAccelerator.Core.Resource

Represents a cloud resource with roles, software, and relationships.

### AzureRMFAccelerator.Core.LinkedResource

Represents a directional link between two resources.

### System.String

{{ Fill in the Description }}

### AzureRMFAccelerator.Core.ResourceConnection[]

{{ Fill in the Description }}

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
