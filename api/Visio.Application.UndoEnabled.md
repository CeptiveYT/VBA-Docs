---
title: Application.UndoEnabled property (Visio)
keywords: vis_sdr.chm10014610
f1_keywords:
- vis_sdr.chm10014610
ms.prod: visio
api_name:
- Visio.Application.UndoEnabled
ms.assetid: 54890621-84c3-8bde-2043-acb91a5b85dc
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Application.UndoEnabled property (Visio)

Determines whether undo information is maintained in memory. Read/write.


## Syntax

_expression_.**UndoEnabled**

_expression_ A variable that represents an **[Application](Visio.Application.md)** object.


## Return value

Boolean


## Remarks

When Microsoft Visio starts, the value of the  **UndoEnabled** property is **True**. Setting the value of the **UndoEnabled** property to **False** discontinues the collection of undo information in memory and clears the existing undo information.

You should attempt to maintain the property at its current value across the complete operation that you perform. In other words, use code structured like this:




```vb
blsPrevious = Application.UndoEnabled 
Application.UndoEnabled = False 
 
'Large operation here 
Application.UndoEnabled = blsPrevious 

```


## Example

The following Microsoft Visual Basic for Applications (VBA) macro shows how to use the  **UndoEnabled** method to disable and then re-enable undo behavior in Visio.


```vb
Public Sub UndoEnabled_Example() 
 
 'Disable undo 
 Application.UndoEnabled = False 
 
 'Draw three shapes. 
 ActivePage.DrawRectangle 1, 2, 2, 1 
 ActivePage.DrawOval 3, 4, 4, 3 
 ActivePage.DrawLine 4, 5, 5, 4 
 
 'Enable undo. 
 Application.UndoEnabled = True 
 
End Sub
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]