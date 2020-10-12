<properties
         pageTitle="Scoping questions for issue with delete or retain data"
         description="Scoping questions for issue with delete or retain data"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632785"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="532fa46c-9d45-454c-84d5-fce64a5d639d"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for issue with delete or retain data
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue with delete or retain data",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "error_message",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text here",
            "required": true
        },
        {
            "id": "item_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter protected item name(s) that you are trying to delete/retain data:",
            "watermarkText": "Enter protected item name(s) comma separated",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
