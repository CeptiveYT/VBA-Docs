---
title: RuleConditions.NotTo property (Outlook)
keywords: vbaol11.chm2306
f1_keywords:
- vbaol11.chm2306
ms.prod: outlook
api_name:
- Outlook.RuleConditions.NotTo
ms.assetid: 9889e503-05cd-ebf8-40e0-358327798b6a
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# RuleConditions.NotTo property (Outlook)

Returns a **[RuleCondition](Outlook.RuleCondition.md)** object with a **[RuleCondition.ConditionType](Outlook.RuleCondition.ConditionType.md)** of **olConditionNotTo**. Read-only.


## Syntax

_expression_. `NotTo`

_expression_ A variable that represents a [RuleConditions](Outlook.RuleConditions.md) object.


## Remarks

Use the returned  **RuleCondition** object when enumerating the rule conditions or exception conditions of an existing rule, or when creating a new rule that specifies the condition or exception condition that your name is not in the **To** box.

This property of the  **[RuleConditions](Outlook.RuleConditions.md)** collection always returns a **RuleCondition** object regardless of whether the rule associated with this **RuleConditions** collection has defined such a rule condition. If the rule has defined and enabled such a rule condition, then **[RuleCondition.Enabled](Outlook.RuleCondition.Enabled.md)** will be **True**.


## See also


[RuleConditions Object](Outlook.RuleConditions.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]