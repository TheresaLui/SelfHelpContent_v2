<properties
    pageTitle="How can you define custom alerts for when certain thresholds are reached"
    description="How can you define custom alerts for when certain thresholds are reached"
    service="scalesets"
    author="negat"
    displayOrder="21"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How can you define custom alerts for when certain thresholds are reached?


You have some flexibility how you handle alerts; for example you can define customized webhooks like this example from a Resource Manager template:
```json
   {
         "type": "Microsoft.Insights/autoscaleSettings",
	       "apiVersion": "[variables('insightsApi')]",
	             "name": "autoscale",
		           "location": "[parameters('resourceLocation')]",
			         "dependsOn": [
				         "[concat('Microsoft.Compute/virtualMachineScaleSets/', parameters('vmSSName'))]"
				 ],
				 "properties": {
				         "name": "autoscale",
					 "targetResourceUri": "[concat('/subscriptions/',subscription().subscriptionId, '/resourceGroups/',  resourceGroup().name, '/providers/Microsoft.Compute/virtualMachineScaleSets/', parameters('vmSSName'))]",
					 "enabled": true,
					 "notifications": [{
					 		  "operation": "Scale",
							  "email": {
							  	   "sendToSubscriptionAdministrator": true,
							  	   "sendToSubscriptionCoAdministrators": true,
							  	   "customEmails": [
							  		  "youremail@address.com"
							  	   ]},
							  "webhooks": [{
									"serviceUri": "https://events.pagerduty.com/integration/0b75b57246814149b4d87fa6e1273687/enqueue",
									"properties": {
										"key1": "custommetric",
										"key2": "scalevmss"
									}
									}
							  ]}],
```

In this example, an alert goes to Pagerduty when a threshold is reached.


