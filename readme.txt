git push -u origin master
---------------------------------------
deploy na vagranta:
-umie�ci� paczk� z apk� do folderu vagranta
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
�cie�ki do apki: 
http://192.168.33.10:8080/myApp/
-----------------------------------------------------------------
ustawianie debuggera :
vagrant ssh
2x cd ..
cd usr/share/tomcat8/bin
utworzy� plik setenv.sh
doda� do niego linijk�: export JPDA_OPTS="-agentlib:jdwp=transport=dt_socket, address=8000, server=y, suspend=n" //(sudo vi setenv.sh)
edycja startup.sh//(sudo vi startup.sh)
w ostatniej lini podmieni� exec "$PRGDIR"/"$EXECUTABLE" start "$@" na exec "$PRGDIR"/"$EXECUTABLE" jpda start "$@" //doda� po prostu jpda