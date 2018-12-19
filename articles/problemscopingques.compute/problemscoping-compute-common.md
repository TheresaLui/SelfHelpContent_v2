<properties
        pageTitle="Scoping questions for issue with Azure Compute"
        description="This is the scoping question for the VM deployment failure"
        authors="Sudip Lama"
        authorAlias="sulama"
        selfHelpType="problemScopingQuestions"
        supportTopicIds="32628247, 32628262, 32628252, 32628259, 32628255, 32628279"
        productPesIds="14749, 15571, 15797, 16454"
        cloudEnvironments="public"
        schemaVersion="1"
        articleId="c1d52907-63c1-4d7e-8fa2-87051c4d1faa"
    />
# Problem with Creating VM
---
{
    "resourceRequired": true,
    "title": "Problem with Creating VM",
    "fileAttachmentHint": "null",
    "formElements": [
        {
            "id": "resourceGroup",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select Deployment Faied Resource Group",
            "watermarkText": "Choose an resource group",
            "content": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [{
						"value": "Unable to get the list of resource group",
						"text": "Unable to get the list of resource group."
					}
					],
            "required": true
        },{
            "id": "correlationId",
            "order": 2,
            "visibility": "resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Select Deployment Failure",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "dependOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/resourcegroups/{resourceGroup}/providers/Microsoft.Resources/deployments/?api-version=2018-05-01&$filter=provisioningState%20eq%20'Failed'&$top=10",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "correlationId",
                "textPropertyRegex": "[^/]+$"   
            },
            "dropdownOptions": [{
						"value": "Unable to get the list of Deployment Failure",
						"text": "Unable to get the list of Deployment Failure."
					}
					],
            "required": false
        }
    ]
}
---
