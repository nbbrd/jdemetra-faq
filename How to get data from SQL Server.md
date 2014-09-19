# How to get data from SQL Server

## Install the JDBC driver for SQL server
Open the context menu of the `JDBC resource` node in the `Providers Window` tab and click on `Configure` in order to manage the JDBC drivers. Note that this operation is done once.

![Configure JDBC resouce](/images/configure_jdbc_resource.png)
 
Expand the `Databases` node, open the context menu of the `Drivers` node and click on `New Driver…` in order to configure a new JDBC driver.

![Add new driver](/images/add_new_driver.png)
 
Click on the `Add…` button and select the file named `jtds-ntlmauth-1.3.1.0.jar` (Note that you need to download it first) and click on the `Ok` button to close the dialog.

![Driver wizard](/images/driver_wizard.png)
 
## Create a connection to a database
Open the context menu of the `jTDS` node and click on `Connect Using…`.

![Connect using driver](/images/connect_using_driver.png)
 
Fill in the form with your specific parameters.

![Connection wizard](/images/connection_wizard.png)

Under Windows, the JDBC driver uses the user’s credential so you don’t need to fill in the user/password fields. 
Click on the `Test Connection` button to check your configuration.
Click on the button `Next` to go to the next pages of the wizard where you can select the default schema and give a name to the new connection.
 
## Create a data source from a table
Open the context menu of your connection node (DemoSQLServer in this example) and click on `Open as JDemetra+ DataSource`.
 
![Open connection as datasource](/images/open_connection_as_datasource.png)
 
Fill in the form with your specific parameters.
 
![JDBC datasource open dialog](/images/jdbc_datasource_open_dialog.png)
 
## Troubleshooting

### IOException after JDemetra+ restart
 
![Closed connection](/images/closed_connection.png)

The JDBC provider does not automatically restore the connections to the databases when JDemetra+ starts. Therefore, you need to go to the `Service` tab, open the context menu of the connection you wish to use and click on `Connect…`.

![Open connection](/images/open_connection.png)
 
Open the context menu of your failing data source and click on `Reload`.
 
![Reload JDBC datasource](/images/reload_jdbc_datasource.png)
