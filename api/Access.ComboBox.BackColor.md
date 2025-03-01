---
title: ComboBox.BackColor property (Access)
keywords: vbaac10.chm11406
f1_keywords:
- vbaac10.chm11406
ms.prod: access
api_name:
- Access.ComboBox.BackColor
ms.assetid: 63e7e016-f06f-4426-748a-b01d5550f727
ms.date: 02/28/2019
ms.localizationpriority: medium
---


# ComboBox.BackColor property (Access)

Gets or sets the interior color of the specified object. Read/write **Long**.


## Syntax

_expression_.**BackColor**

_expression_ A variable that represents a **[ComboBox](Access.ComboBox.md)** object.


## Remarks

The **BackColor** property contains a numeric expression that corresponds to the color used to fill a control's or section's interior.

You can set the default for this property by using a control's default control style or the **[DefaultControl](access.form.defaultcontrol.md)** property in Visual Basic.

To use the **BackColor** property, the **BackStyle** property, if available, must be set to Normal.


## Example

The following example uses the **RGB** function to set the **BorderColor**, **BackColor**, and **ForeColor** properties depending on the value of the **txtPastDue** text box. You can also use the **QBColor** function to set these properties. Putting the following code in the **Form_Current( )** event sets the control display characteristics as soon as the user opens a form or moves to a new record.

```vb
Sub Form_Current() 
 Dim curAmntDue As Currency, lngBlack As Long 
 Dim lngRed As Long, lngYellow As Long, lngWhite As Long 
 
 If Not IsNull(Me!txtPastDue.Value) Then 
 curAmntDue = Me!txtPastDue.Value 
 Else 
 Exit Sub 
 End If 
 lngRed = RGB(255, 0, 0) 
 lngBlack = RGB(0, 0, 0) 
 lngYellow = RGB(255, 255, 0) 
 lngWhite = RGB(255, 255, 255) 
 If curAmntDue > 100 Then 
 Me!txtPastDue.BorderColor = lngRed 
 Me!txtPastDue.ForeColor = lngRed 
 Me!txtPastDue.BackColor = lngYellow 
 Else 
 Me!txtPastDue.BorderColor = lngBlack 
 Me!txtPastDue.ForeColor = lngBlack 
 Me!txtPastDue.BackColor = lngWhite 
 End If 
End Sub
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]