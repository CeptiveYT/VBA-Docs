---
title: InvisibleApp.DataRecordsetChanged event (Visio)
ms.prod: visio
api_name:
- Visio.InvisibleApp.DataRecordsetChanged
ms.assetid: da80f525-ccf6-3d9b-789c-a4dd866ebf4c
ms.date: 06/25/2019
ms.localizationpriority: medium
---


# InvisibleApp.DataRecordsetChanged event (Visio)

Occurs when a data recordset changes as a result of being refreshed.

> [!NOTE] 
> This Visio object or member is available only to licensed users of Visio Professional 2013.


## Syntax

_expression_.**DataRecordsetChanged** (_DataRecordsetChanged_)

_expression_ An expression that returns an **[InvisibleApp](Visio.InvisibleApp.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _DataRecordsetChanged_|Required| **[IVDATARECORDSETCHANGEDEVENT]**|The data recordset that changed.|

## Remarks

When the **DataRecordsetChanged** event fires, the **[DataRecordsetChangedEvent](Visio.DataRecordsetChangedEvent.md)** object is passed to the **[IVisEventProc.VisEventProc](Visio.IVisEventProc.VisEventProc.md)** method as the _pSubjectObj_ parameter, which represents the subject of the event&mdash;the object to which the event occurs.

If you are using Microsoft Visual Basic or Visual Basic for Applications (VBA), the syntax in this topic describes a common, efficient way to handle events.

If you want to create your own **Event** objects, use the **[Add](visio.eventlist.add.md)** or **[AddAdvise](visio.eventlist.addadvise.md)** method. 

To create an **Event** object that runs an add-on, use the **Add** method as it applies to the **EventList** collection. 

To create an **Event** object that receives notification, use the **AddAdvise** method. 

To find an event code for the event that you want to create, see [Event codes](../visio/Concepts/event-codesvisio.md).



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]