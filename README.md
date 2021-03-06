Master Branch: [![Travis CI](https://travis-ci.org/caofangkun/version-maven-plugin.svg?branch=master)](https://travis-ci.org/caofangkun/version-maven-plugin)

# version-maven-plugin
Generate Release Version Information for Maven Project

# Pom info Example

```
            <plugin>
               <groupId>com.github.caofangkun</groupId>
               <artifactId>version-maven-plugin</artifactId>
               <executions>
                 <execution>
                   <id>version-info</id>
                   <phase>generate-resources</phase>
                   <goals>
                     <goal>version-info</goal>
                   </goals>
                   <configuration>
                   <source>
                      <directory>${basedir}/src/</directory>
                      <includes>
                        <include>src/**/*.java</include>
                        <include>clj/**/*.clj</include>
                      </includes>
                  </source>
                 </configuration>
               </execution>
             </executions>
          </plugin>

```

# Example Usage 

```
git clone https://github.com/caofangkun/version-maven-plugin.git
cd version-maven-plugin
mvn clean && mvn install 
cd examples/version-example
mvn clean && mvn install 

bin/version 
Version 1.0-SNAPSHOT
URL https://github.com/caofangkun/version-maven-plugin.git -r c51a3be9a59a5c65a5d6e7b370ee637926b62939
Branch master
Compiled by caokun on 2015-03-05T02:37Z
From source with checksum d41d8cd98f0b24e980998ecf8427e
```
