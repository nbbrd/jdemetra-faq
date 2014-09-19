# How to get data from SQL Server

## Install the JDBC driver for SQL server
Open the context menu of the “JDBC resource” node in the “Providers Window” tab and click on “Configure” in order to manage the JDBC drivers. Note that this operation is done once.
 
Expand the “Databases” node, open the context menu of the “Drivers” node and click on “New Driver…” in order to configure a new JDBC driver.
 
Click on the “Add…” button and select the file named “jtds-ntlmauth-1.3.1.0.jar” (Note that you need to download it first) and click on the “Ok” button to close the dialog.
 
 
## Create a connection to a database
Open the context menu of the “jTDS” node and click on “Connect Using…”.
 
## Fill in the form with your specific parameters.
 
Under Windows, the JDBC driver uses the user’s credential so you don’t need to fill in the user/password fields. 
Click on the “Test Connection” button to check your configuration.
Click on the button “Next” to go to the next pages of the wizard where you can select the default schema and give a name to the new connection.
 
## Create a data source from a table
Open the context menu of your connection node (DemoSQLServer in this example) and click on “Open as JDemetra+ DataSource”.
 
## Fill in the form with your specific parameters.
 
 
## FAQ
IOException after JDemetra+ restart
 
The JDBC provider does not automatically restore the connections to the databases when JDemetra+ starts. Therefore, you need to go to the “Service” tab, open the context menu of the connection you wish to use and click on “Connect…”.
 
Open the context menu of your failing data source and click on “Reload”.
 
