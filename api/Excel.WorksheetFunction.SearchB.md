---
title: WorksheetFunction.SearchB method (Excel)
keywords: vbaxl10.chm137155
f1_keywords:
- vbaxl10.chm137155
ms.prod: excel
api_name:
- Excel.WorksheetFunction.SearchB
ms.assetid: 10a39f1f-98d1-e264-7b20-078175dc4606
ms.date: 05/25/2019
ms.localizationpriority: medium
---


# WorksheetFunction.SearchB method (Excel)

**Search** and **SearchB** locate one text string within a second text string, and return the number of the starting position of the first text string from the first character of the second text string.


## Syntax

_expression_.**SearchB** (_Arg1_, _Arg2_, _Arg3_)

_expression_ A variable that represents a **[WorksheetFunction](Excel.WorksheetFunction.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Arg1_|Required| **String**|Find_text - the text that you want to find.|
| _Arg2_|Required| **String**|Within_text - the text in which you want to search for find_text.|
| _Arg3_|Optional| **Variant**|Start_num - the character number in within_text at which you want to start searching.|

## Return value

**Double**


## Remarks

**Search** is intended for use with languages that use the single-byte character set (SBCS), whereas **SearchB** is intended for use with languages that use the double-byte character set (DBCS). The default language setting on your computer affects the return value in the following way:

- **Search** always counts each character, whether single-byte or double-byte, as 1, no matter what the default language setting is.
    
- **SearchB** counts each double-byte character as 2 when you have enabled the editing of a language that supports DBCS, and then sets it as the default language. Otherwise, **SearchB** counts each character as 1.
    
- The languages that support DBCS include Japanese, Chinese (Simplified), Chinese (Traditional), and Korean.

Use **Search** and **SearchB** to determine the location of a character or text string within another text string so that you can use the **Mid** and **MidB** or **Replace** and **ReplaceB** functions to change the text.
    
**Search** and **SearchB** are not case-sensitive. If you want to do a case-sensitive search, you can use **Find** and **FindB**.
    
You can use the wildcard characters, question mark (?) and asterisk (*), in find_text. A question mark matches any single character; an asterisk matches any sequence of characters. If you want to find an actual question mark or asterisk, type a tilde (~) before the character.
    
If find_text is not found, the #VALUE! error value is returned.
    
If start_num is omitted, it is assumed to be 1.
    
If start_num is not greater than 0 (zero) or is greater than the length of within_text, the #VALUE! error value is returned.

Use start_num to skip a specified number of characters. Using **Search** as an example, suppose you are working with the text string `AYF0093.YoungMensApparel`. To find the number of the first `"Y"` in the descriptive part of the text string, set start_num equal to 8 so that the serial-number portion of the text is not searched. **Search** begins with character 8, finds find_text at the next character, and returns the number 9. 

**Search** always returns the number of characters from the start of within_text, counting the characters you skip if start_num is greater than 1.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]