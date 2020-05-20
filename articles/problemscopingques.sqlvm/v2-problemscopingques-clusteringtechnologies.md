<properties pageTitle="Clustering technologies"
	 description="Clustering technologies"
	 authors="ujpat,amamun,vadeveka"
         ms.author="ujpat,amamun,vadeveka"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32740075"
	 productPesIds="16342"
	 cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	 schemaVersion="1"
	 articleId="f6ec0d8b-2241-476a-99d0-fbedbe6e4dc3"
	ownershipId="AzureData_AzureSQLVM"
/>
# Clustering Technologies
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Clustering technologies",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "configure_pacemaker",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you configured pacemaker on each cluster node?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Yes or having issues configuring",
                    "value": "Yes_Configured"
                },
                {
                    "text": "No",
                    "value": "No_NotConfigured"
                },
                {
                    "text": "I’m not sure/don’t know",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
         {
             "id": "Which_doc",
             "visibility": null,
             "order": 3,
             "controlType": "dropdown",
             "displayLabel": "Have you followed out public documentation for configuring pacemaker?",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "Yes",
                     "value": "Yes_Followed"
                 },
                 {
                     "text": "No",
                     "value": "No_NotFollowed"
                 },
                 {
                     "text": "I’m not sure/don’t know",
                     "value": "dont_know_answer"
                 }
             ],
             "dynamicDropdownOptions": null,
             "required": true,
             "maxLength": 0,
             "useAsAdditionalDetails": false,
             "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
