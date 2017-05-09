
# DirectMemorySize

## add sa-jdi in local maven repo
    mvn install:install-file  -Dfile=/usr/local/java/jdk1.7.0_40/lib/sa-jdi.jar \
        -DgroupId=sun.jvm.hotspot \
        -DartifactId=sa-jdi \
        -Dversion=24.0-b56.BuildVersion \
        -Dpackaging=jar \
        -DgeneratePom=true \
        -DcreateChecksum=true
## mvn install
    it will get java-${version}.jar
## use it to get direct memory info
    java -cp .:$JAVA_HOME/lib/sa-jdi.jar:java-1.0-SNAPSHOT.jar basic.direct.DirectMemorySize -e -v ${pid}
