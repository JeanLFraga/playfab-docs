---
author: jdeweyMSFT
title: "PartyDisconnectChatControlCompletedStateChange"
description: "Information specific to the *DisconnectChatControlCompleted* type of state change."
ms.author: jdewey
ms.topic: reference
ms.prod: playfab
ms.date: 03/11/2022
---

# PartyDisconnectChatControlCompletedStateChange  

Information specific to the *DisconnectChatControlCompleted* type of state change.  

## Syntax  
  
```cpp
struct PartyDisconnectChatControlCompletedStateChange {  
    PartyStateChangeResult result;  
    PartyError errorDetail;  
    PartyNetwork* network;  
    PartyLocalChatControl* localChatControl;  
    void* asyncIdentifier;  
}  
```
  
### Members  
  
**`result`** &nbsp; [PartyStateChangeResult](../enums/partystatechangeresult.md)  
  
Indicates that the operation Succeeded or the reason that it failed.
  
**`errorDetail`** &nbsp; PartyError  
  
A diagnostic value providing additional troubleshooting information regarding any potential error condition.
  
The human-readable form of this error detail can be retrieved via [PartyManager::GetErrorMessage()](../classes/PartyManager/methods/partymanager_geterrormessage.md).
  
**`network`** &nbsp; [PartyNetwork](../classes/PartyNetwork/partynetwork.md)*  
  
The network used in the call associated with this state change.
  
**`localChatControl`** &nbsp; [PartyLocalChatControl](../classes/PartyLocalChatControl/partylocalchatcontrol.md)*  
  
The chat control provided to the call associated with this state change.
  
**`asyncIdentifier`** &nbsp; void*  
  
The async identifier provided to the call associated with this state change.
  
  
## Requirements  
  
**Header:** Party.h
  
## See also  
[Party members](../party_members.md)  
[PartyNetwork::DisconnectChatControl](../classes/PartyNetwork/methods/partynetwork_disconnectchatcontrol.md)
  
  
