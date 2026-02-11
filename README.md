# ROS2 Java Bindings
![Build Status](https://github.com/workerrobotics/ros-rcl-java-bindings/actions/workflows/create-java-bindings.yml/badge.svg)
![Jazzy Version](https://img.shields.io/github/v/tag/WorkerRobotics/ros-rcl-java-bindings?filter=jazzy-*&label=jazzy)
![Kilted Version](https://img.shields.io/github/v/tag/WorkerRobotics/ros-rcl-java-bindings?filter=kilted-*&label=kilted)
![License](https://img.shields.io/github/license/workerrobotics/ros-rcl-java-bindings)
![GitHub last commit](https://img.shields.io/github/last-commit/workerrobotics/ros-rcl-java-bindings)

## Description
Generated java bindings of ros distro's with the java tool JExtract. JExtract is still early-access and part of Project Panama.

---

### Dependency
To use these bindings add the following dependency to your `pom.xml`. Change the version number accordingly.

The version number format should be read like this: {JDK_VERSION}.{MAJOR_VERSION}.{BUILD_VERSION}

For ROS - Kilted
```xml
<dependency>
  <groupId>com.github.WorkerRobotics</groupId>
  <artifactId>ros2-java-bindings-kilted</artifactId>
  <version>25.0.10</version>
</dependency>
```

For ROS - Jazzy
```xml
<dependency>
  <groupId>com.github.WorkerRobotics</groupId>
  <artifactId>ros2-java-bindings-jazzy</artifactId>
  <version>25.0.10</version>
</dependency>
```