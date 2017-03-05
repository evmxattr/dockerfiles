FROM ubuntu:14.04

RUN \
  echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  apt-get update && \
  apt-get install -y software-properties-common && \
  add-apt-repository -y ppa:webupd8team/java && \
  apt-get install -y libgtk2.0-0 libxtst6 && \
  apt-get update && \
  apt-get install -y oracle-java8-installer && \
  apt-get --purge autoremove -y software-properties-common && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/* && \
  rm -rf /var/cache/oracle-jdk8-installer

WORKDIR /opt/burp

ENV JAVA_HOME /usr/lib/jvm/java-8-oracle

CMD ["java", "-jar", "/opt/burp/burp.jar"]
