---
title: OptionButton.StatusBarText property (Access)
keywords: vbaac10.chm10573
f1_keywords:
- vbaac10.chm10573
ms.prod: access
api_name:
- Access.OptionButton.StatusBarText
ms.assetid: d3cda3a2-1b19-6b12-6d22-0cfd1b869933
ms.date: 02/26/2019
ms.localizationpriority: medium
---


# OptionButton.StatusBarText property (Access)

You can use the **StatusBarText** property to specify the text that is displayed in the status bar when a control is selected. Read/write **String**.


## Syntax

_expression_.**StatusBarText**

_expression_ A variable that represents an **[OptionButton](Access.OptionButton.md)** object.


## Remarks

You set the **StatusBarText** property by using a string expression up to 255 characters long. The length of the text that you can display in the status bar depends on your computer hardware and video display.

You can use the **StatusBarText** property to provide specific information about a control. For example, when a text box has the focus, a brief instruction can tell the user what kind of data to enter.

If you create a control by dragging a field from the field list, the value in a field's **Description** property is copied to the **StatusBarText** property.

> [!TIP] 
> You can also use the **ControlTipText** property to display a ScreenTip for a control.


## Example

The following example sets the status bar text to be displayed when the **Address_TextBox** control in the **Mailing List** form has the focus in Form view. 


```vb
Forms("Mailing List").Controls("Address_TextBox"). _ 
 StatusBarText = "Enter the company's mailing address." 

```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]