[root@ip-172-31-44-19 tmp]# sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-37-209.eu-central-1.compute.internal -utemp -ptemp --scm-host ip-172-31-44-19.eu-central-1.compute.internal scm scm scm
JAVA_HOME=/usr/java/jdk1.8.0_152
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.8.0_152/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!
