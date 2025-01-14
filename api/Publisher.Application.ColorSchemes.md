---
title: Application.ColorSchemes property (Publisher)
keywords: vbapb10.chm131080
f1_keywords:
- vbapb10.chm131080
ms.prod: publisher
api_name:
- Publisher.Application.ColorSchemes
ms.assetid: b991d8a2-d25d-839a-c14a-18cb6d126d33
ms.date: 06/04/2019
ms.localizationpriority: medium
---


# Application.ColorSchemes property (Publisher)

Returns a **[ColorSchemes](Publisher.ColorSchemes.md)** collection that represents the color schemes available.


## Syntax

_expression_.**ColorSchemes**

_expression_ A variable that represents an **[Application](Publisher.Application.md)** object.


## Return value

ColorSchemes


## Example

The following example loops through the **ColorSchemes** collection and displays the name of each color scheme and the RGB value of the color for followed hyperlinks in each scheme.

```vb
Dim cscLoop As ColorScheme 
Dim cscAll As ColorSchemes 
 
Set cscAll = Application.ColorSchemes 
 
For Each cscLoop In cscAll 
 With cscLoop 
 Debug.Print "Color scheme: " & .Name _ 
 & " / Followed hyperlink color: " _ 
 & .Colors(ColorIndex:=pbSchemeColorFollowedHyperlink).RGB 
 End With 
Next cscLoop
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]