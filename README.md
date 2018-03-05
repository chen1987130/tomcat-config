# tomcat-config
JVM配置 <br/>
JAVA_OPTS="-Xms4096m -Xmx4096m -Xmn512m -XX:PermSize=256m -XX:MaxPermSize=256m -XX:+UseConcMarkSweepGC -XX:+UseCMSCompactAtFullCollection -XX:CMSInitiatingOccupancyFraction=70 -XX:+CMSParallelRemarkEnabled -XX:SoftRefLRUPolicyMSPerMB=0 -XX:+CMSClassUnloadingEnabled -XX:SurvivorRatio=8  -XX:+DisableExplicitGC" <br/>
 <br/>
tomcat优化 <br/>
\<Executor name="tomcatThreadPool" namePrefix="catalina-exec-" maxThreads="2048" minSpareThreads="25" maxIdleTime="60000"/> <br/>
<br/>
\<Connector executor="tomcatThreadPool" port="8080" protocol="HTTP/1.1" connectionTimeout="20000" enableLookups="false" 
           acceptCount="1024" redirectPort="8443" compression="on" compressionMinSize="2048" 
	         compressableMimeType="text/html,text/xml,text/javascript,text/css,text/plain"
	         server="FNApache/1.0" maxKeepAliveRequests="1000" URIEncoding="UTF-8"/> <br/>
