FROM openjdk:latest
COPY server.jar /opt/minecraft/server.jar
COPY server.properties /opt/minecraft/server.properties
WORKDIR /opt/minecraft/
RUN echo eula=true > eula.txt
CMD ["java", "-Xmx2048M", "-Xms1024M", "-jar", "server.jar", "nogui"]