<properties
	pageTitle="Messaging and queuing/Service broker"
	description="Messaging and queuing/Service broker, query notifications"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637305"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="16ea70ec-9b16-446a-8861-5a61f72ccc2a"
	ownershipId="AzureData_AzureSQLMI"
/>

# Service broker and Query Notifications

[Service broker](https://docs.microsoft.com/sql/database-engine/configure-windows/sql-server-service-broker?toc=%2Fazure%2Fsql-database%2Ftoc.json) technology in Managed Instance enables you to implement native and reliable in-database asynchronous message passing functionalities.

## **Recommended Steps**

If you are experiencing some issues with Service Broker or Query notifications, some of the following steps might help you to troubleshoot the issues:

- Look at the [known issues and limitations](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#service-broker) and check are you using some unsupported syntax or feature. As an example, cross-instance message passing or [Event notifications](https://docs.microsoft.com/sql/relational-databases/service-broker/event-notifications?view=sql-server-2017) are not supported.
- Check the status of the messages in `sys.transmission_queue` view.
- If you are using message passing with encryption, make sure that you have setup database encryption keys.
- Try to identify some issues in error log such as `Message Service Broker needs to access the master key in the database`.
- Monitor Service Broker using [XEvents](https://docs.microsoft.com/sql/relational-databases/event-classes/broker-event-category)
- Use Profiler to track the following events: `Broker/Broker:Conversation`, `Broker/Broker:Message Undeliverable` and `Broker/Broker:Remote Message Acknowledgement`.
- Make sure that you implement retry-logic in the application code that handles Query Notifications. Depending on the value of [SqlNotificationInfo](https://docs.microsoft.com/dotnet/api/system.data.sqlclient.sqlnotificationinfo) in [SqlNotificationEventArgs](https://docs.microsoft.com/dotnet/api/system.data.sqlclient.sqlnotificationeventargs) you need to handle events such as `Error` or `Restart` and retry the query.
- If the messages are sent but the activation procedure is not triggered, check does the user who is authorized to run the procedure has enough permission. As a temporary solution try to assign more permission to the user using `ALTER AUTHORIZATION ON DATABASE::<database name> TO <login name>` or set `ALTER DATABASE <database name> SET TRUSTWORTHY ON` to see would this resolve the issue.

## **Recommended Documents**

- [Service broker in Managed Instance](https://docs.microsoft.com/sql/database-engine/configure-windows/sql-server-service-broker?toc=%2Fazure%2Fsql-database%2Ftoc.json)
