<properties pageTitle="User-initiated password reset" 
	 description="Password Management/User-initiated password reset" 
	 authors="hsku" 
	 ms.author="hsku"
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32615416" 
	 productPesIds="16579" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
	 articleId="c0816905-886c-41cc-acab-516a43988111"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/> 
# Problem with user-initiated password reset 
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with password management user-initiated",
    "fileAttachmentHint": null,
    "diagnosticCard": {
        "title": "Problem with password management",
        "description": "Our self-service password reset troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your inputs."
    },
    "formElements": [
        {
            "id": "correlationId",
            "visibility": false,
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Correlation ID from Error message:",
            "content": null,
            "watermarkText": "Copy the correlation ID from the error message and paste it here",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "timestamp",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Timestamp from Error message:",
            "content": null,
            "watermarkText": "Copy the timestamp from the error message and paste it here",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "userId",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which user is experiencing this problem?",
            "content": null,
            "watermarkText": "For example 'joe@contoso.com'.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "If you received an error, please provide the error message details:",
            "content": null,
            "watermarkText": "AADSTSXXXXX: error message, Error message from the application, etc... ",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 3
        },
		{
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
