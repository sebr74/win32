---
title: INapEnforcementClientConnection GetEnforcerPrivateData method
description: Is used by the enforcer to get private data.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- GetEnforcerPrivateData method NAP
- GetEnforcerPrivateData method NAP , INapEnforcementClientConnection interface
- INapEnforcementClientConnection interface NAP , GetEnforcerPrivateData method
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# INapEnforcementClientConnection::GetEnforcerPrivateData method

> [!Note]  
> The Network Access Protection platform is not available starting with Windows 10

 

The **INapEnforcementClientConnection::GetEnforcerPrivateData** method is used by the enforcer to get private data.

## Syntax


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## Parameters

<dl> <dt>

*privateData* \[out\]
</dt> <dd>

A pointer to a pointer to a [**PrivateData**](/windows/desktop/api/NapTypes/ns-naptypes-tagprivatedata) opaque data blob that only the enforcer can interpret.

</dd> </dl>

## Return value

Other COM-specific error codes also may be returned.



| Return code                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S\_OK** </dt> </dl>           | Operation succeeded.<br/>                                    |
| <dl> <dt>**E\_ACCESSDENIED** </dt> </dl> | Permissions error, access denied.<br/>                       |
| <dl> <dt>**E\_OUTOFMEMORY** </dt> </dl>  | System resource limit, could not perform the operation.<br/> |



 

## Requirements



|                                     |                                                                                                     |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                                      |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## See also

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 




