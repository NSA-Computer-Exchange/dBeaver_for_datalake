# dBeaver_for_datalake
dBeaver Setup Instructions


	1. Download dBeaver Community from here
	https://dbeaver.io/download

	2. Install dBeaver on your PC or workstation or server

	3. Create a working folder on your system. IE: C:\projects\datalake\

	4. Download the Infor Compass JDBC driver from your Infor Tenant

IONDesk > Configuration > Downloads



	5. Save the JDBC driver to your working folder

	6. Create a Backend Service

Infor ION API > Authorized Apps > Non-Infor New Authorized App > Backend Service



	7. Download the IONAPI Credentials




	• In the Download Credentials Dialog
	• Select Create Service Account
	• Enter a user from the list of users in InforOS Users.  




	• Download and save the file to your working folder
	
	• ** Save or rename the file as indicated below **
		Infor Compass JDBC Driver.ionapi

	8. Open the dBeaver application and create a database driver

	• On the menu bar select Database > Driver Manager > New
	• Fill in the following information:
	
	Driver Name: Infor Datalake
	Driver Type: Generic
	Class Name: com.infor.idl.jdbc.Driver
	URL Template: jdbc.infordatalake://<tenant name>:.




	Select the Libraries Tab:

	• Click Add File
		Browse for and select the infor-compass-jdbc-20xx-xx.jar driver file
	• Click Add Folder
		Select your working folder (the folder holding your JDBC driver file)

	• Click Ok:


	• The Infor Datalake driver is now added to the Driver Manager
	• Click Close

	9. Back in dBeaver select Database from the menu.
	• Select  New Database Connection

	• Scroll and look for the Infor Datalake from the grid.



	• Click Next 
	• Click Connection details (name, type…)

	• Change Connection name to Infor DataLake
	• Click Test Connection





Once the test succeeds, click OK > Finish

	10. To execute an SQL query,
	• Select and expand the Infor DataLake connection from the Database Navigator Pane
	• Expand the default node
	• Right click the default node 
	• Select SQL Editor > New SQL Script

In the <Infor DataLake > Script pane type your SQL query 

Example:              SELECT TOP 50 * FROM ARSC

Right Click anywhere in the SQL script pane and select  Execute > Execute SQL Statement

=======================================================================================
![image](https://user-images.githubusercontent.com/15594519/133474386-65bd440c-602d-411e-85ef-343e32c4b921.png)
