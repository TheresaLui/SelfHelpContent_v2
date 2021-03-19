<properties
pageTitle="All Issues"
description="All Issues"
service="Microsoft.StorSimple"
resource="allIssues"
authors="vimunuku"
ms.author="vimunuku"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32630492,32630493,32630496,32630507,32630495,32630498,32630504,32630508,32630494,32630506,32630500,32630501,32630502,32630509,32630510"
resourceTags=""
productPesIds="16161"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="storsimple-all-issues"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# All Issues
---
{

    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "All Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storsimple_devices",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Device name",
            "watermarkText": "Choose an option",
            "required": false,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.StorSimple/managers/{resourceName}/devices?&api-version=2017-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "valuePropertyRegex": "^+$",
                    "defaultDropdownOptions": {
                        "value": "dont_know_answer",
                        "text": "Not applicable/No devices available"
                    }
            }
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---