from java:11

copy . myjava  

workdir myjava

RUN apt-get install -y wget

RUN wget http://repos.fedorapeople.org/repos/dchen/apache-maven/epel-apache-maven.repo -O /etc/yum.repos.d/epel-apache-maven.repo

RUN sed -i s/\$releasever/6/g /etc/yum.repos.d/epel-apache-maven.repo

RUN yum install -y apache-maven

RUN mvn clean install

COPY ./target/onlinebookstore.war /usr/local/tomcat/webapps