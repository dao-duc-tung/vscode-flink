```bash
# https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html
mvn archetype:generate -DgroupId=com.groupid.tung -DartifactId=artifact-id-tung-1 -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false

# check java version used by mvn
mvn --version

# change java version
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

# https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html
mvn validate
mvn compile
mvn test
mvn package
mvn integration-test
mvn verify
# mvn install
# mvn deploy

# run in terminal
# required running: mvn package
java -cp target/artifact-id-tung-1-1.0-SNAPSHOT.jar com.groupid.tung.App

# debug in vscode
# required running: mvn compile
# just run debug the file App.java

mvn clean
```
