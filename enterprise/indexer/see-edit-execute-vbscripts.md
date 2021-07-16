# Enterprise / Indexer / See, edit and execute VBScripts on indexer

> Since v1.0.2.63

!> Important: VBScripts are an advance feature, make sure to give this permission only to advanced users

For being able to see, edit and execute VBScripts field events on enterprise indexer, please follow these steps.

## 1. Give specific permission to desired user on the application route

!> User has to be an **admin**

```
Users > [Desired admin user] > Edit > Permissions > check "Allow: See/Edit/Execute VBScripts on Indexer" option.
```

<img src="./_images_/vbscript/user_permission.png" width="820" height="auto">  



## 2. Seeing, editing and executing VBScripts on indexer

Once the user has the proper permission, fields with event scripts (onenteredit, onendedit, onkillfocus, onvaluechanged, onhelplistselect) will appear with the VB code icon on their right.

<img src="./_images_/vbscript/vb_icon.jpg" width="420" height="auto">  

If the icon is clicked, the editing dialog window will appear.

<img src="./_images_/vbscript/dialog.jpg" width="420" height="auto">  

* The dialog will show, allowing editing and executing the scripts that the field has, by clicking on the field.event buttons
* The "Execute script" button will trigger the current selected field event

> When this feature is enabled, always a script is executed, a notification alert like the following is shown on the indexer

<img src="./_images_/vbscript/alert.png" width="420" height="auto">  

