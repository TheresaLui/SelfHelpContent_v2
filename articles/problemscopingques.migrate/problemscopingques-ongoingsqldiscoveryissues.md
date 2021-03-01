<properties
         pageTitle="Scoping questions for ongoing SQL discovery issues"
         description="Scoping questions for ongoing SQL discovery issues"
         authors="bhpat"
         ms.author="bhpat"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32786258"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="11701a4c-7b74-c7fe-2819-2dcc880bfc11"
	ownershipId="Compute_AzureMigrate"
/>

# Ongoing SQL Discovery issues

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Discovery issues",
    "fileAttachmentHint": "",
    "formElements": [
         {
            "id": "access_privileges",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you have contributor or access to create Azure resources in the subscription?",
            "watermarkText": "Select",
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
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "appliance_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the appliance",
            "watermarkText": "E.g. MyContosoAppliance",
            "required": false
        },
        {
            "id": "host_details",
            "order": 3,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the vCenterServer/Hyper-V host details",
            "watermarkText": "E.g. IP = 172.22.60.1",
            "required": false
        },
	{
            "id": "problem_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Your problem is related to",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Not able to identify SQL instances in respective Servers",
                    "text": "Not able to identify SQL instances in respective Servers"
                },
                {
                    "value": "Not able to populate details/ properties such as number of user databases for discovered SQL instances",
                    "text": "Not able to populate details/ properties such as number of user databases for discovered SQL instances"
                },
                {
                    "value": "Not able to discover SQL databases and their properties",
                    "text": "Not able to discover SQL databases and their properties"
                },
		{
                    "value": "Not able to see latest SQL discovery data",
                    "text": "Not able to see latest SQL discovery data"
                },
		{
                    "value": "dont_know_answer",
                    "text": "None of the above"
                }
            ],
            "required": true
        },
	{
            "id": "sql_name",
            "order": 5,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the impacted SQL instance(s)",
	    "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
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
