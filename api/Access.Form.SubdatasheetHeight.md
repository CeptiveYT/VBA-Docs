---
title: Form.SubdatasheetHeight property (Access)
keywords: vbaac10.chm13510
f1_keywords:
- vbaac10.chm13510
ms.prod: access
api_name:
- Access.Form.SubdatasheetHeight
ms.assetid: 0db2e4b5-e64b-6f55-ebfa-bcce98734491
ms.date: 03/15/2019
ms.localizationpriority: medium
---


# Form.SubdatasheetHeight property (Access)

You can use the **SubdatasheetHeight** property to specify or determine the default display height of a subdatasheet when expanded. Read/write **Integer**.


## Syntax

_expression_.**SubdatasheetHeight**

_expression_ A variable that represents a **[Form](Access.Form.md)** object.


## Remarks

the **SubdatasheetHeight** property's value is expressed in [twips](../language/glossary/vbe-glossary.md#twip).

To set the **SubdatasheetHeight** property by using Visual Basic, you must first create the property by using the DAO **CreateProperty** method.

If the subdatasheet includes more records than the height setting can accommodate, a vertical scrollbar is displayed.

The **SubdatasheetHeight** property setting includes the New Record row if adding new records is supported. It does not include the column header row or scrollbar region.

The **SubdatasheetHeight** and **SubdatasheetExpanded** properties take effect on the subform control when the form is in Datasheet view.


## Example

The following example resizes the height of the subdatasheet in the **Purchase Orders** form (containing a subform) to show only one line of the subdatasheet at a time (measured at about 400 twips), accompanied by a vertical scrollbar. The number 400 is arbitrary, and will vary based on monitor resolution and default font size. This behavior can only be seen in Datasheet view.

```vb
Forms("Purchase Orders").SubdatasheetHeight = 400
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]