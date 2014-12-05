# How to get data from SQL Server

SQL Server is accessed through the JDBC provider.

As explained in the JDBC provider [documentation](How%20to%20get%20data%20from%20JDBC.md), you need to install a driver in order to connect to an instance of the database. There are several drivers available for free but if you don't know which one to choose, download this one: [jtds-ntlmauth-netbeans](https://github.com/nbbrd/jtds-ntlmauth-netbeans/releases).

This driver is distributed as a plugin compatible with JDemetra+ and therefore should simplify its installation. It also uses the Windows authentification (NTLM) to connect to an instance of SQL Server, thus freeing the users from typing their credentials.
