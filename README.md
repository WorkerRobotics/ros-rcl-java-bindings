# ROS2 Java Bindings
![Build Status](https://github.com/workerrobotics/ros-rcl-java-bindings/actions/workflows/publish-bindings.yml/badge.svg)
![License](https://img.shields.io/github/license/workerrobotics/ros-rcl-java-bindings)
![Maven Central](https://img.shields.io/maven-central/v/com.worker-robotics/ros2-java-bindings-jazzy?label=Maven%20Central)
![GitHub last commit](https://img.shields.io/github/last-commit/workerrobotics/ros-rcl-java-bindings)

## Description
Generated java bindings of ros distro Jazzy and Kilted with the java tool JExtract. JExtract is still early-access and part of Project Panama.
The bindings are generated for x64 linux based operating systems.

Bindings based on ROS versions for Windows (x64) and MacOS (x64 / aarch64) may be added in the future.

---

### Dependency
To use these bindings add the following dependency to your `pom.xml`. Change the version number accordingly.

The version number format should be read like this: {JDK_VERSION}.{MAJOR_VERSION}.{BUILD_VERSION}

For ROS - Kilted
```xml
<dependency>
  <groupId>com.github.WorkerRobotics</groupId>
  <artifactId>ros2-java-bindings-kilted</artifactId>
  <version>25.0.20</version>
</dependency>
```

For ROS - Jazzy
```xml
<dependency>
  <groupId>com.github.WorkerRobotics</groupId>
  <artifactId>ros2-java-bindings-jazzy</artifactId>
  <version>25.0.20</version>
</dependency>
```

Don't forget to add the JVM flag `--enable-native-access=ALL-UNNAMED` and add the ros distro lib folder to the java runtime library path.

```xml
<configuration>
    <argLine>
        --enable-native-access=ALL-UNNAMED
        -Djava.library.path=/opt/ros/jazzy/lib
    </argLine>
</configuration>
```

The `ALL-UNNAMED` value is based on giving native access to all classes which are not mentioned in a specific `module-info.java`, if you're using `module-info.java` please use the name of the targeted modules.

To retain the packages from the GitHub packages you'll need to add the github repository of WorkerRobotics to your repository list and add your username and generated personal token to your settings.xml. This is because GitHub requires an authenticated user to download packages from their maven repositories.

Note: This project only contains the bindings, you'll need a loader which loads the ros distro lib folder for the SymbolLookup process of the bindings.
