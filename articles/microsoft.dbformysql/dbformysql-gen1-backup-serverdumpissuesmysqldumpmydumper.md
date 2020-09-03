<properties
    pageTitle="Issues with backup using mysqldump and mydumper"
    description="Issues with backup using mysqldump and mydumper"
    service="microsoft.dbformysql"
    resource="servers"
    authors="mksuni"
    ms.author="sumuth"
    displayOrder="110"
    selfHelpType="generic"
    supportTopicIds="32747585"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a8300a93-870a-4396-a250-5eae34feacf3"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Issues with backup using mysqldump and mydumper
You can backup your databases using mysqldump and mydumper and then restore it on to Azure Database for MySQL Single server.
## **Recommended steps**
* Check if the version of **mysqldump** or **mysqldumper** to make sure they are the same version as that of MySQL Single or Flexible server.

* Checkout all known issues for [mydumper](https://github.com/maxbube/mydumper/issues) and if your issue is related to any of those.

* If you are getting an error like *MySQL has gone away*  or *Lost connection to MySQL server during query* during the backup, it could be timing out if the data being backup is large. You should increase the **max_allowed_packet**, **net_write_timeout**, **net_read_timeout** values to appropriate levels to fix the error. See [how to configure server parameters in portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters). This applies to both **mysqldump** and **mydumper**.

* If you get **access denied** error when trying to run the command, check if you client machine has access. Review firewall configuration of your [Single server](https://docs.microsoft.com/azure/mysql/howto-manage-firewall-using-portal).

## **Recommended documents**
* [How to configure server parameters in portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters).
* [MyDumper documentation](https://github.com/maxbube/mydumper)
* [mysqldump documentation](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)


