---
title: ShadowFormat.Creator property (Word)
keywords: vbawd10.chm164365289
f1_keywords:
- vbawd10.chm164365289
ms.prod: word
api_name:
- Word.ShadowFormat.Creator
ms.assetid: 070a17aa-d979-1ab5-e741-d9aaf3e61c3a
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# ShadowFormat.Creator property (Word)

Returns a 32-bit integer that indicates the application in which the specified object was created. Read-only  **Long**.


## Syntax

_expression_.**Creator**

_expression_ Required. A variable that represents a **[ShadowFormat](Word.ShadowFormat.md)** object.


## Remarks

If the object was created in Microsoft Word, the **Creator** property returns the hexadecimal number 4D535744, which represents the string "MSWD." This property was primarily designed to be used on the Macintosh, where each application has a four-character creator code. For example, Microsoft Word has the creator code MSWD. For additional information about this property, consult the language reference Help included with Microsoft Office Macintosh Edition.


## See also


[ShadowFormat Object](Word.ShadowFormat.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]