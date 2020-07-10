<properties
	articleId="f044f076-315f-4a5e-b98f-ea28367e9a38"
	pageTitle="Scoping Questions for HDInsight Service Unhealthy or Alert or Metrics Issue"
	description="Scoping Questions for HDInsight Service Unhealthy or Alert or Metrics Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636430, 32636448, 32636453, 32636466, 32636472, 32636480, 32636497, 32636503, 32636418, 32636446, 32636449, 32636457, 32636462, 32636468, 32636478, 32636493, 32636499, 32636427, 32636447, 32636450, 32636463, 32636469, 32636494, 32636500"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# Service Unhealthy or Alert Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight Service Unhealthy or Alert or Metrics Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "changes_category",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Any change made to any of these components?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "HDInsight_cluster",
                    "text": "HDInsight cluster configuration"
                },
                {
                    "value": "reboot",
                    "text": "Node or service reboot"
                },
                {
                    "value": "Network",
                    "text": "Network"
                },
                {
                    "value": "Storage_account",
                    "text": "Storage account"
                },
                {
                    "value": "access",
                    "text": "Password, access key, or certificate rotation"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "changes_detail",
            "visibility": "changes_category != dont_know_answer",
            "order": 50,
            "controlType": "multilinetextbox",
            "displayLabel": "Detail of the changes",
            "watermarkText": "Please describe the changes in detail",
            "required": false
        },
        {
            "id": "load_increase",
            "order": 80,
            "controlType": "dropdown",
            "displayLabel": "Increase in load?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Numberjobs",
                    "text": "Increased number of jobs"
                },
                {
                    "value": "Moredata",
                    "text": "More data to be processed"
                },
                {
                    "value": "skew",
                    "text": "Increased skew in data to be processed"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "mitigation",
            "order": 200,
            "controlType": "multilinetextbox",
            "displayLabel": "Mitigating actions taken so far",
            "watermarkText": "Mitigating actions taken so far and the result",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text, exception callstack if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
