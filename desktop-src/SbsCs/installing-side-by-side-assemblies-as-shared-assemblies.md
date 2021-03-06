---
Description: The following procedure describes how to install side-by-side assemblies as shared assemblies.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Installing Side-by-side Assemblies as Shared Assemblies
ms.topic: article
ms.date: 05/31/2018
---

# Installing Side-by-side Assemblies as Shared Assemblies

The following procedure describes how to install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [shared assemblies](https://docs.microsoft.com/windows/desktop/Msi/shared-assemblies).

**To install a side-by-side assembly as a shared assembly**

1.  Sign and create a catalog for the files in the assembly.

    Files must be signed to install them as side-by-side assemblies. For more information, see [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).

2.  You should install shared side-by-side assemblies as components of a Windows Installer package. This can be the same installation package used to install or update your application. If the shared assembly is shipped as part of multiple applications, you should provide a merge module that can be incorporated into these applications' installation packages and create a catalog for the files in the assembly.

    Windows Installer version 2.0 or later is required to install assemblies. For more information, see the [Windows Installer](https://msdn.microsoft.com/library/Cc185688(v=VS.85).aspx) SDK and the sections under [Installation of Win32 Assemblies](https://msdn.microsoft.com/library/Aa369292(v=VS.85).aspx).

 

 



