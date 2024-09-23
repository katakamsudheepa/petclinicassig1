# petclinicassig1
•	Clone the Petclinic Repository:
git clone https://github.com/spring-projects/spring-petclinic.git
cd spring-petclinic
./mvnw package
dOCKER FILE:
# Dockerfile
FROM openjdk:17-jDK-slim
VOLUME /tmp
COPY target/spring-petclinic-*.jar app.jar
ENTRYPOINT ["java", "-jar", "/app.jar"]
#DOCKER IMAGE
docker build -t SKATAKAM19/petclinic:latest .
iNSTANCES
docker run -d -p 8080:8080 SKATAKAM19/petclinic:latest
docker run -d -p 8081:8080 SKATAKAM19/petclinic:latest
docker ps
#push the image
docker login
docker push skatakam19/petclinic:latest
•  http://localhost:8080 (first instance)

•  http://localhost:8081 (second instance)
![image](https://github.com/user-attachments/assets/74a97cfb-7ae9-49d6-bd46-207e06442f4c)
