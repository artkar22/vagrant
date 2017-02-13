git push -u origin master

sudo cp ../vagrant/SpringApp-1.0-SNAPSHOT.war var/lib/tomcat7/webapps

java zmiana: 
cd etc/default 
nano tomcat7
JAVA_HOME=/usr/lib/jvm/openjdk-6-jdk -> JAVA_HOME=/usr/lib/jvm/java-8-oracle