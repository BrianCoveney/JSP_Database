JSP_Database
============

Database name = users
users values  = id, email, password

Configure the JNDI DataSource in Tomcat by adding a declaration for your resource to your Context.
Copy and paste the following into    Servers > context.xml

<Resource name="jdbc/TestDB" auth="Container" type="javax.sql.DataSource"
               maxTotal="100" maxIdle="30" maxWaitMillis="10000"
               username="javauser" password="javadude" driverClassName="com.mysql.jdbc.Driver"
               url="jdbc:mysql://localhost:3306/javatest"/>
               
Get above from googling -> tomcat 8 jndi datasource
