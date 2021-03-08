<properties
         pageTitle="Scoping questions for Issue with creating private endpoints"
         description="Scoping questions for Issue with creating private endpoints"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32785501"
         productPesIds="15207,15571,15797,16454,16470,14749"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	articleId="42f49209-c57d-4993-9a28-bf661c00d095"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Issue with creating private endpoints
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue with creating private endpoints",
    "fileAttachmentHint": "",
    "formElements": [
        {     "id": "Issue_Type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you protected or attempted to protect any items to this vault?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "DNS_Type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the type of DNS usage",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Private DNS",
                    "text": "Azure Private DNS"
                },
                {
                    "value": "Custom DNS",
                    "text": "Custom DNS"
                },
                {
                    "value": "Both",
                    "text": "Both"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "Error_message",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": false,
            "displayLabel": "Share the error message you are seeing",
            "watermarkText": "Error code: Error message",
            "required": true
        },
         {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
	     "useAsAdditionalDetails": true
        }
        ],
    "$schema": "SelfHelpContent"
}
---
