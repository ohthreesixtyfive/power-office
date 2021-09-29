# poweroffice
A Power Automate Scope Definition to Populate Office Templates (Word/PowerPoint)

## Minimum Path to Use

In Power Automate
- Copy scope_definition.json to your clipboard.
- In Power Automate/Flow, click '+ New step'.
- Select 'My clipboard'.
- Press [Ctrl] + 'V' to make the Scope available in Microsoft Flow.
- Select 'Populate-Office-Template' to insert the Scope into your Flow.
- Provide inputs from your Trigger for the actions inside of the 'Inputs You Provide' scope.
- As desired, add actions to the Yes/No branches of 'If-Send-Docuent-To-Is-Not-Empty' Condition.

In Your Application
- Add Flow to your application.
- Convert your 2-Column Collection (Key/Value) into a JSON String using the JSON() function and provide that as the input to whatever populates the Replacement-Table-String action.
- Convert your 3-Column Collection (Filename/Url/Content) into a JSON String using the JSON() function and provide that as the input to whatever populates the Image-Replacement-String action.
