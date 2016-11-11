<properties
	pageTitle="configuration and management/creating or deleting web app"
	description="configuration and management/creating or deleting web app"
	service="microsoft.web"
	resource="sites"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542209"
	resourceTags=""
	productPesIds="14748, 16170"
	cloudEnvironments="public"
/>

# configuration and management/creating or deleting web app

## **Recommended steps**
If you are unable to delete your App Service Plan please check if there are resources associated with the App Service Plan you are trying to delete. Remove all the associated entities from the plan and this should allow you to delete.

Another common issue is experiencing a 'Provisioning Failed' error while trying to create a web site with a name that had been previously deleted. Please follow the steps below to resolve the problem:

1. Connect to the new portal (portal.azure.com) with the Subscription ID where you created the web site originally.
2. Create a web site with the exact name that you are trying to create. This will connect a new website with the previously deleted site.
3. Go to the old portal (manage.windowsazure.com) and delete the site. This will delete whatever was left from the previous web site.
4. In the old portal create the web site again.

## **Recommended documents**
[The limits per App Service Plan are documented here](https://azure.microsoft.com/pricing/details/app-service/plans/)
