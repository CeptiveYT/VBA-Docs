---
title: Master.ConvertToGroupCanceled event (Visio)
keywords: vis_sdr.chm10719370
f1_keywords:
- vis_sdr.chm10719370
ms.prod: visio
api_name:
- Visio.Master.ConvertToGroupCanceled
ms.assetid: b585e434-fd81-93ae-92a6-5cc1d21c1afa
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Master.ConvertToGroupCanceled event (Visio)

Occurs after an event handler has returned  **True** (cancel) to a **QueryCancelConvertToGroup** event.


## Syntax

_expression_.**ConvertToGroupCanceled** (_Selection_)

_expression_ A variable that represents a **[Master](Visio.Master.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Selection_|Required| **[IVSELECTION]**|The selection of shapes that was going to be grouped.|

## Remarks

If you are using Microsoft Visual Basic or Visual Basic for Applications (VBA), the syntax in this topic describes a common, efficient way to handle events.

If you want to create your own **Event** objects, use the **[Add](visio.eventlist.add.md)** or **[AddAdvise](visio.eventlist.addadvise.md)** method. 

To create an **Event** object that runs an add-on, use the **Add** method as it applies to the **EventList** collection. 

To create an **Event** object that receives notification, use the **AddAdvise** method. 

To find an event code for the event that you want to create, see [Event codes](../visio/Concepts/event-codesvisio.md).

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]