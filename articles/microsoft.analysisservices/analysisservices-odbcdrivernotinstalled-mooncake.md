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
	cloudEnvironments="MoonCake"
/>

# 'Driver' property doesn't correspond to an installed ODBC driver

## **Recommended steps**

1. Open elevated cmd.exe (run as administrator) and run **%windir%\system32\odbcad32.exe** to open the 64bit ODBC Data Source Administrator.
2. Go to **Drivers** tab, make sure the desired ODBC driver shows up.
3. If not, install the 64-bit ODBC driver correctly.
4. Restart the gateway service.

## **Recommended documents**

[ODBC Data Source Administrator](https://docs.microsoft.com/sql/odbc/admin/odbc-data-source-administrator) <br />
[Viewing ODBC Drivers](https://docs.microsoft.com/sql/odbc/admin/viewing-drivers)
