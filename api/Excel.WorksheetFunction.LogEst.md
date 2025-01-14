---
title: WorksheetFunction.LogEst method (Excel)
keywords: vbaxl10.chm137105
f1_keywords:
- vbaxl10.chm137105
ms.prod: excel
api_name:
- Excel.WorksheetFunction.LogEst
ms.assetid: 1730086d-5d14-4d9f-dc0e-5186cf932099
ms.date: 05/24/2019
ms.localizationpriority: medium
---


# WorksheetFunction.LogEst method (Excel)

In regression analysis, calculates an exponential curve that fits your data, and returns an array of values that describes the curve. Because this function returns an array of values, it must be entered as an array formula.


## Syntax

_expression_.**LogEst** (_Arg1_, _Arg2_, _Arg3_, _Arg4_)

_expression_ A variable that represents a **[WorksheetFunction](Excel.WorksheetFunction.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Arg1_|Required| **Variant**|Known_y's - the set of y-values that you already know in the relationship y = b*m^x.|
| _Arg2_|Optional| **Variant**|Known_x's - an optional set of x-values that you may already know in the relationship y = b*m^x.|
| _Arg3_|Optional| **Variant**|Const - a logical value specifying whether to force the constant b to equal 1.|
| _Arg4_|Optional| **Variant**|Stats - a logical value specifying whether to return additional regression statistics.|

## Return value

**Variant**

## Remarks

The equation for the curve is `y = b*m^x` or `y = (b*(m1^x1)*(m2^x2)*_)` (if there are multiple x-values), where the dependent y-value is a function of the independent x-values. The m-values are bases corresponding to each exponent x-value, and b is a constant value. Note that y, x, and m can be vectors. The array that **LogEst** returns is `{mn,mn-1,...,m1,b}`.

If the array known_y's is in a single column, each column of known_x's is interpreted as a separate variable.
    
If the array known_y's is in a single row, each row of known_x's is interpreted as a separate variable.  

The array known_x's can include one or more sets of variables. If only one variable is used, known_y's and known_x's can be ranges of any shape, as long as they have equal dimensions. If more than one variable is used, known_y's must be a range of cells with a height of one row or a width of one column (which is also known as a vector).
    
If known_x's is omitted, it is assumed to be the array `{1,2,3,...}` that is the same size as known_y's.
    
- If const is **True** or omitted, b is calculated normally. 
    
- If const is **False**, b is set equal to 1, and the m-values are fitted to `y = m^x`. 
    
- If stats is **True**, **LogEst** returns the additional regression statistics, so the returned array is {mn,mn-1,...,m1,b;sen,sen-1,...,se1,seb;r 2,sey; F,df;ssreg,ssresid}.
    
- If stats is **False** or omitted, **LogEst** returns only the m-coefficients and the constant b.
    
For information about additional regression statistics, see **[LinEst](excel.worksheetfunction.linest.md)**.

The more a plot of your data resembles an exponential curve, the better the calculated line will fit your data. Like **LinEst**, **LogEst** returns an array of values that describes a relationship among the values, but **LinEst** fits a straight line to your data; **LogEst** fits an exponential curve. For more information, see **[LinEst](excel.worksheetfunction.linest.md)**.
    
When you have only one independent x-variable, you can obtain y-intercept (b) values directly by using the following formula:

- Y-intercept (b): `INDEX(LOGEST(known_y's,known_x's),2)` You can use the `y = b*m^x` equation to predict future values of y, but Microsoft Excel provides the **[Growth](excel.worksheetfunction.growth.md)** function to do this for you.
    
Formulas that return arrays must be entered as array formulas.
    
- When entering an array constant such as known_x's as an argument, use commas to separate values in the same row and semicolons to separate rows. Separator characters may be different depending on your locale setting in **Regional and Language Options** in **Control Panel**.   
- You should note that the y-values predicted by the regression equation may not be valid if they are outside the range of y-values that you used to determine the equation.
    



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]