<properties
	pageTitle="Creating Function Apps"
	description="Creating Function Apps"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,cts-shrahman"
    ms.author="shrahman, danzha"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32518043"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public"
/>

# Creating Function Apps

## **Recommended documents**

Azure Function Apps uses the Azure App Service infrastructure. A function app is the container that hosts the execution of individual functions. You can create a function app in [Azure Portal](https://docs.microsoft.com/azure/azure-functions/functions-create-function-app-portal),  or using script [Azure CLI](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function-azure-cli#create-a-function-app), or [Azure ARM template](https://docs.microsoft.com/azure/azure-functions/functions-infrastructure-as-code).  You can also choose to create a function app when deploy a function project from Visual Studio, Visual Studio Code.<br> 

If function app creation fails in Azure Portal, please reproduce the issue and capture F12 trace. For Azure CLI, please share the command that report error. For ARM deployment failure, you can find the error message in Azure portal -> Resource Group -> Deployments, please share the failed task Correlation ID, for further investigation.<br> 

Microsoft would recommend that you follow these steps.<br>
1. Check if this issue was raised in the [forums](https://social.msdn.microsoft.com/Forums/home?forum=azurefunctions).
2. Check if the issue was raised on Stack Overflow. 
3. Check if the issue was raised on [GitHub](https://github.com/Azure/azure-functions-host).
4. If there isn’t any matching discussion then please open an issue on [GitHub](https://github.com/Azure/azure-functions-host).