<properties pageTitle="Problem assigning licenses to a user" 
	 description="problemassigninglicensetoauser" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570959" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
	articleId="e485ed69-c238-43c6-b316-4501279f828f"
/> 
# Problem assigning licenses to a user 
---
{
    "resourceRequired": false,
    "title": "Problem assigning licenses to a user",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whereProblem",
            "visibility": null,
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What environment are you using to assign a license to a user?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure portal",
                    "value": "azurePortal"
                },
                {
                    "text": "Office portal",
                    "value": "officePortal"
                },
                {
                    "text": "PowerShell cmdlets",
                    "value": "powerShell"
                },
                {
                    "text": "Microsoft Graph APIs",
                    "value": "msGraph"
                },
                {
                    "text": "Not sure",
                    "value": "other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
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
            "id": "gblUse",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you using group-based licensing in your tenant to automate license assignment to users?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes",
                    "value": "yes"
                },
                {
                    "text": "No",
                    "value": "no"
                },
                {
                    "text": "Not sure",
                    "value": "dontknow"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
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
            "id": "gblAndDirectAssignment",
            "visibility": "gblUse!=no",
            "order": 3,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "<a href='https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-advanced#direct-licenses-coexist-with-group-licenses'>When users inherit licenses from groups it may not be possible to modify or remove the license from a user. Azure portal displays useful error details in such cases - make sure to click the error notification when your operation fails to find out more. Click here to read about group-based licensing.</a>",
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
            "id": "userId",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Object ID or user name of the user you are having problems with?",
            "content": null,
            "watermarkText": "The Object ID and user name (user@domain.com) can be found by opening the user in the portal, in the Overview tab in the Essentials box on the very top.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "symptoms",
            "visibility": null,
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
            "content": null,
            "watermarkText": "Additional details that might help us diagnose and solve the problem, such as the name of the product license you are assigning. Consider clicking on the error notification in the portal to display full information about the problem and copy the error details.",
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
            "id": "problem_start_time",
            "visibility": null,
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "content": null,
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
            "id": "problem_description",
            "visibility": null,
            "order": 7,
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
    ],
    "$schema": "SelfHelpContent"
}
---