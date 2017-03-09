---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-AzureRmServiceBusTopicKey

## SYNOPSIS
Regenerates the primary or secondary connection strings for the Service Bus topic.

## SYNTAX

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> [-NamespaceName] <String> [-TopicName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-AzureRmServiceBusTopicKey** cmdlet generates a primary or secondary connection string for the specified Service Bus topic and authorization rule.

## EXAMPLES

### Example 1: Regenerate the primary connection string for a namespace
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup "Default-ServiceBus-WestUS" -NamespaceName "SB-Example1" -TopicName "SB-Topic_example1" -AuthorizationRuleName "SBTopicAuthoRule1" -RegenerateKeys "PrimaryKey"
```

This command regenerates the primary connection string for the namespace named SB-Example1.

### Example 2: Regenerate the secondary connection string for a namespace
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup "Default-ServiceBus-WestUS" -NamespaceName "SB-Example1" -TopicName "SB-Topic_example1" -AuthorizationRuleName S"BTopicAuthoRule1" -RegenerateKeys "SecondaryKey"
```

This command regenerates the secondary connection string for the namespace named SB-Example1.

## PARAMETERS

### -AuthorizationRuleName
Specifies the name of the authorization rule.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
Specifies the name of the Service Bus namespace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RegenerateKeys
Specifies whether to regenerate the primary or secondary keys.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Specifies the name of the resource group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
Specifies the name of the Service Bus topic.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### -ResourceGroup
 System.String
 

### -NamespaceName
 System.String
 

### -AuthorizationRuleName
 System.String
 

### -TopicName
 System.String
 

### -RegenerateKeys
 System.String

## OUTPUTS

### Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes
PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi
                            c_exampl1
SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi
                            c_exampl1
PrimaryKey                : {PrimaryKey value}
SecondaryKey              : {SecondaryKey value}
KeyName                   : SBTopicAuthoRule1

## NOTES

## RELATED LINKS

[Get-AzureRmServiceBusTopicKey](./Get-AzureRmServiceBusTopicKey.md)