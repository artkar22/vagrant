git push -u origin master
---------------------------------------
deploy na vagranta:
-umie�ci� paczk� z apk� do folderu vagranta
-git bash ->vagrant ssh -> 2x cd .. ->
sudo cp ../vagrant/myApp.war var/lib/tomcat8/webapps
---------------------------------------------------------------
java zmiana: 
cd etc/default 
nano tomcat7
JAVA_HOME=/usr/lib/jvm/openjdk-6-jdk -> JAVA_HOME=/usr/lib/jvm/java-8-oracle
---------------------------------------------------------------------
�cie�ki do apki: 
http://192.168.33.10:8080/myApp/