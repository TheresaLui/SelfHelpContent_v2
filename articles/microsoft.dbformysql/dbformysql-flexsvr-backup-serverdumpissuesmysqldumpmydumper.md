<properties
    pageTitle=""
    description=""
    service="microsoft.dbformysql"
    resource="servers"
    authors=""
    ms.author=""
    displayOrder="120"
    selfHelpType="generic"
    supportTopicIds="32747637"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="9f6ab11f-d9a6-426d-8854-51849d8016f1"
/>

# Issues with backup using mysqldump and mydumper
[!Note]  **Flexible Servers is in public preview**

You can backup your databases using mysqldump and mydumper and then restore it on to Azure Database for MySQL Flexible server.

## **Recommended steps**
* Check if the version of **mysqldump** or **mysqldumper** to make sure they are the same version as that of MySQL Flexible server.

* Checkout all known issues for [mydumper](https://github.com/maxbube/mydumper/issues) and if your issue is related to any of those.

* If you are getting an error like *MySQL has gone away*  or *Lost connection to MySQL server during query* during the backup, it could be timing out if the data being backup is large. You should increase the **max_allowed_packet**, **net_write_timeout**, **net_read_timeout** values to appropriate levels to fix the error. See [how to configure server parameters in portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters). This applies to both **mysqldump** and **mydumper**.

* If you get **access denied** error when trying to run the command, check if you client machine has access. Review firewall configuration of your [Flexible server](https://docs.microsoft.com/en-us/azure/mysql/flexible-server/how-to-manage-firewall-portal#create-a-firewall-rule-after-server-is-created)

## **Recommended documents**
* [How to configure server parameters in portal](https://docs.microsoft.com/azure/mysql/howto-server-parameters).
* [MyDumper documentation](https://github.com/maxbube/mydumper)
* [mysqldump documentation](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)


