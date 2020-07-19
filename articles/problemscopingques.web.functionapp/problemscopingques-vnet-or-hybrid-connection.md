<properties
	articleId="problemscopingques-vnet-or-hybrid-connection"
	pageTitle="VNET or Hybrid Connection"
	description="VNET or Hybrid Connection"
	supportTopicIds="32630473"
	authors="khaled-zayed"
	ms.author="khzayed"
	selfHelpType="problemScopingQuestions"
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_AppService"
/>
# VNET or Hybrid Connection
---
{
    "resourceRequired": false,
    "title": "VNET or Hybrid Connection",
    "fileAttachmentHint": "Please attach any relevant logs/screenshots",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Incident time",
            "required": true
        },
        {
            "id": "2",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have any NSGs which may be hindering the connectivity?",
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
            "id": "3",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the name of VNET?",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "4",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the Hybrid Connection (HC) URL? (You can find this in the Hybrid Connection Manager details for the HC or in the connection string shown in the portal.)",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "5",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the status of the HC? (Not connected, Connected, Status unknown, etc.)",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "6",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is the HC endpoint? (The endpoint that is visible in the Azure portal.)",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "7",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What's the exact name and port combination you are using to connect to the target through HC? ",
            "watermarkText": "...",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
