<properties
	pageTitle="Modify a template"
	description="Modify a template"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a30c4544-8077-4571-875a-8ccfdbe9b892"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Modify a template 

Modify the template by changing the storage account name and region. 

To deploy a template by using Azure portal: 

1. In the Azure portal, select Create a resource. 
2. In Search the Marketplace, type template deployment, and then press ENTER. 
3. Select Template deployment. 
4. Select Create. 
5. Select Build your own template in the editor. 
6. Select Load file, and then follow the instructions to load the template json file that you downloaded in the last section. 
7. In the template json file, name the target storage account by setting the default value of the storage account name. This example sets the default value of the storage account name to mytargetaccount. 

~~~json

                  'defaultValue': 'mytargetaccount',  

~~~

8. Edit the location property in the template.json file to the target region. This example sets the target region to centralus. 

~~~json

                'location': 'centralus'   

~~~

To obtain region location codes, see [Azure Locations](https://azure.microsoft.com/en-us/global-infrastructure/locations/) 