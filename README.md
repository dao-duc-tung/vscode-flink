# Develop Flink app in vscode

```bash
# Init project
# https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html
mvn archetype:generate -DgroupId=com.groupid.tung -DartifactId=artifact-id-tung-1 -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false

# Check java version used by mvn
mvn --version

# Change java version
# in pom.xml, modify this:
# <properties>
#     <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
#     <maven.compiler.source>11</maven.compiler.source>
#     <maven.compiler.target>11</maven.compiler.target>
# </properties>

# or add this
# <plugin>
#     <groupId>org.apache.maven.plugins</groupId>
#     <artifactId>maven-compiler-plugin</artifactId>
#     <version>3.8.0</version>
#     <configuration>
#         <release>11</release>  <!--or <release>10</release>-->
#     </configuration>
# </plugin>

# Common mvn commands
# https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html
mvn clean
mvn validate
mvn compile
mvn test
mvn package
mvn integration-test
mvn verify
# mvn install
# mvn deploy

# Debug in vscode
# require running: mvn clean && mvn compile
# just run debug in file App.java

# Run in terminal
# require uncomment this in pom.xml
# <exclude>org.slf4j:*</exclude>
# <exclude>org.apache.logging.log4j:*</exclude>
# require running: mvn clean && mvn package
java -cp target/artifact-id-tung-1-1.0-SNAPSHOT.jar com.groupid.tung.App
```
