FROM ubuntu:18.04
RUN apt update -y \
&& apt install git -y \
&& git clone -b postgres https://github.com/wilczynski87/QAProject
RUN apt install default-jdk -y \
&& apt install maven -y
RUN apt install postgresql-client-common -y
RUN apt install postgresql-client -y
#RUN psql postgresql://postgres:1234@172.18.0.5:5432 -c "\l"
#RUN rm ./QAProject/src/main/resources/application-dev.properties
#RUN touch ./QAProject/src/main/resources/application-dev.properties
#RUN echo "spring.datasource.url=jdbc:postgresql:172.19.0.3:5432/db" >> ./QAPro>
#RUN echo "spring.datasource.username=postgres" >> ./QAProject/src/main/resourc>
#RUN echo "spring.datasource.password=1234" >> ./QAProject/src/main/resources/a>
#RUN echo "spring.jpa.hibernate.dll-auto=create" >> ./QAProject/src/main/resour>
RUN cat /QAProject/src/main/resources/application-dev.properties
RUN apt install iputils-ping -y
#RUN ping -c 2 172.18.0.5
#RUN psql postgresql://postgres:1234@172.18.0.5:5432 -c "\l"
RUN cd ./QAProject \
&& mvn install -X
WORKDIR /QAProject/target
CMD ["java", "-jar", "QAProject-0.0.1-SNAPSHOT.jar"]
