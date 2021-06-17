FROM maven:3.8.1-jdk-8

COPY src /app/src/
COPY pom.xml /app/
WORKDIR /app
RUN mvn clean package test

# RUN mkdir /adv; cd /adv; mvn archetype:generate \
#     -DarchetypeArtifactId=maven-archetype-quickstart \
#     -DinteractiveMode=false \
#     -DgroupId=com.sample \
#     -DartifactId=hello

# RUN pwd; ls -l

# RUN cd /adv/hello; cat src/test/java/com/sample/AppTest.java
