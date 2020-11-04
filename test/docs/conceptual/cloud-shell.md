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
feedback_system: None
---

# Get started with the Cloud Shell

The Azure CLI 2.0 is Azure's new command line experience for managing Azure resources.

## Create a Resource Group Using Azure CLI

Now that we've got everything set up, let's use the Azure CLI to create resources within Azure.

First, create a Resource Group.  Resource Groups in Azure provide a way to manage multiple resources that you 
want to logically group.  For example, you might create a Resource Group for an application or project
and add a virtual machine, a database and a CDN service within it.

Let's create a resource group named "MyResourceGroup" in the *westus2* region of Azure.  To do so type the following command:

```azurecli-interactive
az group create -n MyResourceGroup -l westus2 
```

Once the resource group has been created, the `az group create` command outputs several properties of the newly created resource:

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

## Create a resource group using Azure PowerShell

Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.

First, create a Resource Group. Resource Groups in Azure provide a way to manage multiple resources
that you want to logically group together. For example, you might create a Resource Group for an
application or project and add a virtual machine, a database and a CDN service within it.

Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure. To do so
type the following command:

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
