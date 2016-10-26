<properties
	pageTitle="open source technologies/mysql"
	description="open source technologies/mysql"
	service="microsoft.web"
	resource="sites"
	authors="cts-shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32444077"
	resourceTags=""
	productPesIds="14748, 16170"
	cloudEnvironments="public"
/>

# Open Source Technologies/MySQL

## **Recommended steps**
Issue: You see errors: "Error connecting to database" or "Error establishing a database connection" on your site or you see an "Invalid Settings" message when connecting to MySQL In App through PHPMyAdmin. 

Resolution: 

1. Login into Azure Portal, Browse to your App Service and under Settings section choose Application Settings.
2. Add a key value entry in App Settings like below:

    
    key:      WEBSITE_MYSQL_ARGUMENTS <br>
    value:   --default_password_lifetime=0 
    

For more information, please visit the forum post [here](http://bit.ly/2dXlqMy). 


## **Recommended documents**

[Announcing Azure App Service MySQL in-app (preview)](https://azure.microsoft.com/blog/mysql-in-app-preview-app-service/)<br>
[MySQL in-app Wiki](https://github.com/projectkudu/kudu/wiki/MySQL-in-app-(preview))<br>