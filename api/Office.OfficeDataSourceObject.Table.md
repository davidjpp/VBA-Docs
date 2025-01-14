---
title: OfficeDataSourceObject.Table property (Office)
keywords: vbaof11.chm232002
f1_keywords:
- vbaof11.chm232002
ms.prod: office
api_name:
- Office.OfficeDataSourceObject.Table
ms.assetid: 5c65237a-49fc-3de1-3de7-267ad7db44a1
ms.date: 01/22/2019
ms.localizationpriority: medium
---


# OfficeDataSourceObject.Table property (Office)

Gets a **String** that represents the name of the table within the data source file that contains the mail merge records. The returned value may be blank if the table name is unknown or not applicable to the current data source. Read-only.


## Syntax

_expression_.**Table**

_expression_ A variable that represents an **[OfficeDataSourceObject](Office.OfficeDataSourceObject.md)** object.


## Example

This example sets the name of the table if the table name is currently blank.


```vb
Sub OfficeTest() 
 
 Dim appOffice As OfficeDataSourceObject 
 
 Set appOffice = Application.OfficeDataSourceObject 
 appOffice.Open bstrConnect:="DRIVER=SQL Server;SERVER=ServerName;" & _ 
 "UID=user;PWD=;DATABASE=Northwind", bstrTable:="Employees" 
 
 If appOffice.Table = "" Then 
 appOffice.Table = "Employees" 
 End If 
 
End Sub 

```


## See also

- [OfficeDataSourceObject object members](overview/library-reference/officedatasourceobject-members-office.md)




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]