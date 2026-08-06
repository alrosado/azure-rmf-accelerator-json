# Release Notes

## 1.0.1 — Initial Release

Bug fixes and changes based on json schema updates.

## 1.0.0 — Initial Release

First public release of the **AzureRMFAccelerator** PowerShell module.

### What's included

The module provides a full set of cmdlets for creating, loading, updating, validating, and saving ARA JSON files — the structured system definition format used by the Azure RMF Accelerator.

#### File / session management
| Cmdlet | Description |
|--------|-------------|
| `New-ARAFile` | Creates and initializes a new ARA JSON file |
| `Connect-ARAFile` | Loads an existing ARA JSON file into session |
| `Test-ARAFile` | Validates the loaded file against its JSON schema (local or HTTP) |
| `Get-ARASystem` | Returns top-level system metadata |
| `Set-ARASystem` | Updates system name, version, or customer |

#### Roles
`New-ARARole` · `Get-ARARole` · `Add-ARARole` · `Set-ARARole` · `Remove-ARARole`

#### Environments
`New-ARAEnvironment` · `Get-ARAEnvironment` · `Add-ARAEnvironment` · `Set-ARAEnvironment` · `Remove-ARAEnvironment`

#### Resource groups
`New-ARAResourceGroup`

#### Resources
`New-ARAResource` · `Get-ARAResource` · `Add-ARAResource` · `Set-ARAResource` · `Remove-ARAResource`

#### Linked resources
`New-ARALinkedResource` · `Add-ARALinkedResource` · `Set-ARALinkedResource` · `Remove-ARALinkedResource`

#### Resource types
`New-ARAResourceType` · `Get-ARAResourceType` · `Add-ARAResourceType` · `Set-ARAResourceType` · `Remove-ARAResourceType`

#### Software catalog
`Get-ARASoftware` · `Add-ARASoftware` · `Set-ARASoftware` · `Remove-ARASoftware`

#### STIGs
`New-ARAStig` · `Get-ARASTIG` · `Add-ARASTIG` · `Set-ARASTIG` · `Remove-ARASTIG`

#### Configuration strings
`New-ARAConfigurationString` · `Get-ARAConfigurationString` · `Add-ARAConfigurationString` · `Set-ARAConfigurationString` · `Remove-ARAConfigurationString`

### Requirements
- PowerShell 5.1 or later
- Internet access required when validating against the hosted schema (`https://` schema URI)

### Known limitations
- The module uses global session state (`$global:ARAFile`, `$global:path`). Only one ARA file can be active per session.
- `Test-ARAFile` performs structural JSON schema validation only; cross-reference integrity (e.g., role keys referenced by resources) is partially validated in-module but not covered by the schema itself.
