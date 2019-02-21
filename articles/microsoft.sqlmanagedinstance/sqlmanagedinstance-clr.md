<properties
	pageTitle="Development/SQL CLR development"
	description="Development/SQL CLR development"
	service="microsoft.sql"
	resource="servers"
	authors="rohitnayakmsft"
    ms.author="rohitna"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32594733"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public"
	articleId="f2b8c435-97ff-4c45-a810-f85ca6dddcd0"
/>

# SQL CLR development

## **Recommended Steps**

* Managed Instance cannot access file shares and Windows folders, so the following constraints apply:<br>

	* Only CREATE ASSEMBLY FROM BINARY is supported. See [CREATE ASSEMBLY FROM BINARY](https://docs.microsoft.com/sql/t-sql/statements/create-assembly-transact-sql)<br>
	* CREATE ASSEMBLY FROM FILE is not supported. See [CREATE ASSEMBLY FROM FILE](https://docs.microsoft.com/sql/t-sql/statements/create-assembly-transact-sql)<br>
	* ALTER ASSEMBLY cannot reference files. See [ALTER ASSEMBLY](https://docs.microsoft.com/sql/t-sql/statements/alter-assembly-transact-sql)<br>
