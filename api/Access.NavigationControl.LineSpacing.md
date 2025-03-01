---
title: NavigationControl.LineSpacing property (Access)
keywords: vbaac10.chm11140
f1_keywords:
- vbaac10.chm11140
ms.prod: access
api_name:
- Access.NavigationControl.LineSpacing
ms.assetid: bf1d5cef-8f0e-f759-3499-2f567097800e
ms.date: 03/23/2019
ms.localizationpriority: medium
---


# NavigationControl.LineSpacing property (Access)

You can use the **LineSpacing** property to specify or determine the location of information displayed within a label or text box control. Read/write **Integer**.


## Syntax

_expression_.**LineSpacing**

_expression_ A variable that represents a **[NavigationControl](Access.NavigationControl.md)** object.


## Remarks

A control's displayed information location is the distance measured between each line of the displayed information. To use a unit of measurement different from the setting in the **Regional Options** dialog box in the Windows Control Panel, specify the unit, such as cm or in (for example, 3 cm or 2 in).

In Visual Basic, use a numeric expression to set the value of this property. Values are expressed in [twips](../language/glossary/vbe-glossary.md#twip).


## Example

The following example sets the line spacing to 0.25 inches for the text box **PurchaseOrderDescription** on the **Purchase Orders** form.

```vb
' 0.25 inches = 360/1440 twips. 
 Forms("Purchase Orders").Controls("PurchaseOrderDescription").LineSpacing = 360
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]