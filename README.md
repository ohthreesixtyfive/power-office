# poweroffice
A Power Automate Scope Definition to Populate Office Templates (Word/PowerPoint)

## Minimum Path to Use

In Your Office Document Template
- Add placeholder values in their appropriate locations, encapsulated by a delimiter (eg: ` ||Customer Name|| `, ` ||Invoice Number|| ` )

Here in GitHub
- Copy the entirety of [scope_definition.json](https://github.com/ohthreesixtyfive/poweroffice/blob/main/scope_definition.json) to your clipboard.

In Power Automate
- In Power Automate/Flow, click ` + New step `.
- Select ` My clipboard `.
- Press ` [Ctrl] ` + ` V ` to make the Scope available in Microsoft Flow.
- Select ` Populate-Office-Template ` to insert the Scope into your Flow.
- Provide inputs from your Trigger for the actions inside of the ` Inputs You Provide ` scope.
- As desired, add actions to the Yes/No branches of ` If-Send-Document-To-Is-Not-Empty ` Condition.
- Update all SharePoint Actions with the proper Connection References.

In Your Application
- Add ` Flow ` to your application.
- Convert a 2-column collection (Key/Value) containing your placeholders (**without delimiters**) and their replacement values into a JSON String using the JSON() function and provide that as the input to whatever populates the ` Replacement-Table-String ` action.

<table>
<tr>
<td><strong>Key</strong></td>
<td><strong>Value</strong></td>
</tr>
<tr>
<td> Customer Name </td>
<td> Oh! Three Sixty Five </td>
</tr>
<tr>
<td> Invoice Number </td>
<td> INV-12345 </td>
</tr>
<tr>
<td> Invoice Date </td>
<td> 10/26/2021 </td>
</tr>
</table>
 
Additional Features

- If you'd like to try out the ` repeating table functionality `:
  - Provide a JSON String representation of your desired table's collection as a replacement value.
- If you'd like to try out the ` image replacement functionality `:
  - Convert a 3-column collection (Filename/Url/Content) into a JSON String using the `JSON()` function and provide that as the input to whatever populates the `Image-Replacement-String` action.
