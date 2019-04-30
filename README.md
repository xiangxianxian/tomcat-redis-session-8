# tomcat-redis-session-8

#[root@localhost tomcat9001]# cd conf/context.xml 配置 
<!-- 
com.orangefunction.tomcat.redissessions 是自定义maven项目的报名路径，切需要与maven 中 RedisSessionManager的serializationStrategyClass值一致
-->
 
<!-- redis session 共享配置 -->
<Valve className="com.orangefunction.tomcat.redissessions.RedisSessionHandlerValve" />  
<Manager className="com.orangefunction.tomcat.redissessions.RedisSessionManager"  
    host="127.0.0.1"  
    port="6379"  
    database="0"  
    maxInactiveInterval="60" />
