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

Azure SQL Database - Managed Instance enables you to directly send the email messages to the external email servers. You can send email messages directly using [sp_send_dbmail](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-send-dbmail-transact-sql) procedure or via SQL Agent Jobs as [alerts](https://docs.microsoft.com/azure/sql-database/sql-database-job-automation-overview#job-notifications). Learn more about [Database Mail here](https://docs.microsoft.com/sql/relational-databases/database-mail/database-mail).

## **Recommended Steps**

If you are experiencing issues with sending emails or alerting, the following sections can help you to find a way to troubleshoot the issues.

### Database mail

If you are the experiencing some issues with sending email messages, try some of the following troubleshooting steps:

- Check that the options 'Database Mail XPs' and 'show advanced options' enabled in [sys.configurations](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sys-configurations-transact-sql) view.
- Check that you are using [supported syntax for Database Mail](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#database-mail-db_mail). Windows Authentication and attachments are not supported.
- If you are getting error "Msg 22050, Level 16, State 1", see [known issue with **@query** parameter](https://docs.microsoft.com/azure/azure-sql/database/doc-changes-updates-release-notes?tabs=managed-instance#procedure-sp_send_dbmail-may-transiently-fail-when--parameter-is-used).
- Check you can reach the mail server from Managed Instance using SQL Agent Job that tests the network connection:

  - Create SQL Agent job that has one PowerShell task that executes command like **tnc smtp.sendgrid.net -Port 25**, run the job and check the job output in the job history. This is public mail server that should be reached from your Managed Instance, unless if you have explicitly blocked that name and/or port. If the job step fails review your networking configuration or create a support ticket under **Availability and Connectivity**/*Virtual network or subnet configuration* category.
  - If the previous step succeed, replace the name of the mail server and/or port in the job with the mail server and port that you are using and repeat the previous step by executing **tnc YOUR_EMAIL_SERVER -Port -YOUR_EMAIL_SERVER_PORT** in SQL Agent Job on Managed Instance. If the job step fails review your networking configuration or create a support ticket under **Availability and Connectivity**/*Virtual network or subnet configuration* category.
  - Check that you have enabled the port that is used to communicate with the email server. Port should be added in the [Outbound security rules](https://docs.microsoft.com/azure/virtual-network/tutorial-filter-network-traffic#create-security-rules) of the Network Security Group that controls the access to your Managed Instance.

- Check the status of email messages sent with database mail in [Database Mail Log](https://docs.microsoft.com/sql/relational-databases/database-mail/check-the-status-of-e-mail-messages-sent-with-database-mail), [msdb.dbo.sysmail_event_log](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-event-log-transact-sql), [msdb.dbo.sysmail_faileditems](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-faileditems-transact-sql), [msdb.dbo.sysmail_allitems](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-allitems-transact-sql), [msdb.dbo.sysmail_sentitems](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-sentitems-transact-sql), and [msdb.dbo.sysmail_unsentitems](https://docs.microsoft.com/sql/relational-databases/system-catalog-views/sysmail-unsentitems-transact-sql)
- Check have you correctly configured email profile with correct email server name/IP address, port, and account information (username and password). Check the known issues or limitation in [Azure SQL Database documentation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#database-mail) that might cause the issue.
- Verify your email configuration (credentials, mail server and port) with following PowerShell script. If you can send an email with the script, you configuration is correct.
{
$anonUsername = "<user@email.com>"
$anonPassword = ConvertTo-SecureString -String "<password>" -AsPlainText -Force
$anonCredentials = New-Object System.Management.Automation.PSCredential($anonUsername,$anonPassword)
Send-MailMessage -smtpServer <mail_server> -to "<test@email.com>" -from $anonUsername -subject "Test subject" -credential $anonCredentials -Port <mail_server_port>
}
- Script the email profile that you are using on Managed Instance, setup the identical email profile on SQL Server and try to send the email there. If possible, try to place SQL Server in Azure Virtual machine in the same VNet where your Managed Instance is placed (in the different subnet) to ensure that you have similar networking environment.
- Check are there any known issues in [Azure SQL Database documentation](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#database-mail)
- Find more information in [Troubleshooting Database Mail](https://docs.microsoft.com/previous-versions/sql/sql-server-2008-r2/ms188663%28v=sql.105%29) article

### SQL Agent email alerts

If you are the experiencing issues with sending email alerts from SQL Agent, try some of the following troubleshooting steps:

- Check that you have an email profile called **[AzureManagedInstance_dbmail_profile](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent)**, the profile must have this specific name in order to bind SQL Agent with Database Mail. If this profile is missing you can see errors like "profile name is not valid [SQLSTATE 42000] Error 14607."
- Try to send an email using [sp_send_dbmail](https://docs.microsoft.com/sql/relational-databases/system-stored-procedures/sp-send-dbmail-transact-sql) procedure on **AzureManagedInstance_dbmail_profile** profile with T-SQL script
- Repeat the steps from the previous section to troubleshoot the potential database email issues
- Check if there is any [SQL Agent limitations](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#sql-server-agent) causing this issue

## **Recommended Documents**

- [Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/database-mail)
- [Configure Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/configure-database-mail)
- [Troubleshooting Database Mail](https://docs.microsoft.com/sql/relational-databases/database-mail/database-mail-general-troubleshooting)