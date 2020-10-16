<properties
	articleId="unable-to-see-the-volume-after-the-move"
	pageTitle="Unable to see the volume after the move"
	description="Unable to see the volume after the move"
	authors="b-mayada"
	ms.author="b-mayada"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777918"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to see the volume after the move
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to see the volume after the move",
    "fileAttachmentHint": "",
    "formElements": [
		{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
				{
            "id": "source_volume_resource_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Resource ID of the source volume",
            "watermarkText": "Select the volume and click on properties under Settings to get resource id",
            "required": true
        },
		{
            "id": "source_capacity_pool_service_level",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Service level of the source capacity pool",
            "watermarkText": "QoS type of the source capacity pool",
			"dropdownOptions": [
				{
                    "value": "Standard",
                    "text": "Standard"
                },
                {
                    "value": "Premium",
                    "text": "Premium"
                },
				                {
                    "value": "Ultra",
                    "text": "Ultra"
                }
					
			],
            "required": true
        },
		{
            "id": "source_capacity_pool_qos",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "QoS type of the source capacity pool",
            "watermarkText": "QoS type of the source capacity pool",
			"dropdownOptions": [
				{
                    "value": "Auto",
                    "text": "Auto"
                },
                {
                    "value": "Manual",
                    "text": "Manual"
                }							
			],
            "required": true
        },
				
		{
            "id": "destination_pool_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Destination capacity pool name",
            "watermarkText": "Destination capacity pool name",
            "required": true
        },
		{
            "id": "destination_pool_service_level",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Service level of the destination pool",
            "watermarkText": "Service level of the destination pool",
			"dropdownOptions": [
				{
                    "value": "Standard",
                    "text": "Standard"
                },
                {
                    "value": "Premium",
                    "text": "Premium"
                },
				                {
                    "value": "Ultra",
                    "text": "Ultra"
                }
					
			],
            "required": true
        },
				{
            "id": "destination_pool_qos",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "QoS type of the destination pool",
            "watermarkText": "QoS type of the destination pool",
			"dropdownOptions": [
				{
                    "value": "Auto",
                    "text": "Auto"
                },
                {
                    "value": "Manual",
                    "text": "Manual"
                }							
			],
            "required": true
        }
		
    ],
    "$schema": "SelfHelpContent"
}
---
