---
title: PageNumbers.Creator property (Word)
keywords: vbawd10.chm159777769
f1_keywords:
- vbawd10.chm159777769
ms.prod: word
api_name:
- Word.PageNumbers.Creator
ms.assetid: bfd4e131-9c8a-2b37-b62c-fb8728b0e974
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# PageNumbers.Creator property (Word)

Returns a 32-bit integer that indicates the application in which the specified object was created. Read-only  **Long**.


## Syntax

_expression_.**Creator**

_expression_ Required. A variable that represents a **[PageNumbers](Word.PageNumbers.md)** object.


## Remarks

If the object was created in Microsoft Word, the **Creator** property returns the hexadecimal number 4D535744, which represents the string "MSWD." This property was primarily designed to be used on the Macintosh, where each application has a four-character creator code. For example, Microsoft Word has the creator code MSWD. For additional information about this property, consult the language reference Help included with Microsoft Office Macintosh Edition.


## See also


[PageNumbers Collection Object](Word.pagenumbers.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]