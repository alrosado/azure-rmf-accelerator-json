# ARA PowerShell Module — Cmdlet Reference

Module: **AzureRMFAccelerator**  
The ARA PowerShell module provides cmdlets for creating, loading, validating, and managing Azure RMF Accelerator (ARA) JSON files. Commands follow the standard PowerShell `Verb-Noun` naming convention and are grouped by the resource type they manage.

---

## Cmdlets

### File and Session

| Cmdlet | Description |
|--------|-------------|
| [New-ARAFile](#new-arafile) | Creates a new ARA JSON file and initializes global session state. |
| [Connect-ARAFile](#connect-arafile) | Loads an existing ARA JSON file into the in-memory session. |
| [Test-ARAFile](#test-arafile) | Validates the current ARA file against its JSON schema. |

### System Metadata

| Cmdlet | Description |
|--------|-------------|
| [Get-ARASystem](#get-arasystem) | Retrieves the top-level system metadata (name, version, customer, schema). |
| [Set-ARASystem](#set-arasystem) | Updates system metadata fields. |

### Roles

| Cmdlet | Description |
|--------|-------------|
| [New-ARARole](#new-ararole) | Returns an empty `ARARole` object for manual population. |
| [Get-ARARole](#get-ararole) | Retrieves one or all roles. |
| [Add-ARARole](#add-ararole) | Adds a new role to the ARA file. |
| [Set-ARARole](#set-ararole) | Updates an existing role. |
| [Remove-ARARole](#remove-ararole) | Removes a role from the ARA file. |

### Environments

| Cmdlet | Description |
|--------|-------------|
| [New-ARAEnvironment](#new-araenvironment) | Returns an empty `ARAEnvironment` object for manual population. |
| [Get-ARAEnvironment](#get-araenvironment) | Retrieves one or all environments. |
| [Add-ARAEnvironment](#add-araenvironment) | Adds a new environment to the ARA file. |
| [Set-ARAEnvironment](#set-araenvironment) | Updates an existing environment. |
| [Remove-ARAEnvironment](#remove-araenvironment) | Removes an environment from the ARA file. |

### Resources

| Cmdlet | Description |
|--------|-------------|
| [New-ARAResourceGroup](#new-araresourcegroup) | Returns an empty `ARAResourceGroup` object for manual population. |
| [New-ARAResource](#new-araresource) | Returns an empty `ARAResource` object for manual population. |
| [Get-ARAResource](#get-araresource) | Retrieves one or all resources, optionally filtered. |
| [Add-ARAResource](#add-araresource) | Adds a new resource to a resource group. |
| [Set-ARAResource](#set-araresource) | Updates an existing resource. |
| [Remove-ARAResource](#remove-araresource) | Removes a resource from a resource group. |

### Linked Resources

| Cmdlet | Description |
|--------|-------------|
| [New-ARALinkedResource](#new-aralinkedresource) | Returns an empty `ARALinkedResource` object for manual population. |
| [Add-ARALinkedResource](#add-aralinkedresource) | Adds a relationship link between two resources. |
| [Set-ARALinkedResource](#set-aralinkedresource) | Updates an existing relationship link. |
| [Remove-ARALinkedResource](#remove-aralinkedresource) | Removes a relationship link between two resources. |

### Resource Types

| Cmdlet | Description |
|--------|-------------|
| [New-ARAResourceType](#new-araresourcetype) | Returns an empty `ARAResourceType` object for manual population. |
| [Get-ARAResourceType](#get-araresourcetype) | Retrieves one or all resource types. |
| [Add-ARAResourceType](#add-araresourcetype) | Adds a new resource type to the ARA file. |
| [Set-ARAResourceType](#set-araresourcetype) | Updates an existing resource type. |
| [Remove-ARAResourceType](#remove-araresourcetype) | Removes a resource type from the ARA file. |

### Software

| Cmdlet | Description |
|--------|-------------|
| [Get-ARASoftware](#get-arasoftware) | Retrieves one or all software components. |
| [Add-ARASoftware](#add-arasoftware) | Adds a new software component to the ARA file. |
| [Set-ARASoftware](#set-arasoftware) | Updates an existing software component. |
| [Remove-ARASoftware](#remove-arasoftware) | Removes a software component from the ARA file. |

### STIGs

| Cmdlet | Description |
|--------|-------------|
| [New-ARASTIG](#new-arastig) | Returns an empty `ARAStig` object for manual population. |
| [Get-ARASTIG](#get-arastig) | Retrieves one or all STIG requirements. |
| [Add-ARASTIG](#add-arastig) | Adds a new STIG requirement to the ARA file. |
| [Set-ARASTIG](#set-arastig) | Updates an existing STIG requirement. |
| [Remove-ARASTIG](#remove-arastig) | Removes a STIG requirement from the ARA file. |

### Configuration Strings

| Cmdlet | Description |
|--------|-------------|
| [New-ARAConfigurationString](#new-araconfigurationstring) | Returns an empty `ARAConfigurationString` object for manual population. |
| [Get-ARAConfigurationString](#get-araconfigurationstring) | Retrieves one or all configuration strings. |
| [Add-ARAConfigurationString](#add-araconfigurationstring) | Adds a new configuration key-value pair to the ARA file. |
| [Set-ARAConfigurationString](#set-araconfigurationstring) | Updates an existing configuration string value. |
| [Remove-ARAConfigurationString](#remove-araconfigurationstring) | Removes a configuration string from the ARA file. |

---

## Cmdlet Details

---

### New-ARAFile

Creates a new ARA JSON file on disk and initializes the global session state (`$global:ARAFile`).

#### Syntax

```powershell
New-ARAFile
    -system <String>
    -version <String>
    -customer <String>
    -path <String>
    [-schema <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `system` | String | Yes | The system name. |
| `version` | String | Yes | The system version. |
| `customer` | String | Yes | The customer name. |
| `path` | String | Yes | File path where the new ARA JSON file will be written. |
| `schema` | String | No | JSON schema URI. Defaults to the latest published v1 schema. |

#### Example

```powershell
New-ARAFile -system "MySystem" -version "1.0.0" -customer "Contoso" -path ".\contoso-system.json"
```

---

### Connect-ARAFile

Loads an existing ARA JSON file and deserializes it into in-memory PowerShell class objects. Sets `$global:ARAFile` and `$global:path`. Must be called before any `Add-*`, `Set-*`, `Remove-*`, or `Get-*` cmdlets.

#### Syntax

```powershell
Connect-ARAFile
    -path <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `path` | String | Yes | File path to the ARA JSON file to load. |

#### Example

```powershell
Connect-ARAFile -path ".\contoso-system.json"
```

---

### Test-ARAFile

Validates the currently loaded ARA file against its JSON schema. Returns an object with `IsValid` and `Errors` properties.

#### Syntax

```powershell
Test-ARAFile
    [-schemaPath <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `schemaPath` | String | No | Path or URL to the JSON schema. Defaults to the `$schema` value embedded in the ARA file. |

#### Outputs

`PSCustomObject` with:
- `IsValid` — `[bool]`
- `Errors` — `[string[]]`

#### Example

```powershell
$result = Test-ARAFile
if (-not $result.IsValid) {
    $result.Errors
}
```

---

### Get-ARASystem

Retrieves the top-level system metadata from the current ARA session.

#### Syntax

```powershell
Get-ARASystem
```

#### Outputs

`PSCustomObject` with `system`, `version`, `customer`, and `schema` properties.

#### Example

```powershell
Get-ARASystem
```

---

### Set-ARASystem

Updates one or more top-level system metadata fields and saves the ARA file.

#### Syntax

```powershell
Set-ARASystem
    [-system <String>]
    [-version <String>]
    [-customer <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `system` | String | No | Updated system name. |
| `version` | String | No | Updated system version. |
| `customer` | String | No | Updated customer name. |

#### Example

```powershell
Set-ARASystem -system "MySystem" -version "2.0.0" -customer "Contoso"
```

---

### New-ARARole

Returns a new empty `ARARole` object. Use this to manually populate fields before calling `Add-ARARole -role`.

#### Syntax

```powershell
New-ARARole
```

---

### Get-ARARole

Retrieves a specific role by key, or all roles if no key is provided.

#### Syntax

```powershell
Get-ARARole
    [-key <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | No | Unique role key. Omit to return all roles. |

#### Example

```powershell
Get-ARARole -key "admin"
Get-ARARole
```

---

### Add-ARARole

Adds a new role to the ARA file. Throws if the key already exists.

#### Syntax

```powershell
# Object parameter set
Add-ARARole
    -role <ARARole>

# Properties parameter set
Add-ARARole
    -name <String>
    -key <String>
    -group <String>
    -active <Boolean>
    -description <String>
    [-members <String[]>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `role` | ARARole | Yes (Object) | Pre-constructed role object. |
| `name` | String | Yes (Properties) | Display name of the role. |
| `key` | String | Yes (Properties) | Unique key identifier. |
| `group` | String | Yes (Properties) | Group assignment. |
| `active` | Boolean | Yes (Properties) | Whether the role is active. |
| `description` | String | Yes (Properties) | Description of the role. |
| `members` | String[] | No | Array of member identifiers. |

#### Example

```powershell
Add-ARARole -name "Administrator" -key "admin" -group "admins" -active $true -description "System administrator role"
```

---

### Set-ARARole

Updates an existing role. Throws if the key does not exist.

#### Syntax

```powershell
# Object parameter set
Set-ARARole
    -role <ARARole>

# Properties parameter set
Set-ARARole
    -key <String>
    [-name <String>]
    [-group <String>]
    [-active <Boolean>]
    [-description <String>]
    [-members <String[]>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `role` | ARARole | Yes (Object) | Updated role object. |
| `key` | String | Yes (Properties) | Key of the role to update. |
| `name` | String | No | Updated display name. |
| `group` | String | No | Updated group. |
| `active` | Boolean | No | Updated active state. |
| `description` | String | No | Updated description. |
| `members` | String[] | No | Updated member array. |

#### Example

```powershell
Set-ARARole -key "admin" -description "Updated admin role description"
```

---

### Remove-ARARole

Removes a role from the ARA file. Throws if the key does not exist.

#### Syntax

```powershell
Remove-ARARole
    -key <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | Yes | Key of the role to remove. |

#### Example

```powershell
Remove-ARARole -key "admin"
```

---

### New-ARAEnvironment

Returns a new empty `ARAEnvironment` object. Use this to manually populate fields before calling `Add-ARAEnvironment -environment`.

#### Syntax

```powershell
New-ARAEnvironment
```

---

### Get-ARAEnvironment

Retrieves a specific environment by key, or all environments if no key is provided.

#### Syntax

```powershell
Get-ARAEnvironment
    [-key <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | No | Environment key. Omit to return all environments. |

#### Example

```powershell
Get-ARAEnvironment -key "prod"
Get-ARAEnvironment
```

---

### Add-ARAEnvironment

Adds a new environment to the ARA file. Throws if the key already exists.

#### Syntax

```powershell
# Object parameter set
Add-ARAEnvironment
    -environment <ARAEnvironment>

# Properties parameter set
Add-ARAEnvironment
    -key <String>
    [-resourcegroups <ARAResourceGroup[]>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `environment` | ARAEnvironment | Yes (Object) | Pre-constructed environment object. |
| `key` | String | Yes (Properties) | Unique environment key. |
| `resourcegroups` | ARAResourceGroup[] | No | Initial resource groups. |

#### Example

```powershell
Add-ARAEnvironment -key "prod"
Add-ARAEnvironment -key "dev"
```

---

### Set-ARAEnvironment

Updates an existing environment. Throws if the key does not exist.

#### Syntax

```powershell
# Object parameter set
Set-ARAEnvironment
    -environment <ARAEnvironment>

# Properties parameter set
Set-ARAEnvironment
    -key <String>
    -resourcegroups <ARAResourceGroup[]>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `environment` | ARAEnvironment | Yes (Object) | Updated environment object. |
| `key` | String | Yes (Properties) | Key of the environment to update. |
| `resourcegroups` | ARAResourceGroup[] | Yes (Properties) | Updated resource groups. |

#### Example

```powershell
Set-ARAEnvironment -key "prod" -resourcegroups $updatedResourceGroups
```

---

### Remove-ARAEnvironment

Removes an environment from the ARA file. Throws if the key does not exist.

#### Syntax

```powershell
Remove-ARAEnvironment
    -key <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | Yes | Key of the environment to remove. |

#### Example

```powershell
Remove-ARAEnvironment -key "dev"
```

---

### New-ARAResourceGroup

Returns a new empty `ARAResourceGroup` object for manual population.

#### Syntax

```powershell
New-ARAResourceGroup
```

---

### New-ARAResource

Returns a new empty `ARAResource` object for manual population.

#### Syntax

```powershell
New-ARAResource
```

---

### Get-ARAResource

Retrieves resources. All parameters are optional; combine them to narrow results.

#### Syntax

```powershell
Get-ARAResource
    [-environment <String>]
    [-resourceGroup <String>]
    [-type <String>]
    [-name <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `environment` | String | No | Filter by environment key. |
| `resourceGroup` | String | No | Filter by resource group name. |
| `type` | String | No | Filter by resource type. |
| `name` | String | No | Filter by resource name. |

#### Example

```powershell
Get-ARAResource -environment "prod" -resourceGroup "web-rg" -type "Microsoft.Compute/virtualMachines" -name "web-01"
Get-ARAResource
```

---

### Add-ARAResource

Adds a new resource to a resource group. Throws if the resource already exists.

#### Syntax

```powershell
# Object parameter set
Add-ARAResource
    -resource <ARAResource>

# Properties parameter set
Add-ARAResource
    -environment <String>
    -resourceGroup <String>
    -type <String>
    -name <String>
    -description <String>
    -active <Boolean>
    [-iacModule <ARAIacModule>]
    [-linkedResources <ARALinkedResource[]>]
    [-friendlyName <String>]
    [-roles <ARAResourceRole[]>]
    [-software <ARAResourceSoftware[]>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resource` | ARAResource | Yes (Object) | Pre-constructed resource object. |
| `environment` | String | Yes (Properties) | Environment key. |
| `resourceGroup` | String | Yes (Properties) | Resource group name. |
| `type` | String | Yes (Properties) | Resource type (e.g., `Microsoft.Compute/virtualMachines`). |
| `name` | String | Yes (Properties) | Resource name unique within the resource group. |
| `description` | String | Yes (Properties) | Resource description. |
| `active` | Boolean | Yes (Properties) | Whether the resource is active. |
| `iacModule` | ARAIacModule | No | IaC module reference. |
| `linkedResources` | ARALinkedResource[] | No | Related resource links. |
| `friendlyName` | String | No | Human-readable display name. |
| `roles` | ARAResourceRole[] | No | Role assignments. |
| `software` | ARAResourceSoftware[] | No | Deployed software. |

#### Example

```powershell
Add-ARAResource -environment "prod" -resourceGroup "web-rg" `
    -type "Microsoft.Compute/virtualMachines" -name "web-01" `
    -description "Primary web server" -active $true
```

---

### Set-ARAResource

Updates an existing resource. Throws if the resource does not exist.

#### Syntax

```powershell
# Object parameter set
Set-ARAResource
    -resource <ARAResource>

# Properties parameter set
Set-ARAResource
    -environment <String>
    -resourceGroup <String>
    -type <String>
    -name <String>
    [-description <String>]
    [-active <Boolean>]
    [-iacModule <ARAIacModule>]
    [-linkedResources <ARALinkedResource[]>]
    [-friendlyName <String>]
    [-roles <ARAResourceRole[]>]
    [-software <ARAResourceSoftware[]>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resource` | ARAResource | Yes (Object) | Updated resource object. |
| `environment` | String | Yes (Properties) | Environment key. |
| `resourceGroup` | String | Yes (Properties) | Resource group name. |
| `type` | String | Yes (Properties) | Resource type identifier. |
| `name` | String | Yes (Properties) | Resource name. |
| `description` | String | No | Updated description. |
| `active` | Boolean | No | Updated active state. |
| `iacModule` | ARAIacModule | No | Updated IaC module. |
| `linkedResources` | ARALinkedResource[] | No | Updated linked resources. |
| `friendlyName` | String | No | Updated display name. |
| `roles` | ARAResourceRole[] | No | Updated role assignments. |
| `software` | ARAResourceSoftware[] | No | Updated software. |

#### Example

```powershell
Set-ARAResource -environment "prod" -resourceGroup "web-rg" `
    -type "Microsoft.Compute/virtualMachines" -name "web-01" `
    -description "Updated description" -active $false
```

---

### Remove-ARAResource

Removes a resource from a resource group. Throws if the resource does not exist.

#### Syntax

```powershell
Remove-ARAResource
    -environmentKey <String>
    -resourceGroupName <String>
    -type <String>
    -name <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `environmentKey` | String | Yes | Environment key. |
| `resourceGroupName` | String | Yes | Resource group name. |
| `type` | String | Yes | Resource type identifier. |
| `name` | String | Yes | Resource name. |

#### Example

```powershell
Remove-ARAResource -environmentKey "prod" -resourceGroupName "web-rg" `
    -type "Microsoft.Compute/virtualMachines" -name "web-01"
```

---

### New-ARALinkedResource

Returns a new empty `ARALinkedResource` object for manual population before calling `Add-ARALinkedResource -linkedResource`.

#### Syntax

```powershell
New-ARALinkedResource
```

#### Outputs

`[ARALinkedResource]`

#### Example

```powershell
$link = New-ARALinkedResource
$link.resource    = $childResource
$link.linkType    = "depends-on"
$link.active      = $true
Add-ARALinkedResource -parentResource $parentResource -linkedResource $link
```

---

### Add-ARALinkedResource

Adds a directional relationship link from a parent resource to a child resource. Throws if the link already exists.

#### Syntax

```powershell
# Object parameter set
Add-ARALinkedResource
    -linkedResource <ARALinkedResource>
    -parentResource <ARAResource>

# Properties parameter set
Add-ARALinkedResource
    -parentResource <ARAResource>
    -childResource <ARAResource>
    -linkType <String>
    -active <Boolean>
    [-description <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `linkedResource` | ARALinkedResource | Yes (Object) | Pre-constructed linked resource object. |
| `parentResource` | ARAResource | Yes | The source resource. |
| `childResource` | ARAResource | Yes (Properties) | The target resource. |
| `linkType` | String | Yes (Properties) | Relationship type (e.g., `depends-on`). |
| `active` | Boolean | Yes (Properties) | Whether the link is active. |
| `description` | String | No | Optional description of the relationship. |

#### Example

```powershell
$parent = Get-ARAResource -environment "prod" -resourceGroup "web-rg" -type "Microsoft.Compute/virtualMachines" -name "web-01"
$child  = Get-ARAResource -environment "prod" -resourceGroup "data-rg" -type "Microsoft.Sql/servers" -name "sql-01"
Add-ARALinkedResource -parentResource $parent -childResource $child -linkType "depends-on" -active $true
```

---

### Set-ARALinkedResource

Updates an existing relationship link. Throws if the link does not exist.

#### Syntax

```powershell
# Object parameter set
Set-ARALinkedResource
    -linkedResource <ARALinkedResource>
    -parentResource <ARAResource>

# Properties parameter set
Set-ARALinkedResource
    -parentResource <ARAResource>
    -childResource <ARAResource>
    -linkType <String>
    [-description <String>]
    [-active <Boolean>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `linkedResource` | ARALinkedResource | Yes (Object) | Updated linked resource object. |
| `parentResource` | ARAResource | Yes | The source resource. |
| `childResource` | ARAResource | Yes (Properties) | The target resource. |
| `linkType` | String | Yes (Properties) | Relationship type used to identify the link. |
| `description` | String | No | Updated relationship description. |
| `active` | Boolean | No | Updated active state. |

#### Example

```powershell
Set-ARALinkedResource -parentResource $parent -childResource $child -linkType "depends-on" -active $false
```

---

### Remove-ARALinkedResource

Removes a relationship link from a parent resource. Throws if the link does not exist.

#### Syntax

```powershell
Remove-ARALinkedResource
    -parentResource <ARAResource>
    -childResource <ARAResource>
    -linkType <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `parentResource` | ARAResource | Yes | The source resource. |
| `childResource` | ARAResource | Yes | The target resource. |
| `linkType` | String | Yes | Relationship type identifying the link to remove. |

#### Example

```powershell
Remove-ARALinkedResource -parentResource $parent -childResource $child -linkType "depends-on"
```

---

### New-ARAResourceType

Returns a new empty `ARAResourceType` object for manual population.

#### Syntax

```powershell
New-ARAResourceType
```

---

### Get-ARAResourceType

Retrieves a specific resource type by key, or all resource types if no key is provided.

#### Syntax

```powershell
Get-ARAResourceType
    [-key <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | No | Resource type key. Omit to return all resource types. |

#### Example

```powershell
Get-ARAResourceType -key "vm"
Get-ARAResourceType
```

---

### Add-ARAResourceType

Adds a new resource type to the ARA file. Throws if the key already exists.

#### Syntax

```powershell
# Object parameter set
Add-ARAResourceType
    -resourceType <ARAResourceType>

# Properties parameter set
Add-ARAResourceType
    -key <String>
    -friendlyName <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resourceType` | ARAResourceType | Yes (Object) | Pre-constructed resource type object. |
| `key` | String | Yes (Properties) | Unique resource type key. |
| `friendlyName` | String | Yes (Properties) | Human-readable name. |

#### Example

```powershell
Add-ARAResourceType -key "vm" -friendlyName "Virtual Machine"
```

---

### Set-ARAResourceType

Updates an existing resource type. Throws if the key does not exist.

#### Syntax

```powershell
# Object parameter set
Set-ARAResourceType
    -resourceType <ARAResourceType>

# Properties parameter set
Set-ARAResourceType
    -key <String>
    -friendlyName <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resourceType` | ARAResourceType | Yes (Object) | Updated resource type object. |
| `key` | String | Yes (Properties) | Key of the resource type to update. |
| `friendlyName` | String | Yes (Properties) | Updated human-readable name. |

#### Example

```powershell
Set-ARAResourceType -key "vm" -friendlyName "Azure Virtual Machine"
```

---

### Remove-ARAResourceType

Removes a resource type from the ARA file. Throws if the key does not exist.

#### Syntax

```powershell
Remove-ARAResourceType
    -key <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | Yes | Key of the resource type to remove. |

#### Example

```powershell
Remove-ARAResourceType -key "vm"
```

---

### Get-ARASoftware

Retrieves a specific software component by name and version, or all software if no filter is provided.

#### Syntax

```powershell
Get-ARASoftware
    [-name <String>]
    [-version <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `name` | String | No | Software name. Must be combined with `version` to retrieve a specific entry. |
| `version` | String | No | Software version. Must be combined with `name` to retrieve a specific entry. |

#### Example

```powershell
Get-ARASoftware -name "Windows Server" -version "2022"
Get-ARASoftware
```

---

### Add-ARASoftware

Adds a new software component to the ARA file. Throws if the name/version combination already exists.

#### Syntax

```powershell
# Object parameter set
Add-ARASoftware
    -software <ARASoftware>

# Properties parameter set
Add-ARASoftware
    -name <String>
    -version <String>
    -description <String>
    [-type <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `software` | ARASoftware | Yes (Object) | Pre-constructed software object. |
| `name` | String | Yes (Properties) | Software name. |
| `version` | String | Yes (Properties) | Software version. |
| `description` | String | Yes (Properties) | Software description. |
| `type` | String | No | Software type classification (e.g., `OS`, `Application`). |

#### Example

```powershell
Add-ARASoftware -name "Windows Server" -version "2022" -description "Server OS" -type "OS"
```

---

### Set-ARASoftware

Updates an existing software component. Throws if the name/version combination does not exist.

#### Syntax

```powershell
# Object parameter set
Set-ARASoftware
    -software <ARASoftware>

# Properties parameter set
Set-ARASoftware
    -name <String>
    -version <String>
    [-description <String>]
    [-type <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `software` | ARASoftware | Yes (Object) | Updated software object. |
| `name` | String | Yes (Properties) | Software name. |
| `version` | String | Yes (Properties) | Software version. |
| `description` | String | No | Updated description. |
| `type` | String | No | Updated type classification. |

#### Example

```powershell
Set-ARASoftware -name "Windows Server" -version "2022" -description "Updated OS description"
```

---

### Remove-ARASoftware

Removes a software component from the ARA file. Throws if the name/version combination does not exist.

#### Syntax

```powershell
Remove-ARASoftware
    -name <String>
    -version <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `name` | String | Yes | Software name. |
| `version` | String | Yes | Software version. |

#### Example

```powershell
Remove-ARASoftware -name "Windows Server" -version "2022"
```

---

### New-ARASTIG

Returns a new empty `ARAStig` object for manual population before calling `Add-ARASTIG -stigObject`.

#### Syntax

```powershell
New-ARASTIG
```

#### Outputs

`[ARAStig]`

#### Example

```powershell
$stig = New-ARASTIG
$stig.resourceType = Get-ARAResourceType -key "vm"
$stig.stig         = "V-93369"
$stig.applier      = Get-ARARole -key "admin"
Add-ARASTIG -stigObject $stig
```

---

### Get-ARASTIG

Retrieves a specific STIG requirement by resource type key, or all STIGs if no key is provided.

#### Syntax

```powershell
Get-ARASTIG
    [-resourceTypeKey <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resourceTypeKey` | String | No | Resource type key. Omit to return all STIGs. |

#### Example

```powershell
Get-ARASTIG -resourceTypeKey "vm"
Get-ARASTIG
```

---

### Add-ARASTIG

Adds a new STIG requirement to the ARA file. Throws if a STIG for the resource type already exists.

#### Syntax

```powershell
# Object parameter set
Add-ARASTIG
    -stigObject <ARAStig>

# Properties parameter set
Add-ARASTIG
    -resourceType <String | ARAResourceType>
    -stig <String>
    -applier <String | ARARole>
    [-description <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `stigObject` | ARAStig | Yes (Object) | Pre-constructed STIG object. |
| `resourceType` | String or ARAResourceType | Yes (Properties) | Resource type key or object. |
| `stig` | String | Yes (Properties) | STIG identifier. |
| `applier` | String or ARARole | Yes (Properties) | Role key or object responsible for applying the STIG. |
| `description` | String | No | STIG description. |

#### Example

```powershell
Add-ARASTIG -resourceType "vm" -stig "V-93369" -description "OS Hardening" -applier "admin"
```

---

### Set-ARASTIG

Updates an existing STIG requirement. Throws if the STIG does not exist.

#### Syntax

```powershell
# Object parameter set
Set-ARASTIG
    -stigObject <ARAStig>
    -resourceType <String | ARAResourceType>

# Properties parameter set
Set-ARASTIG
    -resourceType <String | ARAResourceType>
    [-stig <String>]
    [-description <String>]
    [-applier <String | ARARole>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `stigObject` | ARAStig | Yes (Object) | Updated STIG object. |
| `resourceType` | String or ARAResourceType | Yes | Resource type key or object identifying the STIG to update. |
| `stig` | String | No | Updated STIG identifier. |
| `description` | String | No | Updated description. |
| `applier` | String or ARARole | No | Updated applier role. |

#### Example

```powershell
Set-ARASTIG -resourceType "vm" -description "Updated OS hardening requirement" -applier "secops"
```

---

### Remove-ARASTIG

Removes a STIG requirement from the ARA file. Throws if the STIG does not exist.

#### Syntax

```powershell
Remove-ARASTIG
    -resourceTypeKey <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `resourceTypeKey` | String | Yes | Resource type key identifying the STIG to remove. |

#### Example

```powershell
Remove-ARASTIG -resourceTypeKey "vm"
```

---

### New-ARAConfigurationString

Returns a new empty `ARAConfigurationString` object for manual population.

#### Syntax

```powershell
New-ARAConfigurationString
```

---

### Get-ARAConfigurationString

Retrieves a specific configuration string by key, or all configuration strings if no key is provided.

#### Syntax

```powershell
Get-ARAConfigurationString
    [-key <String>]
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | No | Configuration key. Omit to return all configuration strings. |

#### Example

```powershell
Get-ARAConfigurationString -key "tenant"
Get-ARAConfigurationString
```

---

### Add-ARAConfigurationString

Adds a new configuration key-value pair to the ARA file. Throws if the key already exists.

#### Syntax

```powershell
# Object parameter set
Add-ARAConfigurationString
    -configStringObject <ARAConfigurationString>

# Properties parameter set
Add-ARAConfigurationString
    -key <String>
    -value <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `configStringObject` | ARAConfigurationString | Yes (Object) | Pre-constructed configuration string object. |
| `key` | String | Yes (Properties) | Configuration key. |
| `value` | String | Yes (Properties) | Configuration value. |

#### Example

```powershell
Add-ARAConfigurationString -key "tenant" -value "contoso.onmicrosoft.com"
```

---

### Set-ARAConfigurationString

Updates the value of an existing configuration string. Throws if the key does not exist.

#### Syntax

```powershell
Set-ARAConfigurationString
    -key <String>
    -value <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | Yes | Configuration key to update. |
| `value` | String | Yes | New configuration value. |

#### Example

```powershell
Set-ARAConfigurationString -key "tenant" -value "fabrikam.onmicrosoft.com"
```

---

### Remove-ARAConfigurationString

Removes a configuration string from the ARA file. Throws if the key does not exist.

#### Syntax

```powershell
Remove-ARAConfigurationString
    -key <String>
```

#### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `key` | String | Yes | Configuration key to remove. |

#### Example

```powershell
Remove-ARAConfigurationString -key "tenant"
```
