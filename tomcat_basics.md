Mostly used for `java` applications.

```
yum install java-1.8.0-openjdk-devel

wget https://downloads.apache.org/tomcat/tomcat-8/v8.5.53/bin/apache-tomcat-8.5.53.tar.gz

tar xvf apache-tomcat-8.5.53.tar.gz

./apache-tomcat-8.5.53/bin/startup.sh
```

Once up, it is available on `8080` on `localhost`

Configuration files are in `apache-tomcat-8.5.53/conf`

Port `8080` is configured through `conf/server.xml` 

Logs are in `apache-x/logs`

App logic will be present in `apache-x/webapps`

---

If you have a `.war` file -- just put it in `apache-x/webapps`. Apache will take care of extracting it automatially.

Such extractions can be seen in logs at `apache-x/logs/catalina.out`

---

