---
title: AppointmentItem.InternetCodepage property (Outlook)
keywords: vbaol11.chm916
f1_keywords:
- vbaol11.chm916
ms.prod: outlook
api_name:
- Outlook.AppointmentItem.InternetCodepage
ms.assetid: 7ebb4076-7ba0-cae4-f6d4-e85d37675a8e
ms.date: 07/28/2019
ms.localizationpriority: medium
---


# AppointmentItem.InternetCodepage property (Outlook)

Returns or sets a **Long** that determines the Internet code page used by the item. Read/write.


## Syntax

_expression_.**InternetCodepage**

_expression_ A variable that represents an **[AppointmentItem](Outlook.AppointmentItem.md)** object.


## Remarks

The Internet code page defines the text encoding scheme used by the item.

The following table lists the values that are supported by the **InternetCodePage** property.

|Name|Character set|Code page|
|:---|:------------|:--------|
|Arabic (ISO)| iso-8859-6|28596|
|Arabic (Windows) |windows-1256|1256|
|Baltic (ISO)| iso-8859-4|28594|
|Baltic (Windows)|windows-1257|1257|
|Central European (ISO)|iso-8859-2 |28592|
|Central European (Windows) |windows-1250|1250|
|Chinese Simplified (GB2312)|gb2312| 936|
|Chinese Simplified (HZ)|hz-gb-2312 |52936|
|Chinese Traditional (Big5)|big5|950|
|Cyrillic (ISO) |iso-8859-5 |28595|
|Cyrillic (KOI8-R)|koi8-r|20866|
|Cyrillic (KOI8-U)|koi8-u|21866|
|Cyrillic (Windows)|windows-1251|1251|
|Greek (ISO)|iso-8859-7| 28597|
|Greek (Windows)|windows-1253|1253|
|Hebrew (ISO-Logical)|iso-8859-8-i|38598|
|Hebrew (Windows) |windows-1255|1255|
|Japanese (EUC)|euc-jp|51932|
|Japanese (JIS)| iso-2022-jp|50220|
|Japanese (JIS-Allow 1 byte Kana)|csISO2022JP|50221|
|Japanese (Shift-JIS) | iso-2022-jp|932|
|Korean| ks_c_5601-1987| 949|
|Korean (EUC)| euc-kr|51949|
|Latin 3 (ISO)|iso-8859-3| 28593|
|Latin 9 (ISO)|iso-8859-15 | 28605|
|Thai (Windows) |windows-874 |874|
|Turkish (ISO)| iso-8859-9|28599|
|Turkish (Windows) |windows-1254|1254|
|Unicode (UTF-7)|utf-7| 65000|
|Unicode (UTF-8)|utf-8|65001|
|US-ASCII| us-ascii| 20127|
|Vietnamese (Windows)|windows-1258|1258|
|Western European (ISO)| iso-8859-1|28591|
|Western European (Windows)|Windows-1252|1252|

<br/>

The following table lists the code pages Microsoft recommends that you use for the best compatibility with older email systems.

|Name|Character set|Code page|
|:---|:------------|:--------|
|Arabic (Windows)| windows-1256|1256|
|Baltic (ISO)| iso-8859-4|28594|
|Central European (ISO)|iso-8859-2 |28592|
|Chinese Simplified (GB2312)| gb2312|936|
|Chinese Traditional (Big5)|big5|950|
|Cyrillic (KOI8-R) | koi8-r|20866|
|Cyrillic (Windows)|windows-1251|1251|
|Greek (ISO)| iso-8859-7|28597|
|Hebrew (Windows) |windows-1255|1255|
|Japanese (JIS)|iso-2022-jp|50220|
|Korean|ks_c_5601-1987|949|
|Thai (Windows)| windows-874|874|
|Turkish (ISO)|iso-8859-9|28599|
|Unicode (UTF-8)|utf-8|65001|
|US-ASCII|us-ascii |20127|
|Vietnamese (Windows)|windows-1258|1258|
|Western European (ISO)| iso-8859-1|28591|



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]