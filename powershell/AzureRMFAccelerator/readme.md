# ARA PowerShell Module (`AzureRMFAccelerator`)

## Purpose
`AzureRMFAccelerator` is the domain module for managing Azure RMF Accelerator (ARA) data as strongly typed PowerShell objects and JSON.

It provides:
- Class models for ARA concepts (roles, environments, resource groups, resources, software, STIGs, and configuration strings)
- CRUD commands for each model
- File load/save workflows for ARA JSON files
- Validation helpers to validate ARA JSON content against schema

## What `AzureRMFAccelerator.psm1` manages
The module represents and persists:
- System metadata: `system`, `version`, `customer`, `$schema`
- Security roles and members
- Resource types
- Software catalog
- STIG mappings to resource types and appliers
- Environments, resource groups, resources, and linked resources
- Key/value configuration strings

## Key module behavior
- `Connect-ARAFile` loads an ARA JSON file into in-memory objects (`$global:ARAFile`).
- Most `Add-*`, `Set-*`, and `Remove-*` commands call `Save-ARAFile`.
- `Save-ARAFile` serializes the in-memory model back to JSON and reloads via `Connect-ARAFile` to keep references consistent.

## Main command groups
- File/session: `New-ARAFile`, `Connect-ARAFile`, `Test-ARAFile`
- Roles: `New/Get/Add/Set/Remove-ARARole`
- Environments: `New/Get/Add/Set/Remove-ARAEnvironment`
- Resources: `New/Get/Add/Set/Remove-ARAResource`
- Linked resources: `New/Add/Set/Remove-ARALinkedResource`
- Resource types: `New/Get/Add/Set/Remove-ARAResourceType`
- Software: `Get/Add/Set/Remove-ARASoftware`
- STIGs: `New/Get/Add/Set/Remove-ARASTIG`
- Configuration strings: `New/Get/Add/Set/Remove-ARAConfigurationString`
- System metadata: `Get-ARASystem`, `Set-ARASystem`

Refer to the [cmdlet reference](reference.md) for a full list of available commands and the [release notes](release.md) for version history.

## Typical usage flow
1. Import and connect:

```powershell
Install-Module -Name AzureRMFAccelerator -Scope CurrentUser
Import-Module AzureRMFAccelerator
Connect-ARAFile -Path .\contoso-system.json
```

2. Update data:

```powershell
Add-ARAEnvironment -Key "dev"
Add-ARAResourceType -Key "vm" -FriendlyName "Virtual Machine"
Add-ARARole -Key "admin" -Name "Administrator" -Group "Admins" -Active $true -Description "Admin role"
```

3. Validate:

```powershell
$result = Test-ARAFile
$result.IsValid
$result.Errors
```

## Notes
- The module uses global state (`$global:ARAFile` and `$global:path`) while connected.
- `Connect-ARAFile` should be called before CRUD operations.
- Validation supports local schema files and HTTP(S) schema URLs.
