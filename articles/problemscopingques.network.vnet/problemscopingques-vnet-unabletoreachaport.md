<properties
    pageTitle="Unable to reach a port"
    description="Unable to reach a port"
    authors="anavinahar"
    ms.author="anavin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32584255"
    productPesIds="15526"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="8766b9f2-62d3-4dc0-8b81-597d2b0536ea"
/>

# Unable to reach a port

---
{
    "resourceRequired": true,
    "title": "Unable to reach a port",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "public_ip_changed",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the virtual machine you are facing connectivity issues with",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/virtualMachines/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
                        "dropdownOptions": [
                {
                    "value": "Unable to get the list of Virtual Machines",
                    "text": "Unable to get the list of Virtual Machines"
                }
            ],
            "required": false
        },
            {
            "id": "port number",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the port you are unable to reach",
            "watermarkText": "Enter the port",
            "required": true
        }
    ]
}
---
