
<properties
pageTitle="Container monitoring"
description="Container monitoring"
articleId="problemscopingques-Container_monitoring"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612445"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
/>

# Container monitoring
---
{
    "resourceRequired": true,
    "title": "Restore deleted workspace",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "what_container_monitoring_tools",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What container monitoring tools are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Monitor for Container (Container Insights)",
                    "text": "Azure Monitor for Container (Container Insights)"
                },
                {
                    "Container Monitoring Solution",
                    "text": "Container Monitoring Solution"
                },
                {
                    "value": "Not sure",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ]
}
---