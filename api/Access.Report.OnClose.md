---
title: Report.OnClose property (Access)
keywords: vbaac10.chm13764
f1_keywords:
- vbaac10.chm13764
ms.prod: access
api_name:
- Access.Report.OnClose
ms.assetid: 640b5540-4b0d-6649-0a36-9dd63a437c84
ms.date: 03/15/2019
ms.localizationpriority: medium
---


# Report.OnClose property (Access)

Sets or returns the value of the **On Close** box in the Properties window of a form or report. Read/write **String**.


## Syntax

_expression_.**OnClose**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

This property is helpful for programmatically changing the action that Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered.

The **Close** event occurs when a form or report is closed and removed from the screen.

The **OnClose** value will be one of the following, depending on the selection chosen in the Choose Builder window (accessed by choosing the **Build** button next to the **On Close** box in the object's Properties window):


- If you choose Expression Builder, the value will be =_expression_, where _expression_ is the expression from the Expression Builder window.
    
- If you choose Macro Builder, the value is the name of the macro. 
    
- If you choose Code Builder, the value will be [Event Procedure]. 
    
If the **On Close** box is blank, the property value is an empty string.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]