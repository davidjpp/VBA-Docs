---
title: Line.BorderTint property (Access)
keywords: vbaac10.chm14602
f1_keywords:
- vbaac10.chm14602
ms.prod: access
api_name:
- Access.Line.BorderTint
ms.assetid: 904bd124-3f3e-40ac-77b7-4ba10716ae02
ms.date: 02/20/2019
ms.localizationpriority: medium
---


# Line.BorderTint property (Access)

Gets or sets the tint that is applied to the theme color in the **BorderColor** property of the specified object. Read/write **Single**.


## Syntax

_expression_.**BorderTint**

_expression_ A variable that represents a **[Line](Access.Line.md)** object.


## Remarks

The **BorderTint** property contains a numeric expression that can be used to lighten the theme color in the **BorderColor** property. The default value of the **BorderTint** property is 100, which is neutral, and does not change the theme color. 

To lighten the color, first determine the percentage by which to lighten from 1 to 100, and then subtract that value as a whole number from 100 and use the remainder. For example, to lighten the theme color by 75%, subtract 75 from 100 and use the remainder, which is 25.

This property is not surfaced in the property sheet.


## Example

The following code example lightens the **BorderColor** property by 75%.


```vb
Me.ctl.BorderTint=25
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]