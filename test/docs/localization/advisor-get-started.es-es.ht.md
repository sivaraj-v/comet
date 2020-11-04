---
title: "Introducción a Azure Advisor | Microsoft Docs"
description: "Introducción a Azure Advisor."
services: advisor
documentationcenter: NA
author: manbeenkohli
manager: carmonm
editor: 
ms.assetid: 
ms.service: advisor
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: NA
ms.date: 02/10/2017
ms.author: makohli
ms.openlocfilehash: dc89cd29e1e8038f0ff317ff6acee332218ebce7
ms.sourcegitcommit: ce934aca02072bdd2ec8d01dcbdca39134436359
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/08/2017
bilingual_type: hover over
---
# <a name="get-started-with-azure-advisor"></a>Introducción a Azure Advisor

Obtenga información acerca de cómo acceder a Advisor mediante Azure Portal y obtener e implementar recomendaciones.

## <a name="get-advisor-recommendations"></a>Obtención de recomendaciones de Advisor

1. Inicie sesión en el [Portal de Azure](https://portal.azure.com).

2. En el panel izquierdo, haga clic en **Advisor**.  Si no ve Advisor en el panel izquierdo, haga clic en **Más servicios**.  En el panel de menú de servicio, en **Supervisión y administración**, haga clic en **Advisor**.
 Se muestra el panel de Advisor.

   ![Acceso a Azure Advisor mediante Azure Portal](./media/advisor-get-started/advisor-portal-menu.png) 

4. El panel de Advisor mostrará un resumen de las recomendaciones para todas las suscripciones seleccionadas.  Puede elegir las suscripciones que desee que muestren las recomendaciones para usar el menú desplegable del filtro de suscripción.

5. Para obtener recomendaciones para una categoría específica, haga clic en una de las pestañas **High Availability** (Alta disponibilidad), **Security** (Seguridad), **Performance** (Rendimiento) o **Cost** (Costo).
 
> [!NOTE]
> Para utilizar Azure Advisor con una suscripción, debe iniciarse una suscripción *Propietario* en el panel de Advisor.  Esta acción registra la suscripción con Advisor.  Desde ese momento, cualquier suscripción *Propietario*, *Colaborador* o *Lector* puede acceder a las recomendaciones de Advisor para la suscripción.  

  ![Panel de Azure Advisor](./media/advisor-overview/advisor-dashboard.png)

## <a name="get-advisor-recommendation-details-and-implement-a-solution"></a>Obtener detalles de recomendaciones de Advisor e implementar una solución

Puede seleccionar una recomendación en Advisor para ver detalles adicionales, como las acciones de recomendación y los recursos afectados, y para implementar la solución para la recomendación.  

1. Inicie sesión en [Azure Portal](https://portal.azure.com) y después abra [Azure Advisor](https://aka.ms/azureadvisordashboard).

2. Seleccione una categoría de recomendación para mostrar la lista de recomendaciones dentro de esa categoría o seleccionar la pestaña **Todas** para ver todas las recomendaciones.

3. Haga clic en una recomendación que desee revisar en detalle.

4. Revise la información acerca de la recomendación y los recursos que se aplican a la recomendación.

5. Haga clic en **Acción recomendada** para implementar la recomendación.

## <a name="filter-advisor-recommendations"></a>Filtrado de recomendaciones de Advisor

Puede filtrar las recomendaciones para explorar en profundidad lo que es más importante para usted.  Puede filtrar por suscripción, tipo de recurso o estado de recomendación.  

1. Inicie sesión en [Azure Portal](https://portal.azure.com) y después abra [Azure Advisor](https://aka.ms/azureadvisordashboard).

2.  Use los menús desplegables en el panel de Advisor para filtrar por suscripción, tipo de recurso o estado de recomendación.

    ![Criterios de filtro de búsqueda de Advisor](./media/advisor-get-started/advisor-filters.png)

## <a name="snooze-or-dismiss-advisor-recommendations"></a>Posponer o descartar recomendaciones de Advisor

1. Inicie sesión en [Azure Portal](https://portal.azure.com) y después abra [Azure Advisor](https://aka.ms/azureadvisordashboard).

2. Vaya hasta la recomendación que desee posponer o descartar.

3. Haga clic en la recomendación.

4. Haga clic en **Posponer**. 

5. Puede especificar el tiempo que se pospondrá o seleccionar **Never** (Nunca) para descartar la recomendación.

## <a name="exclude-subscriptions-or-resource-groups-from-advisor"></a>Exclusión de las suscripciones o grupos de recursos de Advisor

Puede que tenga grupos de recursos o suscripciones para los que no desee recibir recomendaciones de Advisor: como recursos de prueba.  Puede configurar Advisor para que solo genere recomendaciones para grupos de recursos y suscripciones específicos.

> [!NOTE]
> Para incluir o excluir una suscripción o grupo de recursos de Advisor, debe ser propietario de una suscripción.  Si no tiene los permisos necesarios para una suscripción o grupo de recursos, la opción de incluir o incluir está deshabilitada en la interfaz de usuario.

1. Inicie sesión en [Azure Portal](https://portal.azure.com) y después abra [Azure Advisor](https://aka.ms/azureadvisordashboard).

2. Haga clic en **Configurar** en la barra de acción.

3. Desactive las suscripciones o grupos de recursos para las que no desee recibir recomendaciones de Advisor.

    ![Ejemplo de recursos de configuración de Advisor](./media/advisor-get-started/advisor-configure-resources.png)

4. Haga clic en el botón **Apply** (Aplicar).

## <a name="configure-the-average-cpu-utilization-rule-for-the-low-usage-virtual-machine-recommendation"></a>Recomendación de la configuración de la regla de uso promedio de CPU para una máquina virtual con poco uso

Advisor supervisa la utilización de las máquinas virtuales durante 14 días e identifica aquellas con una utilización escasa. Se considera que una máquina virtual tiene una utilización escasa si su uso promedio de CPU es del 5 % o menos y el de la red es de 7 MB o menos durante cuatro o más días.

Si le gustaría que fuera más exigente en la identificación de las máquinas virtuales con poco uso, puede ajustar la regla de uso promedio de la CPU según la suscripción.  La regla de uso promedio de CPU puede establecerse en 5 %, 10 %, 15 % o 20 %.

> [!NOTE]
> Para ajustar la regla de uso promedio de CPU para identificar las máquinas virtuales de poco uso, debe ser *Propietario* de una suscripción.  Si no tiene los permisos necesarios para una suscripción o grupo de recursos, la opción de incluir o incluir estará deshabilitada en la interfaz de usuario. 

1. Inicie sesión en [Azure Portal](https://portal.azure.com) y después abra [Azure Advisor](https://aka.ms/azureadvisordashboard).

2. Haga clic en **Configurar** en la barra de acción.

3. Haga clic en la pestaña **Reglas**.

4. Seleccione las suscripciones para las que les gustaría ajustar la regla de uso promedio de CPU y, luego, haga clic en **Editar**.

5. Seleccione el valor de uso promedio de CPU y, luego, haga clic en **Aplicar**.

6. Haga clic en **Actualizar recomendaciones** para actualizar las recomendaciones existentes para usar la nueva regla de uso promedio de CPU. 

   ![Ejemplo de reglas de recomendación de configuración de Advisor](./media/advisor-get-started/advisor-configure-rules.png)

## <a name="download-your-advisor-recommendations"></a>Descarga de las recomendaciones de Advisor

Advisor le permite descargar un resumen de sus recomendaciones.  Puede descargar las recomendaciones como un archivo PDF o un archivo CSV.  La descarga de recomendaciones permite el uso compartido sencillo con sus colegas o la realización de su propio análisis en la parte superior de los datos de recomendación.

1. Inicie sesión en [Azure Portal](https://portal.azure.com) y después abra [Azure Advisor](https://aka.ms/azureadvisordashboard).

2. Haga clic en **Descargar como CSV** o **Descargar como PDF** en la barra de acción.

La opción de descarga respeta los filtros aplicados en el panel de Advisor.  Si selecciona la opción de descarga mientras visualiza una recomendación o categoría de recomendación específicas, el resumen descargado solo incluye información para esa categoría o recomendación. 

## <a name="next-steps"></a>Pasos siguientes

Para más información sobre Advisor, consulte:
* [Introducción a Azure Advisor](advisor-overview.md)
* [Recomendaciones sobre alta disponibilidad de Advisor](advisor-high-availability-recommendations.md)
* [Recomendaciones sobre seguridad de Advisor](advisor-security-recommendations.md)
-  [Recomendaciones sobre rendimiento de Advisor](advisor-performance-recommendations.md)
* [Recomendaciones sobre el costo de Advisor](advisor-performance-recommendations.md)