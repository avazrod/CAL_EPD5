# Usa la imagen base de Ubuntu 20.04
FROM ubuntu:20.04

# Actualiza el sistema y luego instala Java 8
RUN apt-get update && \
    apt-get install -y openjdk-8-jdk

# Instala Tomcat 8
RUN apt-get install -y tomcat8

# Descarga la última versión de Jenkins en formato .war
RUN wget -O /usr/local/tomcat/webapps/jenkins.war https://updates.jenkins.io/latest/jenkins.war

# Expone el puerto 8080
EXPOSE 8080

# Arranca Tomcat al iniciar el contenedor
CMD ["catalina.sh", "run"]
