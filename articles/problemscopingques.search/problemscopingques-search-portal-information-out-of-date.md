<properties
	pageTitle="Portal/Service information displayed in portal is incorrect or out of date"
	description="Why is the information displayed in the portal out of date"
	authors="liamca"
	ms.author="liamca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681386"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="6c761075-df06-422c-bd20-301ca77a1268"
	ownershipId="AzureSearch_AzureSearch"
/>
# Portal/Service information displayed in portal is incorrect or out of date
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Information displayed in portal is incorrect or out of date",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the information that was out of date?",
            "required": true,
            "useAsAdditionalDetails": true
        },
		{
            "id": "issue_timeframe",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the data more than an hour out of date?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last attempt to delete the service?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---