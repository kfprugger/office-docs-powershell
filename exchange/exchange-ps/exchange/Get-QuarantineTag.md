---
external help file: Microsoft.Exchange.TransportMailflow-Help.xml
online version: https://docs.microsoft.com/powershell/module/exchange/get-quarantinetag
applicable: Exchange Online, Exchange Online Protection
title: Get-QuarantineTag
schema: 2.0.0
author: chrisda
ms.author: chrisda
ms.reviewer:
---

# Get-QuarantineTag

## SYNOPSIS
This cmdlet is available only in the cloud-based service.

Use the Get-QuarantineTag cmdlet to view quarantine tags in your cloud-based organization.

**Note**: We recommend that you use the Exchange Online PowerShell V2 module to connect to Exchange Online PowerShell. For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell).

For information about the parameter sets in the Syntax section below, see [Exchange cmdlet syntax](https://docs.microsoft.com/powershell/exchange/exchange-cmdlet-syntax).

## SYNTAX

```
Get-QuarantineTag [[-Identity] <QuarantineTagIdParameter>]
 [-QuarantineTagType <QuarantineTagTypeEnum>]
 [<CommonParameters>]
```

## DESCRIPTION
Quarantine tags allow you to configure the allowed end-user actions on quarantined messages in supported features that quarantine messages.

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see [Find the permissions required to run any Exchange cmdlet](https://docs.microsoft.com/powershell/exchange/find-exchange-cmdlet-permissions).

## EXAMPLES

### Example 1
```powershell
Get-QuarantineTag | Format-Table Name
```

This example returns as summary list of all quarantine tags.

### Example 2
```powershell
Get-QuarantineTag -Identity NoAccess
```

This example returns detailed information about the quarantine tag named NoAccess.

### Example 3
```powershell
Get-QuarantineTag -QuarantineTagType GlobalQuarantineTag
```

This example returns detailed information about the default quarantine tag named GlobalDefaultTag that controls the global end-user spam notification settings.

## PARAMETERS

### -Identity
The Identity parameter specifies the quarantine tag you want to view. You can use any value that uniquely identifies the quarantine tag. For example:

- Name
- Distinguished name (DN)
- GUID

```yaml
Type: QuarantineTagIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Online, Exchange Online Protection

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -QuarantineTagType
The QuarantineTagType parameter filters the results by the specified quarantine tag type. Valid values are:

- PolicyQuarantineTag: This is the default value, and returns built-in and custom quarantine tags.
- GlobalQuarantineTag: This value is required to return the global settings (end-user quarantine notification settings) in the quarantine tag named GlobalDefaultTag.

```yaml
Type: QuarantineTagTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: PolicyQuarantineTag, GlobalQuarantineTag
Applicable: Exchange Online, Exchange Online Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  

## OUTPUTS

###  

## NOTES

## RELATED LINKS