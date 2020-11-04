---
title: 在 SharePoint 模式下安装第一个 Report Server | Microsoft Docs
ms.custom: ''
ms.date: 10/05/2017
ms.prod: reporting-services
ms.prod_service: reporting-services-sharepoint
ms.service: ''
ms.component: install-windows
ms.reviewer: ''
ms.suite: pro-bi
ms.technology: ''
ms.tgt_pltfrm: ''
ms.topic: article
author: markingmyname
ms.author: maghan
manager: kfile
ms.workload: On Demand
ms.openlocfilehash: 796eed171b40234af4ab00877a5e73121b49368e
ms.sourcegitcommit: 6bd21109abedf64445bdb3478eea5aaa7553fa46
ms.translationtype: MT
bilingual_type: hover over
ms.contentlocale: zh-CN
ms.lasthandoff: 03/20/2018
---
# <a name="install-the-first-report-server-in-sharepoint-mode"></a><span data-ttu-id="604ef-102">在 SharePoint 模式下安装第一个 Report Server</span><span class="sxs-lookup"><span data-stu-id="604ef-102">Install the first Report Server in SharePoint mode</span></span>

  <span data-ttu-id="604ef-104">本主题中的过程将指导你完成以 SharePoint 模式在单服务器上安装 Reporting Services。</span><span class="sxs-lookup"><span data-stu-id="604ef-104">The procedures in this topic guide you through a single server installation of Reporting Services in SharePoint mode.</span></span> <span data-ttu-id="604ef-105">涉及的步骤包括运行 SQL Server 安装向导以及使用 SharePoint 管理中心的配置任务。</span><span class="sxs-lookup"><span data-stu-id="604ef-105">The steps include running the SQL Server installation wizard as well as configuration tasks that use SharePoint Central Administration.</span></span> <span data-ttu-id="604ef-106">本主题还可用于更新现有安装的单独过程，例如创建 Reporting Services 服务应用程序。</span><span class="sxs-lookup"><span data-stu-id="604ef-106">The topic can also be used for individual procedures for updating an existing installation, for example to create a Reporting Services service application.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="604ef-107">自 SQL Server 2016 之后，不再提供 Reporting Services 与 SharePoint 的集成这一功能。</span><span class="sxs-lookup"><span data-stu-id="604ef-107">Reporting Services integration with SharePoint is no longer available after SQL Server 2016.</span></span>
  
 <span data-ttu-id="604ef-108">有关将更多 Reporting Services 服务器添加到现有场的信息，请参阅以下内容：</span><span class="sxs-lookup"><span data-stu-id="604ef-108">For information on adding more Reporting Services servers to an existing farm, see the following:</span></span>  
  
  
 <span data-ttu-id="604ef-111">单服务器安装对于开发和测试方案很有用，但不建议用于生产环境。</span><span class="sxs-lookup"><span data-stu-id="604ef-111">A single server installation is useful for development and testing scenarios but it is not recommended for production environments.</span></span>  
  
##  <a name="bkmk_singleserver"></a> <span data-ttu-id="604ef-112">单服务器部署示例</span><span class="sxs-lookup"><span data-stu-id="604ef-112">Example single-server deployment</span></span>

 <span data-ttu-id="604ef-113">单服务器安装对于开发和测试方案很有用，但不建议将单服务器用于生产环境。</span><span class="sxs-lookup"><span data-stu-id="604ef-113">A single-server installation is useful for development and testing scenarios but a single-server is not recommended for a production environment.</span></span> <span data-ttu-id="604ef-114">单服务器环境是指 SharePoint 和 Reporting Services 组件安装在同一台计算机上的一台计算机。</span><span class="sxs-lookup"><span data-stu-id="604ef-114">The single-server environment refers to a single computer that has SharePoint and Reporting Services components installed on the same computer.</span></span> <span data-ttu-id="604ef-115">本主题不涉及具有多个 Reporting Services 服务器的扩展环境。</span><span class="sxs-lookup"><span data-stu-id="604ef-115">The topic does not cover scale-out with multiple Reporting Services servers.</span></span>  
  
 <span data-ttu-id="604ef-116">以下关系图阐明了属于单服务器 Reporting Services 部署的一部分的组件。</span><span class="sxs-lookup"><span data-stu-id="604ef-116">The following diagram illustrates the components that are part of a single server Reporting Services deployment.</span></span>  
   
##  <a name="bkmk_setupaccounts"></a> <span data-ttu-id="604ef-133">安装帐户</span><span class="sxs-lookup"><span data-stu-id="604ef-133">Setup accounts</span></span>

 <span data-ttu-id="604ef-134">本部分介绍在 SharePoint 模式下用于主要 Reporting Services 部署步骤的帐户和权限。</span><span class="sxs-lookup"><span data-stu-id="604ef-134">This section describes the accounts and permissions used for the primary deployment steps of Reporting Services in SharePoint mode.</span></span>  
  
 <span data-ttu-id="604ef-135">**安装并注册 Reporting Services 服务：**</span><span class="sxs-lookup"><span data-stu-id="604ef-135">**Installation and registering the Reporting Services Service:**</span></span>  
  
##  <a name="bkmk_install_SSRS"></a> <span data-ttu-id="604ef-146">步骤 1：在 SharePoint 模式下安装 Reporting Services 报表服务器</span><span class="sxs-lookup"><span data-stu-id="604ef-146">Step 1: Install Reporting Services Report Server in SharePoint mode</span></span>

 <span data-ttu-id="604ef-147">此步骤在 SharePoint 模式下安装 Reporting Services 报表服务器以及用于 SharePoint 产品的 Reporting Services 外接程序。</span><span class="sxs-lookup"><span data-stu-id="604ef-147">This step installs a Reporting Services report server in SharePoint mode and the Reporting Services add-in for SharePoint products.</span></span> <span data-ttu-id="604ef-148">根据已在您的计算机上安装的项，您可能不会看到在下面的步骤中介绍的某些安装页。</span><span class="sxs-lookup"><span data-stu-id="604ef-148">Depending on what is already installed on your computer, you may not see some of the installation pages described in the following steps.</span></span>  
 
 > [!IMPORTANT]
 > <span data-ttu-id="604ef-149">对于 SharePoint 2016，Reporting Services 将安装在其上的 SharePoint 服务器需要具有"自定义"服务器角色。</span><span class="sxs-lookup"><span data-stu-id="604ef-149">For SharePoint 2016, the SharePoint server that Reporting Services will be installed on needs to have the **Custom** server role.</span></span> <span data-ttu-id="604ef-150">Reporting Services 将在不处于"自定义"角色中的 SharePoint 服务器上成功部署，但在下一次 SharePoint 维护时段期间，MinRole 将停止 Reporting Services 服务，因为它检测到 SharePoint 集成模式中的 Reporting Services 不指示对其他任何 SharePoint 服务器角色的支持。</span><span class="sxs-lookup"><span data-stu-id="604ef-150">The deployment of Reporting Services will succeed on a SharePoint server that is not in the **Custom** role, but during the next SharePoint maintenance window, MinRole will stop the Reporting Services service because it detects that Reporting Services in SharePoint-integrated mode does not indicate support for any of the other SharePoint server roles.</span></span> <span data-ttu-id="604ef-151">Reporting Services 服务应用程序仅支持"自定义"角色。</span><span class="sxs-lookup"><span data-stu-id="604ef-151">The Reporting Services service application only supports the **Custom** role.</span></span>
 
 > [!NOTE]
 > <span data-ttu-id="604ef-152">如果你打算同时在 Share Point 2016 上安装 Power Pivot 服务，请在安装 Reporting Services 之前安装。</span><span class="sxs-lookup"><span data-stu-id="604ef-152">If you plan to install the Power Pivot service as well, on SharePoint 2016, install that prior to installing Reporting Services.</span></span> <span data-ttu-id="604ef-153">Power Pivot 服务仅能安装在处于"自定义"角色中的 SharePoint 服务器上。</span><span class="sxs-lookup"><span data-stu-id="604ef-153">The Power Pivot service can only be installed on a SharePoint server in the **Custom** role.</span></span>
 
