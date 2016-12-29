
You need to have the Apache Ant build tool correctly installed on your system
and the Apache Ivy dependency management plugin installed in Ant, to easily run 
this sample application. 

The Apache Ant build tool can be downloaded from this location:
http://ant.apache.org/
The Apache Ivy dependency management plugin can be downloaded from this location:
http://ant.apache.org/ivy/

Please follow their installing instructions to have Apache Ant and Apache Ivy 
working on your system before trying our sample application.

Once you have them installed, launch "ant -p" from the command line in this directory
to learn more about what tasks you could run to build and test the sample.


---------
This application is meant to display Reports designed in Jasper in a web application.
This application makes use of Servlets.

To design the report you need to install JasperSoftStudio (does not work on Windows 10), this 
reports in .JRXML format.

The demo folder consists of:

reports/ - Contains report files (in .jrxml format). The reports need a Northwind database created in PostgresSQL.
images/ - Contains images required by reports.
northwind.postgre.sql - Use this sql script to create the database schema and popluate the Northwind db for testing purpose.

To build:
1. Build source using ant :

ant compile 
ant war

2. Deploy webdemo.war file on Tomcat. (user:tomcat, password: tomcat)

3. When you launch the application web page:

Goto : Compile JRXML link in the menu on the left.
On the "compile JRXML" page:
Choose "Servlet Example" and click "execute". This will compile JRXML to .jasper format
GoTo "fill Report" page:
Choose "Servlet Example" and click "execute". This will fill the report with data from the datasource.
GoTo "export Report" page:
Choose "HTML Report->Servlet Example" and  click "execute". This will display the report in HTML.
