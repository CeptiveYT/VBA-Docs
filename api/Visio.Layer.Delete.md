---
title: Layer.Delete method (Visio)
keywords: vis_sdr.chm11851200
f1_keywords:
- vis_sdr.chm11851200
ms.prod: visio
api_name:
- Visio.Layer.Delete
ms.assetid: 817a06fd-f249-d17a-3f8c-6c132ec38823
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# Layer.Delete method (Visio)

Deletes a  **Layer** object. Can also delete shapes assigned to the deleted layer.


## Syntax

_expression_.**Delete**( `_fDeleteShapes_` )

_expression_ A variable that represents a **[Layer](Visio.Layer.md)** object.


## Parameters



|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _fDeleteShapes_|Required| **Integer**|1 (**True**) to delete shapes assigned to the layer; otherwise, 0 (**False**).|

## Return value

Nothing


## Remarks

When  _fDeleteShapes_ is non-zero, shapes assigned only to the deleted layer are deleted. Otherwise, the shapes are simply no longer assigned to that layer.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]