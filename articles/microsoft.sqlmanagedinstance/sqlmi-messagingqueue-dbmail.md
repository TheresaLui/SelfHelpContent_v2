<properties
  pagetitle="Database Mail&#xD;"
  description="Features/DbMail - server integration and sending emails."
  service="microsoft.sql"
  resource="servers"
  ms.author="jovanpop,sasapopo"
  selfhelptype="Generic"
  supporttopicids="32637260"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="b4b29aa5-b456-4913-ac94-44440bdcb02c"
  ownershipid="AzureData_AzureSQLMI" />
# Database Mail 

Azure SQL Database - Managed Instance enables you to directly send email messages to external email servers using [sp_send_dbmail](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-send-dbmail-transact-sql) procedure or via SQL Agent Jobs as [alerts](https://docs.microsoft.com/azure/sql-database/sql-database-job-automation-overview#job-notifications). Learn more about [Database Mail here](https://docs.microsoft.com/sql/relational-databases/database-mail/database-mail).

## **Recommended Steps**

If you experience issues sending emails or alerting, the following sections can help you troubleshoot the issue.

### Database mail

For issues sending email messages:

- Make sure that the options **Database Mail XPs** and **show advanced options** are enabled in [sys.configurations](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-configurations-transact-sql) view.
- Make sure that you use [supported syntax for Database Mail](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#database-mail-db_mail). Windows Authentication and attachments are not supported.
- If you get the error "Msg 22050, Level 16, State 1", see [known issue with **@query** parameter](https://docs.microsoft.com/azure/azure-sql/database/doc-changes-updates-release-notes?tabs=managed-instance#procedure-sp_send_dbmail-may-transiently-fail-when--parameter-is-used).

- Try to reach the mail server from a Managed Instance using SQL Agent Job that tests the network connection:

   1. Create a SQL Agent job that has one PowerShell task that runs a command like `tnc smtp.sendgrid.net -Port 25`. Run the job and check the job output in the job history. This is a public mail server that you should be able to reach from your Managed Instance, unless you have explicitly blocked that name and/or port. If the job step fails, review your networking configuration or create a support ticket under the **Availability and Connectivity**/*Virtual network or subnet configuration* category.
   2. If the previous step succeeded, replace the name of the mail server and port in the job with the mail server and port you're using, and repeat the previous step. Run `tnc YOUR_EMAIL_SERVER -Port -YOUR_EMAIL_SERVER_PORT` in the SQL Agent Job on Managed Instance. If the job step fails, review your networking configuration, or create a support ticket under **Availability and Connectivity**/*Virtual network or subnet configuration* category.
   3. Make sure that you enabled the port that communicates with the email server. Add the Port in the [Outbound security rules](https://docs.microsoft.com/azure/virtual-network/tutorial-filter-network-traffic#create-security-rules) of the Network Security Group that controls access to your Managed Instance.

- Check the status of email messages sent with database mail in the [Database Mail Log](https://docs.microsoft.com/sql/relational-databases/database-mail/check-the-status-of-e-mail-messages-sent-with-database-mail), [msdb.dbo.sysmail_event_log](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-event-log-transact-sql), [msdb.dbo.sysmail_faileditems](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-faileditems-transact-sql), [msdb.dbo.sysmail_allitems](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-allitems-transact-sql), [msdb.dbo.sysmail_sentitems](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-sentitems-transact-sql), and [msdb.dbo.sysmail_unsentitems](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-unsentitems-transact-sql)

- Make sure that you configured the email profile with the correct email server name, IP address, port, and account information (username and password). Check for known issues and limitations in the [Azure SQL Database documentation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#database-mail) that might cause the issue.
- Verify your email configuration (credentials, mail server and port) with the following PowerShell script. If you can send an email with the script, you configuration is correct.

```
{
$anonUsername = "<user@email.com>"
$anonPassword = ConvertTo-SecureString -String "<password>" -AsPlainText -Force
$anonCredentials = New-Object System.Management.Automation.PSCredential($anonUsername,$anonPassword)
Send-MailMessage -smtpServer <mail_server> -to "<test@email.com>" -from $anonUsername -subject "Test subject" -credential $anonCredentials -Port <mail_server_port>
}
```

- Script the email profile that you use on Managed Instance, set up the identical email profile on SQL Server, and try to send the email there. If possible, try to place the SQL Server in Azure Virtual machine in the same VNet where you placed your Managed Instance (in the different subnet) to ensure that you have similar networking environment.

- Check if there are any known issues in [Azure SQL Database documentation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#database-mail)

- Find more information in [Troubleshooting Database Mail](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms188663%28v=sql.105%29).

### SQL Agent email alerts

For issues sending email alerts from SQL Agent:

- Make sure that you have an email profile called **[AzureManagedInstance_dbmail_profile](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent)**. The profile must have this specific name to bind the SQL Agent with Database Mail. If this profile is missing, you can see errors like "profile name is not valid [SQLSTATE 42000] Error 14607".

- Send a test email using the [sp_send_dbmail](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-send-dbmail-transact-sql) procedure on **AzureManagedInstance_dbmail_profile** profile with T-SQL script
- Repeat the steps from the previous section to troubleshoot the potential database email issues
- Check if there are any [SQL Agent limitations](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent) causing this issue

## **Recommended Documents**

- [Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/database-mail)
- [Configure Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/configure-database-mail)
- [Troubleshooting Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/database-mail-general-troubleshooting)
