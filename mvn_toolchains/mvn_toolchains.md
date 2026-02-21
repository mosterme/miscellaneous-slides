# [Maven Toolchains Plugin](https://maven.apache.org/plugins/maven-toolchains-plugin/)

&#160;

![The Usual Suspects](./toolchains.jpg)

<div class="page">&#160;</div>

# [Maven Toolchains Plugin](https://maven.apache.org/plugins/maven-toolchains-plugin/)

```bash
mvn toolchains:display-discovered-jdk-toolchains
```
```
[INFO] ------------------< org.apache.maven:standalone-pom >-------------------
[INFO] Building Maven Stub Project (No POM)
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] --- toolchains:3.2.0:display-discovered-jdk-toolchains (default-cli) @ standalone-pom ---
[INFO] Found 2 possible jdks: [/usr/lib/jvm/java-25-openjdk-amd64, /usr/lib/jvm/java-21-openjdk-amd64]
[INFO] Discovered 2 JDK toolchains:
[INFO]   - /usr/lib/jvm/java-21-openjdk-amd64
[INFO]     provides:
[INFO]       version: 21.0.10
[INFO]       runtime.name: OpenJDK Runtime Environment
[INFO]       runtime.version: 21.0.10+7-Debian-1deb13u1
[INFO]       vendor: Debian
[INFO]       current: true
[INFO]       lts: true
[INFO]   - /usr/lib/jvm/java-25-openjdk-amd64
[INFO]     provides:
[INFO]       version: 25.0.1
[INFO]       runtime.name: OpenJDK Runtime Environment
[INFO]       runtime.version: 25.0.1+8-Debian-1deb13u1
[INFO]       vendor: Debian
[INFO]       lts: true
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  0.700 s
[INFO] Finished at: 2026-02-02T15:30:45+01:00
[INFO] ------------------------------------------------------------------------
``` 

<div class="page">&#160;</div>

# [JDK Toolchain discovery](https://maven.apache.org/plugins/maven-toolchains-plugin/toolchains/jdk-discovery.html)
```
pom.xml
```
 ```xml
<properties>
    <toolchain.jdk.version>[25,)</toolchain.jdk.version>
</properties>
 ```
 ```xml
 <build>
     <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-toolchains-plugin</artifactId>
            <version>3.2.0</version>
            <executions>
                <execution>
                    <goals>
                        <goal>select-jdk-toolchain</goal>
                    </goals>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
 ```

<div class="page">&#160;</div>

# [ToolchainDiscoverer.java](https://github.com/apache/maven-toolchains-plugin/blob/master/src/main/java/org/apache/maven/plugins/toolchain/jdk/ToolchainDiscoverer.java)

<table border="0"><tr valign="top"><td width="40%">

## Windows
* ``C:\Program Files\Java``
* ``%USERPROFILE%\scoop\apps``

## MacOS
* ``/Library/Java/JavaVirtualMachines``
* ``~/Library/Java/JavaVirtualMachines``

## Linux
* ``/opt/java``
* ``/usr/java``
* ``/usr/jdk``
* ``/usr/lib/jvm``

</td><td width="40%">

## From 3rd Party Tools
* ``~/.jdks``
* ``~/.m2/jdks``
* ``~/.sdkman/candidates/java``
* ``~/.gradle/jdks``
* ``~/.jenv/versions``
* ``~/.jbang/cache/jdks``
* ``~/.asdf/installs``
* ``~/.jabb/jdk``

</td></tr></table>

<div class="page">&#160;</div>

# [JDK Standard Toolchain](https://maven.apache.org/plugins/maven-toolchains-plugin/toolchains/jdk.html)
```
~/.m2/toolchains.xml
```
```xml
<toolchains>
    <toolchain>
        <type>jdk</type>
        <provides>
            <version>17</version>
            <vendor>Eclipse Adoptium</vendor>
        </provides>
        <configuration>
            <jdkHome>/opt/adoptium/temurin/jdk-17.0.18+8</jdkHome>
        </configuration>
    </toolchain>
    <toolchain>
        <type>jdk</type>
        <provides>
            <version>11</version>
            <vendor>Eclipse Adoptium</vendor>
        </provides>
        <configuration>
            <jdkHome>/opt/adoptium/temurin/jdk-11.0.30+7</jdkHome>
        </configuration>
    </toolchain>
</toolchains>
``` 
