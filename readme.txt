git push -u origin master
---------------------------------------
deploy na vagranta:
-umieœciæ paczkê z apk¹ do folderu vagranta
-git bash ->vagrant ssh -> 2x cd .. ->
sudo cp ../vagrant/myApp.war var/lib/tomcat8/webapps

ALBO:
za pierwszym postawieniem vagranta:
2x cd ..
sudo cp ../vagrant/deploy.sh home/ubuntu/
a potem tylko vagrant ssh -> ./deploy.sh
---------------------------------------------------------------
java zmiana: 
cd etc/default 
nano tomcat7
JAVA_HOME=/usr/lib/jvm/openjdk-6-jdk -> JAVA_HOME=/usr/lib/jvm/java-8-oracle
---------------------------------------------------------------------
œcie¿ki do apki: 
http://192.168.33.10:8080/myApp/
-----------------------------------------------------------------
ustawianie debuggera :
/etc/default/tomcat6 
odkomentowaæ: JAVA_OPTS="${JAVA_OPTS} -Xdebug -Xrunjdwp:transport=dt_socket,address=8000,server=y,suspend=n"
//////////////////////////////
logi: /var/log/tomcat8/catalina.out 