---
title: InvisibleApp.QueryCancelWindowClose event (Visio)
ms.prod: visio
api_name:
- Visio.InvisibleApp.QueryCancelWindowClose
ms.assetid: 78fb3502-4827-5add-1ff1-5dd3e3b6f143
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# InvisibleApp.QueryCancelWindowClose event (Visio)

Occurs before the application closes a window in response to a user action in the interface. If any event handler returns  **True**, the operation is canceled.


## Syntax

_expression_.**QueryCancelWindowClose** (_Window_)

_expression_ A variable that represents an **[InvisibleApp](Visio.InvisibleApp.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Window_|Required| **[IVWINDOW]**|The window that is going to be closed.|

## Remarks

A Microsoft Visio instance fires  **QueryCancelWindowClose** after the user has directed the instance to close a window.




- If any event handler returns  **True** (cancel), the instance fires **WindowCloseCanceled** and does not close the window.
    
- If all handlers return  **False** (don't cancel), the instance fires **BeforeWindowClosed** and then closes the window.
    


While a Visio instance is firing a query or cancel event, it responds to inquiries from client code but it refuses to perform operations. Client code can show forms or message boxes while responding to a query or cancel event.

If you are using Microsoft Visual Basic or Visual Basic for Applications (VBA), the syntax in this topic describes a common, efficient way to handle events.

If you want to create your own **Event** objects, use the **[Add](visio.eventlist.add.md)** or **[AddAdvise](visio.eventlist.addadvise.md)** method. 

To create an **Event** object that runs an add-on, use the **Add** method as it applies to the **EventList** collection. 

To create an **Event** object that receives notification, use the **AddAdvise** method. 

To find an event code for the event that you want to create, see [Event codes](../visio/Concepts/event-codesvisio.md).

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]