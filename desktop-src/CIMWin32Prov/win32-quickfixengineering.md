---
Description: The Win32\_QuickFixEngineering&\#8194;WMI class represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.prod: windows-server-dev
ms.technology:
- cimwin32
- windows-management-instrumentation
ms.tgt_platform: multiple
title: Win32\_QuickFixEngineering class
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Win32\_QuickFixEngineering class

The **Win32\_QuickFixEngineering** [WMI class](https://msdn.microsoft.com/cfe4bcca-692e-45cd-a840-93ebfe4ae267) represents a small system-wide update, commonly referred to as a quick-fix engineering (QFE) update, applied to the current operating system. This class returns only the updates supplied by Component Based Servicing (CBS). These updates are not listed in the registry. Updates supplied by Microsoft Windows Installer (MSI) or the Windows update site ([http://update.microsoft.com](Http://go.microsoft.com/fwlink/p/?linkid=84398)) are not returned by **Win32\_QuickFixEngineering**.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties. Properties and methods are in alphabetic order, not MOF order.

## Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## Members

The **Win32\_QuickFixEngineering** class has these types of members:

-   [Properties](#properties)

### Properties

The **Win32\_QuickFixEngineering** class has these properties.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MaxLen**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) (64), [**DisplayName**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Caption")
</dt> </dl>

A short textual description of the object.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**CIM\_Key**](https://msdn.microsoft.com/63bdbafc-51f3-4714-8b7e-9d5a61cef45e), [**MaxLen**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) (256), [**Propagated**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MappingStrings**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("WMI")
</dt> </dl>

Local name of the computer system. The value for this property comes from the [**CIM\_ComputerSystem**](cim-computersystem.md) class.

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Description")
</dt> </dl>

A textual description of the object.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**FixComments**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MappingStrings**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")
</dt> </dl>

Additional comments that relate to the update.

</dd> <dt>

**HotFixID**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](https://msdn.microsoft.com/838d295f-e812-4e46-99a4-d2714a0ae8dc), [**MaxLen**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) (260), [**MappingStrings**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")
</dt> </dl>

Unique identifier associated with a particular update.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Data type: **datetime**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MappingStrings**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Install Date")
</dt> </dl>

Indicates when the object was installed. Lack of a value does not indicate that the object is not installed.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstalledBy**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MappingStrings**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")
</dt> </dl>

Person who installed the update. If this value is unknown, the property is empty.

</dd> <dt>

**InstalledOn**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MappingStrings**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")
</dt> </dl>

Date that the update was installed. If this value is unknown, the property is empty.

> [!Note]  
> This property may use different formats, depending on when the QuickFix was installed. Most systems use a standard date format, such as "23-10-2013". However, some systems may return a 64-bit hexidecimal value in the Win32 [**FILETIME**](https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1) format.

 

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**DisplayName**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Name")
</dt> </dl>

Label by which the object is known. When subclassed, this property can be overridden to be a key property.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ServicePackInEffect**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**key**](https://msdn.microsoft.com/838d295f-e812-4e46-99a4-d2714a0ae8dc), [**MaxLen**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) (260), [**MappingStrings**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Hotfix")
</dt> </dl>

Service pack in effect when the update was applied. If no service pack has been applied, the property takes on the value SP0. If it cannot be determined what service pack was in effect, this property is **NULL**.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Data type: **string**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MaxLen**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) (10), [**DisplayName**](https://msdn.microsoft.com/671ea769-f68d-4788-96f5-c4f86ab3b00e) ("Status")
</dt> </dl>

String that indicates the current status of the object. Operational and non-operational status can be defined. Operational status can include "OK", "Degraded", and "Pred Fail". "Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).

Non-operational status can include "Error", "Starting", "Stopping", and "Service". "Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work. Not all such work is online, but the managed element is neither "OK" nor in one of the other states.

This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).

Values include the following:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degraded** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Stopping** ("Stopping")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Service** ("Service")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**No Contact** ("No Contact")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> </dl>

## Remarks

The **Win32\_QuickFixEngineering** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).

Because updates are stored in two places, an enumeration of this class can result in duplicates.

A hot fix is a temporary operating system patch produced by the Quick Fix Engineering group at Microsoft. Like service packs, hot fixes represent changes that have been made to a version of Windows after the operating system has been released.

Unlike service packs, hot fixes are not intended for blanket installation on all computers. Instead, they are developed to address very specific problems, often for specific computer configurations.

In addition, hot fixes represent independent installations that do not depend on other released hot fixes. For example, a hypothetical hot fix 4 would not include the bug fixes and functionality included in hot fixes 1, 2, and 3. In most cases, there would also be no requirement that you install hot fixes 1, 2, and 3 before installing hot fix 4. This makes enumeration of individual hot fixes an important administrative task: to know the exact configuration of a computer, you need to know not only which service packs have been installed but also which individual hot fixes have been installed.

The **Win32\_QuickFixEngineering** class enables you to enumerate all the hot fixes that have been installed on a computer

## Examples

The [Get Installed Programs](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) PowerShell example returns a full list of installed programs.

The following VBScript sample enumerates the installed hot fixes on a computer


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Operating System Classes](https://www.bing.com/search?q=Operating+System+Classes)
</dt> <dt>

[WMI Tasks: Operating Systems](https://msdn.microsoft.com/a216ad56-2650-4d93-86e1-449b56019361)
</dt> </dl>

 

 



