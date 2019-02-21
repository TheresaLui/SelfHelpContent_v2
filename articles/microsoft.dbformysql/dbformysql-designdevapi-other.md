<properties
	pageTitle="Dummy article for Azure Database for MySQL servers"
	description="This is a dummy article for Azure Database for MySQL servers"
	service=""
	resource=""
	authors="yanyan-lu"
    ms.author="yanylu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628394"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="a62e01be-d188-4e8b-8c41-85d1ba61e66d"
/>


User permissions for database user are managed through the MySQL built-in user management capabilities. Please note that super user acess cannot be granted in the managed service. For more information on how to manage users and roles in MySQL, please refer to the public MySQL community edition documentation for the MySQL version you are using.

## **Recommended Documents**

* [Create users in Azure Database for MySQL] (https://docs.microsoft.com/azure/mysql/howto-create-users)
* [How to connect applcations to Azure Database for MySQL](https://docs.microsoft.com/en-us/azure/mysql/howto-connection-string)
* [Configure SSL connectivity in your application](https://docs.microsoft.com/azure/mysql/howto-configure-ss)

There are several use cases where you will see your VM scheduled for maintenance after you have already completed your maintenance-redeploy:
* You VM was service healed to another node, which has not been updated yet, due to a hardware fault.
* You stopped (deallocated​) and restarted the VM, and it landed on a host that was not updated.
* You have auto shutdown set on the VM, and when it restarted, it was placed on a host that was not yet updated.
