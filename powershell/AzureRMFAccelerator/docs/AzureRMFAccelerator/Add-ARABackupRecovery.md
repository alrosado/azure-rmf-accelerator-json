---
document type: cmdlet
external help file: AzureRMFAccelerator.Module.dll-Help.xml
HelpUri: ''
Locale: en-US
Module Name: AzureRMFAccelerator
ms.date: 08/18/2026
PlatyPS schema version: 2024-05-01
title: Add-ARABackupRecovery
---

# Add-ARABackupRecovery

## SYNOPSIS

Add operation for ARABackupRecovery

## SYNTAX

### Properties (Default)

```
Add-ARABackupRecovery -Strategy <string> -BackupFrequency <string> [-Retention <string>]
 [-RestoreTestFrequency <string>] [-ResponsibleRoleKey <string>] [-Audit <Audit>]
```

### Object

```
Add-ARABackupRecovery -BackupRecovery <BackupRecovery>
```

## ALIASES

This cmdlet has the following aliases,
  {{Insert list of aliases}}

## DESCRIPTION

Adds a new backup and recovery configuration to the connected ARA file.

## EXAMPLES

### Example 1

Add-ARABackupRecovery -Strategy "Full" -BackupFrequency "Daily" -Retention "30 days" -RestoreTestFrequency "Weekly" -ResponsibleRoleKey "BackupAdmin" -Audit $auditObject

Creates a new BackupRecovery object in the currently connected ARA file.

## PARAMETERS

### -Audit

The audit information for the backup and recovery configuration.
Optional; if not provided, defaults to the system's default audit settings.

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

### -BackupFrequency

The frequency of backups.
Mandatory if using the Properties parameter set.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: Named
  IsRequired: true
  ValueFromPipeline: false
  ValueFromPipelineByPropertyName: false
  ValueFromRemainingArguments: false
DontShow: false
AcceptedValues: []
HelpMessage: ''
```

### -BackupRecovery

The BackupRecovery object to add.
If provided, other parameters are ignored.

```yaml
Type: AzureRMFAccelerator.Core.BackupRecovery
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

### -ResponsibleRoleKey

The key of the responsible role for backup and recovery.
Optional; if not provided, defaults to the system's default responsible role.

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

### -RestoreTestFrequency

The frequency of restore tests.
Optional; if not provided, defaults to the system's default restore test frequency.

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

### -Retention

The retention period for backups.
Optional; if not provided, defaults to the system's default retention policy.

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

### -Strategy

The backup strategy to use.

```yaml
Type: System.String
DefaultValue: ''
SupportsWildcards: false
Aliases: []
ParameterSets:
- Name: Properties
  Position: Named
  IsRequired: true
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

### AzureRMFAccelerator.Core.BackupRecovery

Backup and recovery strategy for the system.
This is used to define the backup and recovery strategy for the system and to set expectations for users.

## OUTPUTS

### AzureRMFAccelerator.Core.ARAResult

Result of running a command.

## NOTES




## RELATED LINKS

- [Online Version]()
- [Online Version]()
- [Online Version]()
- [Online Version]()
