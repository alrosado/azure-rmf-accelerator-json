---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Set-ARAChangeManagement
---

# Set-ARAChangeManagement

## SYNOPSIS

Set operation for ARAChangeManagement

## SYNTAX

### Properties (Default)

```
Set-ARAChangeManagement [-Process <string>] [-ApprovalAuthorityRoleKey <string>]
 [-SourceRepository <string>] [-DeploymentMethod <string>] [-ConfigurationBaseline <string>]
 [-Audit <Audit>]
```

### Object

```
Set-ARAChangeManagement -ChangeManagement <ChangeManagement>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Updates the change management settings in the connected ARA file.

## EXAMPLES

### Example 1

Set-ARAChangeManagement -Process "UpdatedProcess" -ApprovalAuthorityRoleKey "UpdatedRole" -SourceRepository "UpdatedRepo" -DeploymentMethod "UpdatedMethod" -ConfigurationBaseline "UpdatedBaseline" -Audit $updatedAuditObject

Modifies the existing ChangeManagement object in the currently connected ARA file.

## PARAMETERS

### -ApprovalAuthorityRoleKey

The key of the approval authority role for change management.
Optional; if not provided, the existing value is unchanged.

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
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Audit

The audit information for the change management configuration.
Optional; if not provided, the existing value is unchanged.

```yaml
Type: AzureRMFAccelerator.Core.Audit
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: Named
  IsRequired: false
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -ChangeManagement

The ChangeManagement object to update.
If provided, other parameters are ignored.

```yaml
Type: AzureRMFAccelerator.Core.ChangeManagement
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

### -ConfigurationBaseline

The configuration baseline for change management.
Optional; if not provided, the existing value is unchanged.

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
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -DeploymentMethod

The deployment method for change management.
Optional; if not provided, the existing value is unchanged.

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
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -Process

The change management process to use.
Optional; if not provided, the existing value is unchanged.

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
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -SourceRepository

The source repository for change management.
Optional; if not provided, the existing value is unchanged.

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

### AzureRMFAccelerator.Core.ChangeManagement

Change management process for the system.
This is used to define the change management process for the system and to set expectations for users.

## OUTPUTS

### AzureRMFAccelerator.Core.ARAResult

Result of running a command.

## NOTES




## RELATED LINKS

- [Online Version]()
- [Online Version]()
- [Online Version]()
- [Online Version]()
