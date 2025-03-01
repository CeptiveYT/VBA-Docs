---
title: Report.OnKeyUp property (Access)
keywords: vbaac10.chm13867
f1_keywords:
- vbaac10.chm13867
ms.prod: access
api_name:
- Access.Report.OnKeyUp
ms.assetid: a31122bb-3f5a-4021-a2b5-16487aa0ce7c
ms.date: 02/23/2019
ms.localizationpriority: medium
---


# Report.OnKeyUp property (Access)

Sets or returns the value of the **On Key Up** box in the Properties window. Read/write **String**.


## Syntax

_expression_.**OnKeyUp**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

This property is helpful for programmatically changing the action that Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered. 

The **KeyUp** event occurs when a user presses a key while a report or control has the focus. This event also occurs if you send a keystroke to a report or control by using the SendKeys action in a macro or the **SendKeys** statement in Visual Basic.

The **OnKeyUp** value will be one of the following, depending on the selection chosen in the Choose Builder window (accessed by choosing the **Build** button next to the **On Key Up** box in the report's Properties window):

- If you choose Expression Builder, the value will be =_expression_, where _expression_ is the expression from the Expression Builder window.
    
- If you choose Macro Builder, the value is the name of the macro. 
    
- If you choose Code Builder, the value will be [Event Procedure]. 
    
If the **On Key Up** box is blank, the property value is an empty string.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]