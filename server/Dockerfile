FROM openjdk:8-jre
ENV HZ_VERSION 3.10-SNAPSHOT
ENV HZ_HOME /opt/hazelcast/
RUN mkdir -p $HZ_HOME
WORKDIR $HZ_HOME
# Download hazelcast jars from maven repo.
ADD hazelcast-all-3.10-SNAPSHOT.jar $HZ_HOME
#ADD log4j.properties $HZ_HOME/log4j.properties
#ADD commons-lang3-3.3.1.jar $HZ_HOME/commons-lang3-3.3.1.jar
#ADD jsonevent-layout-1.7.jar $HZ_HOME/jsonevent-layout-1.7.jar
#ADD json-smart-2.3.jar $HZ_HOME/json-smart-2.3.jar

ADD server.sh /$HZ_HOME/server.sh
RUN chmod +x /$HZ_HOME/server.sh
EXPOSE 5701
# Start hazelcast standalone server.
CMD ["./server.sh"]
