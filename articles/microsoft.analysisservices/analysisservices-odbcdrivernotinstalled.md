<properties
	pageTitle="'Driver' property doesn't correspond to an installed ODBC driver"
	description="'Driver' property doesn't correspond to an installed ODBC driver"
	service="microsoft.analysisservices"
	resource="servers"
	authors="bnmaa"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# 'Driver' property doesn't correspond to an installed ODBC driver

## **Recommended steps**

1. Open elevated cmd.exe and run `%windir%\system32\odbcad32.exe` to open 64bit ODBC Data Source Administrator.
2. Go to **Drivers** tab, make sure desired ODBC driver shows up.
3. If not, install 64-bit ODBC driver correctly.
4. Restart the gateway service.

## **Recommended documents**

[ODBC Data Source Administrator](https://docs.microsoft.com/sql/odbc/admin/odbc-data-source-administrator) <br />
[Viewing ODBC Drivers](https://docs.microsoft.com/sql/odbc/admin/viewing-drivers)
