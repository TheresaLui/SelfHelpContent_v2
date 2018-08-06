<properties pageTitle="Problem using a PowerShell cmdlet" 
	 description="problemwithpowershell" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32586798" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem using a PowerShell cmdlet 
---
{
  "resourceRequired": true,
  "title": "Problem using a PowerShell cmdlet",
  "fileAttachmentHint": "Debug log for PowerShell session",
  "formElements": [
    {
      "id": "whatProblem",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "What is the problem?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "cmdlet is not working or is returning unexpected results",
          "value": "notWorking"
        },
        {
          "text": "I don't know which PowerShell cmdlet to use",
          "value": "whichCmdlet"
        },
        {
          "text": "Other, don't know or not applicable",
          "value": "other"
        }
      ],
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "userInput",
      "visibility": "whatProblem==notWorking",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Input",
      "content": null,
      "watermarkText": "Paste in the text of the PowerShell cmdlet that you are using. Obfuscate any confidential data such as a user password.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 5
    },
    {
      "id": "output",
      "visibility": "whatProblem==notWorking",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Output",
      "content": null,
      "watermarkText": "Paste in the results that PowerShell returns for the above cmdlet.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 5
    },
    {
      "id": "userGoal",
      "visibility": "whatProblem==notWorking",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Goal",
      "content": null,
      "watermarkText": "What are you trying to do with this PowerShell cmdlet?",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 3
    },
    {
      "id": "version",
      "visibility": "whatProblem==notWorking",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Version",
      "content": null,
      "watermarkText": "Which version of Azure AD Powershell are you using?",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 1
    },
    {
      "id": "logTitle",
      "visibility": "whatProblem==notWorking",
      "order": 6,
      "controlType": "infoblock",
      "displayLabel": null,
      "content": "Upload debug log",
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "logHint",
      "visibility": "whatProblem==notWorking",
      "order": 7,
      "controlType": "infoblock",
      "displayLabel": null,
      "content": "In the ‘Problem’ pane to the left, please upload the debug log for the PowerShell session where the problem occurred. For Azure AD PowerShell, this file is in %LOCALAPPDATA%\\\\Microsoft\\\\AzureAD\\\\Powershell. To find the logs for another PowerShell module, please refer to the documentation for that modules.",
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "whatGoal",
      "visibility": "whatProblem!=notWorking",
      "order": 8,
      "controlType": "dropdown",
      "displayLabel": "What are you trying to do with PowerShell?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Enumerate users in my Azure AD",
          "value": "enumerate"
        },
        {
          "text": "Get data about a particular user in my Azure AD",
          "value": "read"
        },
        {
          "text": "Create a user",
          "value": "create"
        },
        {
          "text": "Delete a user",
          "value": "delete"
        },
        {
          "text": "Update a property of a user",
          "value": "update"
        },
        {
          "text": "Add or remove access for a user",
          "value": "access"
        },
        {
          "text": "Other, don't know or not applicable",
          "value": "other"
        }
      ],
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "userInputEnumerate",
      "visibility": "whatGoal==enumerate",
      "order": 9,
      "controlType": "multilinetextbox",
      "displayLabel": "Enumeration: Input",
      "content": null,
      "watermarkText": "Which users do you want to enumerate in your Azure AD? For example, any properties upon which you want to filter upon.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "userInputEnumerateReturns",
      "visibility": "whatGoal==enumerate",
      "order": 10,
      "controlType": "multilinetextbox",
      "displayLabel": "Enumeration: Output",
      "content": null,
      "watermarkText": "What data do you need to be returned about each of those users?",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "userInputRead",
      "visibility": "whatGoal==read",
      "order": 11,
      "controlType": "multilinetextbox",
      "displayLabel": "User properties",
      "content": null,
      "watermarkText": "What data do you need the PowerShell cmdlet to return about a particular user?",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "userInputCreate",
      "visibility": "whatGoal==create",
      "order": 12,
      "controlType": "multilinetextbox",
      "displayLabel": "Creating a user",
      "content": null,
      "watermarkText": "Describe any relevant details about the user(s) you need to create, such as the upn of the user",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "userInputDelete",
      "visibility": "whatGoal==delete",
      "order": 13,
      "controlType": "multilinetextbox",
      "displayLabel": "Deleting a user",
      "content": null,
      "watermarkText": "Describe any relevant details about the user(s) you need to delete, such as the upn of the user",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "userInputUpdate",
      "visibility": "whatGoal==update",
      "order": 14,
      "controlType": "multilinetextbox",
      "displayLabel": "Updating user properties",
      "content": null,
      "watermarkText": "Which property(ies) do you need to update for a user?",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "userInputAccess",
      "visibility": "whatGoal==access",
      "order": 15,
      "controlType": "multilinetextbox",
      "displayLabel": "Add or remove access",
      "content": null,
      "watermarkText": "What access do you need to add or remove for a user?",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "userInputOther",
      "visibility": "whatGoal==other",
      "order": 16,
      "controlType": "multilinetextbox",
      "displayLabel": "Other user management task",
      "content": null,
      "watermarkText": "Describe the user management task for which you want to use Azure AD PowerShell",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 6
    },
    {
      "id": "problemWithPowerShelladditionalDetails",
      "visibility": null,
      "order": 17,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide additional details",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": true,
      "numberOfLines": 0
    }
  ]
}
---