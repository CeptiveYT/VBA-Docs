---
title: TabStrip.MouseIcon Property (Outlook Forms Script)
ms.prod: outlook
ms.assetid: 9a534ed5-3f51-0dd0-5145-099eb86d415c
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# TabStrip.MouseIcon Property (Outlook Forms Script)

Returns a **String** that represents the full path name of a custom icon that is to be assigned to the control. Read-only.


## Syntax

_expression_.**MouseIcon**

_expression_ A variable that represents a **TabStrip** object.


## Remarks

The **MouseIcon** property is valid when the **[MousePointer](Outlook.tabstrip.mousepointer.md)** property is set to 99. The mouse icon of an object is the image that appears when the user moves the mouse across that object.

To assign an image for the mouse pointer, you can either assign a picture to the  **MouseIcon** property or load a picture from a file using the **LoadPicture** function in Visual Basic Scripting Edition.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]