---
title: PageSetup.PrintQuality property (Excel)
keywords: vbaxl10.chm473096
f1_keywords:
- vbaxl10.chm473096
ms.prod: excel
api_name:
- Excel.PageSetup.PrintQuality
ms.assetid: 1c497526-214a-92ed-ce5b-920799ec52ff
ms.date: 05/03/2019
ms.localizationpriority: medium
---


# PageSetup.PrintQuality property (Excel)

Returns or sets the print quality. Read/write **Variant**.


## Syntax

_expression_.**PrintQuality** (_Index_)

_expression_ A variable that represents a **[PageSetup](Excel.PageSetup.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Index_|Optional| **Variant**|Horizontal print quality (1) or vertical print quality (2). Some printers may not support vertical print quality. If you don't specify this argument, the **PrintQuality** property returns (or can be set to) a two-element array that contains both horizontal and vertical print quality.|

## Example

This example sets the print quality on a printer with non-square pixels. The array specifies both horizontal and vertical print quality. This example may cause an error, depending on the printer driver you are using.

```vb
Worksheets("Sheet1").PageSetup.PrintQuality = Array(240, 140)
```

<br/>

This example displays the current setting for horizontal print quality.

```vb
MsgBox "Horizontal Print Quality is " & _ 
 Worksheets("Sheet1").PageSetup.PrintQuality(1)
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]