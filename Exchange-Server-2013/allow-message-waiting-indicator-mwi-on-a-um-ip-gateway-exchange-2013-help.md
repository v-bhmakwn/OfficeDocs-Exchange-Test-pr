﻿---
title: 'Allow Message Waiting Indicator (MWI) on a UM IP gateway: Exchange 2013 Help'
TOCTitle: Allow Message Waiting Indicator (MWI) on a UM IP gateway
ms:assetid: 5667e37c-48c6-4659-9dc9-94b1dd8ba232
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dd297995(v=EXCHG.150)
ms:contentKeyID: 49315421
ms.date: 12/10/2017
mtps_version: v=EXCHG.150
---

# Allow Message Waiting Indicator (MWI) on a UM IP gateway

 

_**Applies to:** Exchange Online, Exchange Server 2013, Exchange Server 2016_


You can allow or prevent voice mail notifications to users for calls received by a Unified Messaging (UM) IP gateway. If you enable this setting, the UM IP gateway can receive and send SIP NOTIFY messages for users. Message Waiting Indicator (MWI) is enabled by default and allows message waiting notifications to be sent to users, but you can turn it off depending on your needs.

A message waiting indicator notifies a user about a new or unheard voice message. It appears in the Inbox in clients such as Outlook and Outlook Web App. It can also be a text (SMS) message sent to a registered mobile phone, an outgoing call made from an Exchange server to a number that's been configured for playing new messages, or a lighted lamp on a user's desktop phone.


> [!TIP]
> MWI notifications can also be enabled and disabled on a UM mailbox policy for a group of users.



For additional management tasks related to UM IP gateways, see [UM IP gateway procedures](um-ip-gateway-procedures-exchange-2013-help.md).

## What do you need to know before you begin?

  - Estimated time to complete: Less than 1 minute.

  - You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "UM IP gateways" entry in the [Unified Messaging permissions](unified-messaging-permissions-exchange-2013-help.md) topic.

  - Before you perform these procedures, confirm that a UM dial plan has been created. For detailed steps, see [Create a UM dial plan](create-a-um-dial-plan-exchange-2013-help.md).

  - Before you perform these procedures, confirm that a UM IP gateway has been created. For detailed steps, see [Create a UM IP gateway](create-a-um-ip-gateway-exchange-2013-help.md).

  - For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts in the Exchange admin center](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md).


> [!TIP]
> Having problems? Ask for help in the Exchange forums. Visit the forums at <A href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</A>, <A href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</A>, or <A href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</A>..



## What do you want to do?

## Use the EAC to allow Message Waiting Indicator

1.  In the EAC, navigate to **Unified Messaging** \> **UM IP Gateways**, select the UM IP gateway you want to change, and then click **Edit** ![Edit icon](images/JJ218640.6f53ccb2-1f13-4c02-bea0-30690e6ea71d(EXCHG.150).gif "Edit icon").

2.  On the **UM IP Gateway** page, select the check box next to **Allow message waiting indicator**.

3.  Click **Save**.

## Use the Shell to allow Message Waiting Indicator

This example allows the message waiting indicator to appear for users who are associated with the UM IP gateway named `MyUMIPGateway` with an IP address of 10.10.10.1.

    Set-UMIPGateway -Identity MyUMIPGateway -Address 10.10.10.1 -MessageWaitingIndicatorAllowed $true

