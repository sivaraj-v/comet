---
title: Get started with Azure CLI 2.0
description: Get started with Azure CLI 2.0 on Linux, Mac, or Windows.
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 85c418a8-6177-4833-bb8d-ff4ce2233c1a
brand: azure
---

# Tabbed Conceptual

The Azure CLI 2.0 is Azure's new command line experience for managing Azure resources.
It can be used on macOS, Linux, and Windows. 

Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line,
and for building automation scripts that work against the Azure Resource Manager.
This article helps get you started using it, and teaches you the core concepts behind it.

For information about the latest release, see the [release notes](release-notes-azure-cli.md).

## Install Azure CLI

The first step is to make sure you have the latest version of the Azure CLI installed:

# [Linux](#tab/linux)

On Linux, first, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group together.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.

# [Windows](#tab/windows)

On Windows, first, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group together.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.

---

First, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group together.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.

# [Bash](#tab/bash/linux)

Bash on Linux

``` azure-cli
az group create -n MyResourceGroup -l westus2
```

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

# [Bash](#tab/bash/windows)

Bash on Windows

```azure-cli
az group create -n MyResourceGroup -l westus2
```

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

# [PowerShell](#tab/powershell/linux)

PowerShell on Linux

```azure-cli
az group create -n MyResourceGroup -l westus2
```

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

# [PowerShell](#tab/powershell/windows)

PowerShell on Windows

```azure-cli
az group create -n MyResourceGroup -l westus2
```

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

# [Azure Portal](#tab/azure-portal)

Azure Portal

lorem ipsum bla bla bla

---

First, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group together.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.

# [Linux](#tab/linux)

On Linux, first, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group together.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.

# [Windows](#tab/windows)

On Windows, first, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group together.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.

---

First, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group together.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.

# [Bash](#tab/bash/linux)

Bash on Linux

``` azure-cli
az group create -n MyResourceGroup -l westus2
```

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

# [Bash](#tab/bash/windows)

Bash on Windows

```azure-cli
az group create -n MyResourceGroup -l westus2
```

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

# [PowerShell](#tab/powershell/linux)

PowerShell on Linux

```azure-cli
az group create -n MyResourceGroup -l westus2
```

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

# [PowerShell](#tab/powershell/windows)

PowerShell on Windows

```azure-cli
az group create -n MyResourceGroup -l westus2
```

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

# [Azure Portal](#tab/azure-portal)

Azure Portal

lorem ipsum bla bla bla

---

First, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group together.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.