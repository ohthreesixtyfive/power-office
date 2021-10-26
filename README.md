# poweroffice
A Power Automate Scope Definition to Populate Office Templates (Word/PowerPoint)

## Minimum Path to Use

Here in GitHub
- Copy the entirety of [scope_definition.json](https://github.com/ohthreesixtyfive/poweroffice/blob/main/scope_definition.json) to your clipboard.

In Power Automate
- In Power Automate/Flow, click '+ New step'.
- Select 'My clipboard'.
- Press [Ctrl] + 'V' to make the Scope available in Microsoft Flow.
- Select 'Populate-Office-Template' to insert the Scope into your Flow.
- Provide inputs from your Trigger for the actions inside of the 'Inputs You Provide' scope.
- As desired, add actions to the Yes/No branches of 'If-Send-Docuent-To-Is-Not-Empty' Condition.
- Update all SharePoint Actions with the proper Connection References.

In Your Application
- Add Flow to your application.
- Convert your 2-Column Collection (Key/Value) into a JSON String using the JSON() function and provide that as the input to whatever populates the Replacement-Table-String action.
  - If you'd like to test out the *repeating table functionality*, provide a JSON String representation of your desired table's collection as a replacement value.
- Convert your 3-Column Collection (Filename/Url/Content) into a JSON String using the JSON() function and provide that as the input to whatever populates the Image-Replacement-String action.
