# How to get data from ODBC

The ODBC provider uses the **ODBC-JDBC Bridge** to query a database.

Unfortunatly, **this solution is no more viable**. This bridge has two big problems:

1. Starting with Java SE 8, the JDBC-ODBC Bridge is [no longer included with the JDK](http://docs.oracle.com/javase/7/docs/technotes/guides/jdbc/bridge.html).  
2. The 64bit version of the JDBC-ODBC Bridge [throws exceptions randomly](https://bugs.openjdk.java.net/browse/JDK-8038751).  

Therefore, the ODBC provider is disabled in each case.

It is recommend to [use a JDBC driver](How%20to%20get%20data%20from%20JDBC.md) provided by the vendor of your database or a commercial JDBC Driver instead of the JDBC-ODBC Bridge.

## Migration to JDBC

If you are currently using the ODBC provider, you should migrate as soon as possible to the [JDBC provider](How%20to%20get%20data%20from%20JDBC.md).

Here is a quick migration plan:

1. List the DSN currently used
2. Identify the drivers used by ODBC (launch `odbcad32.exe`)
3. Download the counterparts JDBC drivers
5. Install the JDBC drivers into JDemetra+
6. Create a connection for each DSN
7. Replace the previous data sources with new ones

