---
title: ToggleButton.Click event (Access)
keywords: vbaac10.chm14147
f1_keywords:
- vbaac10.chm14147
ms.prod: access
api_name:
- Access.ToggleButton.Click
ms.assetid: ba9f17a4-70ec-f4b8-fb21-01350ebf572d
ms.date: 02/12/2019
ms.localizationpriority: medium
---


# ToggleButton.Click event (Access)

The **Click** event occurs when the user presses and then releases a mouse button over an object.


## Syntax

_expression_.**Click**

_expression_ A variable that represents a **[ToggleButton](Access.ToggleButton.md)** object.

## Remarks

This event doesn't apply to check boxes, option buttons, or toggle buttons in an option group. It applies only to the option group itself.

This event applies to a control containing a hyperlink.
    
To run a macro or event procedure when this event occurs, set the **OnClick** property to the name of the macro or to [Event Procedure].

For a control, this event occurs when the user:

- Clicks a control with the left mouse button. Clicking a control with the right or middle mouse button does not trigger this event.
    
- Clicks a control containing hyperlink data with the left mouse button. Clicking a control with the right or middle mouse button does not trigger this event. When the user moves the mouse pointer over a control containing hyperlink data, the mouse pointer changes to a "hand" icon. When the user clicks the mouse button, the hyperlink is activated, and then the **Click** event occurs.
    
- Selects an item in a combo box or list box, either by pressing the arrow keys and then pressing the Enter key or by clicking the mouse button.
    
- Presses Spacebar when a command button, check box, option button, or toggle button has the focus.
    
- Presses the Enter key on a form that has a command button whose **Default** property is set to Yes.
    
- Presses the Esc key on a form that has a command button whose **Cancel** property is set to Yes.
    
- Presses a control's access key. For example, if a command button's **Caption** property is set to &Go, pressing Alt+G triggers the event.

Typically, you attach a **Click** event procedure or macro to a command button to carry out commands and command-like actions. For the other applicable controls, use this event to trigger actions in response to one of the occurrences discussed earlier in this topic.

You can use a CancelEvent action in a DblClick macro to cancel the second **Click** event. For more information, see the **[DblClick](access.togglebutton.dblclick.md)** event topic.

To distinguish between the left, right, and middle mouse buttons, use the **MouseDown** and **MouseUp** events.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]