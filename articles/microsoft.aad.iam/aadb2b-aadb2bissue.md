<properties pageTitle="Problem with AAD B2B" 
	 description="aadb2bissue" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32565671" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with AAD B2B 
---
{
  "resourceRequired": false,
  "title": "Problem with AAD B2B",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "whichUser",
      "visibility": null,
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Enter the username or email address of the user in your org trying to add/remove/manage/work with the B2B user.",
      "content": null,
      "watermarkText": "Enter user’s user name or email address",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "guestOrMember",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Is this user a member of your organization or is he or she external to your organization?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Belongs to my organization",
          "value": "member"
        },
        {
          "text": "Is an external user (guest/B2B user)",
          "value": "externalUser"
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
      "id": "whichB2BUser",
      "visibility": null,
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Enter the email address of the B2B user you're trying to add.",
      "content": null,
      "watermarkText": "Enter user’s user name or email address",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "whereProblem",
      "visibility": null,
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Where does the problem occur?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Azure portal",
          "value": "azurePortal"
        },
        {
          "text": "PowerShell",
          "value": "powerShell"
        },
        {
          "text": "B2B API",
          "value": "invitationAPI"
        },
        {
          "text": "Access panel",
          "value": "accessPanel"
        },
        {
          "text": "Other Application",
          "value": "otherApp"
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
      "id": "reproStepsText",
      "visibility": null,
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": " What specific steps did you or the user follow that resulted in the error?",
      "content": null,
      "watermarkText": " List each specific step taken, and where those steps were performed in the Azure AD user experience.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 10
    },
    {
      "id": "symptoms",
      "visibility": null,
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": " What are the symptoms of the problem?",
      "content": null,
      "watermarkText": " Examples: error message in the Azure portal, error message on signing in, incorrect data on user profile page. Provide a description of the specific error you or the user saw, including any error codes or other details.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 10
    },
    {
      "id": "errorText",
      "visibility": null,
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": " Paste in the error text including the correlation ID if any.",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 10
    },
    {
      "id": "URL",
      "visibility": null,
      "order": 8,
      "controlType": "textbox",
      "displayLabel": " What is the URL of the page you saw the problem on?",
      "content": null,
      "watermarkText": " Enter the URL you were trying to access when the error happened. Note that the error page itself may have a URL, that’s not the one we need.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "aadB2BIssueadditionalDetails",
      "visibility": null,
      "order": 9,
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