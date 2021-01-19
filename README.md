# cloudnative-quarkus
#### สร้าง Database

```
[linxianer12@localhost cloudnative-quarkus]$ oc -n openshift process mysql-persistent --parameters
NAME                    DESCRIPTION                                                             GENERATOR           VALUE
MEMORY_LIMIT            Maximum amount of memory the container can use.                                             512Mi
NAMESPACE               The OpenShift Namespace where the ImageStream resides.                                      openshift
DATABASE_SERVICE_NAME   The name of the OpenShift Service exposed for the database.                                 mysql
MYSQL_USER              Username for MySQL user that will be used for accessing the database.   expression          user[A-Z0-9]{3}
MYSQL_PASSWORD          Password for the MySQL connection user.                                 expression          [a-zA-Z0-9]{16}
MYSQL_ROOT_PASSWORD     Password for the MySQL root user.                                       expression          [a-zA-Z0-9]{16}
MYSQL_DATABASE          Name of the MySQL database accessed.                                                        sampledb
VOLUME_CAPACITY         Volume space available for data, e.g. 512Mi, 2Gi.                                           1Gi
MYSQL_VERSION           Version of MySQL image to be used (8.0, or latest).                                         8.0
```

oc new-app mysql-persistent -e MYSQL_USER=linxianer12 -e MYSQL_PASSWORD=cyberpunk2077 -e MYSQL_ROOT_PASSWORD=cyberpunk2077 -e MYSQL_DATABASE=subscription

oc new-app


