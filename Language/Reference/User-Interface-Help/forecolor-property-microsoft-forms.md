---
title: ForeColor property (Microsoft Forms)
keywords: fm20.chm2001220
f1_keywords:
- fm20.chm2001220
ms.prod: office
ms.assetid: 00b455d1-adce-ebb2-bb15-34cafebc5b75
ms.date: 11/16/2018
ms.localizationpriority: medium
---


# ForeColor property (Microsoft Forms)

Specifies the [foreground color](../../Glossary/glossary-vba.md#foreground-color) of an object.

## Syntax

_object_.**ForeColor** [= _Long_ ]

The **ForeColor** property syntax has these parts:

|Part|Description|
|:-----|:-----|
| _object_|Required. A valid object.|
| _Long_|Optional. A value or constant that determines the foreground color of an object.|

## Settings

You can use any integer that represents a valid color. You can also specify a color by using the [RGB](../../Glossary/glossary-vba.md#rgb) function with red, green, and blue color components. The value of each color component is an integer that ranges from zero to 255. For example, you can specify teal blue as the integer value 4966415 or as red, green, and blue color components 15, 200, 75.

## Remarks

Use the **ForeColor** property for controls on forms to make them easy to read or to convey a special meaning. For example, if a text box reports the number of units in stock, you can change the color of the text when the value falls below the reorder level.

For a **[ScrollBar](scrollbar-control.md)** or **[SpinButton](spinbutton-control.md)**, **ForeColor** sets the color of the arrows. 

For a **[Frame](frame-control.md)**, **ForeColor** changes the color of the caption. 

For a **[Font](font-object-microsoft-forms.md)** object, **ForeColor** determines the color of the text.

## See also

- [Microsoft Forms examples](examples-microsoft-forms.md)
- [Microsoft Forms reference](reference-microsoft-forms.md)
- [Microsoft Forms concepts](concepts-microsoft-forms.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]