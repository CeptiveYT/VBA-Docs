---
title: DataLabel.FormulaR1C1 property (PowerPoint)
keywords: vbapp10.chm696006
f1_keywords:
- vbapp10.chm696006
ms.prod: powerpoint
api_name:
- PowerPoint.DataLabel.FormulaR1C1
ms.assetid: e1a129c2-e891-35cd-8751-9262fce99647
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# DataLabel.FormulaR1C1 property (PowerPoint)

Returns or sets the formula for the object, using R1C1-style notation in the language of the macro. Read/write  **String**.


## Syntax

_expression_.**FormulaR1C1**

_expression_ A variable that represents a [DataLabel](PowerPoint.DataLabel.md) object.


## Remarks

If the cell contains a constant, this property returns the constant. If the cell is empty, the property returns an empty string. If the cell contains a formula, the property returns the formula as a string, in the same format in which it would be displayed in the formula bar (including the equal sign).

If you set the value or formula of a cell to a date, Microsoft PowerPoint verifies whether that cell is already formatted with one of the date or time number formats. If not, the number format is changed to the default short date number format.

If the range is a one-dimensional or two-dimensional range, you can set the formula to a Visual Basic array of the same dimensions. Similarly, you can put the formula into a Visual Basic array.

Setting the formula of a multiple-cell range fills all cells in the range with the formula.


## See also


[DataLabel Object](PowerPoint.DataLabel.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]