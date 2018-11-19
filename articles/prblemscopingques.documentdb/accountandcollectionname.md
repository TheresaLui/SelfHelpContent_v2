<properties
	pageTitle="CosmosDb Account and Collection Info"
	description="CosmosDb Account and Collection Info"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions" supportTopicIds="32597477,32597529,32597537,32597555,32597558,32597478,32597490,32597500,32597506,32597513,32597519,32597528,32597538,32597546,32597562,32597484,32597493,32597497,32597503,32597509,32597516,32597522,32597527,32597544,32597547,32597554,32597561,32597563,32597492,32597499,32597502,32597508,32597515,32597521,32597524,32597541,32597480,32597491,32597498,32597501,32597507,32597514,32597520"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# CosmosDb Account and Collection Info
---
{
    "resourceRequired": true,
    "title": "CosmosDb Account and Collection Info",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "database_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": true,
            "hints": [
                {
                    "text": "Name of the database that is affected"
                }
            ]
        },
        {
            "id": "collection_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Collection name",
            "required": true,
            "hints": [
                {
                    "text": "Name of the collection that is affected"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you were facing",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Read/Write regions where the issue is experienced"
                },
                {
                    "text": "Activity Id of the request (if available)."
                }
            ]
        }
    ]
}
---
