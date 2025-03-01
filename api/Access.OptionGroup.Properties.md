---
title: OptionGroup.Properties property (Access)
keywords: vbaac10.chm10813
f1_keywords:
- vbaac10.chm10813
ms.prod: access
api_name:
- Access.OptionGroup.Properties
ms.assetid: d6e75b49-9b97-6018-1277-6cc6ef8558df
ms.date: 02/23/2019
ms.localizationpriority: medium
---


# OptionGroup.Properties property (Access)

Returns a reference to a control's **[Properties](Access.Properties.md)** collection object. Read-only.


## Syntax

_expression_.**Properties**

_expression_ A variable that represents an **[OptionGroup](Access.OptionGroup.md)** object.


## Remarks

The **Properties** collection object is the collection of all the properties related to a control. You can refer to individual members of the collection by using the member object's index or a string expression that is the name of the member object. 

The first member object in the collection has an index value of 0, and the total number of member objects in the collection is the value of the **Properties** collection's **Count** property minus 1.


## Example

The following procedure uses the **Properties** property to print all the properties associated with the controls on a form to the Debug window. To run this code, place a command button named **cmdListProperties** on a form and paste the following code into the form's Declarations section. Click the command button to print the list of properties in the Debug window.


```vb
Private Sub cmdListProperties_Click() 
 ListControlProps Me 
End Sub 
 
Public Sub ListControlProps(ByRef frm As Form) 
 Dim ctl As Control 
 Dim prp As Property 
 
 On Error GoTo props_err 
 
 For Each ctl In frm.Controls 
 Debug.Print ctl.Properties("Name") 
 For Each prp In ctl.Properties 
 Debug.Print vbTab & prp.Name & " = " & prp.Value 
 Next prp 
 Next ctl 
 
props_exit: 
 Set ctl = Nothing 
 Set prp = Nothing 
Exit Sub 
 
props_err: 
 If Err = 2187 Then 
 Debug.Print vbTab & prp.Name & " = Only available at design time." 
 Resume Next 
 Else 
 Debug.Print vbTab & prp.Name & " = Error Occurred: " & Err.Description 
 Resume Next 
 End If 
End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]