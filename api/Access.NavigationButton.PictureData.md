---
title: NavigationButton.PictureData property (Access)
keywords: vbaac10.chm10453
f1_keywords:
- vbaac10.chm10453
ms.prod: access
api_name:
- Access.NavigationButton.PictureData
ms.assetid: 3154933c-0945-81b8-272b-3e37fa819b05
ms.date: 03/05/2019
ms.localizationpriority: medium
---


# NavigationButton.PictureData property (Access)

You can use the **PictureData** property to copy the picture to another object that supports the **Picture** property. Read/write **Variant**.


## Syntax

_expression_.**PictureData**

_expression_ A variable that represents a **[NavigationButton](Access.NavigationButton.md)** object.


## Remarks

The **PictureData** property setting is the **PictureData** property of another control, form, or report.

You can use this property to display different background pictures in a form, depending on actions taken by the user. For example, you might open a **Customers** form by using a different background picture, depending on whether the form is opened for data entry or for browsing.

You can also use the **PictureData** property together with the **[Timer](access.form.timer.md)** event and the **[TimerInterval](access.form.timerinterval.md)** property to perform simple animation on a form.


## Example

The following example uses three image controls to animate a butterfly image across a form. The Hidden1 image control contains a picture of a butterfly with its wings up, and the Hidden2 image control contains a picture of the same butterfly with its wings down. Both image controls have their **Visible** property set to **False**. 

The **TimerInterval** property is set to 200. Each time the **Timer** event occurs, the picture in the image control Visible1 is changed by using the **PictureData** property of the hidden image controls, and the visible image control is moved 200 [twips](../language/glossary/vbe-glossary.md#twip) to the right. The visible image control is moved back to the left side of the form when its **Left** property value is greater than the width of the form stored in the public variable `gfrmWidth`. The value of  `gfrmWidth` is set to `Me.Width` in the form's open event.

```vb
Private Sub Form_Timer() 
 
 Static intPic As Integer 
 
 Select Case intPic 
 Case Is = 1 
 Me!Visible1.PictureData = Me!Hidden1.PictureData 
 Case Is = 2 
 Me!Visible1.PictureData = Me!Hidden2.PictureData 
 Case Else 
 End Select 
 
 If intPic = 2 Then intPic = 0 
 intPic = intPic + 1 
 If (Me!Visible1.Left > gfrmWidth) Then Me!Visible1.Left = 0 
 Me!Visible1.Left = Me!Visible1.Left + 200 
 
End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]