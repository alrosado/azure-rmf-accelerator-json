---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Set-ARAResource
---

# Set-ARAResource

## SYNOPSIS

Set operation for ARAResource

## SYNTAX

### Properties (Default)

```
Set-ARAResource [-Environment] <string> [-ResourceGroup] <string> [-Type] <string> [-Name] <string>
 [-Description <string>] [-FriendlyName <string>] [-IacModuleName <string>]
 [-IacModulePath <string>] [-Roles <ResourceRole[]>] [-Software <string[]>]
 [-LinkedResources <LinkedResource[]>] [-Connections <ResourceConnection[]>] [-InBoundary <bool>]
```

### Object

```
Set-ARAResource -Resource <Resource>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Updates an existing ARA resource in the connected ARA file.

## EXAMPLES

### Example 1

Set-ARAResource -Environment "MyEnvironment" -ResourceGroup "MyResourceGroup" -Type "MyResourceType" -Name "MyResourceName" -Description "UpdatedDescription" -FriendlyName "UpdatedFriendlyName" -IacModuleName "UpdatedIacModule" -IacModulePath "C:\New\Path\To\Module" -Roles $updatedRolesArray -Software $updatedSoftwareArray -LinkedResources $updatedLinkedResourcesArray -Connections $updatedConnectionsArray -InBoundary $false

Supports two parameter sets: provide a Resource object, or provide individual properties.

## PARAMETERS

### -Connections

The updated connections array.
If not provided, existing value is unchanged.

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

### -Environment

The environment name of the resource to update.

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
  Position: Named
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: true
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -IacModuleName

The updated IAC module name.
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

### -IacModulePath

The updated IAC module path.
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

### -InBoundary

Whether the resource is within the system boundary.
If not provided, existing value is unchanged.

```yaml
Type: System.Boolean
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

### -LinkedResources

The updated linked resources array.
If not provided, existing value is unchanged.

```yaml
Type: AzureRMFAccelerator.Core.LinkedResource[]
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

The resource name to update.

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

### -Resource

The updated Resource object.

```yaml
Type: AzureRMFAccelerator.Core.Resource
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

### -ResourceGroup

The resource group name of the resource to update.

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

### -Roles

The updated roles array.
If not provided, existing value is unchanged.

```yaml
Type: AzureRMFAccelerator.Core.ResourceRole[]
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

### -Software

The updated software array.
If not provided, existing value is unchanged.

```yaml
Type: System.String[]
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

### -Type

The resource type of the resource to update.

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

### System.String

{{ Fill in the Description }}

### AzureRMFAccelerator.Core.Resource

Represents a cloud resource with roles, software, and relationships.

### AzureRMFAccelerator.Core.ResourceRole[]

{{ Fill in the Description }}

### System.String[]

{{ Fill in the Description }}

### AzureRMFAccelerator.Core.LinkedResource[]

{{ Fill in the Description }}

### AzureRMFAccelerator.Core.ResourceConnection[]

{{ Fill in the Description }}

### System.Boolean

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
