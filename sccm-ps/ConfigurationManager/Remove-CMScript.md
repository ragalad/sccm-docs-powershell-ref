﻿---
title: Remove-CMScript
titleSuffix: Configuration Manager
description: Removes Configuration Manager Powershell scripts.
ms.date: 11/15/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Remove-CMScript

## SYNOPSIS

Removes Configuration Manager Powershell scripts.

## SYNTAX

### SearchByValueMandatory (Default)

```powershell
Remove-CMScript [-Force] -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm]
```

### SearchByNameMandatory

```powershell
Remove-CMScript [-Force] -ScriptName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm]
```

## DESCRIPTION

The **Remove-CMScript** cmdlet removes one or more Microsoft System Center Configuration Manager scripts. System Center Configuration Manager has an integrated ability to run Powershell scripts. The scripts simplify building custom tools to administer software and let you accomplish mundane tasks quickly, allowing you to get large jobs done more easily and more consistently.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove a script by using the script name

```powershell
PS XYZ:\> Remove-CMScript -ScriptName "getUsers"
```

This command removes a script that has the name getUesrs.

## PARAMETERS

### -DisableWildcardHandling

DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies a **CMScript** object.
To obtain a **CMScript** object, use [Get-CMScript](Get-CMScript.md).

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Script

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ScriptName

Specifies a script name.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## RELATED LINKS

[Approve-CMScript](Approve-CMScript.md)

[Deny-CMScript](Deny-CMScript.md)

[Get-CMScript](Invoke-CMScript.md)

[Invoke-CMScript](Invoke-CMScript.md)

[Set-CMScriptDeploymentType](Set-CMScriptDeploymentType.md)

[Add-CMScriptDeploymentType](Add-CMScriptDeploymentType.md)
