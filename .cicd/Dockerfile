# Dockefile for user , 
FROM openjdk:18.0.2.1-jdk
ARG JAR_DEST
ENV JAR_DEST ${JAR_DEST}
ARG JAR_SOURCE
ENV JAR_SOURCE ${JAR_SOURCE}
# certificates, jks, app.properties 
RUN mkdir -p /opt/i27/
WORKDIR /opt/i27
COPY ["${JAR_SOURCE}", "/opt/i27/i27cart-user.jar"]
# JAR_SOURCE will be passed during the docker build command
RUN chmod 777 /opt/i27
EXPOSE 8232
USER root
CMD ["java", "-jar", "/opt/i27/i27cart-user.jar"]

# docker run --name usercont -p hp:cp
# docker run --name usercont -P ====> hp(dynamic) ====> container (fetching from dockerfile)
# using EXPOSE 
