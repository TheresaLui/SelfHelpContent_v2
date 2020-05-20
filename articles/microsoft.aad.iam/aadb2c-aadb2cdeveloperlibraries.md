<properties pageTitle="Problem with AAD B2C developer libraries" 
	 description="aadb2cdeveloperlibraries" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32633308,32633312,32633321,32633324,32633595" 
	 productPesIds="16580" 
     authors="parakhj"
	 ms.author="parja"
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
   articleId="74bb6c16-6466-495c-a460-bc8fa2effaf8"
    	ownershipId="AzureIdentity_B2C"
/> 

# Problem with AAD B2C developer libraries 
---
{
    "resourceRequired": false,
    "title": "Problem with AAD B2C developer libraries",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whichTenant",
            "visibility": null,
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which Azure AD B2C tenant are you using?",
            "content": null,
            "watermarkText": "Enter the name of the tenant (for example: contosoB2C.onmicrosoft.com)",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "policyURL",
            "visibility": null,
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide a sample URL of the sign-up OR sign-in request that you are calling",
            "content": null,
            "watermarkText": "This is similar to the 'Run Now' URL of the policy that you are using.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "isRecentChange",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did this work previously or is this a new configuration?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Worked previously",
                    "value": "no"
                },
                {
                    "text": "New configuration",
                    "value": "yes"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "recentChangeDetails",
            "visibility": "isRecentChange==yes",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Summarize the changes that you made recently.",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "correlationId",
            "visibility": null,
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Correlation ID",
            "content": null,
            "watermarkText": "Enter the correlation ID if one was shown when a user attempted to sign in",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "symptoms",
            "visibility": null,
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
            "content": null,
            "watermarkText": "Examples: error message in the Azure portal, error message on signing in, incorrect data on application properties page",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 8,
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