<properties
	pageTitle="deployment/ftp"
	description="deployment/ftp"
	service="microsoft.web"
	resource="sites"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542213"
	resourceTags=""
	productPesIds="14748, 16170"
	cloudEnvironments="public"
/>

# deployment/ftp

## **Recommended steps**
Issue: FTP to Website fails

1. Please check that you are entering the correct host name and credentials
2. Please check that the ports are not blocked by a firewall
	1. FTP control connection port: 21  
	2. FTP data connection port: 989 , 10001-10300

## **Recommended documents**
[Accessing Files via FTP](https://github.com/projectkudu/kudu/wiki/Accessing-files-via-ftp)<br>
[File structure on azure](https://github.com/projectkudu/kudu/wiki/File-structure-on-azure)
