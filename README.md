# Teststudie
Snabb jämförelse mellan JVM och GraalVM i Docker. Test inför examensarbete.

En iteration:

JVM: ```Started TestApplication in 1.495 seconds (process running for 1.935)```

GraalVM: ```Started TestApplication in 0.041 seconds (process running for 0.044)```

https://github.com/graalvm/graalvm-demos/tree/master/spring-native-image

Build JVM Image: ```docker build -f Dockerfiles/Dockerfile.jvm --build-arg APP_FILE=benchmark-jibber-0.0.1-SNAPSHOT.jar -t jibber-benchmark:jvm.0.0.1-SNAPSHOT .```


Build AOT Image: ```docker build -f Dockerfiles/Dockerfile.native --build-arg APP_FILE=benchmark-jibber -t jibber-benchmark:native.0.0.1-SNAPSHOT .```
