---
title: AnimationBehavior.Parent property (PowerPoint)
keywords: vbapp10.chm657002
f1_keywords:
- vbapp10.chm657002
ms.prod: powerpoint
api_name:
- PowerPoint.AnimationBehavior.Parent
ms.assetid: cef1124b-fe7d-df0a-5a62-68b77d8022fb
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# AnimationBehavior.Parent property (PowerPoint)

Returns the parent object for the specified object.


## Syntax

_expression_.**Parent**

_expression_ A variable that represents an [AnimationBehavior](PowerPoint.AnimationBehavior.md) object.


## Return value

Object


## Example

This example adds an oval containing text to slide one in the active presentation and rotates the oval and the text 45 degrees. The parent object for the text frame is the  **Shape** object that contains the text.


```vb
Set myShapes = ActivePresentation.Slides(1).Shapes

With myShapes.AddShape(Type:=msoShapeOval, Left:=50, _
        Top:=50, Width:=300, Height:=150).TextFrame
    .TextRange.Text = "Test text"
    .Parent.Rotation = 45
End With
```


## See also


[AnimationBehavior Object](PowerPoint.AnimationBehavior.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]