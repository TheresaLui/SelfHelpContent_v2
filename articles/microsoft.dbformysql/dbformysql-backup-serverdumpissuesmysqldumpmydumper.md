<properties
    pageTitle="Issues with backup using mysqldump and myDumper"
    description="Issues with backup using mysqldump and myDumper"
    service="microsoft.dbformysql"
    resource="servers"
    authors="mksuni"
    ms.author="sumuth"
    displayOrder="530"
    selfHelpType="generic"
    supportTopicIds="32747992"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="88598dd7-c578-4b47-b8ea-6b9f7b61748e"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Issues with backup using mysqldump and myDumper

You can backup your databases using mysqldump and myDumper and then restore it on to Azure Database for MySQL Single server or Flexible server.

## **Recommended Steps**

* Check if the version of **mysqldump** or **mysqldumper** to make sure they are the same version as that of MySQL Single or Flexible server
* Checkout all known issues for [myDumper](https://github.com/maxbube/myDumper/issues) and if your issue is related to any of those
* If you are getting an error like *MySQL has gone away*  or *Lost connection to MySQL server during query* during the backup, it could be timing out if the data being backup is large. You should increase the **max_allowed_packet**, **net_write_timeout**, **net_read_timeout** values to appropriate levels to fix the error. See [how to configure server parameters in portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters). This applies to both **mysqldump** and **myDumper**.
* If you get **access denied** error when trying to run the command, check if you client machine has access. Review firewall configuration of your [Single server](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal) or [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-firewall-portal#create-a-firewall-rule-after-server-is-created).

## **Recommended Documents**

* [MyDumper documentation](https://github.com/maxbube/myDumper)
* [mysqldump documentation](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)
