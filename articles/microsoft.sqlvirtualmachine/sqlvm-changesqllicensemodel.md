<properties
	pageTitle="licensing/changing sql licensing model"
	description="licensing/changing sql licensing model"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="yareyes"
	displayOrder=""
	articleId="970bab6b-86f0-4b9b-b2f8-3f37c6e9875d"
	selfHelpType="generic"
	supportTopicIds="32593728"
	resourceTags="WindowsSQL"
	productPesIds="14745"​
	cloudEnvironments="public"
/>

# licensing/changing sql licensing model

## **Recommended steps**

1. Switch your SQL license: The ability to switch between licensing models is a feature provided by the new SQL VM resource provider. The ability to convert the licensing model is currently only available when starting with a pay-as-you-go SQL Server VM image. If you start with a bring-your-own-license image from the portal, you will not be able to convert that image to pay-as-you-go. For detailed steps and restrictions: [How to change the licensing model for a SQL Server virtual machine in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-ahb).<br>

* Register to the new Resource Provider using Azure CLI. Note: It may take up to 5 minutes.
```
	az provider register --namespace Microsoft.SqlVirtualMachine
```

* Convert your virtual machine to AHUB.
```
	az sql vm create -n <VM Name> -g <Resource Group Name> -l <VM Location> --license-type AHUB
```

* Convert your virtual machine to PAYG.
```
	az sql vm create -n <VM Name> -g <Resource Group Name> -l <VM Location> --license-type PAYG
```

## **Recommended documents**

[Virtual Machines Licensing FAQ](https://azure.microsoft.com/en-us/pricing/licensing-faq/)<br>
[Install Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)<br>
[Azure SQL VM CLI](https://docs.microsoft.com/en-us/cli/azure/sql/vm?view=azure-cli-latest)

