# How to get data from JDBC

The JDBC provider uses the **[JDBC API](http://www.oracle.com/technetwork/java/overview-141217.html)** to query a database.

In order to get data from a database, you need to:

1. Install a compatible driver
2. Configure a connection to a database
3. Create a data source from a table

Note that the drivers are not distributed with JDemetra+ because they are numerous and their licenses may conflict with each other.

## Install a JDBC driver 
To connect to a database, you need to install its specific driver first. This operation is done once per database type.

Open the context menu of the `JDBC resource` node in the `Providers Window` tab and click on `Configure` to manage the drivers. 

![Configure JDBC resouce](/images/configure_jdbc_resource.png)
 
Expand the `Databases` node, open the context menu of the `Drivers` node and click on `New Driver…` to configure a new driver.

![Add new driver](/images/add_new_driver.png)
 
Click on the `Add…` button and select a driver in your file system (i.e. `jtds-ntlmauth-1.3.1.0.jar`) and click on the `Ok` button to close the dialog.

![Driver wizard](/images/driver_wizard.png)
 
## Create a connection to a database
To retrieve data, you need to create a connection to an instance of a database.

First, select the right driver (`jTDS` in this example), open its context menu and click on `Connect Using…`.

![Connect using driver](/images/connect_using_driver.png)
 
Then, fill in the form with your specific parameters.

![Connection wizard](/images/connection_wizard.png)

Click on the `Test Connection` button to check your configuration.
Click on the button `Next` to go to the next pages of the wizard where you can select the default schema and give a name to the new connection.
 
## Create a data source from a table
Open the context menu of your connection node (`DemoSQLServer` in this example) and click on `Open as JDemetra+ DataSource`.
 
![Open connection as datasource](/images/open_connection_as_datasource.png)
 
Fill in the form with your specific parameters.
 
![JDBC datasource open dialog](/images/jdbc_datasource_open_dialog.png)

Click `OK` and this new data source should be available in the `Providers Window` tab.
 
## Troubleshooting

### IOException after JDemetra+ restart
 
![Closed connection](/images/closed_connection.png)

The JDBC provider does not automatically restore the connections to the databases when JDemetra+ starts. Therefore, you need to go to the `Service` tab, open the context menu of the connection you wish to use and click on `Connect…`.

![Open connection](/images/open_connection.png)
 
Open the context menu of your failing data source and click on `Reload`.
 
![Reload JDBC datasource](/images/reload_jdbc_datasource.png)
