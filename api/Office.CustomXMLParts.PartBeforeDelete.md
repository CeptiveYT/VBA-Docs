---
title: CustomXMLParts.PartBeforeDelete event (Office)
keywords: vbaof11.chm299002
f1_keywords:
- vbaof11.chm299002
ms.prod: office
api_name:
- Office.CustomXMLParts.PartBeforeDelete
ms.assetid: 50fa1172-3eac-e091-660e-693a91aaf330
ms.date: 01/07/2019
ms.localizationpriority: medium
---


# CustomXMLParts.PartBeforeDelete event (Office)

Occurs just before a **CustomXMLPart** object is deleted from the **CustomXMLParts** collection.


## Syntax

_expression_.**PartBeforeDelete** (_OldPart_)

_expression_ An expression that returns a **[CustomXMLParts](Office.CustomXMLParts.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _OldPart_|Required|**CustomXMLPart**|The part that is about to be deleted.|

## Example

The following example confirms that the user wants to delete the custom XML part, and then deletes the part if the user chooses **Yes** in the dialog box.


```vb
Sub CustomXMLParts_PartBeforeDelete(ByVal oldPart As CustomXMLPart) 
Dim result As Boolean 
 
result = MsgBox("Are you sure you want to delete the " & oldPart.ID & " part?", vbYesNo) 
 
If result Then 
   oldPart.Delete 
End If 
 
End Sub
```


## See also

- [CustomXMLParts object members](overview/library-reference/customxmlparts-members-office.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]