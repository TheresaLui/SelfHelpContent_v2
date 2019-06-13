<properties
	pageTitle="Features/Linked server"
	description="Features/Linked server."
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
	ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637270,32637271"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public"
	articleId="c3892e31-23ea-4afa-827c-b6c4dbd34ce3"
/>

# Linked server

Azure SQL Database - Managed Instance enables you to directly execute the queries on other Managed Instances, Azure SQL Single Databases, and SQL Servers using [Linked server technology](https://docs.microsoft.com/sql/relational-databases/linked-servers/linked-servers-database-engine?toc=%2Fazure%2Fsql-database%2Ftoc.json).

## **Recommended Steps**

If you are experiencing some issues with querying remote data using linked servers, the following steps can help you to find a way to troubleshoot the issues.

- Check the [linked server constraints](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#linked-servers) in Managed Instances to identify are you using some unsupported feature (for example, connection to unsupported data sources).
- Check are the options 'remote access' and 'show advanced options' enabled in `sys.configurations` view.
- Check have you correctly created the linked server with the correct remote server name/IP address, port, and account information (username and password).
- Make sure that you are using SQL Server Authentication because Linked server in Managed Instance cannot use Windows or Azure Active Directory authentication.
- Check whether you can reach the remote server from Managed Instance.

  - Create SQL Agent job that has one PowerShell task that executes command like `tns <remote-server> -1433`, run the job and check the job output in the job history.
  - Check have you enabled the port that is used to communicate with the remote server. Port should be added in the [Outbound security rules](https://docs.microsoft.com/azure/virtual-network/tutorial-filter-network-traffic#create-security-rules) of the Network Security Group that controls the access to your Managed Instance.

- Check are you using `DISTRIBUTED TRANSACTION` because [MS DTC is not supported](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#distributed-transactions) in Managed Instance.
- Script the linked server that you are using on Managed Instance, setup the identical linked server  on SQL Server and try to run the query there. If possible, try to place SQL Server in Azure Virtual machine in the same VNet where your Managed Instance is placed (in the different subnet) to ensure that you have similar networking environment.

## **Recommended Documents**

- [Linked server](https://docs.microsoft.com/sql/relational-databases/linked-servers/linked-servers-database-engine?toc=%2Fazure%2Fsql-database%2Ftoc.json)
