---
title: New-CMGlobalConditionFile
titleSuffix: Configuration Manager
description: Creates a File System type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# New-CMGlobalConditionFile

## SYNOPSIS

Creates a File System type global condition in Configuration Manager.

## SYNTAX

### NewFileSystem (Default)

```powershell
New-CMGlobalConditionFile [-IsFolder] -Path <String> -FileOrFolderName <String> [-IncludeSubfolder <Boolean>]
 [-Is64Bit <Boolean>] -Name <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling]
```

### NewFileSystemFile

```powershell
New-CMGlobalConditionFile -FilePath <String> [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

The **New-CMGlobalConditionFile** cmdlet creates a File System type global condition in Microsoft System Center Configuration Manager.

A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

## EXAMPLES

### Example 1

```powershell
$GlobalFloder = New-CMGlobalConditionFile -Path c:\ -FileOrFolderName test -IsFolder $true -Name Folder 
```

This command creates a File System type folder global condition in Configuration Manager.

### Example 1

```powershell
$GlobalFile = New-CMGlobalConditionFile -FilePath c:\test  -Name file
```

This command creates a File System type file global condition in Configuration Manager.

## PARAMETERS

### -Description

Specifies a description.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -FileOrFolderName

Specifies the name of the file or folder object that will be searched for. You can specify system environment variables and the %USERPROFILE% environment variable in the file or folder name. You can also use the * and ? wildcards in the file name.

```yaml
Type: String
Parameter Sets: NewFileSystem
Aliases: FileName, FolderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath

Specifies the path to the specified file on client computers. You can specify system environment variables and the %USERPROFILE% environment variable in the path.

```yaml
Type: String
Parameter Sets: NewFileSystemFile
Aliases:

Required: True
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

### -IncludeSubfolder

Enable this option if you also want to search any sub-folders under the specified path.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: IncludeSubfolders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Is64Bit

Indicates whether the 64-bit system file location (%windir%\system32) should be searched in addition to the 32-bit system file location (%windir%\syswow64) on Configuration Manager clients that run a 64-bit version of Windows.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsFolder

Indicate whether it is a folder.

```yaml
Type: SwitchParameter
Parameter Sets: NewFileSystem
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies a name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path

Specifies the path to the specified  folder on client computers. You can specify system environment variables and the %USERPROFILE% environment variable in the path.

```yaml
Type: String
Parameter Sets: NewFileSystem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## OUTPUTS

### System.Object

## RELATED LINKS

- [Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)
- [New-CMGlobalCondition](./New-CMGlobalCondition.md)
- [New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)
- [New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)
- [New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)
- [New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)
- [New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)
- [New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)
- [New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)
- [New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)
- [New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)
- [New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)

