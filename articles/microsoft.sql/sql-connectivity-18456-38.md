<properties
	pageTitle="Login failed - User missing or orphaned user"
	description="Login failed because the provided login does not have a corresponding user inside the database"
	infoBubbleText="We ran diagnostics on your resource and found that login failed because the provided login does not have a corresponding user inside the database"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_38"
	diagnosticScenario="SqlConnectivity"
	selfHelpType="diagnostics"
	supportTopicIds="32630429"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
/>
# Login failed - User missing or orphaned user

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> we were able to detect login failures:<br>
<!--$FailedLogins18456State38--> FailedLogins18456State38 <!--/$FailedLogins18456State38-->
<!--/issueDescription-->
<br>
The error returned indicated that the corresponding user does not exist inside the database, or the database user is orphaned due to a SID mapping mismatch between the user and the login in master.
<br>

## **Recommended Steps**

1. Compare SQL logins in the master database with users in the user database.

a) Open a connection to the master database. Execute the following T-SQL to return a list of configured SQL logins in the master database:

```sql
SELECT [name], SID
FROM sys.sql_logins 
WHERE type = 'S';
```

b) Open a connection to the user database. Execute the following T-SQL to return a list of configured users in the user database:

```sql
SELECT [name], SID, principal_id
FROM sys.database_principals 
WHERE type = 'S' 
  AND name NOT IN ('guest', 'INFORMATION_SCHEMA', 'sys')
  AND authentication_type_desc = 'INSTANCE';
```

2. If the required user does not exist in the user database, add the user by executing the CREATE USER statement in the user database, specifying the login name:

```sql
CREATE USER <user_name> FOR Login <login_name>; 
```

3. If the requested user does exist in the user database, the error is likely due to an orphaned user. In this case, comparing the two lists from step 1 should reveal a SID mismatch between the login in the master database and the user in the user database.

To map an orphaned user to a login which already exists in master, execute the ALTER USER statement in the user database, specifying the login name:

```sql
ALTER USER <user_name> WITH Login = <login_name>;
```

## **Recommended Documents**

* [Create Users](https://docs.microsoft.com/sql/t-sql/statements/create-user-transact-sql/)

* [Troubleshoot Orphaned Users](https://docs.microsoft.com/sql/sql-server/failover-clusters/troubleshoot-orphaned-users-sql-server/)