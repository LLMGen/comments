
# Build Maven Projects

### pmq
java v8
```bash
cd mq_client
mvn clean install
cd ..
mvn clean package
```

### roubsite
java v8
```bash
mvn clean install
```

### knetbuilder
java v21 \
mannually downgrade xstream lib to below 1.4.13, need to be packaged to jar first
```bash
mvn clean package
```

### IPED
java v11 \
mannully added openjfx dependency in geo and viewers-impl
```bash
sudo apt install openjfx libopenjfx-java libopenjfx-jni -y
git checkout origin/#580_in_3.18.x
```

### cde
java 11 \
The vulnurable lib located in core module, and the code module can be compiled, all tests run\
```bash
mvn clean install
```

### arraybase
java 8 \
fixed pom a lot \
mannually download ojdbc8 and flanagan from website \
missing ABIndexer class in the sourcecode, so added vitual class in /com/arraybase/plugin/ABIndexer.java for compile \
```bash
mvn clean install
```


# build gradle project

### library of alaxandris
java 8 \
downgrade tika version to 1.19 in build.gradle under load-service/loa-document-parser-service/src
```bash
gradle build
```

###  PlmCodeTemplate
java 8, mvn 3.8.7 \
mannually add lombok dependency \
fixed fastjson dependency version under javasource-springboot \
fixed ResultBeanControllerBean.java \
```bash
cd source
mvn clean compile
mvn test
```

### aegis
install android sdk first (Android Studio) \
add local.properties and sdk.dir = android path \
mannually download trustedintents.jar to /app/lib and fixed dependency \
git clone TextDrawable repo to /app/lib \
```bash
./gradlew build -x lint
```

### ANET
 Java 8
remove dependencies markdown.convert, markdownToHtml in gradle.build
```bash
./gradlew compileJava
./gradlew compileTestJava
```
some testcase related to sqlserver failured

### rsdb
java 11 \
remove exlipse plugin, many fix in gradle.build
```bash
#intall gradle wrapper
gradle wrapper --gradle-version=7.6
./gradlew build
```

### communote_server
java 11 \
first solve imaging dependency, it need to be download and installed mannually \
fix ImageReadException and ImageWriteException in source code
```bash
cd core
mvn clean install
```

### jmeter
java 11
