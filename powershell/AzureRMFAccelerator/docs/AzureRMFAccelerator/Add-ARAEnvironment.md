---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Add-ARAEnvironment
---

# Add-ARAEnvironment

## SYNOPSIS

Add operation for ARAEnvironment

## SYNTAX

### Properties (Default)

```
Add-ARAEnvironment [-Key] <string> [[-Name] <string>] [-ResourceGroups <ResourceGroup[]>]
 [-Roles <EnvironmentRole[]>]
```

### Object

```
Add-ARAEnvironment -Environment <Environment>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Adds a new ARA environment to the connected ARA file.

## EXAMPLES

### Example 1

Add-ARAEnvironment -Key "Dev" -Name "Development" -ResourceGroups $resourceGroups -Roles $roles

Supports two parameter sets: provide an Environment object, or provide individual properties.
            Use Save-ARAFile to persist changes.

## PARAMETERS

### -Environment

The complete Environment object to add.

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

The unique key identifier for the new environment.

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

The friendly name for the environment (e.g., "Development", "Production").

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

Array of ResourceGroup objects contained in this environment.

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

Array of EnvironmentRole objects defining roles for this environment.

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

{{ Fill in the Description }}

### AzureRMFAccelerator.Core.Environment

Represents an environment (e.g.
dev, staging, production) containing resource groups.

### AzureRMFAccelerator.Core.ResourceGroup[]

{{ Fill in the Description }}

### AzureRMFAccelerator.Core.EnvironmentRole[]

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
